# core-code-from-scratch-readme

## Week 1
### Date: 04/05/2022
**Interpreted and compiled programming languages**
1. Interpreted languages have a shared source code that can be run in most devices. The advantage of these programming languages is that they are easier to debug and make changes to them, without having to remake the whole code written for a certain app.
2. Compiled languages tend to be faster and allow the programmer to decide how the hardware will interact with the user. They are faster, but usually need an extra program to run in a variety of devices. For example, a program/app could be built in a compiled language but will need to be developed for Mac, Windows or Linux.

**Is Java compiled or interpreted, or both?**

Java program is first compiled into bytecode which JRE can understand. ByteCode is then interpreted by the JVM making it as interpreted language. Note that Java implementations typically use a two-step compilation process. Java source code is compiled down to bytecode by the Java compiler. The bytecode is executed by a Java Virtual Machine (JVM). Modern JVMs use a technique called Just-in-Time (JIT) compilation to compile the bytecode to native instructions understood by hardware CPU on the fly at runtime.

**Pseudocode Currency Converter exercise**
```
START

USD Amount <-- GET

BTCprice <-- GET FROM(https://www.coindesk.com/price/bitcoin/)

Total <-- USD Amount / BTCprice

PRINT Total

END
```

### Date: 04/06/2022

[**Your date of birth in the matrix?**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week01/exercises/e01/desc)

My DOB is 12/04/1994, which in binary is 1100/1/1111100101.

**MIPS Excercises**

[**1. Create a program that adds any two given numbers provided by the user**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week01/exercises/e02/desc)


```MIPS
  .data
	      number1: .asciiz "\nEnter Number 1 : "
	      number2: .asciiz "\nEnter Number 2: "
	      number3: .asciiz "\nResult: "
  .text
	      main:
              li $v0, 4
              la $a0, number1
              syscall

              li $v0, 5
              syscall

              move $t0, $v0

              li $v0, 4
              la $a0, number2
              syscall

              li $v0, 5
              syscall

              move $t1, $v0

              li $v0, 1
              move $a0, $t0
              syscall
              
              add $t2, $t1, $t0
              syscall
              
              li $v0, 4
              la $a0 number3
              syscall
              
              li $v0, 1
              move $a0, $t2
              syscall
```       

[**2. Create a program that displays your name**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week01/exercises/e02/desc)

```
.data
	      Name: .asciiz "\nMoises Benjamin Villagran Ortiz"
  .text
	      main:
              li $v0, 4
              la $a0, Name
              syscall
```


### Date: 04/07/2022

[**1. Print Special Numbers**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week01/exercises/e03/desc)
```javascript
for (var i = 0; i <= 100; i = i + 2) {
  console.log(i);
}
```

[**2. Bad Code 1**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week01/exercises/e04/desc)

