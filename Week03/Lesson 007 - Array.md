# Array

## Concept

**Array** is the data structure that contains many values in successive order.

An example of the array is sequence, such as $[2, 3, 5, 7, 11, 13]$.

But you don't need to be bounded to the sequence. As long as the desired data type exists, such as string, you can save it.

## Syntax

### Declaration

- `<Type> <VarName>[<Size>]`: Declares the array of length `Size` and contains the `Type`, named `VarName`.
  - `int arr[10]`: Array of size 10, type of int, named `arr`.
  - `double x[72]`: Array of size 72, type of double, named `x`.
- You can declare multiple arrays like declaring multiple variables.
  - `<Type> <Name1>[<Size1>], <Name2>[<Size2>];` and stuff.

- You can also initialize an array while declaring it.
  - `<Type> <Name>[<Size>] = {<Element0>, <Element1>, <...>};`
  - You don't need to fill every element. In this case, the remaining elements will be set to 0.


### Accessing

- `<VarName>[<Index>]`: Access the `Index`th element of `VarName`.
  - Important Note: Index starts at **0**. Therefore, the highest index you can use is **Size - 1**.
  - `arr[0]`: Access the 0th element of `arr`.
  - `x[71]`: Access the 71st (thus, last) element of `x`.
  - `x[1217]`: Access the 1217th element, which does not exists. Thus results in Undefined Behavior.
  - `x[72]`: Access the 72nd element, which does not exists. Thus results in Undefined Behavior.
  - `x[-1]`: Access the -1st element, which does not exists. Thus results in Undefined Behavior.
- You can use the individual element in array, just like any other variable.
  - Thus, `arr[5] += 10;` or `if (x[10] > 0.3){ arr[3] -= arr[6]; }` are allowed.

- You are, however, not allowed to use the entire array like other variable.
  - So even if `int arr[10], brr[10];` was declared, you cannot do `arr = brr;` and other stuff.

- You are also allowed to put integer value into the Index, as long as the value is between 0 and Size - 1.
  - Note that the description said **integer value**. So values such as `3.0` are not allowed, even if `3.0 == 3`.


### Example Code

```cpp
#include <iostream>
using namespace std;

int main(){
    int arr[10] = {1, 2, 3, 4, 5};
    for (int i = 0; i < 10; i++){ cout << arr[i] << ' '; }
    cout << endl;
    for (int i = 0; i < 10; i++){ arr[i] = 2*i; }
    for (int i = 1; i < 10; i++){ arr[i] += arr[i-1]; }
    for (int i = 0; i < 10; i++){ cout << arr[i] << ' '; }
}
```

```
< 1 2 3 4 5 0 0 0 0 0
< 2 6 12 20 30 42 56 72 90 110
```

## Extension: Multi-Dimension

- `<Type> <Name>[<Size1>][<Size2>];`: Declares **2D** array called `Name`, which saves the `Type`, with each dimension have the `Size1` and `Size2`, respectively.
  - You can think of it as Array of 1D Arrays.
  - Initialization, Accessing through index is also similar to the 1D case.
- You can also put more dimensions to it by putting more `[Size]`s.
- You can also declare multiples arrays with different dimensions.

```cpp
#include <iostream>
using namespace std;

int main(){
    int arr[3][4] = { {1, 2, 3, 4}, {5, 6, 7, 8}, {9, 10, 11, 12} };
    for (int i = 0; i < 3; i++){
        for (int j = 0; j < 4; j++){ cout << arr[i][j] << ' '; }
        cout << endl;
    }
}
```

```
< 1 2 3 4
< 5 6 7 8
< 9 10 11 12
```

