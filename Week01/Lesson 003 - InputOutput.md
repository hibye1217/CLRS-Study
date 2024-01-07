## Input and Output

### Print the Variable

Just like `cout << "Hello World!"`, `cout << Variable;` will do.

To print the Newline Character `\n`, you can either print `'\n'` itself, or use `endl`[^1].

[^1]: `'\n'` and `endl` is actually different, which will be discussed later when we do FastIO.

#### Print the Real Number, up to Specific Precision

```cpp
#include <iostream>
using namespace std;

int main(){
    cout.setf(ios::fixed);
    cout.precision(3); cout << 10.8197 << endl;
    cout.precision(5); cout << 10.8197 << endl;
    cout.precision(10); cout << 10.8197 << endl;
}
```

```
< 10.820
< 10.81970
< 10.8197000000
```

- `cout.setf(ios::fixed)`: fixes the number of digits printed after the decimal point.
- `cout.precision(x)`: set the number of digits printed after the decimal point to $x$.

Rounding happens when you need to truncate some of the lower digits.

### Get Input, and Store it into the Variable

`cout << x` is for Output, `cin >> x` is for Input.

Just like how you print $x$ to the output, you can store the value $x$ from the input.

#### Warning: Whitespace

Since whitespaces (space `' '`, tab `'\t'`, newline `'\n'`) are used as the seperaters of the input, you cannot get the whole line as input using `cin`.

```cpp
#include <iostream>
using namespace std;

int main(){
    string s; cin >> s;
    cout << s;
}
```

```diff
> Hello World
< Hello
```

If you want to get the whole line, use `getline(cin, s);` instead.

```cpp
#include <iostream>
using namespace std;

int main(){
    int x; cin >> x;
    cin.ignore();
    string s; getline(cin, s);
    cout << x << ' ' << s;
}
```

```
> 10
> Hello World
< 10 Hello World
```

`cin.ignore()` is for clearing the buffer, which contains `\n` after getting input $x$.
