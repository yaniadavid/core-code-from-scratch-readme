# core-code-from-scratch-readme
Repository for Bootcamp "Core Code from scratch"

# Tuesday, April 5th
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

# Wednesday, April 6th 
## Your date of birth in the matrix?
Year: 2002 <br><br>
2002 --> 1024 + 512 + 255 + 128 + 64 + 16 + 2 <br><br>
2002 - 2^10 = 2002 - 1024 = 978 <br>
978 - 2^9 = 978 - 512 = 466 <br>
466 - 2^8 = 466 - 255 = 210 <br>
210 - 2^7 = 210 - 128 = 82 <br>
82 - 2^6 = 82 - 64 = 18 <br>
18 - 2^4 = 18 - 16 = 2 <br>
2 - 2^1 = 2 - 2 = 0 <br>
<br>
| 2^10  | 2^9  | 2^8  | 2^7  | 2^6  | 2^5  | 2^4  | 2^3  | 2^2  | 2^1  | 2^0 |
| :------------: | :------------: | :------------: | :------------: | :------------: | :------------: | :------------: | :------------: | :------------: | :------------: | :------------: |
| 1 | 1 | 1 | 1 | 1 | 0 | 1| 0 | 0 | 1 | 0 |
<br>
2002 --> 11111010010

## MIPS
Create a program that displays yout name: <br>

     .data
            myName: .asciiz "\nYania Dávid\n"
      .text
            main:
                  li $v0, 4
                  la $a0, myName
                  syscall

Create a program that adds any two given numbers provided by the user: <br>

     .data
            number1: .asciiz "\nIngrese el primer numero: "
    	number2: .asciiz "\nIngrese el segundo numero: "
    	message: .asciiz "\nLa suma de los valores ingresados es: "
      .text
            main:
                  li $v0, 4
                  la $a0, number1
                  syscall
                  
                  li $v0, 5
                  syscall
                  
                  move $t0, $v0
                  
                  li $v0, 4
                  la $a0, number2
                  syscall
                  
                  li $v0, 5
                  syscall
                  
                  move $t1, $v0
                  
                  
                  add $t2, $t1, $t0
                  
                  li $v0, 4
                  la $a0 message
                  syscall
                  
                  li $v0, 1
                  move $a0, $t2
                  syscall



# Thursday, April 7th
## Print special numbers
```javascript
console.log('Even Numbers from 0 to 100');
console.log('With For -->');
var num = 0;
for(let i = 0; i < 101; i++){
    if(num % 2 == 0) console.log(num);
    num+=1;
}
```

## Bad Code
Original Code --> 
```javascript
var cond = false;

if ((cond = true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```

Solution -->
```javascript
var cond = false;

if ((cond == true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```

## Bad Code 2
Original Code --> 
```javascript
var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
if (n < 1000) {
  console.log('');
} else {
  console.log('Just a regular number');
}
if (n % 10 == 0) {
  console.log('This number is multiple of 10');
}
```

Solution -->
```javascript
if(n % 10 == 0){
    if(n<1000){
        if(n==100){
            console.log('This is a special number!');
        }else{
            console.log('This number is almost special');
        }
    }
}else{
    console.log('Just a regular number');
}
```

# Tuesday, April 19th
## Multiply exercise
```javascript
function multiply(a, b) {
  a * b;
}
```

```javascript
function multiply(a, b) {
  return a * b;
}
```

