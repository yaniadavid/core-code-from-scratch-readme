# Week 3
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



