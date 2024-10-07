# Introduction

### Language Processors
"_A compiler is a program that can read a program in one language (source language) and translate it into equivalent program in another language (target language)._"  
An important job of a compiler is to report any errors in the source program that it detects during translation process.  
  
Interpreter is another common kind of Language processor. Instead of producing a target program, it directly executes the instructions. 


### Structure of a Compiler 
The Compiler is divided into many parts:   
1. Frontend (Analysis)  
2. Intermediate Representation   
3. Backend (Synthesis)  
4. Lookup Table / Symbol Table   

Frontend performs checks on the syntax of the source code.  
The _synthesis_ part constructs desired program from intermediate representation and the information in the symbol table.  
Symbol table is used to store information about the source code (such as variable location in memory).  
  
These separations helps to design the compiler in a more modular fashion.  
For example: The same frontend can be used in all the OS/Architecture, as the syntax is dependent on them. And the Backend is where executable is made, and it uses architecture (ex:ARM, X86) specific code. And Intermediate Representation acts as an interface between Frontend & Backend.
   
Here's more of an detailed view of how things work out, think of each step as a sort of pipeline which connects to other step:  
First of the character stream is send to    
1. Lexical Analysis/ Scanner (which produces token stream).  
2. Parsing (It is where our syntax gets grammer)

