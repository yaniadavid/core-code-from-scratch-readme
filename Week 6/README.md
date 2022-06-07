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
