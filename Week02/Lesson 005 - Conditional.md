# Conditional

## Operators

Everything below returns the boolean value, that is, basically `true` or `false`.

### Comparators

- `a > b`: is $a$ greater than $b$?
- `a < b`: is $a$ less than $b$?
- `a <= b`: is $a$ greater than or equal to $b$?
- `a >= b`: is $a$ less than or equal to $b$?
- `a == b`: is $a$ equal to $b$?
- `a != b`: is $a$ not equal to $b$?

### Boolean Operators

- `a || b`: is $a$ or $b$, or both are true?
- `a && b`: is $a$ and $b$ are both true?
- `!a`: is $a$ not true?

## Keyword: `if`, `else`

- `if (condition){ statements; }`: execute the `statement`, **if** the `condition` is true.
  - You can remove the curly brackets, if the statement is single line.

```cpp
#include <iostream>
using namespace std;

int main(){
    int a; cin >> a;
    if (a < 15){ cout << "This number is small enough."; }
}
```

```
> 12
< This number is small enough.
```

```
> 17
```

- `else{ statements; }`: paired with `if`, execute the `statement` if the `condition` in `if` is false.
  - The `if` should be directly before the `else`. There should be nothing in-between.
  - Just like `if`, you can remove the curly brackets if the statement is single line.

```cpp
#include <iostream>
using namespace std;

int main(){
    int a; cin >> a;
    if (a < 15){ cout << "This number is small enough."; }
    else{ cout << "This number is too big!"; }
}
```

```
> 12
< This number is small enough.
```

```
> 17
< This number is too big!
```



```cpp
#include <iostream>
using namespace std;

int main(){
    int a; cin >> a;
    if (a < 15){ cout << "This number is small enough."; }
    cout << "This Number is what?" << endl;
    else{ cout << "This number is too big!"; } // Compilation Error, since this 'else' cannot find the matching 'if'.
}
```

- `else if (condition){ statements; }`: Syntactic Sugar to merge `else` and `if` into 1 line.
  - The `else` means that the `if ` above should be false.
  - Then, they check the `contidion` and execute the `statement` if the condition is true.

```cpp
#include <iostream>
using namespace std;

int main(){
    int a; cin >> a;
    if (a == 1){ cout << "This Number is 1."; }
    else if (a <= 10){ cout << "It is still 1 digit number."; }
    else if (a <= 100){ cout << "Maybe bigger?"; }
    else{ cout << "What even is this number??"; }
}
```

```
> 1
< This Number is 1.
```

```
> 7
< It is still 1 digit number.
```

```
> 12
< Maybe bigger?
```

```
> 998244353
< What even is this number??
```

Note that because of the combination of `else ` and `if`, you do not execute the lower `else if`s if the condition is satisfied at one point. So you don't print `Maybe bigger?` at input `7` even if it's still lower than `100`.

## Ternary Operator: `?:`

- `condition ? statement1 : statement2`: almost equivalent to the following:

  ```cpp
  if (condition) statement1;
  else statement2;
  ```

  - The statement should be single line.
  - Some statement cannot be executed using this.
    - But those are rare, so mostly it's ok.
  - 2 statements should return the same **type** of value.