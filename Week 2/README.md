# Week 2
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
