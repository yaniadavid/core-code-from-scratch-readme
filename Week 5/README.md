# <center> Week 5 </center>
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
