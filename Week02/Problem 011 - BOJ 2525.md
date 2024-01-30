# BOJ 2525: 오븐 시계 (Oven Clock)

[**Problem Link**](https://www.acmicpc.net/problem/2525)

The electric company KOI invented the new AI oven which cooks the meat in perfect condition. You just need to put in the meat, and AI will calculate the finishing time of the cook by itself.

This oven also have the digital clock that displays the finishing time of the cooking process.

Given the time we start cooking, and the duration we need to cook the meat, calculate the finishing time of the cook.

## Input

The first line of the input contains 2 integers $A$ and $B$, which denotes the starting time in hour and minute. $(0 \le A \le 23;$ $0 \le B \le 59)$

The second line of the input contains 1 integer $C$, which denotes the duration we need to cook the meat. $(0 \le C \le 1\,000)$

## Output

On the first line of the output, print the finishing time of the cook in hour and minute. Do not print leading zero, even if the value is single digit.

A minute after the 23:59 is 00:00.

## Example

### Input 1

```
14 30
20
```

### Output 1

```
14 50
```

### Input 2

```
17 40
80
```

### Output 2

```
19 0
```

### Input 3

```
23 48
25
```

### Output 3

```
0 13
```