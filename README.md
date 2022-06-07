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
### Date: 05/09/2022
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

### Date: 05/12/2022
[**1. What's Your Poison?**](https://www.codewars.com/kata/58c47a95e4eb57a5b9000094/train/javascript)
```javascript
function find(rats) {
  return rats.reduce((a,b)=>a+Math.pow(2,b),0)
}
```

[**2. Array.diff**](https://www.codewars.com/kata/523f5d21c841566fde000009/train/javascript)
```javascript
function arrayDiff(a, b) {
  return a.filter(e => !b.includes(e));
}
```

## Week 6
### Date: 05/16/2022
[**2. Square(n) Sum**](https://www.codewars.com/kata/515e271a311df0350d00000f/train/typescript)

```typescript
export function squareSum(numbers: number[]): number {
  return numbers.reduce((a,b) => a+Math.pow(b,2),0)

}
```

[**3. Growth Of A Population**](https://www.codewars.com/kata/563b662a59afc2b5120000c6/train/typescript)

```typescript
export class G964 {
    public static nbYear = (p0, percent, aug, p) => {
        let years = 0;
        for (years; p0 < p; years++) {
          p0 += parseInt(p0 * (percent / 100) + aug);
        }
        return years;
    }
}
```

[**4. Mumbling**](https://www.codewars.com/kata/5667e8f4e3f572a8f2000039/train/typescript)

```typescript
export function accum(s: string): string {
  const result = []
  const lowerStr = s.toLowerCase()

  for(let i = 0; i < lowerStr.length; i++) {
    let str = lowerStr[i].toUpperCase()
    for(let j = 0; j < i; j++) {
      str += lowerStr[i]
    }
    result.push(str)
  }

  return result.join("-")
  
}
```

[**5. A Wolf In Sheep's Clothing**](https://www.codewars.com/kata/5c8bfa44b9d1192e1ebd3d15/train/typescript)

```typescript
export function warnTheSheep(queue: string[]): string {
    if (queue[queue.length -1] === 'wolf') {
    return 'Pls go away and stop eating my sheep';
    } else {
     let index = queue.findIndex( (x) => x == 'wolf' );
     return `Oi! Sheep number ${queue.length - index - 1}! You are about to be eaten by a wolf!`;
    }
}
```

### Date: 05/17/2022
[**1. A Rule Of Divisibility By 13**](https://www.codewars.com/kata/564057bc348c7200bd0000ff/train/typescript)
```typescript
export function thirt(n: number): number {
  let remainders: number[] = [1, 10, 9, 12, 3, 4];
  let result = n
    .toString()
    .split('')
    .reverse()
    .map((c: string, i: number) => parseInt(c) * remainders[i % 6])
    .reduce((p: number, c: number) => (p += c));
  return n == result ? result : thirt(result);
}
```

[**2. Playing with digits**](https://www.codewars.com/kata/5552101f47fc5178b1000050/train/typescript)
```typescript
export function thirt(n: number): number {
  let remainders: number[] = [1, 10, 9, 12, 3, 4];
  let result = n
    .toString()
    .split('')
    .reverse()
    .map((c: string, i: number) => parseInt(c) * remainders[i % 6])
    .reduce((p: number, c: number) => (p += c));
  return n == result ? result : thirt(result);
}
```

[**3. Valid Braces**](https://www.codewars.com/kata/5277c8a221e209d3f6000b56/train/typescript)

```typescript
export function validBraces(braces: string): boolean {
  while (/\(\)|\[\]|\{\}/g.test(braces)) {
    braces = braces.replace(/\(\)|\[\]|\{\}/g, '');
  }
  return braces.length === 0;
}
```

[**4. Tic-Tac-Toe**](https://www.codewars.com/kata/5216a87cbf53a9c30f0000dc/train/javascript)

```javascript
function solveTTT(b) {
  var xwin = [
    [0, 1, 2],
    [3, 4, 5],
    [6, 7, 8],
    [0, 3, 6],
    [1, 4, 7],
    [2, 5, 8],
    [0, 4, 8],
    [2, 4, 6],
  ];
  for (var i in xwin)
    if (xwin[i].map((x) => b[x]).join('') == 'XX')
      return xwin[i].reduce((x, y) => (b[y] == '' ? x + y : x), 0);
  for (var i in b) if (b[i] == '') return +i;
}
```

[**5. Tic-Tac-Toe-like table Generator**](https://www.codewars.com/kata/5b817c2a0ce070ace8002be0/train/javascript)

```javascript
function displayBoard(board, width){
  let result = '';
  let currentCol = 0;
  for (let i = 0; i < board.length; i++) {
    const element = board[i];
    result += ` ${element} ${currentCol === (width - 1) ? '\n' : '|'}`;
    currentCol++;
    if (currentCol == width) {
      currentCol = 0;
      if (i !== board.length - 1) {
        result += '-'.repeat((width * 3) + (width - 1)) + '\n';
      }
    }
  }
  result = result.slice(0, -1);
  return result;
}
```

### Date: 05/18/2022
[**1. Duplicate Encoder**](https://www.codewars.com/kata/54b42f9314d9229fd6000d9c/train/typescript)
```typescript
export function duplicateEncode(word: string){
    return word
    .toLowerCase()
    .split('')
    .map((a: string, i: number, w: string[]) => {
      return w.indexOf(a) == w.lastIndexOf(a) ? '(' : ')';
    })
    .join('');  
}
```

[**2. Find the odd int**](https://www.codewars.com/kata/54da5a58ea159efa38000836/train/typescript)
```typescript
export function findOdd(xs: number[]): number {
  return (
    xs.find(
      (x: number, i: number, a: number[]) =>
        a.filter((y: number) => y === x).length % 2 === 1
    ) || -1
  );
}
```

[**3. Which Are In?**](https://www.codewars.com/kata/550554fd08b86f84fe000a58/train/typescript)
```typescript
export class G964 {
  // inArray is a function that takes in two string-array parameters
  // to compare the second string-array parameter with the first string-array 
  // parameter in order to retrieve a string-array containing the first string-array
  // parameter elements which are contained in one or more elements of the
  // second string-array parameter.
  public static inArray(a1: string[], a2: string[]): string[] {
    // result is the store string-array that we utilize to store the final result
    // elements.
    let result : string[] = [];
    // Loop starts.
    for(let wordA1 in a1){
      for(let wordA2 in a2){
        // We check if second string-array parameter elements contain the 
        // first string-array as well as if we have already put this in the result
        // array that we output at the end of this function.
        if (a2[wordA2].indexOf(a1[wordA1]) >= 0 && result.indexOf(a1[wordA1]) < 0) {
          result.push(a1[wordA1]);
        }
      }
    }
    // Finally we sort the result string-array alphabetically.
    return result.sort();
  }
}
```

[**4. Sums of Parts**](https://www.codewars.com/kata/5ce399e0047a45001c853c2b/train/typescript)
```typescript
export function partsSums(ls: number[]): number[] {
  // We create an empty array that will contain the sum of all the numbers per iteration
  const response: number [] = [];
  //By using the reduce property with "ls" we sum all the numbers in the array and send each loop sum iteration to the "response"
  //empty array.
  const total = ls.reduce((prev: number, curr: number) => prev + curr, 0);
  response.push(total);
  // With the new "response" array created, the for loop will be subtracting each element until the final result is an empty array []
  for (let i = 0; i < ls.length; i++) {
    response.push(response[i] - ls[i]);
  }
  return response;
}
```

[**5. Consecutive strings**](https://www.codewars.com/kata/56a5d994ac971f1ac500003e/train/typescript)
```typescript	
export function longestConsec(strarr: string[], k: number): string {
  let arrLength = strarr.length;
  let arr = [];
  
  if(arrLength == 0 || k > arrLength || k <= 0) return "";
    
  for(let i = 0; i <= arrLength - k; i++){
    let current = strarr[i];
    for(let ii = k, jj = 1; ii > 1; ii--, jj++){
      current += strarr[i+jj]
    }
  arr.push(current);
  }
 return arr.reduce(function (a, b) {
        return a.length > b.length ? a : a.length == b.length ? a : b;
    });
  
}
```

### Date: 05/19/2022
[**1. Tile**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week06/exercises/e14/desc)
```typescript	
export class Tile {
  letter: string;
  value: number;

  constructor(letter: string, value: number) {
    this.letter = letter;
    this.value = value;
  }

  printTile() {
    console.log(`
        ===========================
          Letter: ${this.letter}
          Value: ${this.value}
        ===========================
    `);
  }
}
```

[**2. Time**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week06/exercises/e15/desc)
```typescript	
export class Time {
  hour: number;
  minute: number;
  second: number;

  constructor(hour: number, minute: number, second: number) {
    this.hour = hour;
    this.minute = minute;
    this.second = second;
  }

  printTime() {
    console.log(`
        ===========================
          Hours: ${this.hour}
          Minutes: ${this.minute}
          Seconds: ${this.second}
        ===========================
    `);
  }

  getInSeconds(): number {
    const minutes = this.hour * 60 + this.minute;
    return minutes * 60 + this.second;
  }
}
```

[**3. Rational**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week06/exercises/e16/desc)
```typescript
export class Rational {
  numerator: number;
  denominator: number;

  constructor(numerator: number, denominator: number) {
    this.numerator = numerator;
    this.denominator = denominator;
  }

  printRational() {
    console.log(`${this.numerator} / ${this.denominator}`);
  }

  invert() {
    [this.numerator, this.denominator] = [this.denominator, this.numerator];
  }

  toFloat(): number {
    return this.numerator / this.denominator;
  }

  gcd(n: number, d: number): number {
    if (d == 0) return n;
    return this.gcd(d, n % d);
  }

  reduce() {
    const gcd = this.gcd(this.numerator, this.denominator);
    this.numerator = this.numerator / gcd;
    this.denominator = this.denominator / gcd;
  }
}
```
## Week 7
### Date: 05/25/2022
[**1. Interfaces Guided Exercies**](https://docs.microsoft.com/en-us/learn/modules/typescript-implement-interfaces/)

**Code 1**
```typescript
interface IceCream{
    flavor: string;
    scoops: number;
    instructions?: string;
}

interface Sundae extends IceCream {
    sauce: "chocolate" | "caramel" | "strawberry";
    nuts?: boolean;
    whippedCream?: boolean;
    instructions?: string;
}

let myIceCream: Sundae = {
    flavor: "vanilla",
    scoops: 2,
    sauce: "caramel",
    nuts: true
}

console.log(myIceCream.flavor);

function tooManyScoops (dessert: Sundae){
    if (dessert.scoops >= 4) {
        return dessert.scoops + " is too many scoops!";
    } else {
        return "Your order will be ready soon!";
    }
}

console.log(tooManyScoops({flavor: "vanilla", scoops: 5, sauce: "caramel"}));
```
**Code 2**
```typescript
interface IceCreamArray {
    [index: number]: string;
}

let myIceCream: IceCreamArray;
myIceCream = ["chocolate", "vanilla", "strawberry"];
let myStr: string = myIceCream[0];
console.log(myStr);
```

**Code 3**
```typescript
/* Module 3: Implement interfaces in TypeScript
   Lab Start  */

/*  EXERCISE 1
    TODO: Declare the Loan interface. */

interface Loan {
    principal: number,
    interestRate: number //* Intereset rate percentage (eg. 14 is 14%)
}

/*  TODO: Declare the ConventionalLoan interface. */

interface ConventionalLoan extends Loan {
    months: number //* Total number of months
} 


/*  TODO: Update the calculateInterestOnlyLoanPayment function. */

function calculateInterestOnlyLoanPayment(loanTerms: Loan): string {
    // Calculates the monthly payment of an interest only loan
    let interest: number = loanTerms.interestRate / 1200; // Calculates the Monthly Interest Rate of the loan
    let payment: number;
    payment = loanTerms.principal * interest;
    return 'The interest only loan payment is ' + payment.toFixed(2);
}

/*  TODO: Update the calculateConventionalLoanPayment function. */

function calculateConventionalLoanPayment(loanTerms: ConventionalLoan): string {
    // Calculates the monthly payment of a conventional loan
    let interest: number = loanTerms.interestRate / 1200; // Calculates the Monthly Interest Rate of the loan
    let payment: number;
    payment = loanTerms.principal * interest / (1 - (Math.pow(1 / (1 + interest), loanTerms.months)));
    return 'The conventional loan payment is ' + payment.toFixed(2);
}

let interestOnlyPayment = calculateInterestOnlyLoanPayment({principal: 30000, interestRate: 5});
let conventionalPayment = calculateConventionalLoanPayment({principal: 30000, interestRate: 5, months: 180});

console.log(interestOnlyPayment);     //* Returns "The interest only loan payment is 125.00" 
console.log(conventionalPayment);     //* Returns "The conventional loan payment is 237.24" 
```
[**2. Build Tower**](https://www.codewars.com/kata/576757b1df89ecf5bd00073b/train/typescript)
```typescript
export const towerBuilder = (nFloors: number): string[] => {
var tower = [];
for (var i = 0; i < nFloors; i++) {
tower.push(" ".repeat(nFloors - i - 1)
+ "*".repeat((i * 2)+ 1)
+ " ".repeat(nFloors - i - 1))
}
return tower;
}
```

[**3. Meeting**](https://www.codewars.com/kata/59df2f8f08c6cec835000012/train/typescript)
```typescript
export function meeting(s: string): string {
  return s
    .toUpperCase()
    .split(';')
    .sort((a: string, b: string) => {
      const [aFirstName, aLastName] = a.split(':');
      const [bFirstName, bLastName] = b.split(':');
      if (aLastName === bLastName) {
        return aFirstName > bFirstName ? 1 : bFirstName > aFirstName ? -1 : 0;
      }
      return aLastName > bLastName ? 1 : bLastName > aLastName ? -1 : 0;
    })
    .map((fullName: string) => {
      const [firstName, lastName] = fullName.split(':');
      return `(${lastName}, ${firstName})`;
    })
    .join('');
}
```
## Week 8
### Date: 06/01/2022
[**2. Make the Deadfish Swim**](https://www.codewars.com/kata/51e0007c1f9378fa810002a9/train/typescript)
```typescript
export function parse(data: string): number[] {
let response:number[] = [];
let num: number = 0;

data.split("").forEach(function(val) {

if (val == "d") {
  num--;
} else if (val == "i") {
  num ++;
} else if (val == "s") {
  num = num*num;
} else if (val == "o") {
  response.push(num);
}
 
});
return response;
}
```
### Date: 06/02/2022
[**1. Generics Exercise**](https://github.com/corecodeio/devguide-from-scratch-2022-02/tree/main/src/technologies/2022/week08/exercises/e00/desc)
```typescript
export function parse(data: string): number[] {
let response:number[] = [];
let num: number = 0;

data.split("").forEach(function(val) {

if (val == "d") {
  num--;
} else if (val == "i") {
  num ++;
} else if (val == "s") {
  num = num*num;
} else if (val == "o") {
  response.push(num);
}
 
});
return response;
}
```
