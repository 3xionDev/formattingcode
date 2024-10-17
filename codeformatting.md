        How to Format Code Correctly  
For those who for some reason can’t figure it out

[**1\. Indent-alignment**](#indent-alignment)

[**2\. Variables**](#variables)

[**3\. Operations**](#operations)

[**4\. Conditionals**](#conditionals)

[**5\. Comments**](#comments)

[**6\. Escape sequences**](#escape-sequences)

[**7\. Errors**](#errors)

[**8\. Common sense practices**](#common-sense-practices)

[**9\. Practice**](#practice)

[**10\. Solutions**](#solutions)

1. ## Indent-alignment {#indent-alignment}

   1. Indent-alignment is when a line of code begins in the same horizontal position as the previous line, in other words it is **aligned** with the previous line.  
   2. Generally speaking, a line of code should not be indented unless it is inside a statement, be it a function definition or a conditional.  
   3. Any line of code can be indented.  
   4. Your code should ***always*** be indent-aligned when possible.  
   5. Any self-respecting IDE will automatically indent-align written code, however this is generally dependent on the programmer in some way.  
   6. Automatic indent-alignment ***will not work*** if you make an alignment error somewhere in the code. It will start off aligning the code correctly, however it will begin to make alignment errors immediately after the one you make.  
   7. If your alignment starts looking strange, it’s because *you* made a mistake earlier in the code, not the IDE.  
   8. Take care not to make indent alignment errors, as it is often necessary to manually re-align every subsequent line of code.  
   9. Some IDEs have a “Cleanup” function, where you can press a hotkey and it will automatically re-align most or all of your code.

2. ## Variables {#variables}

   1. A **variable** is a piece of code that stores a value, be it a text string, a numeric integer, or an ASCII character.  
   2. There are many types of variables, and different languages have different types, however the most common are:  
      1. String (most commonly used to store text, however it can be used to store a number, which makes it unusable by mathematical operations)  
      2. integer (used to store whole numbers from \-2,147,483,648 to 2,147,483,647, the 32-bit integer limit)  
      3. float/double (used to store numbers with decimal points, i.e. numbers that aren’t whole.   
      4. char (used to store a single ASCII character, generally a letter. This character *must be stored in single quotes ‘like this’*, as opposed to Strings that are held in double quotes “like this.”)  
      5. Boolean (can store only two values \- **true** and **false**. Depending on the language, creating a boolean with a different value may evaluate to true or false \- for example, in some languages, setting a boolean to 1 will evaluate to true and setting it to 0 will evaluate to false. This is not true for every language.)  
      6. long (like an integer, but can store values from \-9,223,372,036,854,775,808 to 9,223,372,036,854,775,808, the 64-bit integer limit.)  
   3. Variables are defined like this: 

```
x = 2
```

   4. Depending on the language, you may need to declare the type of the variable before defining the name and value, like this: 

```
int x = 2
Boolean myBool = true
String y = "Hello world!"
char z = 'a'
//or, alternatively, you might need to define the write permissions for the variable, like this:
const num = 5 //const means the variable can't be changed; it is "constant"
//write permission definition is not something that is included in most languages
```

   5. Generally, variables can be defined on separate lines or on the same line, assuming they are of the same type, like this: 

```
int num1 = 1, num2 = 2, num3 = 3, num4 = 4, num5 = 5; //this works
int num1 = 1, num2 = "hello!", num3 = 'e', num5 = true; //this does not
```

   6. You should try to keep similar variable definitions on the same line when feasible, as it looks neater and is easier to read:

```
int num1 = 1, num2 = 2, num3 = 3, num4 = 4; //this looks nice
int num1 = 1; //this looks ugly and adds more lines to the program
int num2 = 2;
int num3 = 3;
int num4 = 4;
```

   7. Don’t use variables when they’re not necessary; for example, when you need to perform math on another variable:

```
//this is not good and wastes memory and time
x = 5
xMult = x * 2
print("x multiplied by 2 is: " + xMult)
//this is ideal as it uses less memory and takes less time to write
x = 5
print("x multiplied by 2 is: " + (x * 2))
//it's acceptable to define a variable as a math operation on another variable when the operation is complicated and would make the code difficult to read, like this:
x = 5
print("The output number is: " + (2*(x^(x-1))/(x%7)) //bad and hard to read
--
xOperated = (2*(x^(x-1))/(x%7))
print("The output number is: " + xOperated) //better and easier to read
```

3. ## Operations {#operations}

   1. All languages have certain **operators** that allow the program to do math.  
   2. The operators generally follow a common character scheme regardless of language:  
      1. “+” is addition  
      2. “-” is subtraction  
      3. “\*” is multiplication  
      4. “/” is division  
      5. “%” is modulus (remainder)

```
float add = 5, sub = 5, mul = 5, div = 5, modulus = 5
add = add + 1 //result: add = 6
sub = sub - 1 //result: sub = 4
mul = mul * 5 //result: mul = 20
div = div / 2 //result: div = 2.5
modulus = modulus % 2 //result: modulus = 1
```

   3. There is also another type of operator called **operate-assign** operators. These allow you to condense your math into shorthand by performing the operation and then assigning the result value to the left operand:  
      1. “+=” is add-assign  
      2. “-=” is subtract-assign  
      3. “\*=” is multiply-assign  
      4. “/=” is divide-assign  
      5. “%=” is modulo-assign

```
float add = 5, sub = 5, mul = 5, div = 5, modulus = 5
add += 1 //result: add = 6
sub -= 1 //result: sub = 4
mul *= 5 //result: mul = 20
div /= 2 //result: div = 2.5
modulus %= 2 //result: modulus = 1
```

   4. The final operator type are iterators:  
      1. “++” adds one to the value  
      2. “--” subtracts one from the value

```
int add = 0, sub = 0
add++ //result: add = 1
sub-- //resilt: sub = -1
```

   5. Not every language has operate-assign operators or iterators.

4. ## Conditionals {#conditionals}

   1. Most languages contain **conditional** operators and statements which are used to compare two values and execute code based on the result.  
   2. The conditional operators are as follows:  
      1. “==” checks if a value equals another value  
      2. “\>” checks if the left value is greater than the right value  
      3. “\<” checks if the left value is less than the right value  
      4. “\>=” checks if the left value is greater than or equal to the right value  
      5. “\<=” checks if the left value is less than or equal to the right value  
      6. “\!=” or “\~=” checks if a value is not equal to another value

```
int equal = 1, greaterThan = 2, lessThan = 1, greatOrEqual = 3, lessOrEqual = 1, notEqual = 0
//the following is written in pseudocode, a way of making code easily readable at a glance. it is not real code, do not follow the way this code is written
is equal == 1? //result: true
is greaterThan > 1? //result: true
is lessThan < 2? //result: true
is greatOrEqual >= 3? //result: true
is lessOrEqual <= 1? //result: true
is notEqual !=/~= 1? //result: true
```

   3. All languages also contain **conditional statements** which use the result of a conditional operator comparison to decide which code is run:  
   4. The most common conditional statements are:  
      1. “If (condition) then {code} else {code}” executes code that is written within the “then” portion only when the “if” portion evaluates to true. When the “if” portion is not true, it will instead run the code within the “else” portion (if present). The “else” portion is not required.  
      2. “While (condition) do {code}” repeats the code within itself only if the “while” condition evaluates to true.  
      3. “For {initialize} (condition) {iterate} do {code}” is used to run a block of code an exact number of times. The “initialize” portion is run once, when the loop is executed for the first time. The “condition” portion checks a condition every time the code loops. The “iterate” portion is executed every time the code loops. 

```


int i = 1
//this is also in pseudocode, previous disclaimer applies
//if...then...else conditional
if i == 1 then
	print "hello"
else
	print "no hello"
end 
//result: exactly one "hello." If i != 1, it would print "no hello"
//while conditional
while i == 1 do 
	print "hello"
end
//result: an unending string of "hello" outputs
//for conditional
for i = 1, i != 11, i++ do
	print "hello"
end
//result: exactly ten instances of "hello" being outputted, because the loop sets i to 1 when first run, will only run if i does not equal 11, and adds 1 to i every time it's run
```

   5. The “for {initialize} (condition) {iterate} do {code}” conditional can also be written as:

```
//you guessed it, pseudocode
int i
i = 1 //the {initialize}
while i != 11 do //the (condition)
	print "hello" //the {code}
	i++ //the {iterate}
end
```

   6. “For” conditional loops are notoriously easy to mess up. If you’re unsure about whether your “for” loop is working, try writing it in the way the “while” loop is written above. It is not recommended to use a “for” loop if you don’t 100% know with absolute certainty that you’re writing the initializer, comparator, and iterator correctly.  
   7. Though it may seem tempting, it’s generally not okay to create an infinite execution loop using a conditional that always evaluates to true, such as:

```
//pseudocode

while 1 == 1 do
print "infinity"
end

//OR:

int i
i = 1
while i == 1 do
	print "infinity"
end

//while this may work as an infinite loop, many languages contain native methods for creating a program loop. this method is memory inefficient and may cause errors depending on the language. don't do this.
```

   8. You can make conditionals with more than one condition. The most common way that this is used is with the “if…then…else” statement, with the expander “else if”:

```
//pseudocode

int i = 1
if i == 1 then 
	print "its one!"
else if i == 2
	print "its two!"
else
	print "its not one or two :("
end

//the following code prints "its one!" if i = 1, prints "its two!" if i = 2, and prints "its not one or two :(" if i != 1 or 2.
```

   9. Another way this can be done is inside the conditional statement itself using logical AND and logical OR. The syntax for logical AND/OR is one of the most varying cases for programming languages. Some languages use “&&” to denote AND and “||” to denote OR, some languages literally use AND and OR, there is much variation. For the sake of simplicity, we will use AND and OR to denote logical functions and leave it to you to figure out what your language uses:

```
//pseudocode

int x = 1
int y = 2

if x == 1 AND y == 2 then
	print "both conditions true!"
end

//prints "both conditions true!" only if x = 1 and y = 2. consider this next example:

int x = 1
int y = 2

if x == 1 OR y == 1 then
	print "one or both conditions true!"
end

//prints "one or both conditions true!" if x == 1 and y != 1, if x != 1 and y == 1, if x == 1 and y == 1, but NOT if x != 1 and y != 1
```

   10. A conditional can have as many conditions as you want, and logical AND and logical OR can be combined in one conditional. In the case of multiple logical operators, the condition that the AND/OR compares with will generally be the left condition. Most languages allow comparisons to be nested inside of explicit parentheses to denote that you are enacting AND/OR on the result of another AND/OR comparison:

```
//pseudocode
//example of multiple, mixed logic conditionals
int x = 1
int y = 1

if x == 1 AND y == 1 OR y >= 3 AND x != 3 then
	print "conditions!"
end

//example of logic conditionals inside explicit parentheses:

int x = 1
int y = 1

if (x == 1 AND y == 1) OR (y >= 3 AND x != 3) then
	print "conditions!"
end

//the above program takes the comparison of "does x equal one AND y equal one" OR "is y greater than or equal to three AND x is not equal to three" and runs the if...then based on the result
```

5. ## Comments {#comments}

   1. Every programming language allows the developer to prefix text with a certain combination of characters (a character code) that prevents the code interpreter from reading that text. This text is known as a **comment**, and the prefix code is called the **comment prefix**. This prefix is one of the most varied parts of syntax in the programming world. Virtually every programming language has its own comment prefix. Some languages use “//”, some use “/\*”, and so on. This makes generalizing comments very hard in pseudocode, as there is no set prefix for every language. Therefore, there will not be any pseudocode in this section.  
   2. Some languages have separate prefixes for **single line** and **multiline** comments. These are precisely what they sound like; single line comments only include one line in the comment, while multiline comments include all text from the beginning prefix to the ending suffix, allowing multiple newline characters to be included.   
   3. As previously mentioned, multiline comments have both a **comment prefix** and a **comment suffix**. The comment prefix marks where the comment text begins, and the comment suffix marks where the comment text ends. The comment suffix may be an inverted version of the prefix, as is the case with “/\* comment \*/”, however this is not always the case.   
   4. Comments, specifically multiline comments, are very commonly used to temporarily disable one or more lines of code during debugging if they are suspected to be causing an issue. All one needs to do this is to place the multiline prefix before the target code and to place the multiline suffix after the target code. This will essentially remove the code from the program while still being visible to the developer.   
   5. Single line comments **do** **not** have an ending suffix. They comment out the entire line after the prefix. This is the reason that multiline comments are used to disable a specific portion of code.   
   6. To find your language’s respective comment prefixes and suffixes, simply google “(language) comment syntax” and it should tell you.

6. ## Escape sequences {#escape-sequences}

   1. Most languages have a series of **escape sequences**, which allow certain reserved characters to be stored in a string.  
   2. Reserved characters are language-specific character sequences that perform an operation within a string. These characters are also represented as escape sequences, and are therefore discussed here. Operation sequences and reserve-allow sequences are generally the same across languages. For convenience, operation sequences and reserve-allow sequences will be separated.   
   3. The common operation sequences are as follows:  
      1. “\\n” within a string denotes a new line at that point in the string.  
      2. “\\t” within a string denotes an indent at that point in the string.  
      3. “\\b” within a string denotes a backspace at that point in the string. This sequence is special in that its result differs across interpreters; in most IDEs, the text caret is moved backwards one character. However, depending on the IDE, the character that the caret moves over may or may not be deleted.   
      4. “\\r” within a string denotes a carriage return. This means that the text caret is moved back to the beginning of the current line.  
   4. The common reserve-allow sequences are as follows:  
      1. “\\”” within a string denotes a double quote inserted at that point in the string. This is useful when writing dialogue within a print statement, where double quotes are used to mark the beginning and end of the text to be printed. Inserting a double quote without an escape sequence would prematurely end the string and cause the interpreter to believe that there is an extra double quote present on that line, causing an error.   
      2. “\\’” within a string denotes a single quote inserted at that point in the string. This is used in the same situation as the previous sequence.  
      3. “\\\\” denotes a backslash inserted at that point in the string. This is useful because if a backslash is added without an escape sequence, it would cause the interpreter to believe that the next character is an escape sequence and would cause an error. This is not the case with some languages.

```
//pseudocode to demonstrate escape sequences

print "Hello! \nMy name is \"Nolan.\" \nI like using escape sequences \n \t like this indent here. \nI can also use \'single quotes!\' \nThe only problem with escape sequences is that you can\'t insert a backslash without using another escape sequence like this: \\ \nI can also use a backspace like this\b\"back\". \n\nThe last one I can use is the carriage return \r like this! "

//result:
Hello!
My name is "Nolan."
I like using escape sequences
	like this indent here.
I can also use 'single quotes!'
The only problem with escape sequences is that you can't insert a backslash without using another escape sequence like this: \
I can also use a backspace like thi"back"s.

like this! The last one I can use is the carriage return
```

7. ## Errors {#errors}

   1. When a program runs into a problem, it generally returns an **error statement**. These are useless unless you know how to read them, in which case they can tell you exactly what is wrong with the program.  
   2. Most error statements follow a similar format, with some languages having their own quirks. The common format is as follows:

```
at <file name>.<file extension>:<line that the error is found on>
	error: at <file name>.<file extension>:<error line>:<character that
begins the problematic code>: <error type>: <short 
explanation of the error>
program stopped with exit code <error code>
<number of errors> error(s)
```

   3. So, a basic error would look like this:

```
String str = "Hello!"
i = str - 1
print i

-- Error statement --

at main.pseudocode:2
	error: at main.pseudocode:2:8: typeError: Failed to parse data type
String as data type int
program stopped with exit code 0xfff00000
1 error(s)
```

   4. Analyzing the error statement, we can see that the error is in the file main.pseudocode, on the second line of that file, beginning at the eighth character on that line, and that the interpreter got confused by incompatible data types. In this case, we tried to use a String in a mathematical operation, and the interpreter rejected this because we didn’t parse the String as an int beforehand.   
   5. It’s often fine to ignore the exit code unless you need to search the error up. The exit code is simply a number that represents the type of error that the interpreter pushed. You do not need to know how to read or remember exit codes. More often than not, they are written in hexadecimal and are difficult to decode and are unnecessary anyway.  
   6. It’s not uncommon for an error to be caused by another line of code earlier that invalidated later code. In this case, the error that is pushed will be that of the invalidated line rather than the actual problematic line. This means that the error statement is rather pointless when determining the real problem. If this is the case, find the invalidated line via the error statement and then disregard the rest of the statement, as there is not truly an issue with the line the error pushed but there is an issue with a previous line that the interpreter glazed over because it came before the line that caused the error.  
   7. There are many types of errors, however there are a few that are common across languages:  
      1. Syntax error \- these usually occur when the programmer makes a typo when writing a line of code. Syntax errors are often remedied simply by fixing the typo. Syntax errors are likely the most common type of catchable error.  
      2. Logic error \- these are not caught by the interpreter’s error handler and therefore do not produce error statements. Rather, logical errors occur when a program works, but does not function as intended due to incorrect logic.  
      3. Arithmetic error \- these are caught by the error handler. These occur when there is an error with a portion of arithmetic performed by the program. A classic example of this is the divide-by-zero error.   
      4. Runtime error \- these are caught by the error handler. These occur at runtime of the program, typically caused by a piece of code that interferes with the program running.  
      5. Compiler error \- these are caught by the error handler. Typically caused by something in the program interfering with the compiler’s ability to, well, compile.

8. ## Common sense practices {#common-sense-practices}

   1. This section is dedicated to common sense practices that a programmer should do:  
      1. Unless you’re minimizing your code (you shouldn’t be), the amount of lines within the program does not matter. Never write an entire statement on one line like this:

```
int i = 1
while i = 1 do print "i is one!" end
//DO NOT DO THIS
```

         1. Writing an entire statement on one line makes it difficult to read, will probably cause an error, and only allows you to execute one function within the statement, as there is no way to easily and legibly force the program to consider two functions separate.  
      2. Prioritize readability. You can’t debug your code if you can’t understand it. Always try to make the code as readable as possible, even if it means doing something like adding a blank line between every line of real code.  
      3. Add comments. I cannot stress this enough; even if nobody but you will be viewing your code, leave comments for yourself that explain what certain portions of code do. Add important information, common issues, etc.   
      4. **Do not attempt to teach yourself how to use a function via trial and error**. More often than not, you will not succeed and will hold yourself up. Even if you manage to get it functioning, it is likely that you are doing it wrong and an error will crop up somewhere along the line. If you don’t know how to use a function, **look it up**.  
      5. Do not be afraid to ask for help. This is something that many beginner developers have. Nobody will judge you, nobody is expecting you to know how to code from the get-go. If you’re having trouble, ask somebody who has more experience and often they can help.  
      6. When in doubt, google it. There are millions of programmers on the internet that have likely already posted the solution to the problem you’re having. Don’t make it harder for yourself by trying to re-discover the solution yourself; check if someone’s fixed it already.

9. ## Practice {#practice}

   1. Indent-align this pseudocode (hint: all pseudocode in this paper is indent-aligned, use that as reference):

```
	int i = 0

while i <= 20 do
print "i is less than or equal to 20 \n"
 print "here's what i is equal to: \n"
	   print i
print "\ni <= 20"
	i++
  end
```

   2. Debug this declaration:

```
//pseudocode
int a = 1, b = "10", c = 'a'

--- Error statement ---

at main.pseudocode:1
error: at main.pseudocode:1:16: typeError: cannot parse type String as type integer
program stopped with exit code 0x29302000

at main.pseudocode:1
	error: at main.pseudocode:1:26: typeError: incompatible type char declared as type 
int
program stopped with exit code 0x29302128
2 error(s)
```

   3. How would I write a program that takes a value, squares it, assigns that value to a variable, and then adds one to it?  
   4. Say I want to make a for loop that prints “Hello\!” exactly 25 times. How would I do this?  
   5. Say I want to disable a certain snippet of code because it might be causing a bug. How would I do this easily?  
   6. I want to write a string that contains the word “Hello\!” and then inserts a new line after it. How do I do this?  
   7. What is the bug indicated in this error code? Give the line number, the character number, the error type, and what is causing the error.

```
at main.pseudocode:47
	error: at main.pseudocode:47:23: arithmeticException: cannot resolve integer, 
double, float, byte, short, long divided by zero, result NaN
program stopped with exit code 0x29370200
1 error(s)
```

   8. What is the bug in this one?

```
at main.pseudocode:81
	error: at main.pseudocode:81:10: typeError: cannot evaluate variable "i", 
variable "i" not found
program stopped with exit code 0x19110000
1 error(s)
```

   9. If you can’t figure something out for yourself, what do you do? What do you **never** do?

10. ## Solutions {#solutions}

    1. Aligned pseudocode:

```
int i = 0

while i <= 20 do
print "i is less than or equal to 20 \n"
print "here's what i is equal to: \n"
print i
print "\ni <= 20"
i++
end
```

    2. Debugged code:

```
int a = 1, b = 10
//"c" cannot be cast to an integer since it is a char, so we remove it entirely
```

    3. Completed program:

```
i = 1 //take the value
s = i * i //square it and assign it to "s"
s++ //add one to "s"
```

    4. Completed loop:

```
i = 0
for i = 0, 1 <= 25, i++
	print "Hello!"
end
```

    5. You would use a multiline comment to disable the snippet of code temporarily.  
    6. String:

```
String a = "Hello!\n"
```

    7. The indicated bug is found at line 47, character 23, is an arithmeticException error, and is caused by the program attempting to divide a number by 0\.  
    8. The indicated bug is found at line 81, character 10, is a typeError, and is caused not by incompatible type definition but is caused by the variable “i” not being defined.  
    9. If you can’t figure it out yourself, ask for help or google the answer. **Never** try to push yourself to figure it out without help, you’ll mess yourself up.
