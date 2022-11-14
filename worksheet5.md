```UFCFGL-30-1 Programming in c++```

# Worksheet 5:

## Arrays, Strings and String Manipulation

```c++
#include <iostream>
int main(){
  	char title[9] = {'S','t','r','i','n','g','s','\n','\0'};
		std::cout << title;
    return 0;
};
```

The marking scheme for this session is as follows:

- Task 1 : 30 marks
- Task 2 : 30 marks
- Task 3 : 40 marks
- Task 4 : 0 marks 



A project is provided for you at the following link:

https://gitlab.uwe.ac.uk/br-gaster/worksheet5_tasks



You will also **need to install Python** for this worksheet if you do not already have it.

https://www.python.org/downloads/windows/



## C Style Strings

Whilst we have the option of using ```std::string``` in C++, it is important to understand how the C programming language represents strings too.



C uses arrays of characters as strings and denotes the end of a string with the 'null terminator' 

character: ```\0```.

This means that a C string always needs to be oversized by one character to accommodate the null terminator.

Fortunately, rather than having to initialise each element individually, we can use a string literal to assign to a ``` char``` array and the null terminator will automatically be added (so we just need to ensure the size is correct.)

```c++
char str[8] = "String\n";
```



This gives us the following array. Note that ```\n``` and ```\0``` are single characters as far as the compiler is concerned. 

| [0]  | [1]  | [2]  | [3]  | [4]  | [5]  | [6]  | [7]  |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | ---- |
|  S   |  t   |  r   |  i   |  n   |  g   |  \n  | \0   |



## Accessing Array Elements / Manipulating Strings



The most basic and common way to access elements in an array is using a variable as an index into the array. Using a ```for``` loop, we can increment the variable to move through the range of accepted values.

As we know, we can declare and increment a variable a for loop (see previous worksheets and videos to revise the for loop if you are unsure). By ensuring we count up to one less that the length of a string (remember elements start at zero), we can use this variable as the index.

Here's an example where we get the length of a string by using the ```strlen()``` function (found in ```#include <cstring>```):

```c++
char str[8] = "String\n";
int len = std::strlen(str);
for(int i = 0; i < len; i++){
	std::cout << "letter at pos: " << i << " is: " << str[i] <<'\n';
}
```

> Note ```strlen``` counts up to a null terminator, but does not include it. This means that we can leave it unaffected and continue to use the string as a null terminated c string. For use with other arrays, ```sizeof()``` should be used.



Instead of printing using c++, you can manipulate a string by accessing the individual elements (in this example using ```str[i]``` for the current element in the array called ```str```). You can then assign to this value using the assignment operator ```=```.



For example, we can replace each character with an x, using the following code:

```c++
char str[8] = "String\n";
int len = std::strlen(str);
for(int i = 0; i < len; i++){
	 str[i] = 'x';
}
std::cout << str <<'\n';
```



## Cyphers



What is Caesar Cipher?

Supposedly, Caesar (yes, that Caesar) used to "encrypt" (i.e., conceal in a reversible way) confidential messages by shifting each letter therein by some number of places. For instance, he might write A as B, B as C, C as D, …, and, wrapping around alphabetically, Z as A. And so, to say HELLO to someone, Caesar might write IFMMP. Upon receiving such messages from Caesar, recipients would have to "decrypt" them by shifting letters in the opposite direction by the same number of places.

The secrecy of this "cryptosystem" relied on only Caesar and the recipients knowing a secret, the number of places by which Caesar had shifted his letters (e.g., 1). Not particularly secure by modern standards, but, hey, if you’re perhaps the first in the world to do it, pretty secure!



Unencrypted text is generally called plaintext. Encrypted text is generally called ciphertext. And the secret used is called a key.

 

For more details check out the Wikipedia page:  https://en.wikipedia.org/wiki/Caesar_cipher





# Tasks



**Task 1 -** Implement the initials function that given a string, returns a users initials.



**Task 2 -** Implement Caesar Cypher



**Task 3 -** Implement the Substitution Cypher



**Task 4 -** Commit and push to git 

