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


