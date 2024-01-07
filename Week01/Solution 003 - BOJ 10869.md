# BOJ 10869 - 사칙연산 (Arithmetic)

In order to print $A+B$, you need to print `A + B`.

In order to print $A-B$, you need to print `A - B`.

In order to print $A \times B$, you need to print `A * B`.

In order to print $A \div B$ (quotient), you need to print `A / B`, using integer division.

In order to print $A \bmod B$ (remainder), you need to print `A % B`.

To start a new line (printing a linebreak character), you need to print `endl` (or `\n`).

```cpp
#include <iostream>
using namespace std;

int main(){
    int A, B; cin >> A >> B;
    cout << A+B << endl;
    cout << A-B << endl;
    cout << A*B << endl;
    cout << A/B << endl;
    cout << A%B << endl;
}
```
