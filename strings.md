# 06 Strings

Unlike other \(primitive\) variable types, strings are instantiated using `String` with a capital S. This is because a string is actually an array of `chars` - in other words a collection of characters.

{% hint style="info" %}
By the end of this chapter you should be able to:

* [ ] Create Strings
* [ ] Use a variety of string functions
* [ ] Create a password checking app
{% endhint %}

## 6.1 Strings in context

In other languages, such as Java, there are dedicated _String_ data types, but in C the convention is to use an array of chars, which does essentially the exact same thing. A C string is any array of chars followed by the null character, `\0`. The null character is also known as the string terminator \(see figure 1\).When you go to run your code the C compiler needs to know where every string ends, or terminates. To do this, the compiler parses your program and everywhere it finds closing quotation marks it inserts a character known as the **string terminator**. The string terminator is simply `\0` and takes up one additional byte of memory. This means that if you create a String variable to store your name, and if your name is 8 characters long, the name variable will actually take up 9 bytes of memory.This section outlines a number of different ways that strings can be created in C, as well as looking at how to manipulate stings with functions from the `string.h` library.

## 6.2 Array of Chars

The long way of creating a string is one character at a time so, if you really want to, you _could_ do the following:

```c
  char str1[20] = {'H','e','l','l','o',' ','W','o','r','l','d', '!'};
```

Note that when working with chars that each element of the array has to be inside single quotes. A more concise way to acheive exactly the same thing is by enclosing the entire string in double quotes like so:

```c
  char str2[20] = "Hello World!";
```

Try creating a program that includes `str1` and `str2` and prints the both to the console.

## 6.3 string.h

Since the original C language doesn't contain functions for working with strings, much of this functionality is provided by the `string.h` library.

## 6.4 String Functions

{% hint style="danger" %}
Don't forget to \#include &lt;string.h&gt;
{% endhint %}

### 6.4.1 Copying Strings

To overwrite an existing string use the `strcpy()` function. This function takes two **arguments** or parameters. Remember, the `strcpy()` function can be used to overwrite _any_ string, so the first thing you need to tell is is what string to replace \(overwrite\), then you need to tell it what to replace it with i.e. the string you wish to duplicate.

What do you expect the output of the following gist will be?

{% embed data="{\"url\":\"https://gist.github.com/domhnallohanlon/a11b3d388b4e5d3f8fe7\#file-strings03\_copying-c\",\"type\":\"rich\",\"title\":\"C: strcpy\(\)\",\"description\":\"C: strcpy\(\) · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/3117345?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\"text/javascript\\" src=\\"https://gist.github.com/a11b3d388b4e5d3f8fe7.js?file=strings03\_copying.c\\"></script>\",\"aspectRatio\":0}}" %}



### 6.4.2 Measuring Strings

To find the length of a string simply use `strlen()` function. This function only accepts one argument, the string you want to measure the length of, and it returns an integer value with the length of the string. Write a program that asks the user for two strings and then tells them which string is longer.

### 6.4.3 Joining Strings

In many areas, particularly when working with databases, you frequently have to put two \(or more\) strings of text together. This joining operation is known as **concatenation**. You can concatenate two strings by using the `strcat()` function. Write a program that ask the user for their first name and their second name and concatenates these two strings, with a space in between, into a third string called full name.

### 6.4.4 Comparing Strings

You can check if two strings are identical or not by using the string compare function `strcmp()`. As you can probably imageine, this function requires two arguments - the two strings you want to compare. If, for example, you want to compare _str1_ and _str2_there are three possile outcomes. They're either identical, or string 1 might be smaller than string 2, or string 1 might be bigger than string 2. The `strcmp(str1, str2)` function returns 0 if both strings are identical, a negative number if _str1_ is less than _str2_or a positive number if _str1_ is greater than _str2_.

## 6.5 Programming Challenge

Create a simple password app. 

* Your code should should include a "default" access key.
* You should also make sure that your user can not enter a password longer than 20 characters.
* You must include some way to check if the users password is the same as your stored key.

{% hint style="warning" %}
The following string functions will make your life a lot easier.
{% endhint %}

Here's an example access key that you could use in your app.

```c
 char key[20] = "OpenSesame";
```



