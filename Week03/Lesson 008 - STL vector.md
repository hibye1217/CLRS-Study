# std::vector

`vector` is a data structure defined in C++ STL, and are free to use.

It is defined in `<vector>` header.

## Concept

It's like an array, but it's size can expand and contract.

## How to Use

For rest of the article, we use `v` for vector's name (Other than the Declaration part).

There are other methods you can use, but it's not discussed in here.

### Declaration

- `vector<Type> Name;`: Declares the `vector` called `Name`, with `Type`.

### Set Size

- `v.resize(N)`: Set the `v`'s size to $N$.
- `v.push_back(x)`: Append the element $x$ to the back of the `v`. This increments the `v`'s size by $1$.
- `v.pop_back()`: Remove the last element from `v`. This decrements the `v`'s size by $1$. If the size was already $0$, then it results in Runtime Error.
- `v.clear()`: Remove every element from `v`. This set's the `v`'s size to $0$.

### Access

- `v[<index>]`: Access the `index`th element of `v`. Note that it's same as normal array.
- `v.front()`: Access the first element of `v`.
- `v.back()`: Access the last element of `v`.