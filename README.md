# core-code-from-scratch-readme
Repository for Bootcamp "Core Code from scratch"

# Tuesday, April 4th
## Interpreted And Compiled Programming Languages
For the various programming languages, there are two ways to run them. These are: Compiled and Interpreted (and some languages use both).
Compiled languages are those where the complete code is taken and converted into machine language as a whole, this translation remains permanent and if changes were made to the original code it must be compiled again.
Interpreted languages, on the other hand, will be translated line by line at the time of execution. Therefore, it will use the original code and it will be modified in each execution

## Is Java compiled or interpreted, or both?
Java works through its own virtual machine, the JVM. Java being a high level language needs a process to be compiled into machine language.
Due to the differences between the machine languages of the operating systems, and the slowness of the interpretation, Java has a system to be in every operating system and with a faster process. The solution to this is to use both execution forms.
As a first step, compile the code to the JVM, and as a second step when executing, interpret this program to the language of the machine that is used.

## Pseudocode currency converter
  1. START
  2. dollars <-- GET
  3. bitcoin <-- 0.000022
  4. total <-- dollars * bitcoin
  5. PRINT total
  6. END
