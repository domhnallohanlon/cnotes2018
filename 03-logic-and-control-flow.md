# 03 Logic & Control Flow

{% hint style="info" %}
By the end of this chapter you should be able to:

* [ ] Use If/Else if/Else statements.
* [ ] Use the ternary operator.
* [ ] Use Switch statements
{% endhint %}

## 3.1 Logic

This section will help you add some "intelligence" or decision making abilities your programs. By the end of this section you will be able to write programs that respond to a variety of different input conditions, and we will conclude this chapter by writing a very simple game.

### 3.1.1 If Statements

Sometimes referred to as branches, if statements contain code that only executes if a certain condition is met. A nice example of an app that makes decisions based on specific events happening is called "IFTTT" which stands for **If This Then That**. As a more everyday example you can imagine the following scenario:  
"If it's raining outside then bring an umbrella". A typical if statement will look like this:

```text
  if(test if true){
    code to run if test is true;
}
```

Try the following out:

```c
int input;

  printf("What is the meaning of life, the universe and everything? \n");
  scanf("%d", &input);

  if (input == 42){
    prinf("Such learning. Many wisdom. Wow");
}
```

### 3.1.2 Else Statements

In the previous example there was only one "correct" answer. When you run the program you only ever get a response if the number '42' is entered. For every other input the program remains silent.

By adding an else condition we can catch all the other alternatives that our if test misses.

The `else` condition is included in the snipped below:

```c
 if(input == 42){
    printf("Such Learning Many Wisdom. Wow");
} else{
    printf("Try again");
}
```

### 3.1.3 Else If Statements

Finally, we can run more than two tests by adding in one \(or more\) `else if` clauses. For example:

```c
 if(input == 42){
    printf("Such Learning Many Wisdom. Wow");
} else if(input == 43){
    printf("Close, but no cigar");
} else if(input == 41){
    printf("Close, but no cigar");
} else{
    printf("Try again");
}
```

## 3.2 Ternary Operator

As with most things in programming, there's a more concise way to write your if statements. We've already seen the a unary operator take one operand, a binary operator takes two and with a ternary operator we can use three operands to handle the "If-Then-Else" elements of an if statement.

```text
  (test) ? trueCode : falseCode;
```

The ternary operator, just like unary and binary operators, can be used as an argument in other functions such as `printf()`. Try this nice way to print plurals correctly!

```c
  int numFriends = 2;

  printf("You have %d friend%s", numFriends, (numFriends!=1) ? "s." : "." );
```

## 3.3 Logic Operators

In the logic tests for the if, else if or ternary operator above you can test if more than one condition is met. This is achieved by using a logic `AND` operator if your want to check if both tests are true or you can test to see if either condition is true using the logic `OR` operator. Here's some pseudo-code to illustrate:

```text
  //logic AND example
  if (test1 && test2){
    code if both are true;
  }

  //logic OR example
  if (test1 || test2){
    code if 1 or 2 is true;
  }
```

Logic and is denoted by `&&` which is Shift + 7 on a UK keyboard. Logic or is denoted by `||` which is Shift + \ on a standard keyboard.

### 3.3.1 Truth Tables

Hopefully you will remember truth tables from your electronics studies in EM113. Just in case you've forgotten, here's what the `OR` and `AND` truth tables look like for two inputs.

### 3.3.2 A OR B

In an "or" gate if either A or B or both are true then the output will be true. Note that the "+" symbol in "A + B" should be read as "A or B". The logical OR operation should not be confused with the arithmetic ADD operation.

| **A** | **B** | **A+B** |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 1 |

### 3.3.3 A AND B

From the truth table below you can see that the output of the "and" gate is only true if both "A and B" are true. Again, in relation to the notation, you might sometimes use "." in arithmetic to denote multiplication but in the context of logic this should be read as "A and B"

| **A** | **B** | **A.B** |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 1 | 1 |

## 3.4 Coding Challenges

Try this coding challenge to test your knowledge of what we covered so far in this chapter:

### 3.4.1 CAO Points Calculator

Write an application that asks for an integer input \(between 0 and 100\) and converts it the corresponding Leaving Cert grade.

| Marks | Grade | Points |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 90-100% | H1 | 100 |
| 80-89% | H2 | 88 |
| 70-79% | H3 | 77 |
| 60-69% | H4 | 66 |
| 50-59% | H5 | 56 |
| 40-49% | H6 | 46 |
| 30-39% | H7 | 37 |
| 0-29% | H8 | 0 |

{% hint style="warning" %}
To complete exercise 3.4.1 you should use a `scanf()` to get an integer value from the user. There are a variety of ways to convert this to a letter grade but one of the most efficient ways to do this using logic operators to check if the input is within a certain range. 
{% endhint %}

## 3.5 Switch Statements

Switch statements are used to test a variable for equivalence against a list of given values. It is conceptually similar to an `if-else if-else` block of code.

#### Visualisation

![switch](http://domhnallohanlon.com/cnotes/images/switch.jpg)

#### Example 1

```text
int main(){
     int input;
     int type;

     printf("Enter a number \n");
     scanf("%d", &input);

     if(input % 2 == 0){
        type = 0;
     }else{
        type = 1;
     }

     switch(type){
        case(0):
            printf("The number is even\n");
            break;
        case(1):
            printf("The number is odd\n");
            break;
        default:
            printf("Sorry, unknown type of number! \n");
            break;
        }

     return 0;
```

#### Example 2

```text
   switch(grade)
   {
   case 'A' :
      printf("Excellent!\n" );
      break;
   case 'B' :
   case 'C' :
      printf("Well done\n" );
      break;
   case 'D' :
      printf("You passed\n" );
      break;
   case 'F' :
      printf("Better try again\n" );
      break;
   default :
      printf("Invalid grade\n" );
   }
```

### 3.5.1 Fizz Buzz 1.0

Ask the user to type in a number from 0 to 30 inclusive.  
If the number is evenly divisible by 3 print "FIZZ" instead of the number.  
If it's evenly divisible by 5 then print "BUZZ" instead of that number.  
If the number is divisible by both 3 && 5 the print "FIZZBUZZ" 

If the number doesn't fall into any of the categories above then simply print the number.

{% hint style="warning" %}
In exercise 3.5.1 you should use a scanf\(\) to obtain a number from the user and then use a switch\(\) statement to which output to use.

Consider adding a 5th option to introduce some error handing into your code.
{% endhint %}

## 

