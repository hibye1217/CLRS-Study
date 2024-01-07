# Week 1

Topic: C++ Basic

## Basic Template

```cpp
#include <iostream>
using namespace std;

int main(){
    cout << "Hello World!";
}
```

```
< Hello World!
```

- `#include <iostream>`: Includes a header called `iostream`.
  - `Input Output STREAM`, if you're wondering.
  - You don't need to understand this deeply for now.
- `using namespace std;`: uses namespace std. 
  - Most of the functions and/or structures are in `namespace` in C++, and in this case we are going to use `std`.
  - Not recommended in actual development, but will be useful for our purpose.
  - You don't need to understand this deeply for now.
- `int main(){ ... }`: `main` is the starting point of the execution.
  - It returns `int`, which is used as the exit code of the program.
  - More on this at Chapter Function. For now, just think of it as starting point.
- `cout << "Hello World!"`: putting the string `"Hello World!"` into the `cout`, which is the output.
