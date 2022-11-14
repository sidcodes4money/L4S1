```UFCFGL-30-1 Programming in c++```
# Vars, expr & ; Worksheet(2)

```c++
#include <cstdio>
int main(){
    char asciiValue = 50;
    printf("Welcome to programming in C++ Session %c", asciiValue);
    return 0;
};
```

The marking scheme for this session is as follows:

- Task 1 : 40 marks
- Task 2 : 30 marks
- Task 3 : 30 marks
- Task 4 : 0 Marks



## Variables

Variables are values that we can refer to by name. By default, in C++ we can modify variables. 

C++ is statically typed, which means we must say what type of data we wish to store in a variable when we make it.

```type``` ```variableName``` ```;```

To create a variable we write the type followed by the name we want to use to refer to it followed by a semicolon. For example:

```c++
int aNumber;
int x;
float value1;
float another_value;
char example;
```

 There are a number of primitive types available in c++.

Types are discussed in this video ([here](https://uwe.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=9c7ab01d-4e38-435e-9e59-ac5201055a03&instance=Blackboard)) but the following are common examples of types:

- ```int``` - Integer numbers (whole numbers that truncate rather than rounding [[more]](https://techterms.com/definition/integer#:~:text=An%20integer%20is%20a%20whole,data%20type%20in%20computer%20programming.) 
- ```float``` - floating point numbers (decimal numbers with some limitations [[more](https://techterms.com/definition/floatingpoint#:~:text=As%20the%20name%20implies%2C%20floating,decimal%20places%20are%20called%20integers.)]
- ```char``` - an 8bit value representing a single ascii character.
- ```bool``` - a type representing either true or false



We can assign values to variables using the ```=``` operator:

```c++
int number = 3;
float pi = 3.141592;
char three = '3';
```

In each case, we must ensure that we provide the right type of data for the variable. Integers cannot have a decimal point, floats should. Characters can be written using single quotes. Therefore, the variable ```three``` actually contains the ascii character 3, not the numeric value 3.



We can assign other variables to variables and use them where we can use a fixed value in expressions.

```c++
int x = 10;
int y = x + 5;
```

 For more on expressions and the operators available in c++, see Ben's video on operators ([here](https://uwe.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=2afae8bd-a465-4f33-bd29-ac52010559dc&instance=Blackboard)).



## Expressions

To understand an expression, we need to know of two terms:

- **Operators** are constructs that are defined in a programming language to perform an operation (such as addition or multiplication)

- **Operands** are the object or value that is operated on, typically a constant value or a variable.

  

An expression is a computation made from a sequence of *operators* and their *operands*. This may sound fancy or complex, but let's see just how simple an expression can be:

```
1 + 1
```



An expression is simply the description of some computation using the available features of the language. Here are some of the common operators we can use in c++:



|   Addition   |  Subtraction  |     Division     | Multiplication |
| :----------: | :-----------: | :--------------: | :------------: |
|   ```+```    |    ```-```    |     ```/```      |    ```*```     |
| **Equal to** | **Not equal** | **Greater than** | **Less than**  |
|   ```==```   |   ```!=```    |     ```>```      |    ```<```     |

> You should take some time to study and familiarize yourself with this more complete list [[here]](https://en.cppreference.com/w/cpp/language/expressions) of operators in C++, as you will need to use most of them!



In expressions, we can use fixed values (called **literals** as the value is literally written) as well as variables. Later we will also observe that we can use functions that return a value in an expression too, though we will explore that in more detail later.



### Variables in Expressions

```c++
// an expression using only literals [evaluates to an int]
1 + 1 / 2
  
// an expression using the variable 'pi' [evaluates to a float]
float pi = 3.141592;
(pi * 10.0) * (pi * 10.0)
  

// an expression that evaluates to true
(84 / 2) == 42
  
 
```



Notes:

- Much like in mathematics, parenthesis ```( ) ``` can be used to show precedence.

- Be careful to match types, you can't add a ```bool``` to an ```int``` - but be particularly careful with mixing ```float``` and ```int``` as decimal places can be dropped (referred to as truncation)

- > ```c++
  > int value = 9.5 * 0.5;
  > // value == 4 
  > ```



## Statements

In C++ we can turn an expression into a statement using the ```;```

Statements are the core of programming in C++, providing sequencing to the programs we write.

Statements are executed in order from top to bottom.



It is possible but entirely useless to create a statement from some expressions ``` 4 + 4;```

Usually an expression will be used to assign to a variable, were the result of the expression is stored in that variable:

```c++
int result = 4 + 4;
```

> Note that care should be taken with the ```=``` assignment operator. Don't confuse it with ```==``` which is used for comparison. 



When programming, don't forget to create statements to sequence your code. If you forget a ```;``` expect an error along the lines of " ```...expected a statement...``` "

# Tasks

**Tasks 1 - 3:** Programming with expressions variables and statements.



Tasks 1 - 3 are provided as a small c++ project. ***Fork*** and ***clone*** the following repo, write solutions and pass them to the relevant test functions.

**Task Repo:** ```https://gitlab.uwe.ac.uk/ng-renney/worksheet2_tasks```



Tasks are provided in code and you should follow the comments to provide solutions to all test functions.

With this repo cloned, you should be able to use ```ctrl + shift + b``` (```cmd``` on OS X), to run the build task - however, note you must select the correct task for your platform each time. 

*Remember to launch VS Code from the Developer console!*



**Task 4:** Check and commit

Check you solutions and then commit and push your solutions to you Gitlab repo using git.

You should have committed changes to **only** the **tasks.cpp**



Ensure that your changes are visible in you gitlab repo to confirm they are up to date and ensure that the permissions for the repo are set to '***internal***' so that we can view them!

