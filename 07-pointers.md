# 08 Pointers

The topic of pointers in C is one that many beginners find challenging, but once you get comfortable with them your applications will become more powerful and more efficient.

{% hint style="info" %}
By the end of this chapter you should be able to:

* [ ] Create pointers.
* [ ] Read and write data to/from physical memory addresses.
* [ ] Use pointers with Arrays and Strings.
{% endhint %}

## 8.1 Pointer Analogy

![Pointers](http://domhnallohanlon.com/cnotes/images/keys.jpg)

A pointer is a special type of variable \(it's actually a constant!\) whose value is the memory address of another variable. To help you visualise this, image a hotel with lots of floors, and many rooms on each floor. The rooms are analogous to locations in computer memory in that they don't ever change their physical location or address. The occupants of the rooms however can change - so your hotel visitors are like programming variables, free to come and go as they please and easily replaced by other variables. ~~We can also extend this analogy a bit by considering twin rooms, double rooms, suites etc. These types of rooms might correspond to different types of data~~

A pointer variable is declared by prefacing its name with an asterisk. The address in memory is a numeric value so it's ok to use an interger as the type, but by starting your variable name with an asterisk \(star\) rather an a letter you are telling the compiler that this variable is actually a pointer rather than a conventional integer.

```c
 int main(){
     int *pointer;

     return 0;
 }
```

You can still declare multiple varaible on one line, but each pointer has to start with `*`

```c
int main(){
    /*one pointer and one integer*/
    int *my_pointer, not_a_pointer;

    /*two pointers*/
    int *first_pointer, *second_pointer;
}
```

### 8.1.1 Conventions

In many cases the accepted convention is to start a pointer variable with the letter p, for example:

```c
 int main(){
    //create an integer variable
     int age;

     //create a pointer variable
     int *pAge;

     return 0;
 }
```

## 8.2 Physical Addresses

To access memory locations in C use a pointer [conversion character:](https://robotfoundry.gitbook.io/cnotes/inputprocessoutput#1-4-conversion-characters)

`%p`

We can echo a memory address to the console using something like the following snippet:

```c
    int i = 42;

    printf("%p ", i);

    return 0;
```

### 8.2.1 Some notes on Hex

Hexadecimal is base 16 rather than base 10. read more in the references.

## 8.3 Creating Pointers

Take for example: `int myInt = 42`, this can store any numeric value between x and y. It has a memory address and we can create `int * pMyInt = &myInt`

## 8.4 Dereference Pointer

If you want to retrieve the value that a pointer points to \(as opposed to the address that it points to\) then you use the unary operator, `*`, which is used to dereference the pointer.

```text
 int i = 42;
 int *prt = &i;

 int main(){
     printf("The address of int i is: %p \n", prt);
     printf("The value stored  at i is: %d \n", *prt);

     return 0;
 }
```

## 8.5 Pointers and Arrays

create and array of vars

```c
int luckyNums[6] = [4,8,15,16,23,42];
```

  
loop through the array and print it's contents, and memory pointer.

```c
printf(" Element \t Address \t Value")
for (i=0; i<6; i++){
    printf(" luckyNums[%d] \t %p \t %d", i, &luckyNums[i], luckyNums[i]);
}

//array names are just pointers to the first element of that array.
printf("\n luckyNums %p", luckyNums);
```

## 8.6 Pointers and Strings

#### Test it Out

```c
 int main(){
    j = 1;
    k = 2;
    ptr = &k;
    printf("\n");
    printf("j has the value %d and is stored at %p\n", j, (void *)&j);
    printf("k has the value %d and is stored at %p\n", k, (void *)&k);
    printf("ptr has the value %p and is stored at %p\n", ptr, (void *)&ptr);
    printf("The value of the integer pointed to by ptr is %d\n", *ptr);

     return 0;
 }
```

## 8.7 Challenge

{% hint style="warning" %}
Notes on this challenge
{% endhint %}

