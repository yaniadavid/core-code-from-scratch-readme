<h1 align="center">Week 7</h1>

Lear about interfaces, data modifiers and function types, along with how to interact with the console using typescript

# Monday, May 23rd
## Input/Output
[Example Project](https://github.com/yaniadavid/core-code-from-scratch-readme/tree/main/Week%207/inout)

## OOP Glosary
Abstraction
Inheritance
Polymorphism
Encapsulation
Class
Object
Instance
Interface
Access Modifiers
Constructors

# Wednesday, May 25th
## [Build Tower](https://www.codewars.com/kata/576757b1df89ecf5bd00073b/train/typescript "Build Tower")
Build a pyramid-shaped tower given a positive integer number of floors. A tower block is represented with "*" character. 🗼
```typescript
export const towerBuilder = (nFloors: number): string[] => {
  let space = "";
  let star = "";
  let result = [];
  for (var i = 1; i <= nFloors; i++) {
    space = (" ").repeat(nFloors - i);
    star = ("*").repeat((2 * i) - 1);
    result.push(space + star + space);
  }
  return result;
}
```

## [Meeting](https://www.codewars.com/kata/59df2f8f08c6cec835000012/train/typescript "Meeting")
Could you make a program that 📩 <br>
makes this string uppercase <br>
gives it sorted in alphabetical order by last name. <br>
```typescript
export function meeting(s: string): string {
  return s
    .toUpperCase()
    .split(';') //Separa cada Persona (con nombre y apellido)
    .map((n: string) => '(' + n.split(':').reverse().join(', ') + ')') //Crea el arreglo separando por nombre y apellido, entre parentesis
    .sort() //Ordena
    .join(''); //Une en un string
}
```


