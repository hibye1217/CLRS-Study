## Data Type

### Declaring the Variable

- `<DataType> <VariableName>`: declares the variable called `VariableName`.
  - `VariableName` can have alphanumeric characters of any length (`0`\~`9`, `A`\~`Z`, `a`\~`z`).
    - First character of the `VariableName` should not be a digit (`0`\~`9`).
  - `int x;`: declares $x$ as the `int`.
  - `long long n;`: declares $n$ as `long long`.
  - `double d;`: declares $d$ as `double`.
  - `string s;`: declares $s$ as `string`.

### Setting the Values into the Variable

- `<VariableName> = <Value>`: set the value of variable `VariableName` to `Value`.
  - `Value` should match the type of the data the variable is.
  - `x = 10;`: set the variable $x$ to $10$ (integer).
  - `d = 12.17;`: set the variable $d$ to $12.17$ (real number).
  - `s = "seonah is GOD"`: set the variable $s$ to `seonah is GOD` (string of characters).

### 1+1 Event: Declare and Set the Variable

- `<DataType> <VariableName> = <Value>`
  - `int x = 10;`: declares an integer $x$, which is set to $10$.
  - `double d = 12.17`: declares a real number $d$, which is set to $12.17$.
  - `string s = "seonah is GOD"`: declares a string of characters $s$, which is set to `seonah is GOD`.

### Additional Event: Declare (and Set) Multiple Variables

- `<DataType> <Name1>, <Name2>, ...`
  - `<Name>` can be replaced with `<Name> = <Value>`, which declare and set the variable.
  - There is no limit on how many variables you can declare in single line.

### Integers

```cpp
#include <iostream>
using namespace std;

int main(){
    int x = 10;
    cout << x << endl;
    x = 15;
    cout << x << endl;
}
```

```
< 10
< 15
```

- `int`: can store any integer in $[-2^{31}, 2^{31})$, normally.
  - $2^{31}$ is approximately $2 \cdot 10^9$.
- `long long`: can store any integer in $[-2^{63}, 2^{63})$, normally.
  - $2^{63}$ is approximately $9 \cdot 10^{18}$.
- You can put `unsigned` in front of the integers, to explicitly show that the negative numbers will not be used.
  - This also creates more positive numbers to be representable.
  - `unsigned int`: $[0, 2^{32})$, normally.
  - `unsigned long long`: $[0, 2^{64})$, normally.

- If you try to store a number that's out of the range of the type of the data, then it causes an **overflow**.
  - Overflow is **Undefined Behavior**, which means that you won't know what happens next.
  - It might just set to values you didn't expect, it might crash~~, and it might launch nukes~~.

Every range comes with the *normally*, as it is *technically* compiler dependent. However, (almost) every compilers will follow the above range.

### Real Numbers

- `float`: Normally have $6$ significant digits.
  - It might sound a lot, but it's really small. Strongly not recommended.
- `double`: Normally have $15$ significant digits.
- `long double`: Normally have $33$ significant digits.

As you can see from the word *significant digit*, the computers store these values in *scientific notation*.

#### Warning for using Real Numbers

Avoid Real Numbers if possible.

```cpp
#include <iostream>
using namespace std;

int main(){
    long double a = 0.1, b = 0.2;
    if (a+b == 0.3){ cout << "0.1 + 0.2 is 0.3". }
}
```

```

```

Because of the way computers store values, most of the time, it will store the approximation of the given value.

Which can cause some funny results, such as $0.1 + 0.2 \neq 0.3$.

One of the solution is to use the constant value $\epsilon$, which is set as really small value (such as $10^{-9}$). And instead of comparing two numbers directly, compare the difference of two number with $\epsilon$. In formular, $|a-b| \le \epsilon = 10^{-9}$.

### Characters, and String of Characters

- `char`: Single Character, in ASCII.
  - Not Unicode. If you need to use Unicode, it is more recommended to use Python.
  - Values which are `char` is in single quote `'`, such as `'a'`, `'1'`, `'.'`.
- `string`: String of Characters, each of which are in ASCII.
  - Values which are `string` is in double quote `"`, such as `"Help"`, `"100000"`, `!@#$%^&*()`.
  - It's actually in `string` header, so it's recommended to `#include <string>` as well.


### Booleans

- `bool`: either `true` or `false`.
  - More on this data type at Conditional Chapter.
  - Any number that is not $0$ will be considered `true`, while $0$ will be considered `false`.
