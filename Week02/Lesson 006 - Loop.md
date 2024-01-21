# Loop

## While Loop

- `while (condition){ statements; }`: Execute the `statements` **while** the `condition` is true.
  - Curly braces can be removed if the statement is single line.

```cpp
#include <iostream>
using namespace std;

int main(){
    int i = 10; while (i >= 0){
        cout << i << endl;
        i -= 1;
    }
}
```

```
< 10
< 9
< 8
< 7
< 6
< 5
< 4
< 3
< 2
< 1
< 0
```

Warning: If the condition never becomes false, then the statements will execute infinitely many times!

## For Loop

- `for (initialization; condition; increment){ statements; }`: Syntactical sugar. Almost equivalent to:

  ```cpp
  initialization; while (condition){
      statements;
      increment;
  }
  ```

  - Just like `while`, curly braces can be removed if the statement is single line.

The code above can be rewritten as:

```cpp
#include <iostream>
using namespace std;

int main(){
    for (int i = 10; i >= 0; i--) cout << i << endl;
}
```

## Flow Control

### Continue

- `continue;`: Go back to the beginning of the loop, **without** executing remaining statements.
  - If it is used in while loop, the `condition` is evaluated next.
  - If it is used in for loop, the `increment` is executed next.

```cpp
#include <iostream>
using namespace std;

int main(){
    for (int i = 10; i >= 0; i--){
    	if (i%3 == 0){ continue; } // Jump over any multiple of 3.
        cout << i << endl;
    }
}
```

```
< 10
< 8
< 7
< 5
< 4
< 2
< 1
```

### Break

- `break;`: Break out to the loop. Next statement executed are the one **right after** the loop.
  - The remaining statements, `increment`, `condition` is not evaluated.

```cpp
#include <iostream>
using namespace std;

int main(){
    for (int i = 10; i >= 0; i--){
    	if (i%3 == 0){ break; } // Stop the looping, and execute the line outside.
        cout << i << endl;
    }
    cout << "Program Halted.";
}
```

```
< 10
< Program Halted.
```

