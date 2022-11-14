```UFCFGL-30-1 Programming in c++```

# Worksheet 6:

## Stacks & RPN Calculator

```c++
class Worksheet{
public:
    Worksheet(int n){
        sessionNo = n;
    }
    void whatSession(){
        printf("Worksheet %d", sessionNo);
    }
private:
    int sessionNo;
};

int main(){
    Worksheet worksheet(6);
    worksheet.whatSession();
    return 0;
}

```

The marking scheme for this session is as follows:

- Task 1 : 40 marks
- Task 2 : 60 marks
- Task 3 : 0 marks



# Stacks



Stacks are a common data structure in computer science and is easily understood with an analogy. A stack can be described using the operations you can apply to a stack of plates, where every plate is a piece of data.

When creating a stack of plates, you can only access the last plate that was placed on top of the stack. We describe this as being first in last out (abbreviated **FILO**). This is in contrast to something like a queue of people which would be First in First out. 

Given a stack of plates we can do the following:

- Add a plate to the top (push)
- Take a plate from the top (pop)
- Count the number of stacked plates (size)
- Check if there are any plates at all (empty)
- Check if the stack is as high as is possible (full)



These analogous operations represent the functions we require to implement a stack.

By then researching reverse Polish notation we can use the stack data structure to implement one and to see how useful stacks can actually be.



# Notes on Classes



For an introduction to Classes you should watch the lecture [here](https://ca-lti.bbcollab.com/recording/1761a921ebbf4f948e90d4a14bd17ef3).

### Using a class

Remember, as discussed in a lecture. Writing a class is like a blueprint. To use you class you need to create an instance of a class (in a similar way to how you declare a variable). You do this by providing the name of the class and then a name for you instance:

```c++
ClassName instance_name;
```



To call member functions, you will need to use the scope operator:

```c++
instance_name.function_call();
```



### Classes split between ```hpp``` and ```cpp``` 

Often, classes are split with declarations in ```.hpp``` files and the corresponding definitions for any member functions in a ```.cpp``` file.

This typically results in the following code:

#### example.hpp

```c++
class Example {
private:
  int data_member;
public:
  int get_data();
  void set_data(int x);
};
```

#### example.cpp

```c++
#include "Example.hpp"

int Example::get_data(){
  return data_member;
}
void Example::set_data(int x){
  data_member = x;
}
```

Note that in order for the function definitions in the ```.cpp``` file to access the internal members of the class (and appropriately define the member functions) the classes namespace is added to the function name with the ```::``` scope operator. For this to work, the ```.hpp``` file **must** be included.





# Tasks



To compile your program, you will need to select the main file and compile from there. Your program will not do anything unless you comment in/out the relevant functions. Use the ```test_stack();``` function when working on task 1 and then ensure you call the ```run();``` function to run your server and test the ```run_eval()``` function.



All of the files you will need to work on are found in the ```tasks/``` directory.

Please also refer to the Readme.md that is best view on the gitlab page for your project. For example [here](https://gitlab.uwe.ac.uk/br-gaster/worksheet6_tasks).



**Task 1 -** Implement a stack using the provided class as a starting point.

- You can find the empty stack class in the tasks directory, in files ```stack.hpp``` & ```stack.cpp```.

- You need to create a class that manages a stack of at least 256 ```integers```.
- You will need to add appropriate member variable(s) to ```stack.hpp```
- You will need to add appropriate function definitions to ```stack.cpp```



**Task 2 -** Using your stack class, implement the reverse polish notation calculator.

- You can find a good explanation of RPN in the related [wikipedia article (here)](https://en.wikipedia.org/wiki/Reverse_Polish_notation) and the popular computer science Youtube channel Computerphile also has an excellent video on how RPN is related to stacks [here](https://www.youtube.com/watch?v=7ha78yWRDlE).

- You need to implement the ```rpn_eval(std::string expr)``` function, found in ```rpn.cpp```. This function receives the expression that is input in the web client and you should return the answer as a string.
  - Note that this with require converting from string to a number then back to a string.
  - You should use your stack class to implement rpn
    - Push on any numbers in the expression
    - When an operator is found, pop the values off and apply the operator to them
    - Push the result back onto the stack and continue to push any remaining values in the expression



**Task 3 -** Commit and push your code to gitlab





