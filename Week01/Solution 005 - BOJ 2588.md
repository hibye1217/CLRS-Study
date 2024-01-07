# BOJ 2588 - 곱셈 (Multiplication)

## Normal Solution, using math

Unlike the other problems in this exercise, you actually need to think about the solution in this problem.

Let's say that $A$ and $B$ are the 2 three digit numbers put onto (1) and (2). Then, the value (6), the final calculation of the multiplication, should be the value $A \times B$.

But what about the values (3), (4), and (5)?

The value (3) is the result of the multiplication of $A$ with the one's digit of $B$. The value (4) and (5) follows the similar pattern, using the ten's digit and the hundred's digit of $B$, respectively.

The one's digit of $B$ is equal to $B \bmod 10$, as the ten's digits and higher will be multiplied by the multiple of $10$[^1].

The ten's digit of $B$ is equal to $\left\lfloor \frac{B}{10} \right\rfloor \bmod 10$, as the one's digit will be removed in $\left\lfloor \frac{B}{10} \right\rfloor$[^2], and rest of the digit, other than the ten's digit will be removed in $\bmod 10$ just like before.

The hundred's digit of $B$ is equal to $\left\lfloor \frac{B}{100} \right\rfloor$, and the reason is same with the above.

Since we now know every values that needed in the calculation, we can use that value in order to print the final answer.

```cpp
#include <iostream>
using namespace std;

int main(){
    int A, B; cin >> A >> B;
    cout << A * (B%10) << endl;
    cout << A * (B/10%10) << endl;
    cout << A * (B/100) << endl;
    cout << A * B << endl;
}
```



[^1]: For example, the value $385$ can be expressed with $3 \cdot 10^2 + 8 \cdot 10 + 5$. Dividing that by 10, taking remainder will remove every part other than the last digit.
[^2]: For example, the value $385$ can be expressed with $3 \cdot 10^2 + 8 \cdot 10 + 5$. Dividing that by 10 will result in $3 \cdot 10 + 8$. Then taking the remainder will result in $8$, as it removes other digits.

## Clever Solution, using string

You can also abuse the fact that the problem explicitly tells you the length of the number.

Let's go back to the point where we need to find the one's, ten's, and hundred's digit of $B$.

Which, if you think about it, is just the third, second, and first character of the $B$, respectively.

Therefore, you just need to know how to convert string to integer, which can be done using `stoi` function.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main(){
    string As, Bs; cin >> As >> Bs;
    int A = stoi(As), B = stoi(Bs);
    cout << A * (Bs[2]-'0') << endl;
    cout << A * (Bs[1]-'0') << endl;
    cout << A * (Bs[0]-'0') << endl;
    cout << A*B << endl;
}
```