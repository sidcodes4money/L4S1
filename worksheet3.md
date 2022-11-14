---
title: "UFCFGL-30-1 Programming in C++ :: Worksheet(3)"
author: []
date: "2020-1-11"
keywords: [Week 3]
header-includes:

  - \hypersetup{colorlinks=false,
            allbordercolors={0 0 0},
            pdfborderstyle={/S/U/W 1}}
...

```c++
#include <cstdio>
int main(){
  	bool worksheet3 = true;
    printf("Functions,");
  	if(worksheet3){
      printf(" Conditionals and");
    }
  	for(int i =0; i < 2; i++){
      printf(" Loops");
    }
    return 0;
};
```

The marking scheme for this session is as follows:

- Task 1 : 10 marks
- Task 2 : 10 marks
- Task 3 : 10 marks
- Task 4 : 30 marks 
- Task 5 : 40 marks 
- Task 6 : 0 marks 



## Hello World!

In this session, we will need to create a project from scratch.

Don't forget to use the ***Developer Prompt for VS***!

``` bash
# Navigate to the directory that you want your projects in (this is an example):
cd Documents/programming-in-cpp/

#create a new directory
mkdir session2
cd seminar2
```

In this directory we should create a ```.cpp``` file for each task. Each will contain a main function and can be compiled by selecting it and building (```ctrl + shift + b```).

>  Don't forget to make your default build task (terminal drop down > Configure default build task)



The main file is so called because it is where we write our 'main' function. This is know as the entry point of the program and is the function that is called when the program begins.

```c++
int main(){

	return 0;
}
```



In c++, functions take the form; ```return type``` **function_name** ( ```arguments``` ), followed by curly braces ```{ }``` which contain the body of the function.

If we take this formula, we see that the main function in the code snippet above has:

- A return type of ```int```
- Is named 'main'
- Has no arguments inside the parentheses ``` ( )```
- Has a single return statement in the body that returns zero (indicating that the program ran successfully).

If we compile and run this program it would do nothing except signal to the OS that it ran successfully.



Printing 'Hello world!' Is the age old way to write your first program. It is doing the simplest thing the language is capable of on the given system and for c++, that is printing to the console (your CLI).



We can use the print statement to print characters to the console:

```c++
printf("Hello World! \n");
```

Try adding the print statement above to the body of the main function and compiling your program.

***Ensure you have selected the correct file in VS Code*** and build the project using ```ctrl ``` + ```shift``` + ```B```. This compiles your code creating a file with the same name as the file you compiled (without the .cpp extension).

To run the program, use ```./``` followed by the name of the newly created executable (which will take the name of the file it is created from) 

> Shortcut: use ```ctrl``` + ``` ` ``` to open a terminal in VS Code

```bash
# On windows probably:
.\tasks.exe
# or 
.\main.exe


# On linux/osx probably:
./tasks
# or 
./a.out 
# or 
./main
```



## Conditionals

There are four conditional statements in C++:

- ```if``` defines a block of code that is executed if a specified expression evaluates to true
-  ```else``` can follow an ```if``` statement to define a block of code that is executed if the preceding expression evaluates to false
- ```else if``` can also follow an ```if``` statement and defines a new expression to test (and code to execute), if the first condition is false. This can be repeated and should typically end in a final ```else``` case to catch the condition of all other expressions being false.
-  ```switch``` is a more terse approach to writing large if else blocks. We won't be needing switch cases for this session but feel free to investigate them separately. 



We define an ```if``` and a corresponding ```else``` block as follows:

> if (```condition```){
>
> ​	// Code to be executed if condition is **true**
>
> ​	// goes here (inside curly braces ```{}```)
>
> } else {
>
> ​	// Code to be executed if condition is **false**
>
> ​	// goes here (inside curly braces ```{}```)
>
> }



We can see some examples in the following block. They show the use of expressions (as discussed in worksheet 2) as the condition in the if statement.



```c++
if ( 10 > 4){
  printf("Ten is greater that four\n");
} else {
  printf("Ten is NOT greater that four!\n");
}

bool test_condition = (10 * 10) == (50 + 50);
if (test_condition){
  printf("Condition is true\n");
}

int a = 42;
int b = 42;

if ( a > b ){
    printf("A is greater than B\n");
} else if ( a >= b ){
  printf("A is greater or equal to B\n");
} else {
  printf("A is less than to B\n");
}

