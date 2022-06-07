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


# Wednesday, May 4th
## Simple Validation Of A Username
Write a simple regex to validate a username. Allowed characters are: <br>
lowercase letters, <br>
numbers, <br>
underscore. <br>
Length should be between 4 and 16 characters (both included).
```javascript

function validateUsr(username) {
  res = /^([a-z]+|\d+|_){4,16}$/.test(username)
 
    //Regex between slashes --> / /
    //Start --> ^
    //End --> $
    //Length between 4 and 16 characters --> {4,16}
    //Lowercase --> [a-z]
    //Numbers --> \d
    //Underscore '_' --> _
    //Repeat one or more times --> +
    //OR --> |

  return res
}
```

## Get Number from String
Write a function which removes from string all non-digit characters and parse the remaining to number.
```javascript
function getNumberFromString(s) {
  
  const regexp = /\D/g; //--> \D todo excepto dígitos
  let numbers = s.replace(regexp, '') // --> reemplaza lo encontrado con el regex a ''
                                      
  return Number(numbers); // --> retorna en número                                 
}
```

# Thursday, May 5th
## String Cleaning
Your program will take in a string and clean out all numeric characters, and return a string with spacing and special characters ~#$%^&!@*():;"'.,? all intact.
```javascript
function stringClean(s){
  ///\d/g --> regex for digits
  return s.replace(/\d/g, '') //--> replace the digits on the text with ''
}
```

## Valid Password
You need to write regex that will validate a password to make sure <br>
[Kata Link](http://https://www.codewars.com/kata/52e1476c8147a7547a000811/train/javascript "Kata Link")
```javascript
function validate(password) {
  // least six characters long --> {6,}
  // contains a lowercase letter --> [a-z]+
  // contains an uppercase letter --> [A-Z]+
  // contains a number --> [0-9]+
  
  return (/^[a-zA-Z0-9]{6,}$/.test(password) 
        && /[a-z]+/.test(password)
        && /[A-Z]+/.test(password)
        && /[0-9]+/.test(password)
         );
}
```
