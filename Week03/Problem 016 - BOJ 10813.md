# BOJ 10813 - 공 바꾸기 (Swapping the Balls)

[**Problem Link**](https://www.acmicpc.net/problem/10813)

Dohyeon have $N$ baskets, each of which are numbered $1$ to $N$. Each basket contains $1$ ball, which is numbered as same as the basket's number.

Dohyeon will swap the balls $M$ times. Each time, Dohyeon will choose $2$ baskets, and exchange the balls inside of these baskets.

Given the order of exchanging the balls, find which basket contains which ball after executing all $M$ exchanges.

## Input

The first line of the input contains 2 integers $N$ and $M$. $(1 \le N, M \le 100)$

For $M$ lines starting from the second contains 2 integers $i$ and $j$, meaning that Dohyeon will exchange the balls in $i$th basket and $j$th basket.

Dohyeon will exchange the balls in given order.

## Output

Print $N$ numbers. $i$th number should contain the ball's number in $i$th basket.

## Example

### Input 1

```
5 4
1 2
3 4
1 4
2 2
```

### Output 1

```
3 1 4 2 5
```

