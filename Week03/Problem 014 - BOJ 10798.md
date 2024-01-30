# BOJ 10798 - 세로읽기 (Reading Down)

[**Problem Link**](https://www.acmicpc.net/problem/10798)

Youngseok, who does not know how to read yet, is playing with the magnetic letters.

The magnetic letters consists of uppercase ('A' ~ 'Z') and lowercase ('a' ~ 'z') of the alphabet, as well as digits ('0' ~ '9'). Youngseok plays with these magnets by putting it in the letters horizontally to make words. And put more letters below to create a total of 5 words. The diagram below shows the one of the result of Youngseok's play:

```
A A B C D D
a f z z
0 9 1 2 1
a 8 E W g 6
P 5 h 3 k x
```

Each word consists of at most 15 letters, with no empty spaces. Each word can have different length.

Yeongseok, getting bored, decided to read these words vertically. Firstly, they read the first letters from top to bottom. Then they read the second letters from top to bottom, and so on, reading the letters in same position, from top to bottom. If there are no letter to read, such as the 2nd word's 5th letter on the example above, he reads nothing and move on to the next letter. So in the example, when they read the 5th letter, they would read `D1gk`.

If Yeongseok reads the diagram above in this way, he would read: `Aa0aPAf985Bz1EhCz2W3D1gkD6x`.

Given 5 words created by Yeongseok, print the letters Yeongseok would read in that order.

## Input

The first 5 lines of the input each contain the word created by Yeongseok. Every word consists of uppercase and lowercase of the alphabet, and digits. There are no whitespace inside of the word.

## Output

Print the letters read by Yeongseok, in that order. Do not print whitespace in between letters.

## Example

### Input 1

```
ABCDE
abcde
01234
FGHIJ
fghij
```

### Output 1

```
Aa0FfBb1GgCc2HhDd3IiEe4Jj
```

### Input 2

```
AABCDD
afzz
09121
a8EWg6
P5h3kx
```

### Output 2

```
Aa0aPAf985Bz1EhCz2W3D1gkD6x
```
