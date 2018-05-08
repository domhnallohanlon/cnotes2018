# 09 Structs

We've seen lots of examples so far of where we would want to store multiple pieces of information. Up until now we've always used an array, however the main drawback of using an array is that it can only store one **type** of information, like an array of ints or an array of chars. The main advantage of using a struct is that it allows you to use different types of data.

{% hint style="info" %}
By the end of this chapter you should be able to:

* [ ] Create a struct and use Typedef
* [ ] Use the dot operator
* [ ] Use pointers to read/write data from structs.
{% endhint %}

## 9.1 Convention

The convention in C is to create your structs in a seperate header `.h` file, but for the time being we'll create them in our main.c files. In this lesson we'll create a basic car structure, make a few different cars and then modify them using a few functions we'll create ourselves.

## 9.2 Creating a struct

In something as complex as car, there are lots of different properties that we might want to assign. We can use strings to represent things like the make, model, features etc. numbers to represent properties such as horse power or top speed and arrays to capture the variety of engine sizes available, or perhaps types of fuel. The properties of a struct are contained between curly braces, and just like when you initialise any other data type, you must end your declaration with a semicolon.

```c
struct car{
    char* make;
    char* model;
    int topSpeed;
    int bhp;
}; //don't forget the semicolon
```

## 9.3 Using a Struct

Now that we've created a prototype for all cars in general, we can now go ahead and make specific cars by using our car struct.

```c
int main(){
    /* Add a new car by using our struct */ 
    struct car bv = {"Bugatti", "Veyron", 1000, 407}; 
    
   return 0;   
}
```

Note that when you are creating a new struct the order of the elements inside the curly braces must correspond with the order that you initially created them in i.e. make, model, horse power and top speed in this example. 

## 9.4 The Dot Operator

The dot operator, `.`, is used to assess specific members \(elements\) of a struct. In the example of our car structure, it has properties, or elements corresponding to the make, model, horse power and, top speed. Each of these can be accessed using the syntax `name.element` like in the example below:

```c
	/* using the dot operator to access data from a struct */

	printf("Make: \t %s\n", bv.make);
	printf("Model: \t %s\n", bv.model);
	printf("Horse Power: %d\n", bv.bhp);
	printf("Top Speed \t %d \n", bv.topSpeed);
```

## 9.5 Putting it all together

{% embed data="{\"url\":\"https://gist.github.com/domhnallohanlon/ac325c300d7f844db548\#file-structs1-c\",\"type\":\"rich\",\"title\":\"Sample code for using structs\",\"description\":\"Sample code for using structs · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/3117345?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\"text/javascript\\" src=\\"https://gist.github.com/ac325c300d7f844db548.js?file=structs1.c\\"></script>\",\"aspectRatio\":0}}" %}

## 9.6 Typedef

## 9.7 Structs and Pointers



{% embed data="{\"url\":\"https://gist.github.com/domhnallohanlon/ac325c300d7f844db548\#file-structs4-c\",\"type\":\"rich\",\"title\":\"Sample code for using structs\",\"description\":\"Sample code for using structs · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/3117345?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\"text/javascript\\" src=\\"https://gist.github.com/ac325c300d7f844db548.js?file=structs4.c\\"></script>\",\"aspectRatio\":0}}" %}



