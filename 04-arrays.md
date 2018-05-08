# 05 Arrays

Up until now we have typically worked with only one piece of information - for example integers, floats, chars etc. In many cases - such as our grade calculator - all the information was of the same type, yet we still created separate variables to store individual grades. Wouldn't it be much simpler if we could collect similar information like this in the same place?

{% hint style="info" %}
By the end of this chapter you should be able to:

* [ ] Create an array
* [ ] Access elements in an array
* [ ] Add elements to an array
{% endhint %}

## 5.1 Collections

An array is just another word of a collection. Examples of arrays can be found in [mathematics](http://en.wikipedia.org/wiki/Matrix_%28mathematics%29), [astronomy](http://www.vla.nrao.edu/), and even [biology.](https://www.google.ie/search?q=array+plate&newwindow=1&source=lnms&tbm=isch) What sort of things do people typically collect? What sort of collections can you think of?

![stamps](http://domhnallohanlon.com/cnotes/images/stamp_collection.jpg)![coins](http://domhnallohanlon.com/cnotes/images/coin_collection.jpg)

In the case of all of these collections, each consists of the same **type** of thing - stamps, coins etc. In programming that same is true. A collection of data, or an **array** must contain items that all have the same data type. For example, an array of ints could contain people's ages, an array of floats might contain bank balances, or an array of chars could store a student's letter grades.

## 5.2 Initialising an Array

What sort of information do you need to know in order to be able to create, or initialise, a loop?

Like any variable, it will need a name. You also need to know what sort of information your working with, so you have to know variable type. Finally you need to know how many items should go in the array.

Typically the syntax for an array is as follows:

```c
 int numbers[5] = {1,2,3,5,8};

 char letters[3] = {'A', 'B', 'C'};

 float myArray[10];
```

## 5.3 Accessing Elements

It is important to note that the first item of an array has an index of 0 \(lives at index 0?\) as this is often the source of off-by-one errors. For example,to print the letter **A** from the array `letters[3]` above, you select the 0th item from the array with the following piece of code:

```c
 printf("%c \n ", letters[0]);
```

## 5.4 Combining with Loops

You can quickly scan items to or prints items from an array by using an incrementer to both keep track of the iterations of your loop and the location \(index\) in the array that you want to access.

{% embed data="{\"url\":\"https://gist.github.com/domhnallohanlon/43a7c5c405d31f8670ca\#file-arrays01-c\",\"type\":\"rich\",\"title\":\"C; read and write to an array\",\"description\":\"C; read and write to an array · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/3117345?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\"text/javascript\\" src=\\"https://gist.github.com/43a7c5c405d31f8670ca.js?file=arrays01.c\\"></script>\",\"aspectRatio\":0}}" %}

## 5.5 Working with unknowns

Let's say that you want your user to enter all of their results - the only problem is you don't know in advance how many exams they've taken. Take a look at the code below and see if you can understand what's going on.

{% embed data="{\"url\":\"https://gist.github.com/domhnallohanlon/10622230e897da0e80fe\#file-arrays02-c\",\"type\":\"rich\",\"title\":\"C: Calculate size of Array\",\"description\":\"C: Calculate size of Array · GitHub\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gist.github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/3117345?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"embed\":{\"type\":\"reader\",\"html\":\"<script type=\\"text/javascript\\" src=\\"https://gist.github.com/10622230e897da0e80fe.js?file=arrays02.c\\"></script>\",\"aspectRatio\":0}}" %}



