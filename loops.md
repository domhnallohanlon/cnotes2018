# 04 Loops

We've already seen a few instances where we wanted to repeatedly print information to the screen. Performing repetitive tasks is one of the things that computers are exceptionally good at doing. In this chapter we'll introduce a variety of different loops that you can use to write better programs.

{% hint style="info" %}
By the end of this chapter you should be able to:

* [ ] Use While and Do-While loops in your code.
* [ ] Create For loops in C.
* [ ] Understand how Break and Continue work.
{% endhint %}

## 4.1 Looping

If you've never done any programming before loops can be a challenging topic due to their unfamiliarity. If you think about it in more general terms, how would you give a computer instruction to do something over and over again?  
How would you avoid getting stuck in an _infinite loop_?

![flowchart](http://domhnallohanlon.com/cnotes/images/xkcd/flowchart.png)

### 4.1.1 Start, Middle, End

When you creating a loop in any programming language you will have tell it when and where to start. Starting a loop is known as **initialising** the loop.

Next you will have some code to run - for example increment at counter, print some text etc. - while the loop is running.

Finally you need an end condition. Once this condition is met or exceeded then the loop should exit gracefully.

## 4.2 While Loops

A `while` loop, as the name implies, executes while a certains condition is true. Once the test condition is no longer true then the loop is broken and code execution moves on to the next line. Try this snippet to get started:

```c
 int main(){

     int counter = 0;

        while(counter < 10){
            printf("the value of the counter is: %d \n", counter);
            counter++
        }

    printf("successfully exited the while loop! \n");

     return 0;
 }
```

#### Syntax

A typical `while` loop will begin with a test condition:

```text
    while(testIfTrue){
        code to run while true;
        incrementer;
}
```

If the test is true then the code inside the loop \(i.e between the braces\) will run - keep in mind that each line must end with a semi-colon. Finally, you'll need to have some sort of incrementer that gets updated during each pass through the loop. This is essential so that you don't get stuck in an infinte loop.

### 4.2.1 While Loop Example

Try the previous example with different test conditions. For example using `while (counter <= 30)` will cause the loop to run an extra time. Similarly you could continue executing the loop while the counter is _not_ equal to a certain value. `while (counter != 30)`

Be careful if you are changing the direction of the inequality!

#### Visualisation

![while loop](http://domhnallohanlon.com/cnotes/images/while.jpg)

### 4.2.2 Programming Challenge

Here's a simple example you can code using `while` loops. Which would you rather; one million euro today or 1 cent, doubled every day for a month \(30 days\)?

{% hint style="warning" %}
Your loop should run 30 times, doubling the value of your variable each time.
{% endhint %}



## 4.3 Do While Loops

With a `while` loop there is always a possibility that the test condition will never be true and that the code within the loop will never run.

A `do while` loop differs from a `while` loop in that it will always run at least once, and the conditional check is performed at the end of the loop, rather than at the beginning.

#### Do While Syntax

```text
    int loopCounter = 1;

   /* do loop execution */
   do
   {
       printf("number of times this loop has run: %d\n", loopCounter);
       loopCounter++;
   }while( loopCounter < 10 );
```

#### Visualisation

![Do While loop](http://domhnallohanlon.com/cnotes/images/doWhile.jpg)

## 4.4 For Loops

The `for` loop contains the starting condition, end condition and incrementer all at the beginning of the loop

#### Syntax

```text
 int main(){

     int counter;

     for(counter = 0; counter < 10; counter++){
        printf("Hello World!");
     }

     return 0;
 }
```

#### Visualisation

![for loop](http://domhnallohanlon.com/cnotes/images/for.jpg)

#### Example

```c
/* Print all the even numbers between 0 and 100 in 3 lines of code */
 int main(){

     int i;

     for(i = 0; i <=100; i++){
        if(i%2 == 0){
            printf("%d \n", i);
        }
     }

     return 0;
 }
```

#### Nesting For loops

A quick challenge to really test your understanding so far.

Create a program that has variables to represent the number of rows and number of colums that a table should have. Then use nested for loop to print a 3 x 3 table to the console.

## 4.5 Break

Lets say that we have some condidtion which, if met, should break us out of our loop immediatley. In such a scenario we would use a `break;` statement.  
Here's a simple example that modifies out doWhile application to exit before it has iterated through the loop 10 times.

```text
 int main(){

    int loopCounter = 1;

   /* do loop execution */
   do
   {
        if(loopCounter == 7){
            break;
        }
       printf("number of times this loop has run: %d\n", loopCounter);
       loopCounter++;
   }while( loopCounter < 10 );


     return 0;
 }
```

## 4.6 Continue

Conceptually this is the opposite of a `break` statement. It's behaviour will differ slightly depending on where it is used. In a `for`loop the `continue` statement will cause the conditional test and increment portions of the loop to execute.

When used in a `while` or `do-while` loop, the `continue` statement causes the program control to pass straight to the conditional tests.

## 

#### Fizz Buzz Revisited

Using a loop of your choosing:

* Print all the numbers from 0 to 30 inclusive.
* If the number is evenly divisibe by 3 print "FIZZ" instead of the number
* If it's evenly divisible by 5 then print "BUZZ" instead of that number.
* If the number is divisible by both 3 && 5 the print FIZZBUZZ

