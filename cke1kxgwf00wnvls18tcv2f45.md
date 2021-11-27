## Pointers in C and C++

Hey there, everybody! I'm back with pointers In C!

C is an old school, functional language and is one of the leading languages on the TIOBE index! I've usually seen people face issues with a topic - Pointers. Hence, I decided to clear it for once and all, for everyone! Let's start 🤘

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1597849502709/1E5oz0dBc.png)

### What are pointers in C?

A pointer is a special type of variable which holds the memory location of a variable. Everytime we print the address, when re-running the program, it gives a random address, because the value is located randomly in the memory, aka RAM [Random access memory]. A Pointer doesn't have a different data type, though. It has it's own simple yet special syntax to store it.

### Why are pointers Required?

There are some reasons why pointers are used in C/C++. They are,

- We can use the pointer to grab the memory address of any variable and pass the reference to modify it directly, instead of providing a copy. This speeds up computation by taking up less space, and giving a boost in calculations!
- Let's say we need a single variable to use it everywhere. If we use the value assigning it to new variables, It takes more space in the memory and can slow down in large programs. Just use the memory address directly, if you want to modify it directly, and don't need to store it. Saves time, and cost.

### Let's explore them through code!

1. How to access the memory address in C, and print it.

```c
#include <stdio.h>

int main(void) {
    int n = 50;
    printf("%p\n", &n);
}
```

Here are the outputs I obtained over 2 different runs.

- FIRST RUN: `0x7fff7d85c3cc`
- SECOND RUN: `0x7fbe015c9dcc`

As you can see they're stored in completely different places with hexadecimal notation, Due to random memory allocation in RAM.

2. Swapping
Let's say, we want to swap values of 2 variables using a function. We have 2 values as so,
```
x is 9, y is 7.
===== After swap, results should be =====
x is 7, y is 9.
```

And, if we write code to swap like this,
```
void swap(int a, int b) {
    int tmp = a;
    a = b;
    b = tmp;
}
```

What happens in the above Code?
> Where we use an extra variable to store the value, and store `a` in `tmp`, then `b` in `a`, and finally `tmp` in `b`

But, if we tried to use that function in a program, we don’t see any changes, because It turns out that the swap function gets its own variables, a and b when they are passed in, that are copies of x and y, and so changing those values don’t change x and y in the main function.

Now, let's say we decided to play with pointers and memory address, the first thing that comes to our mind is, When we reference variables from one to another, it always points to the same variable, but not copy, because we're just extracting the raw location from the memory address.

Let's examine this snippet:
```C
void swap(int *a, int *b) {
    int tmp = *a;
    *a = *b;
    *b = tmp;
}
```

Here this is what happens:
> The addresses of x and y are passed in from main to swap, and we use the int *a syntax to declare that our swap function takes in pointers. We save the value of x to tmp by following the pointer a, and then take the value of y by following the pointer b, and store that to the location a is pointing to (x). Finally, we store the value of tmp to the location pointed to by b (y), and we’re done.

### Some points:

- The address of a variable is called a pointer, which we can think of as a value that “points” to a location in memory. The `*` operator lets us “go to” the location that a pointer is pointing to.
- For example, we can print `*&n`, where we “go to” the address of `n`, and that will print out the value of `n`, 50, since that’s the value at the address of `n`:
- We also have to use the `*` operator (in an unfortunately confusing way) to declare a variable that we want to be a pointer.

Alright Folks! Hope you found this interesting! Be sure to let your issues in programming down below, and I will surely explain every aspect of it! 😄

Stay tuned for awesome blogs and topics. See you soon! 👋😄
