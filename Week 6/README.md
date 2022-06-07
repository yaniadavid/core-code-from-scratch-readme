<h1 align="center">Week 6</h1>
Learn about classes, instances, inheritance and data type with Typescript

# Monday, May 16th
## [Square(n) Sum](https://www.codewars.com/kata/515e271a311df0350d00000f/train/typescript "Square(n) Sum")
Complete the square sum function so that it squares each number passed into it and then sums the results together.
```typescript
export function squareSum(numbers: number[]): number {
    return numbers.reduce(
      (prev: number, curr: number) => prev + Math.pow(curr,2), 0
    );
}
```
## [Growth Of A Population](https://www.codewars.com/kata/563b662a59afc2b5120000c6/train/typescript "Growth Of A Population")
the function nb_year should return n number of entire years needed to get a population greater or equal to p.
```typescript
export class G964 {
    public static nbYear = (p0, percent, aug, p) => {
        for(var y = 0; p0 < p; y++){
          p0 = parseInt(p0 * (1 + percent / 100) + aug);
        }
      return y
    }
}
```
## [Mumbling](https://www.codewars.com/kata/563b662a59afc2b5120000c6/train/typescript "Mumbling")
📖
```typescript
export function accum(s: string): string {
  let text: string = ''
  for(let n = 0; n < s.length; n++){
    if(n == 0){text += s[n].toUpperCase();}
    else{
      for(let i = 0; i < n; i++){
      if(i == 0){text += s[n].toUpperCase();}
      text += s[n].toLowerCase();
    }
    }
    if(n !== s.length - 1){text += '-'}
  }
  return text
}
```
## [A Wolf In Sheep's Clothing](https://www.codewars.com/kata/5c8bfa44b9d1192e1ebd3d15/train/typescript "A Wolf In Sheep's Clothing")
Warn the sheep in front of the wolf that it is about to be eaten. 🐑
```typescript
export function warnTheSheep(queue: string[]): string {
  const thewolf = queue.indexOf('wolf');
  if(thewolf == queue.length - 1){
    return 'Pls go away and stop eating my sheep';
  }else{
    let thesheep = Math.abs(thewolf + 1 - queue.length);
    return 'Oi! Sheep number '+ thesheep + '! You are about to be eaten by a wolf!'
  }
}
```

# Tuesday, May 17th
## [A Rule Of Divisibility By 13](https://www.codewars.com/kata/564057bc348c7200bd0000ff/train/typescript "A Rule Of Divisibility By 13")
"A divisibility rule is a shorthand way of determining whether a given integer is divisible by a fixed divisor without performing the division, usually by examining its digits." 
```typescript
export function warnTheSheep(queue: string[]): string {
  const thewolf = queue.indexOf('wolf');
  if(thewolf == queue.length - 1){
    return 'Pls go away and stop eating my sheep';
  }else{
    let thesheep = Math.abs(thewolf + 1 - queue.length);
    return 'Oi! Sheep number '+ thesheep + '! You are about to be eaten by a wolf!'
  }
}
```

## [Playing with digits](https://www.codewars.com/kata/5552101f47fc5178b1000050/train/typescript "Playing with digits")
we want to find a positive integer k, if it exists, such that the sum of the digits of n taken to the successive powers of p is equal to k * n. 
```typescript
export class G964 {
    public static digPow = (n: number, p: number) => {
        const tot = n.toString()
                      .split('')
                      .map(Number)
                      .reduce((prev: number, curr: number) => prev + Math.pow(curr, p++), 0);
      if (tot % n === 0) return tot / n;
      return -1;
    }
}
```

## [Valid Braces](https://www.codewars.com/kata/5277c8a221e209d3f6000b56/train/typescript "Valid Braces")
Write a function that takes a string of braces, and determines if the order of the braces is valid. It should return true if the string is valid, and false if it's invalid.📎
```typescript
export function validBraces(braces: string): boolean {
  while(/\(\)|\[\]|\{\}/g.test(braces)){
   braces = braces.replace(/\(\)|\[\]|\{\}/g, '')
  }
  return braces.length === 0
}
```

## [Tic-Tac-Toe-like table Generator](https://www.codewars.com/kata/5b817c2a0ce070ace8002be0/train/javascript "Tic-Tac-Toe-like table Generator")
TicTacToe 🕹
```javascript
function displayBoard(board, width){
  let n = 0;
  let text = '';
  let line = '';
  for(let i = 0; i < board.length / width; i++){
    for(let j = 0; j < width; j++){
      if(j == width - 1){text += ' ' + board[n] + ' ';
                        line += '---'}else{
      text += ' ' + board[n] + ' |'
      line += '----'}
      n++;
    }
    if(i !== (board.length / width) - 1){
    text += '\n' + line + '\n';
    line = '';}
  }
  return text
}
```

# Wednesday, May 18th
## [Duplicate Encoder](https://www.codewars.com/kata/54b42f9314d9229fd6000d9c/train/typescript "Duplicate Encoder")
The goal of this exercise is to convert a string to a new string where each character in the new string is "(" if that character appears only once in the original string, or ")" if that character appears more than once in the original string. Ignore capitalization when determining if a character is a duplicate. ⚙
```javascript
export function duplicateEncode(word: string){
   return word.toLowerCase().split('').map((l: string, i: number, w: string[]) => {
                                           if(w.indexOf(l) == w.lastIndexOf(l)){
                                                return '(' 
                                            }else{
                                                return ')'
                                            }             
                                           }
   ).join('');
}
```
