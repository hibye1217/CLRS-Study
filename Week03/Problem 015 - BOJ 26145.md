# BOJ 26145 - 출제비 재분배 (Redistribution of Money)

[**Problem Link**](https://www.acmicpc.net/problem/26145)

There are many administrators which need to hold the HCPC, the programming contest. There are 2 types of administrators, the creator and tester. There are $N$ creators and $M$ testers. The creators have the unique ID from $1$ to $N$, while the testers also have the unique ID from $N+1$ from $N+M$.

After the HCPC is over, the $N+M$ creators and testers divide the money they earned in following way.

First, each creator gets the examination fee. The creator numbered $i$ will receive $S_i$ dollar. After that, the creators are free to give their money to testers. In this process, The creator numbered $i$ will give $T_{i, j}$ dollar to the administrator numbered $j$.

Hibye already knows the amount of money $S_i$ each creators will get, as well as the amount of money $T_{i,j}$ they will give to other administrators. Given that, calculate the final amount of money each administrator will get.

## Input

The first line of the input contains 2 integers $N$ and $M$, the number of creators and testers, respectively. $(1 \le N, M \le 1\,000)$

The second line of the input contains $N$ integers $S_1, S_2, \ldots, S_N$, the amount of money each creators initially gets. $(0 \le S_i \le 100\,000)$

From the third line to $N+2$th line contains $N+M$ integers. The $i+2$th line's $j$th integer represents the amount of money $T_{i, j}$ the $i$th creator is willing to give to $j$th administrator.

## Output

Print $N+M$ integers, where $i$th integer represent the final amount of money $i$th administrator will get.

## Example

### Input 1

```
3 2
200 400 100
0 40 30 10 20
60 0 50 20 40
0 10 0 30 40
```

### Output 1

```
160 280 100 60 100
```

