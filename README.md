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

## ASCII TOTAL
```javascript
function uniTotal (string) {
  let sum = 0;
  for(let i = 0; i < string.length; i++){
    sum += string.charCodeAt(i);
  }
  return sum;
}
```
## Char from ASCII value
```javascript
function getChar(c){
  return String.fromCharCode(c)
}
```
## Binary Addition
```javascript
function addBinary(a,b) {
  return (a+b).toString(2)
}
```
## Student's Final Grade
```javascript
function finalGrade (exam, projects) {
  if(exam > 90 || projects > 10){
    return 100
  }
  if(exam > 75 && projects >= 5){
    return  90
  } 
  if(exam > 50 && projects >= 2){
    return 75
  }
  return 0
}
```

# Wednesday, April 20
## Holiday VII - Duty Free
```javascript
function dutyFree(normPrice, discount, hol){
  let duty = normPrice * (discount/100)
  let quantity = hol / duty
  return Math.floor(quantity)
}
```

## Twice as Old
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  return Math.abs(dadYearsOld - (sonYearsOld * 2))
}
```

## Valid Space
```javascript
function validSpacing(s) {
  if(s[0] === " " || s[s.length - 1] === " "){
    return false
  }
  
  for(let i = 0; i < s.length; i++){
    if(s[i] === ' '){
      if(i != 0 && s[i-1] === ' ') {
        return false;
      }
      if(i != (s.length - 1) && s[i+1] === ' ') {
        return false;
      }
    }
  }
  
  return true
}
```
## Fake Binary
```javascript
function fakeBin(x){
  let result = ''
  for(let i = 0; i < x.length; i++){
    if(x[i] < 5){
      result += '0';
    }else{
      result += '1';
    }
  }
  return result;
}
```

# Thursday, April 21
## Remove All Exclamation Marks From The End of Sentence
```javascript
function remove (string) {  
  let end = string.length - 1;
  for(let i = string.length - 1; i > 0; i--){
    if(string[i] !== '!'){
      return string.substring(0, i + 1)
    }
  }
}
```

## Vowel Remover
```javascript
function shortcut (string) {
  let result = '';
  for(let i = 0; i < string.length; i++){
    if(string[i] !== 'a' && string[i] !== 'e' && string[i] !== 'i' && string[i] !== 'o' && string[i] !== 'u'){
      result += string[i]
    }
  }
  return result;
}
```
## Rock Paper Scissors
```javascript
const rps = (p1, p2) => {
  if(p1 == p2){
    return 'Draw!'
  }else if(p1 == 'rock' && p2 == 'scissors' || p1 == 'scissors' && p2 == 'paper' || p1 == 'paper' && p2 == 'rock'){
    return 'Player 1 won!'
  }else{
    return 'Player 2 won!'
  }
};

```

# Monday, April 25
## Who Likes it?
```javascript
function likes(names) {
  if(names.length == 0){return 'no one likes this'}
  if(names.length == 1){return names[0] + ' likes this'}
  if(names.length == 2){return names[0] + ' and ' + names[1] +' like this'}
  if(names.length == 3){return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this'}
  if(names.length >= 4){let quantity = names.length - 2;
    return names[0] + ', ' + names[1] + ' and ' + quantity + ' others like this'}
}
```

## Bit Counting
```javascript
var countBits = function(n) {
  let bin = n.toString(2);
  let count = 0;
  for(let i = 0; i < bin.length; i++){
    if(bin[i] == 1){
      count += 1;
    }
  }
  return count;
};
```

## You Order, Please
```javascript
function order(words){
  let array_words = words.split(" ");
  let good_words = []
  let array_numbers = []
  for(let i = 0; i < array_words.length; i++){
    for(let j = 0; j < array_words[i].length; j++){
      if((array_words[i][j] == 1 || array_words[i][j] == 2 || array_words[i][j] == 3
      || array_words[i][j] == 4 || array_words[i][j] == 5 || array_words[i][j] == 6
      || array_words[i][j] == 7 || array_words[i][j] == 8 || array_words[i][j] == 9 )){
        good_words[array_words[i][j]] = array_words[i];
      }
    }
  }

  let result = good_words.join(' ')
  if(result[0] == ' '){
    result = result.slice(1, result.length )
  }
  return result;
}

```

# Tuesday, April 26
## Pig Latin
```javascript
function pigIt(str){
  let array_words = str.split(" ");
  let pig_words = []
  let temp;
  let pMarks = ['!', '¡', '?', '¿', '.', ',', ':', ';'];
  for(let i = 0; i < array_words.length; i++){
    if (pMarks.indexOf(array_words[i]) >= 0) {pig_words[i] = array_words[i]; continue;}
    temp = '';
    for(let j = 1; j < array_words[i].length; j++){
       temp += array_words[i][j];
    }
    temp += array_words[i][0];
    temp += 'ay'
    pig_words[i] = temp;
  }
  return pig_words.join(' ')
}
```

# Wednesday, April 27
## Valid Parentheses
```javascript
function validParentheses(parens) {
  let count = 0;
  for(let i = 0; i < parens.length; i++){
    if(parens[i] == '(') count++;
    if(parens[i] == ')') count--;
    if(count < 0) return false;
  }
  return count === 0;
}
```

## Convert String to camel case
```javascript
function toCamelCase(str){
  let result = '';
  for(let i = 0; i < str.length; i++){
    if(i != 0 && str[i - 1] === '_' || str[i - 1] === '-'){
      result += str[i].toUpperCase();
    }else if(str[i] != '_' && str[i] != '-'){
      result += str[i];
    }
  }
  return result;
}
```

## Unique in Order
```javascript
function toCamelCase(str){
  let result = '';
  for(let i = 0; i < str.length; i++){
    if(i != 0 && str[i - 1] === '_' || str[i - 1] === '-'){
      result += str[i].toUpperCase();
    }else if(str[i] != '_' && str[i] != '-'){
      result += str[i];
    }
  }
  return result;
}
```
