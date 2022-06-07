# Week 5
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
## [TypeScript Object Type](http://https://typescript-exercises.github.io/#exercise=1 "TypeScript Object Type")
