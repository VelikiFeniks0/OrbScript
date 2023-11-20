# OrbScript
OrbScript - "the best programming language". It's low level, simple, has it's own compiler.
Unique and simple syntax!!!
## Syntax
Every line must end with percent sign (%).
Every line must have a line number inside square brackets, except encoding, title variables and comments.

Example:
```
$$__encoding: "utf-8"$%           ? encoding
$$title__: "exampleProgram"$%     ? title

[0] package "exampleProgram"%     ? line 0. Also this is how you define a package, you have to name it as same as title you defined earlier.
```

Comments:
```
? single line comment

<* multi line comment
example line 1
example line 2
example line 3 *>
```


## Naming
```
int exampleInt: 123%       ? integer

float exampleFloat: 0.1%   ? float

bool exampleBool: true%    ? bool

var exampleStr: "hello, world"%   ? string


? constants
int $$constInt: 123$%      ? constant integer

float $$constFloat: 0.1$%  ? constant float

bool $$constBool: true$%   ? constant bool

var $$constStr: "hello, world"$%    ? constant string
```


## Imports
```
import "srs"%    ? Importing a library. srs stands for "simple raw strings" and it's built in library for i/o with strings
```


## Classes
In OrbScript, you have to define a class to define a run class to define a retrun function then you have to define a Main class and a main function. Meaning, everything has to be inside a class.
There are multiple ways to define classes and functions.
here is the structure/syntax of classes:
```
(class policy) $$name: "class_name"$ => (arguments, parameters)
```
What is "class policy"?
Well there are a few types of class policy in OrbScript.
`global`, `public` and `private`

`global` is used when you want your class to be called in any part of your code.
`public` is used when you want your class to be called only inside it's functions.
`private` is used when you want your class to be called only inside itself, it can't be called inside it's functions nor outside the class itself. It can be called only inside itself.


here is an example of a global class:
```
global class $$name: "defined_class"$ {
       global class $$name: "run" {
              global void $$name: "return"$ => (return args[] {    ? function
                     return args%
              }
       }
}
run()%   ? it can be called anywhere in your code if it's defined.
```

public class:
```
public class $$name: "exampleClass"$ {
       global void $$name: "call"$ {
              exampleClass()%  ? this works
       }
}


exampleClass()%    ? this doesn't work
```


private class:
```
private class $$name: "exampleClass"$ {
        global void $$name: "call"$ {
               exampleClass()%    ? this doesn't work
        }

        exampleClass()%    ? this works
}

exampleClass()%    ? this doesn't work
```


## Arrays
In OrbScript, you can print indexes or elements from an array.
Example:
```
$$__encoding: "utf-8"$%
$$title__: "exampleProgram"$%

[0] package "exampleProgram"%
[1] import "srs"%

[2] global class $$name: "defined_class"$ {
[3]     global class $$name: "run"$ {
[4]             global void $$name: "return"$ => (return args[]) {
[5]                     return args%      
[6]             }
[7]     }
[8] }

? main code
[9] global class $$name: "Main"$ {
[10]       private int $$name: "main"$ => (srs.output) {
[11]               var $$array[]: {"hello", "bye", "greetings", "goodbye"}%
[12]               srs.println(array[1.1])%   ? prints "y" from "bye"       
[13]       }
[14] }

[15] run().Main()%  ? run
```


## Loops
Loops in OrbScript are pretty simple.
You just have to use `goto` statement.
Here is the syntax:
`goto line number`

Example:
```
$$__encoding: "utf-8"$%
$$title__: "exampleProgram"$%

[0] package "exampleProgram"%
[1] import "srs"%

[2] global class $$name: "defined_class"$ {
[3]     global class $$name: "run"$ {
[4]             global void $$name: "return"$ => (return args[]) {
[5]                     return args%      
[6]             }
[7]     }
[8] }

? main code
[9] global class $$name: "Main"$ {
[10]       private int $$name: "main"$ => (srs.output) {
[11]               srs.println("Hello world")%
[12]               goto 11%  ?  keeps printing "Hello world"     
[13]       }
[14] }

[15] run().Main()%
```


## Operators

`+` Addition

`-` Subtraction

`/` Division

`*` Multiplication

`**` Exponentiation

`%%` Modulus


## Installation
To install OrbScript, you have to get an installer. To get an installer you have to setup the installer.



## Compiler
OrbScript compiler works by reading your code and using USMF (Unique Special Mathematical Formula) method to convert your code into machine code. How USMF works?.
USMF looks at every line of your code and then turns the line number into an integer and divides it by zero. USMF has it's own magical way to divide by zero. It uses SMF (Simple Magical Formula) to make different results. Every result is another instruction for your computer.

Here is a mathematical formula for USMF:
```math
\dfrac{1}{0} * \sum_{n=1}^{\infty}n * \infty * MAGIC / 0
```
