# Week 4
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
