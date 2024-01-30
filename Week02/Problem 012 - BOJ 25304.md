# BOJ 25304: 영수증 (Bill)

[**Problem Link**](https://www.acmicpc.net/problem/25304)

For the first time in his life, Junweon went to the Costco. It was amazing. However, the total price was too high, even though they only bought a few items. So Junweon decided to check the bill, and see they correctly calculated the total price.

Given the each item's price and count in bill, determine whether or not the total price is correct.

## Input

The first line of the input contains a single integer $X$ denoting the total price written in the bill.

The second line of the input contains a single integer $N$ denoting the number of different types of item Junweon bought.

Each of the next $N$ lines contains 2 integers $a$ and $b$ denoting the item's price and number of item they bought.

## Output

If the total price written in the bill is correct, print `Yes`. Otherwise, print `No`.

## Constraint

- $1 \le X \le 1\,000\,000\,000$
- $1 \le N \le 100$
- $1 \le a \le 1\,000\,000$
- $1 \le b \le 10$

## Example

### Input 1

```
260000
4
20000 5
30000 2
10000 6
5000 8
```

### Output 1

```
Yes
```

### Input 2

```
250000
4
20000 5
30000 2
10000 6
5000 8
```

### Output 2

```
No
```