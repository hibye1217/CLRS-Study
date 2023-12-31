# Appendix

## Additional Note

### Code - Input/Output Format

```cpp
#include <iostream>
using namespace std;

int main(){
    int x; cin >> x;
    cout << x*10;
}
```

```
> 10
< 100
```

First Block is for Code, Second Block is for Input and Output.

Input is denoted as `>`, while Output is denoted as `<`. Actual Input/Output does not contain `>` and `<`.

## Week 1

### Interval: Range of Numbers

- **Closed Interval** $[a, b]$: $a \le x \le b$.
- **Open Interval** $(a, b)$: $a < x < b$.
- **Half-Open Interval** $[a, b)$: $a \le x < b$.
- **Half-Open Interval** $[a, b)$: $a < x \le b$.

If $a > b$ in any case, then it's empty.

Sometimes, the interval is defined on Integers, while other times, is defined on Real Numbers. Which numbers are in use must be extracted from the context.

### Scientific Notation

The way of writing number as $a \cdot 10^{b}$ $(1 \le |a| < 10)$.

Number of digits in $a$ are called **significant digits**. In order to preserve the number of significant digits, sometimes it appends trailing zeros, such as $12.10 \cdot 10^{7}$.

### Comments

In C++, the comments are written in one of the following ways.

```cpp
// Comment for One Line

/* Comment for multiple Lines
Until they find the end
which, in this case, happens to be this line */

int x = 10; // You can also use comment at here

double p = /* change this later, imma just use */ 10 /* for now */;
```

- `// ...`: Single Line Comment
- `/* ... */`: Block of Comment