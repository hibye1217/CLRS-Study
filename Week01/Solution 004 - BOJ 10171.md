# BOJ 10171 - 고양이 (Cat)

Simple. Just print the cat.

```cpp
/// Wrong Solution
#include <iostream>
using namespace std;

int main(){
    cout << "\    /\" << endl;
    cout << " )  ( ')" << endl;
    cout << "(  /  )" << endl;
    cout << " \(__)|" << endl;
}
```

... or is it?

Since some of the characters, such as `\` and `'`, is considered as the special character, you need to use escape characters, such as `\\` and `\'` in order to accurately print these characters.

```cpp
#include <iostream>
using namespace std;

int main(){
    cout << "\\    /\\" << endl;
    cout << " )  ( \')" << endl;
    cout << "(  /  )" << endl;
    cout << " \\(__)|" << endl;
}
```