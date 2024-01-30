# BOJ 2753: 윤년 (Leap Year)

[**Problem Link**](https://www.acmicpc.net/problem/2753)

Given a year, determine whether it is a leap year or not.

A year is a leap year if it is a multiple of 4 but not multiple of 100, or it is a multiple of 400.

For example, 2012 is a leap year, because it is multiple of 4 but not multiple of 100. 1900, on the other hand, is not a leap year, becuase it is a multiple of 100 and not multiple of 400. 2000 is a leap year because it is a multiple of 400.

## Input

The first line of the input contains single integer, describing the year. The year given in the input is at least 1 and at most 4000.

## Output

Print 1 if the year is the leap year. Otherwise print 0.

## Example

### Input 1

```
2000
```

### Output 1

```
1
```

### Input 2

```
1999
```

### Output 1

```
0
```