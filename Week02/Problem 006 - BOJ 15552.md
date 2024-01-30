# BOJ 15552: 빠른 A+B (A+B, but faster)

[**Problem Link**](https://www.acmicpc.net/problem/15552)

Before we use the loops (such as `while`, `for`), you need to be aware of the speed of the inputting and outputting process. If the inputting or outputting the value is too slow, then the program might get Time Limit Exceeded.

If you're using C++, and are trying to use `cin` and `cout`, you should first do `cin.tie(NULL);` and `ios_base::sync_with_stdio(false);`, then use `'\n'` instead of `endl`. However, you cannot use `scanf`, `printf`, `puts`, `getchar`, `putchar`, and other C language's input/output method.

If you're using Java, use `BufferedReader` and `BufferedWriter` instead of `Scanner` and `System.out.println`. Only flush the output at the end of the program, using `BufferedWriter.flush`.

If you're using Python, use `sys.stdin.readline` instead of `input`. However, since it also reads the newline character, it's recommended to do `.rstrip()` after input.

Another thing you should know is that the input stream and output stream is two different stream. Therefore, you don't need to get the entire input before dealing with it testcase by testcase. You can get 1 testcase, print the answer of that, and then get next testcase, and so on.

Given 2 integers $A$ and $B$, print the value of $A+B$.

## Input

The first line of the input consists of the number of testcases $T$. $T$ is at most $1\,000\,000$. This is followed by a description of the testcases.

The first line of each testcase contains 2 integers $A$ and $B$. Both $A$ and $B$ are at least $1$, and at most $1\,000$.

## Output

For each testcase, print the value of $A+B$, in each line.

## Example

### Input 1

```
5
1 1
12 34
5 500
40 60
1000 1000
```

### Output 1

```
2
46
505
100
2000
```