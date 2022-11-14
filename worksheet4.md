```UFCFGL-30-1 Programming in c++```
# Conway's Game of Life

```c++
#include <cstdio>
int main(){
    printf("Welcome to programming in C++! Let's get setup...\n");
    return 0;
};
```

The marking scheme for this session is as follows:

- Task 1 : 15 marks
- Task 2 : 15 marks
- Task 3 : 15 marks
- Task 4 : 15 marks 
- Task 5 : 30 marks 
- Task 6 : 10 marks 
- Task 7 : 0 marks 



In this worksheet we will explore writing and calling functions by implementing the rules to Conways Game of life. 

A project is provided for you at the following link:

https://gitlab.uwe.ac.uk/ng-renney/worksheet4_tasks



You should **Fork** this repo, **then clone** the repo that is created in ***your*** account into an appropriate directory. Don't forget to read this worksheet to better understand functions before attempting the tasks.

```bash
# Note this link is not correct - you need to use your url
git clone https://gitlab.uwe.ac.uk/your-username/worksheet4_tasks
```



This task requires programming using all the skills you have accumulated so far, plus the definition and use of your own functions.



# Functions



We have already looked at functions in worksheet 3 in the context of the 'main' function. 

There are two components of functions that we should first consider. 

- A **definition** is the code that *defines* what a function does.
- A **function call** is the use of that function.

> We should also note that we can **declare** functions - which is a way of saying a function exists without defining it yet. This is useful in certain situations that we will see in later worksheets



## Function Definitions



In c++, function definitions take the form, ```return type``` **function_name** ( ```arguments``` ), followed by curly braces ```{ }``` which contain the body of the function.

Like variables, we can use alphanumeric values and underscores for function names. The name must start with a letter and is case sensitive. 

Like an expression, a function is evaluated to a single type (we say returns for a function).Therefore, we must write a return type for the function. We use the ```return``` keyword to indicate a value that should be returned (this value can be a literal, a variable or the result of an expression).

We can write a function using this information that takes no arguments:

```c++
int get_number_ten(){
	return 10;
}
```



If we wish to define a function that acts on values from outside it's scope, we can pass them in as arguments. Arguments are declared like variables, inside the parenthesis ```( )``` and will then exist inside the curly braces ```{ }``` of the function definition and can be separated by commas ```,``` to add multiple arguments.

```c++
int add(int a, int b){
	//returns the result of the expression a + b
	return a + b; 
}
```



If we have a function that only performs some side effect (such as printing a value), we can use the type ```void``` as the return type, to indicate nothing is returned. In this case we do not need to use the ```return``` keyword (though it can be called without a value to return early)

```c++
void print_hello(){
	std::cout << "Hello there!\n";
}
```



## Calling Functions



For the code in a function to be executed, the function must be called somewhere. This will typically mean the function needs to be called from inside another function (such as the entry function **main**!).

> Assume the following examples are called from inside main.



To call a function the function name, followed by parenthesis ```( )```  is used. Functions calls are expressions, meaning that they can be used anywhere an expression can. For example, we can call a function on it's own and use the semicolon to turn it into a statement (meaning it is executed).

```c++
print_hello();
```



We can also call a function in an expression used to initialise/assign to a variable:

```c++
int answer = 10 + get_number_ten();
// answer == 20
```



We can call functions that have arguments by passing in a value in the position that the argument was named:

```c++
int result = add(10,10);
//result == 20
```



As functions return values, we can even use functions to return values for arguments:

```c++
int result = add( 10, get_number_ten() );
//result == 20
```



When that function is run, the value passed in will substitute the arguments and allow the function to be computed. 



# Tasks



You can find a definition of the rules for Conway's Game of life on Wikipedia:

https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life



**Task 1 -** Define the ```rule_one``` function in tasks.cpp for rule one of Conways Game of Life.

> A living cell with less than two living neighbours dies



**Task 2 -** Define the ```rule_two``` function in tasks.cpp for rule two of Conways Game of Life.

> A living cell with two or three living neighbours remains alive



**Task 3 -** Add and define the ```rule_three``` function in tasks.cpp for rule three of Conways Game of Life.

> A living cell with more than three living neighbours dies



**Task 4 -** Add and define the ```rule_four``` function in tasks.cpp for rule four of Conways Game of Life.

> A dead cell with three living neighbours becomes a live cell



**Note -** *You may uncomment the test block in tasks .cpp to test your rules. It is acceptable to submit this way however you will therefore not access the marks available for task 5*



**Task 5 -** Using the Pseudocode below and the library available in the ```gol``` namespace, implement the main function to step through each generation of the Game of life and render out the image frame by frame.



```python
InitialiseGameOfLife
SeedGrid
WriteFrame

NumberOfFrames = 100

for NumberOfFrames {

  for x in Grid {
    for Y in Grid {
      rule_one x y
      rule_two x y
      rule_three x y
      rule_four x y
    }
  }
  WriteFrame
 }
  
RenderImage
```



**Task 6 -** Using the information in the worksheet4_tasks project readme.md file (seen on gitlab) and the GoL wiki (see resources), create your own pattern that explores Conway's Game of Life.



**Task 7 -** As ever, ensure you commit and push your work to Gitlab!



# Resources



- Wikipedia Article on Conways Game of Life [here](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life)

- The Game of Life Wiki [here](https://www.conwaylife.com/wiki/Main_Page) is great for finding more advanced patterns etc.
- Bens videos on Loops [here](https://uwe.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=e8c401e0-8d01-4b3d-ae20-ac5201055a31&instance=Blackboard) and Conditionals [here](https://uwe.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=0748132a-18f4-4135-aca0-ac520105598b&instance=Blackboard)

