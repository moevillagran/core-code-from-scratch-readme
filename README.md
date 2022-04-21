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

**Your date of birth in the matrix?**

My DOB is 12/04/1994, which in binary is 1100/1/1111100101.

**MIPS Excercises**

**1. Create a program that adds any two given numbers provided by the user**
```
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

**2. Create a program that displays your name**
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

**1. Print Special Numbers**
```
for (var i = 0; i <= 100; i = i + 2) {
  console.log(i);
}
```

**2. Bad Code 1**

By using the statement "cond = true", the variable value was changed and the statement was turned in a true statement. Also, when using and if...else statement, the condidition should be between one set of parenthesis not two. Even though I used the documentation on the exercies resources, when running it, it continues to print de "The cond variable is true". :(

```
var cond = false;

if (cond) {
    console.log('The cond variable is true');
} else {
    console.log('The cond variable is false');
}
```

**3. Bad Code 2**

The syntax was incorrect. It should have been: if, else if, else.
```
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
**1. Multiply Exercies**
```
function multiply(a, b){
 return a * b
}
```

**2. ASCII Total Exercies**
```
function uniTotal(str) {
  let count = 0;
  for (let i = 0; i < str.length; i++) {
    count += str.charCodeAt(i);
  }
  return count;
}
```

**3. Char From ASCII Value**
```
function getChar(c){
return String.fromCharCode(c);
}
```

**4. Binary Addition**
```
function addBinary(a,b) {
let sum = a + b;
  return sum.toString(2);
}
```

**5. Student's Final Grade**
```
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

### Date: 04/19/2022

**1. Holiday VIII - Duty Free**
```
function dutyFree(normPrice, discount, hol){
let result1 = ((normPrice * discount) / 100);
let result2 = hol / result1;
let result3 = Math.floor(result2);
  return result3;
}
```

**2. Twice As Old**
```
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let difference = ((dadYearsOld - sonYearsOld) * 2) - dadYearsOld;
  return Math.abs(difference);
}
```

**3. 
