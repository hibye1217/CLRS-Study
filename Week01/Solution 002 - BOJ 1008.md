# BOJ 1008 - A/B

This problems looks easy, just input `A` and `B`, then print `A / B`.

However, if you actually just do that, it will give the incorrect result.

```cpp
/// Wrong Solution
#include <iostream>
using namespace std;

int main(){
    int A, B; cin >> A >> B;
    cout << A / B;
}
```

```
> 1 3
< 0
```

The reason for this is the fact that the integer division (integer divided by another integer) will result in integer.

In order to bypass that, we need to convert the type of the value into real number, such as `double`.

We also need to print enough digits (10 to 15 is preferred) in order to get enough precision, which is done by `cout.precision()`.

```cpp
#include <iostream>
using namespace std;

int main(){
    cout.setf(ios::fixed); cout.precision(10);
    double A, B; cin >> A >> B;
    cout << A/B;
}
```