```



Notice that, as conditional statements (```if``` & ```else```) are predefined statements, we do not need to use a semicolon to make them into statements! We do however need to ensure that the curly braces surround valid statements.

For a more in depth look at using conditionals, see Ben's video [here](https://uwe.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=0748132a-18f4-4135-aca0-ac520105598b&instance=Blackboard).



## Loops

There are a number of different types of loop found in c++, however in this session we will focus on the ```for``` loop.

The for loop allows us to repeat some block of code a specified number of times. 

There are three main components to defining a for loop:

### Initializer

>for(```Initialize```; statement2; statement3; ){
>
>}

The first statement we require in a for loop is the initialization. Here we can declare a variable, and further, initialize it to an appropriate value.

### Condition

>for(Initialize; ```Condition```; statement3; ){
>
>}

The second statement is an expression (something that evaluates to a single value) that should produce a boolean result. While this condition is met, the loop will continue to repeat.

### Update

>for(Initialize; Condition; ```Update```; ){
>
>}

The update statement allows us the opportunity to to modify the variable we defined. We can therefore do things like increment that variable. Combining this with the condition statement allows us to repeat up to some number (ie. Until the condition is met).

For example:

```c++
#include <cstdio>
int main(){
    for(int i = 0; i < 10; i++){
        printf("%d\n", i);
    }
    return 0;
};
```

Ben's video ([here](https://uwe.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=e8c401e0-8d01-4b3d-ae20-ac5201055a31&instance=Blackboard)) is a good reference on loops.



## Functions

We can define (create) our own functions in c/c++ in the following way:

```c++
void functionName(){
 // Code contained in the function goes here.
}
```

A function is structured by first providing a ***return type***.

Types are discussed in this video ([click here](https://www.youtube.com/watch?v=70TAcAJojPY&list=PLe2QYG8u2CjNi6aeW9x6-BDi5T-XJ1VLt&index=1)) but we can quickly define some for example:

- ```int``` - Integer numbers (whole numbers that truncate rather than rounding [[more]](https://techterms.com/definition/integer#:~:text=An%20integer%20is%20a%20whole,data%20type%20in%20computer%20programming.) 

- ```float``` - floating point numbers (decimal numbers with some limitations [[more](https://techterms.com/definition/floatingpoint#:~:text=As%20the%20name%20implies%2C%20floating,decimal%20places%20are%20called%20integers.)]

- ```char``` - an 8bit value representing a single ascii character.

  

The ***return type***, is the type of value that the function returns. If the function doesn't return something specific (ie. it does some side effect like printing) then the function should return ```void``` as in the example above.

The return type is followed by the ***function name*** which you can define using characters and numbers (though numbers are rarely recommended). C++ keywords cannot be used for names.

The name is followed by ```()``` which may contain any arguments the function will be supplied. We will explore this in future and for now, we will supply no arguments and so the function is followed by empty parenthesis which must be included. 

We must then open up the scope to define what the function does. Any code contained in the following curly braces ```{ }``` will be executed when the function is called.

Functions are called in the following manner:

_(note: we no longer write the return type.)_

```c++
int main(){
    // Some code
    functionName();
    // ... more code
}
```



# Tasks



**Task 1 -** Write a program that prints "Hello World".



**Task 2 -** Print a message out 10 times using only a single print statement.



**Task 3 -** Ask the user to input their name and then print back a greeting followed by their name.

> This task includes the use of input and output. It will be discussed in the lectures and you are expected to research more on 



**Task 4 -** Ask the user to input the number of times a statement should be printed. 

>  Consider how you might want to validate the response the user provides. Marks will be awarded for handling of unsuitable input.



**Task 5 -** Fizz Buzz

Fizz Buzz is the age old interview entry level programming question...

- Print out ascending numbers from 0 - 30. 

- Whenever a number is divisible by 3 print 'fizz' instead of the number.

- Whenever a number is divisible by 5 print 'buzz' instead of the number.



**Task 6 -** Check and commit

Check you solutions, ensuring that a single file is supplied for each solution. Commit and push your solutions to you Gitlab repo using git.



You should have committed 5 files:

- task1.cpp
- task2.cpp
- task3.cpp
- task4.cpp
- task5.cpp



Each should include a main function that when compiled produces the output described in the tasks.



