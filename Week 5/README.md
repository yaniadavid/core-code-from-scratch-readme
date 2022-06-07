<h1 align="center">Week 5</h1>
Lear about Typescript and Object Oriented Programming introduction

# Monday, May 8th
## Find The Missing Letter 
Write a method that takes an array of consecutive (increasing) letters as input and that returns the missing letter in the array. <br>
You will always get an valid array. And it will be always exactly one letter be missing. The length of the array will always be at least 2.
The array will always contain letters in only one case.

```javascript
function findMissingLetter(array){
  let count = 0;
  //Bucle que recorre según el Código Ascii hasta encontrar el caracter faltante
  for(let i = array[0].charCodeAt(); i < array[0].charCodeAt() + array.length; i++ ){
    //Si el codigo Ascii encontrado es diferente a i, retorna el letra faltante
    if(array[count].charCodeAt() !== i ){ return String.fromCharCode(i)}
    count++;
  }
  return ' ';
}
```

## Reverse or Rotate?
The input is a string str of digits. Cut the string into chunks (a chunk here is a substring of the initial string) of size sz (ignore the last chunk if its size is less than sz). <br>
If a chunk represents an integer such as the sum of the cubes of its digits is divisible by 2, reverse that chunk; otherwise rotate it to the left by one position. Put together these modified chunks and return the result as a string. <br>
<br>
If <br>
sz is <= 0 or if str is empty return "" <br>
sz is greater (>) than the length of str it is impossible to take a chunk of size sz hence return "". <br>

```javascript
function revrot(str, sz) {
  if(sz <= 0 || str === '' || sz >= str.length){return ""}
  let regex = new RegExp(`\\d{${sz}}`, 'g');
  let chunks = str.match(regex);
  let sum = 0;
  let chunkArray = [];
  let result = chunks.map((chunk) => {
    sum = chunk
      .split('')
      .map((digit) => Math.pow(+digit, 3))
      .reduce((prev, curr) => prev + curr, 0);
    chunkArray = chunk.split('');
    if (sum % 2 === 0) return chunkArray.reverse().join('');
    return chunkArray.push(chunkArray.shift()), chunkArray.join('');
  });
  return result.join('');
  
}
```

# Tuesday, May 8th
## [TypeScript Object Type](https://typescript-exercises.github.io/#exercise=1 "TypeScript Object Type")
Original:
```typescript
export type User = unknown;

export const users: unknown[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: users) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);
```
Solution: 
```typescript
export interface User { 
    name: string;
    age: number;
    occupation: string;
};

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];


export function logPerson(user: User) {        
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);
```

## [TypeScript Unions](https://typescript-exercises.github.io/#exercise=2 "TypeScript Unions")
Original:
```typescript
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = unknown;

export const persons: User[] /* <- Person[] */ = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);
```
Solution: 
```typescript
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: Person) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);
```
# Thursday
## [What's Your Poison?](https://www.codewars.com/kata/58c47a95e4eb57a5b9000094/train/javascript "What's Your Poison?")
You receive an array of integers (0 to 9), each of them is the number of a rat which died after tasting the wine bottles. Return the number of the bottle (1..1000) which is poisoned. 🐀
```javascript
function find(rats) {
    return rats.reduce(
  (previousValue, currentValue) => previousValue + Math.pow(2,currentValue), 0);
}
```

## [Array.diff](https://www.codewars.com/kata/523f5d21c841566fde000009/train/javascript "Array.diff")
It should remove all values from list a, which are present in list b keeping their order. 🔍
```javascript
function arrayDiff(a, b) {
  return result = a.filter((element) => !b.includes(element))
}
```

