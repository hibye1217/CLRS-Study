# Appendix

## Additional Note

### Problem Notation

- `/<id>`: [**Baekjoon Online Judge**](https://www.acmicpc.net/)

Most of the problems will be from Baekjoon Online Judge. I'll translate every problems onto this page, and also put solutions.

#### Problem Difficulty

If you just learned the knowledge in `Lesson ***`, it is recommended to solve the problem up until **Hard** difficulty.

**Expert** and **Master** difficulty is there for more skilled participants, and only recommended after fully understand the knowledge.

- **Easy**: Requires only basic knowledge to solve the problem.
- **Normal**: Requires basic knowledge, but also requires some thinking to solve the problems.
- **Hard**: Requires to understand the internal logic, and apply it to the problem. It might use the technique not discussed in the Lesson[^Technique].
- **Expert**: Requires to fully understand the internal logic, and apply it to the problem. You probably need to use the technique not discussed in the Lesson.
- **Master**: Requires to fully understand the internal logic, and apply it to the problem. You probably need to use the technique not discussed in the Lesson, and you might also need couple of other steps just to apply the knowledge/techniques you learned.
- **Appendix**: Requires some knowledge which is not discussed in the Lesson, but important enough to know. The required knowledge is explained in Appendix file.

[^Technique]: Note the difference between **technique** and **knowledge**. You can derive the required **technique** by applying your **knowledge** learned from the Lesson.

### Code - Input/Output Format

```cpp
#include <iostream>
using namespace std;

int main(){
    int x; cin >> x;
    cout << x*10;
}
```

```
> 10
< 100
```

First Block is for Code, Second Block is for Input and Output.

Input is denoted as `>`, while Output is denoted as `<`. Actual Input/Output does not contain `>` and `<`.

There might be more than 1 Input/Output block, or sometimes even 0.

## Week 1

### Interval: Range of Numbers

- **Closed Interval** $[a, b]$: $a \le x \le b$.
- **Open Interval** $(a, b)$: $a < x < b$.
- **Half-Open Interval** $[a, b)$: $a \le x < b$.
- **Half-Open Interval** $[a, b)$: $a < x \le b$.

If $a > b$ in any case, then it's empty.

Sometimes, the interval is defined on Integers, while other times, is defined on Real Numbers. Which numbers are in use must be extracted from the context.

### Scientific Notation

The way of writing number as $a \cdot 10^{b}$ $(1 \le |a| < 10)$.

Number of digits in $a$ are called **significant digits**. In order to preserve the number of significant digits, sometimes it appends trailing zeros, such as $12.10 \cdot 10^{7}$.

### Comments

In C++, the comments are written in one of the following ways.

```cpp
// Comment for One Line

/* Comment for multiple Lines
Until they find the end
which, in this case, happens to be this line */

int x = 10; // You can also use comment at here

double p = /* change this later, imma just use */ 10 /* for now */;
```

- `// ...`: Single Line Comment
- `/* ... */`: Block of Comment

## Week 2

### Fast Input/Output

Lesson 003 told you that the `cout << endl;` and `cout << '\n';` were basically the same. It's time to show the difference.

Put shortly, `cout << endl` also flushes the buffer, while `cout << '\n'` doesn't. This creates the massive time difference between these two. For this reason, in Problem Solving, they never use `endl` and only use `'\n'`.

This only speeds up the outputting process, but you can also speed up getting input by using the following template.

```cpp
#include <iostream>
#define endl '\n' // Automatically change the endl to '\n', to speed up the ouptut.
using namespace std;

int main(){
    ios_base::sync_with_stdio(0);
    cin.tie(0); // Some article also includes cout.tie(0); But it's redundant.
  	// The main code goes here.
}
```

*You can ignore rest of this part, if you don't want to know the underlying logic. Or if you really want to know the underlying logic as it only explains it briefly, not exactly.*

Then why do they even have `endl`? It's because they **do** flush the buffer.

The programming language knows that the printing the character directly to the console is slow. So they create the small TODO list about printing things. This TODO list is called **buffer**.

So when they think the TODO list is full and cannot put anymore characters, they then prints it to the console.

However, sometimes you need to print to the console, even when the list is not full. Why? Think of the code below.

```cpp
#include <iostream>
using namespace std;

int main(){
    cout << "Input the number N (minimum 1, maximum 10)." << '\n';
    int N; cin >> N;
    cout << "Good Job!";
}
```

Because of the buffer approach, the console might look like the follow:

```
```

The `cout` was executed, but it's content is still in the TODO list, and not in the console. And then the program is waiting for the input because of the `cin`.

Therefore, sometimes you need to print the content faster. One way to tell them is using `endl`, which automatically writes everyting in the TODO list.

Another way is to make the program getting input. When you actually execute the code above, it gives you the nice `Input the number N (minimum 1, maximum 10).` line. The reason is that the program knows that the input and output is closely related. So they **automatically** flushes the content into the console if the `cin` is executed.

However, we don't need to flush the output in Problem Solving[^flush]. So we untie the relationship between the `cin` and `cout`, using `cin.tie(0);` line.

The final thing that left unexplained is the `ios_base::sync_with_stdio(0);`. There are actually more than 1 way to get an input in C++, which is using `cin` and using `scanf`. `scanf` is from the C language, and while it's fast, it's slower than `cin`.

But some programmers might write these kind of code:

```cpp
#include <iostream>
using namespace std;

int main(){
    int N; cin >> N; cout << N << '|n';
    int M; scanf("%d", &M); printf("%d\n", M);
}
```

In which, they cannot maintain 2 different buffers...

```
cout buffer: N, '\n'
printf buffer: M, '\n'
```

```
> 10
> 20
< 20
< 10
```

... as they might mix up the order in buffer case. C++ knows about this, and ties the buffer of the 2 different outputs...

```
tied buffer: N, '\n', M, '\n'
```

... so they never mess up the order. However, this tie-up becomes massive disadvantage for `cin` and `cout`, as it now need to match the speed for the `scanf` and `printf`, making them slower. In fact, slower than `scanf` and `printf`!

The `ios_base::sync_with_stdio(0);` line remove this tie-up. The side effect of this is that you cannot use `cin/cout` and `scanf/printf` at the same time, but as long as you do not use both method, you're good to go.

[^flush]: Ok, we do need to flush, if you're solving an interactive problem. But for the any other type of problems, you don't need to flush it. The reason you need to flush in these type of problem is that the input and output's relation **is** required.

## Week 3

### Undefined Behavior

There are some behavior that is not defined, such as accessing the array with nonexisting index, or using a variable without initializing. This is called **Undefined Behavior**, or **UB** for short.

Undefined Behavior is extremely dangerous, as their behavior is literally not defined. Thus, the program might do anything.

It might print the value as if nothing happened, or just crashes and give you Runtime Error, or maybe they do something that is not intended~~, and even launch nuke~~. OK, the last line was mostly joke. But the point is, the program might do literally anything when UB happens, and we basically cannot predict it's outcome.

One of the most dangerous part of UB is that they **might** produce error. So they might run fine on your computer, but not on the other computers. Or even other way around.