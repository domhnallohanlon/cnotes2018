# 02 Arithmetic in C

{% hint style="info" %}
By the end of this section your should be able to:

* [ ] Perform addition, subtraction, multiplication and division.
* [ ] Use modulo arithmetic to determine if a number is odd or even.
* [ ] Increment a variable using unary operators.
{% endhint %}

## 2.1 Arithmetic

You will recall that a computer is defined as a machine that can perform arithmetic and logic operations. So far we've done neither, so we'll try a bit of arithmetic since it's something that you have been doing since primary school. In the C language  `+` and `-` have the same meaning as you would expect from maths, `*` is used to denote multiplication and `\` is used for division.

```c
  int main(){

    //declare an integer variable
    int a = 7;

    //return the int squared
    printf("%d", a*a); 

    return 0;
  }
```

Great...let's try some more. You code will execute from top to bottom, so new values can be assigned "on-the-fly":

```c
  int main(){

    int currentYear = 2015;
    int zuckerBorn = 1984;
    int babyGates = 1955;
    int age;

    //calculates how old Mark Zuckerberg is:
    age = currentYear - zuckerBorn;
      printf("Mark Zuckerberg is %d years old \n", age);

    //here we reuse the age variable to compute how old Bill Gates is.
    age = currentYear - babyGates;
      printf("Bill Gates is %d years old \n", age);

      return 0;

  }
```

## 2.2 Maths Operators

Also known as binary operators, these mathematical operators require two operands to produce an output. For example, 40 + 2 = 42 requires two inputs to produce an output. As we will see later, programming languages also support unary operators.

| **Operation** | **Symbol** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| addition | + |
| subtraction | - |
| multiplication | \* |
| division | \ |
| modulo | % |
| equivalence | == |
| less than | &lt; |
| less than or = | &lt;= |
| greater than | &gt; |
| greater or = | &gt;= |

### 2.2.1 Working with Modulo

You should be familiar with the first four mathematical operations, but modulo may be new to you. Put simply, modulo tells you the remainder of dividing one number by another. For example `7%2` would return `1`, since 2 goes into 7 three time with a remainder of 1. Similarly `6%3` would return `0` since 3 divides evenly into six.  
In general terms, the modulo operator will always return a number between 0 and d-1, where d is the divisor \(or denominator, if you prefer to think in fractions\).

### 2.2.2 A Simple Incrementer

One of the most common tasks you will encounter in programming \(in any language\) is incrementing a value i.e. increasing it by a specific amount. Take for example scoring points in a game. Every time you hit a pig in Angry Birds 5000 points are added to your score.

Try the following code snippet:

```c
  //initialise a variable to store the number of times 
  // that prinf is run
  int numPrints = 0;

  //increment the variable by one
  numPrints = numPrints + 1;
    printf("The printf function has run %d times \n", numPrints);

  numPrints = numPrints + 1;
    printf("The printf function has run %d times \n", numPrints);

  numPrints = numPrints + 1;
    printf("The printf function has run %d times \n", numPrints);
```

### 2.2.3 Assignment != Equivalence



## 2.3  Unary Operators

Unlike binary operators, unary operators only require one operands. They allow you to write your code more concisely. For example, `i++` or `i--` will increment or decrement the integer `i`. There are several other ways of concisely expressing arithmetic operations, but they are binary rather than unary. For example, if we want to implement the Angry Birds scoring system we could use `myScore+=5000` to increase the score in steps of 5000.

### 2.3.1 Table of Unary Operators

| **Operation** | **Symbol** | **Also** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Increment | x++ | ++x |
| Decrement | x-- | --x |
| Address | &x |  |
| Pointer | `*x` |  |
| Positive | `+x` |  |
| Negative | -x |  |
| Ones Complement | ~x |  |
| Logical negation | !x |  |
| Variable Size | sizeof x | sizeof\(type-name\) |
| Type casting | \(type-name\) |  |

### 2.3.2 A Better Incrementer

The most common amount to increment a variable by is one, in fact it's so common that there's a shorthand for it. All you have to do is write it in the form `myVariable++`, so the example above becomes:

```c
  int numPrints = 0;

  numPrints++;
    printf("The printf function has run %d times \n", numPrints);

  numPrints++;
    printf("The printf function has run %d times \n", numPrints);

  numPrints++;
    printf("The printf function has run %d times \n", numPrints);
```

## 2.4 Performing Calculations in printf\(\)

You can create functions to perform maths operations almost anywhere in your program. It is also worth knowing that you can perform calculations within other functions such as `printf()`. Try the following example:

```c
    printf("Pi is approximately %f", 22/7);
```

## 2. 5 Order of Operations

Multiplication is just a concise way of saying that you want to repeatedly add a number to itself, and similarly division is just a simpler way of saying you want to repeatedly subtract a number. Then when multiplication and division become too cumbersome to work with you can use exponents and radicals \(roots\) to indicate repeated multiplication and division, respectively. This hierarchy is the reason you had to memorise some acronym for the order of mathematical operations.

| **PEMDAS** | **BOMDAS** | **BIMDAS** |
| --- | --- | --- | --- | --- | --- | --- |
| Parentheses | Brackets | Brackets |
| Exponents | Orders | Indices |
| Multiplication | Multiplication | Multiplication |
| Division | Division | Division |
| Addition | Addition | Addition |
| Subtraction | Subtraction | Subtraction |

Unlike many calculators, C is intelligent enough to understand this order and will apply it when making calculations. This means that if you want some particular step of your calculation to happen in a certain order then you will have to make careful use of brackets.

Try the following snippet as an example and see if you can come up with some others.

```c
    printf("%d", 3 + 5 * 7); //returns 38
    printf("%d", (3+5) * 7); //returns 56
```

## 2.6 Programming Challenges

Here are a few simple scenarios to challenge your understanding of the programming concepts we've covered so far.

#### Grade Point Average

Write a simple command line application that accepts 6 integer grades and returns the average of these numbers.

#### Tip Calculator

Write a command line application that accepts a bill amount and return to the user both the value of a 10% tip and the combined amount of initial bill and tip.