By using the statement "cond = true", the variable value was changed and the statement was turned in a true statement. Also, when using and if...else statement, the condidition should be between one set of parenthesis not two. Even though I used the documentation on the exercies resources, when running it, it continues to print de "The cond variable is true". :(

```javascript
var cond = false;

if (cond) {
    console.log('The cond variable is true');
} else {
    console.log('The cond variable is false');
}
```

[**3. Bad Code 2**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week01/exercises/e05/desc)

The syntax was incorrect. It should have been: if, else if, else.
```javascript
var n = 100;

if (n == 100) {
    console.log('This is a special number!');
}
else if (n < 1000 && n % 10 == 0) {
    console.log('This is almost special');
} 
else {
    console.log('Just a regular number');
}
```


## Week 2
### Date: 04/19/2022
[**1. Multiply**](https://www.codewars.com/kata/50654ddff44f800200000004/train/javascript)
```javascript
function multiply(a, b){
 return a * b
}
```

[**2. ASCII Total**](https://www.codewars.com/kata/572b6b2772a38bc1e700007a/train/javascript)
```javascript
function uniTotal(str) {
  let count = 0;
  for (let i = 0; i < str.length; i++) {
    count += str.charCodeAt(i);
  }
  return count;
}
```

[**3. Char From ASCII Value**](https://www.codewars.com/kata/55ad04714f0b468e8200001c/train/javascript)
```javascript
function getChar(c){
return String.fromCharCode(c);
}
```

[**4. Binary Addition**](https://www.codewars.com/kata/551f37452ff852b7bd000139/train/javascript)
```javascript
function addBinary(a,b) {
let sum = a + b;
  return sum.toString(2);
}
```

[**5. Student's Final Grade**](https://www.codewars.com/kata/5ad0d8356165e63c140014d4/train/javascript)
```javascript
function finalGrade(exam, projects) {
  let total = 0;
  
  if (exam > 90 || projects > 10) {
  total = 100;
} else if (exam > 75 && projects >= 5) {
  total = 90;
} else if (exam > 50 && projects >= 2) {
  total = 75; 
} else {
  total = 0;
}
  return total;  
}
```

### Date: 04/20/2022

[**1. Holiday VIII - Duty Free**](https://www.codewars.com/kata/57e92e91b63b6cbac20001e5/train/javascript)
```javascript
function dutyFree(normPrice, discount, hol){
let result1 = ((normPrice * discount) / 100);
let result2 = hol / result1;
let result3 = Math.floor(result2);
  return result3;
}
```

[**2. Twice As Old**](https://www.codewars.com/kata/5b853229cfde412a470000d0/train/javascript)
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let difference = ((dadYearsOld - sonYearsOld) * 2) - dadYearsOld;
  return Math.abs(difference);
}
```

[**3. Valid Spacing Exercise**](https://www.codewars.com/kata/5f77d62851f6bc0033616bd8/train/javascript)
```javascript
function validSpacing(s) {
  if (s.length === 0) return true;
  if (s[0] === ' ' || s[s.length - 1] === ' ') return false;
  let aSpaces0 = s.split(' ');
  for (let i = 0, length = aSpaces0.length; i < length; i++) {
    if (aSpaces0[i] === '') return false;
  }
  return true;
}
```

[**4. Fake Binary**](https://www.codewars.com/kata/57eae65a4321032ce000002d/train/javascript)
```javascript
function fakeBin(x){
let digits = '';
    for (let i = 0; i < x.length; i++) {
      if (parseInt(x[i]) < 5){
        digits = digits + '0';
      } else {
        digits = digits + '1';
      }
    }
  return digits;
}
```

### Date: 04/20/2022
[**1. Remove All Exclamation Marks From The End Of Sentence**](https://www.codewars.com/kata/57faece99610ced690000165/train/javascript)
```javascript
function remove(inputString) {  
let result = inputString;
while (result[result.length - 1] === "!"){
  result = result.slice(0,-1);
}
  return result;  
}
```

[**2. Vowel Remover**](https://www.codewars.com/kata/5547929140907378f9000039/train/javascript)
```javascript
function shortcut(mytext) {
  return mytext.replace(/[aeiou]/g, '');
}
```

[**3. Rock Paper Scissors!**](https://www.codewars.com/kata/5672a98bdbdd995fad00000f/train/javascript)
```javascript
const rps = (user1, user2) => {
  let result = "";
  if (user1 === user2) {
    result = "Draw!";
  }
  else if (user1 === "paper" && user2 === "rock") {
    result = "Player 1 won!";    
  }
  else if (user1 === "scissors" && user2 === "paper") {
    result = "Player 1 won!";
  }
  else if (user1 === "rock" && user2 === "scissors") {
    result = "Player 1 won!";
  }
  else if (user1 === "paper" && user2 === "scissors") {
    result = "Player 2 won!";    
  }
  else if (user1 === "scissors" && user2 === "rock") {
    result = "Player 2 won!";
  }
  else if (user1 === "rock" && user2 === "paper") {
    result = "Player 2 won!";
  }
  return result
} 
```

[**4. Persistent Bugger**](https://www.codewars.com/kata/55bf01e5a717a0d57e0000ec/train/javascript)
```javascript
function persistence(num) {
  let counter = 0;
  
  let digits = num.toString().split(""); // 39 -> "39" -> ["3", "9"]
  
  while (digits.length > 1) {
    let results = 1;
    
    for (let i = 0; i < digits.length; i++){
      results = results * digits[i];
    }
    
    digits = results.toString().split("");
    
    counter = counter + 1;
  }
 
  return counter;
}
```

## Week 3
### Date: 04/25/2022
[**1. Who likes it?**](https://www.codewars.com/kata/5266876b8f4bf2da9b000362/train/javascript)
```javascript
function likes(names) {
  if (names.length == 0) return 'no one likes this';
  if (names.length == 1) return names[0] + ' likes this';
  if (names.length == 2) return names[0] + ' and ' + names[1] + ' like this';
  if (names.length == 3) return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this';
  return (names[0] +', ' + names[1] + ' and ' + (names.length - 2) + ' others like this');
}
```

[**2. Bit Counting**](https://www.codewars.com/kata/526571aae218b8ee490006f4/train/javascript)
```javascript
var countBits = function(n) {
   // make an array with the bit result
   const base = (n).toString(2).split('');
   
   // make a sum with the array and make the index a Number
   const result = base.reduce((sum, num) => sum + Number(num), 0);
   
   return result;
};
```

[**3. Your Order, Please**](https://www.codewars.com/kata/55c45be3b2079eccff00010f/train/javascript)
```javascript
function order(words){
  return words.split(' ').sort(function(a, b){
      return a.match(/\d/) - b.match(/\d/);
   }).join(' ');
}  
```
### Date: 04/26/2022
[**1. Simple Pig Latin**](https://www.codewars.com/kata/520b9d2ad5c005041100000f/train/javascript)
```javascript
function pigIt(str){
  let newArr = [];
  let strArr = str.split(" ")
  strArr.forEach(x => {
    let wordArr = x.split("")
    wordArr.push(wordArr[0], 'ay'), wordArr.shift()
    if (x === "!" || x === "?" || x === "." || x === "," || x === ";"){
      newArr.push(x)
    } else {
      newArr.push(wordArr.join(""))
    }    
  })
  return newArr.join(" ")
  
}
```
[**2. Counting Duplicates**](https://www.codewars.com/kata/54bf1c2cd5b56cc47f0007a1/train/javascript)
```javascript
function duplicateCount(text) {
  const splitString = text.toLowerCase().split("").sort();
  let results = [];

  for (let i = 0; i < splitString.length; i++) {
    if (splitString[i] === splitString[i + 1]) {
      results.push(splitString[i]);
    }
  }
  const setArray = new Set(results);
  return setArray.size;
}
```

[**3. Decode The Morse Code**](https://www.codewars.com/kata/54b724efac3d5402db00065e/train/javascript)
```javascript
decodeMorse = function(morseCode){
  morseCode = morseCode.trim();
  let refinedData = morseCode.split('   ');
  let result = [];
  
  for (let i = 0; i < refinedData.length; i++) {
    let temp = refinedData[i].split(' ');
    for (let j = 0; j < temp.length; j++) {
      if (MORSE_CODE[temp[j]]) {
        result.push(MORSE_CODE[temp[j]]);
      }
    }
    
    if (i !== refinedData.length - 1) {
    result.push(' ');
    }
  }
  return result.join('');
}
```
### Date: 04/27/2022
[**1. Valid Parentheses exercise**](https://www.codewars.com/kata/52774a314c2333f0a7000688/train/javascript)
```javascript
function validParentheses(parens) {
  let openNum = 0;
  for (let i = 0; i < parens.length; i++){
    if (parens[i] == "(") {
      openNum += 1;           
    } else {
      openNum -= 1;
    }
   
    if (openNum < 0){
      return false
    }    
  }
  if (openNum === 0){
    return true    
  } else {
    return false
  }
}
```
[**2. Convert String To Camel Case exercise**](https://www.codewars.com/kata/517abf86da9663f1d2000003/train/javascript)
```javascript
function toCamelCase(str){
  let strArray;
  
  
  if (str === ""){
    return "";    
  }
  
  if (str.indexOf("-") !== -1){
    strArray = str.split("-")
  } else {
    strArray = str.split("_")
  }
  
  let ccString = strArray[0];
  
  for (let i = 1; i < strArray.length; i++){
    ccString += capitalize(strArray[i]);           
  }
  
  return ccString
  
  }
    
  let capitalize = (str) => {
    return str[0].toUpperCase() + str.slice(1);
    
}
```
[**3. Unique In Order exercise**](https://www.codewars.com/kata/54e6533c92449cc251001667/train/javascript)
```javascript
var uniqueInOrder=function(iterable){
  let newArr = []
  for (i = 0; i < iterable.length; i++){
    if (iterable[i] != iterable[i+1]){
      newArr.push(iterable[i])      
    }    
  }  
  return newArr
}
```
### Date: 04/28/2022
[**1. Fold An Array exercise**](https://www.codewars.com/kata/57ea70aa5500adfe8a000110/train/javascript)
```javascript
function foldArray(array, runs) {
  const r = [];
  const c = array.slice();
  while (c.length) r.push(c.pop() + (c.shift() || 0));
  return runs - 1 ? foldArray(r, runs - 1) : r;
}
```

[**2. Encrypt This! exercise***](https://www.codewars.com/kata/5848565e273af816fb000449/train/javascript)
```javascript
var encryptThis = function(str) {
 if(str === '') {return '';
    }else {
        let s = str.split(' ');
        let x = s.map(element => {
            let a = element.split('');
            a[0] = element.charCodeAt(0);
            [a[1], a[a.length - 1]] = [a[a.length - 1], a[1]];
            return a.join('');});
      return x.join(' ');
    }
}
```

**3. 1st. Code Challenge: Mission Statement**

I'm a web developer who is uncomfortable being comfortable. I have a wide range of experiences in very diverse roles, such as customer service, quality assurance, learning and development, and accounting. Most of my work experiences have been in world-wide distributed teams at companies based off the USA. Now, I'm perfecting my software development skills to be one of the best in this industry. Fintech companies interest me the most, since their work and projects relate deeply to my passion for finance/accounting automation. Loyalty is my core value: if I'm asking it from you, you already got it from me.

## Week 4
### Date: 05/04/2022
[**1. Simple Validation Of A Username**](https://www.codewars.com/kata/56a3f08aa9a6cc9b75000023/train/javascript)
```javascript
function validateUsr(username) {
  return /^[a-z0-9_]{4,16}$/g.test(username); 
}
```
[**2. Get Number from String**](https://www.codewars.com/kata/57a37f3cbb99449513000cd8/train/javascript)
```javascript
function getNumberFromString(s) {
   return Number(s.match(/\d/g).join(''));
}
```
### Date: 05/04/2022
[**1. String Cleaning**](https://www.codewars.com/kata/57e1e61ba396b3727c000251/train/javascript)
```javascript
function stringClean(s){
  return s.replace(/\d/g, "");
}
```
[**2. Password Validation**](https://www.codewars.com/kata/52e1476c8147a7547a000811/train/javascript)
```javascript
function validate(password) {
    return /^(?=.*?[A-Z])(?=.*?[a-z])(?=.*?[0-9])[A-Za-z0-9]{6,}$/.test(password);
}
```
[**3. 2nd Core Challenge**](https://corecode.notion.site/LinkedIn-Boost-Guide-5974abb0f917458ea235d3288ac6c7d3)

## Week 5
### Date: 05/09/2020
[**1. Find The Missing Letter**](https://www.codewars.com/kata/5839edaa6754d6fec10000a2/train/javascript)
```javascript
function findMissingLetter(array){
  let first = array[0].charCodeAt(0)
  for (i = 0; i < array.length; i++){
    if (first + i !== array[i].charCodeAt(0)){
      return String.fromCharCode(first + i)
    }
  }
}
```
[**2. Reverse of Rotate?**](https://www.codewars.com/kata/56b5afb4ed1f6d5fb0000991/train/javascript)
```javascript
function revrot(str, sz) {
  //Validates initial conditions
  if (sz <= 0 || str == '' || sz > str.length) return '';
  const arr = [];
  //String to array
  const s = str.split('');
  //Defines the number of chunks according to 'sz' value
  while (s.length >= sz) {
    arr.push(s.splice(0, sz));
  }
  //Apply 'map' instruction to the array
  const res = arr.map((x) => {
    //Calculate the sum of the cubes of the digits in the array
    const sum = x.reduce((a, c) => a + Math.pow(c, 3), 0);
    //Validate if the sum is divisible by 2
    if (sum % 2) {
      //Sent first digit to the back
      x.push(x[0]);
      x.shift();
      return x.join('');
    } else {
      //Reverse chunk
      return x.reverse().join(''); 
    }
  });
  //Show result
  return res.join('');
}
```
### Date: 05/10/2022
[**1. TypeScript Object Type**](https://typescript-exercises.github.io/#exercise=1&file=%2Findex.ts)
```typescript
export interface User {
    name: string;
    age: number;
    occupation: string;
}

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
[**2. TypeScript Unions**](https://typescript-exercises.github.io/#exercise=2)
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
```

