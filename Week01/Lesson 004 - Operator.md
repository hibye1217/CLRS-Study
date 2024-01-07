# Operator

## Arithmetic Operators

- `a+b`: Add two numbers.
  - If $a$ and $b$ are string, then it concatenate the two string.
- `a-b`: Subtract one number from the other.
- `a*b`: Multiply two numbers.
- `a/b`: Divide one number from the other.
  - If $a$ and $b$ are both integer, then it instead calculates the result, then truncate the fractional part.
  - Therefore, $7/3 = 2$, $-5/3 = -1$, and $-3/7 = 0$.
- `a%b`: Calculate the remainder. Only appliable when $a$ and $b$ are both integer.
  - `(a/b)*b + a%b` will be equal to `a`.

## Incremental and Decremental

- `a++`: add $a$ by $1$. If used in expression, adding by $1$ happens after the expression is evaluated.
- `a--`: subtract $a$ by $1$. If used in expression, adding by $1$ happens after the expression is evaluated.
- `++a`: add $a$ by $1$. If used in expression, adding by $1$ happens before the expression is evaluated.
- `--a`: subtract $a$ by $1$. If used in expression, adding by $1$ happens before the expression is evaluated.

```cpp
#include <iostream>
using namespace std;

int main(){
    int x = 0;
    cout << x << endl;   // prints 0
    cout << x++ << endl; // prints 0, then becomes 1
    cout << x << endl;   // prints 1
    cout << ++x << endl; // becomes 2, then prints 2
    cout << x << endl;   // prints 2
}
```

```
< 0
< 0
< 1
< 2
< 2
```

## Assigning Operators

- `a = b`: Assign the value $b$ to the variable $a$. $b$ could be constant, single variable, or expression.
- `a += b`: Add $b$ to the variable $a$, assigning it as well. It is equivalent to `a = a+b`.
  - same thing exists for `-`, `*`, `/`, `%`, `>>`, `<<`, `&`, `^`, `|`.