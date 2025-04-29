1:
At line 12, the value 3 is printed.

This happens because the variable i was declared with var, which makes it scoped to the whole function, not just inside the for loop. After the loop finishes running, i still exists and holds the value that made the loop stop. Since the loop runs while i is less than 3, once it reaches 3, the loop ends. Then console.log(i) prints 3.

There is no error because var allows i to still be accessible outside the loop.

2:
At line 13, the value 150 is printed.

This happens because discountedPrice was declared with var inside the for loop. Since var is function-scoped and not block-scoped, discountedPrice still exists even after the loop finishes. When the loop ends, discountedPrice holds the last value it calculated, which is 150. That is why console.log(discountedPrice) prints 150.

There is no error because var allows discountedPrice to be accessed outside the loop.

3:
At line 14, the value 150 is printed.

This happens because finalPrice is declared with var, which means it exists throughout the entire function. During each loop cycle, finalPrice gets updated with the newly rounded price. After the loop finishes, it keeps the last value that was assigned to it, which in this case is 150.

There’s no error because var allows finalPrice to be accessed outside the loop, and the variable still holds its last value.

4:
The function, as written, will not produce any output because there is no call to console.log() or anything that triggers the result to be printed. The function is correctly calculating the discounted prices and returning them, but unless the result is logged or explicitly returned in a way that gets printed, it will just run without showing anything.

So, with the current code, the function will return `[50, 100, 150]`, but we won't see this output unless we modify the code to log or print it to the console.

5:
At line 12, where console.log(i) is called, I get an error: ReferenceError: i is not defined.

The reason for this is that the variable i is defined inside the for loop with let. In JS, when we use let inside a block, the variable i is scoped to that block, meaning it is only accessible within the loop. Once the loop finishes, i is no longer available outside of it.

When the code reaches console.log(i) after the loop, it tries to access i, but i is not in scope anymore, so we get the ReferenceError.

6:
At line 13, where console.log(discountedPrice) is called, I get an error: ReferenceError: discountedPrice is not defined.

The reason for this is that discountedPrice is declared inside the for loop with let. In JS, variables declared with let inside a block are only available within that block. Once the loop iteration is over, discountedPrice is no longer accessible outside of the loop.

Since I am trying to log discountedPrice outside of the loop, it isn't in scope anymore, so JS will throw a ReferenceError.

7:
At line 14, where console.log(finalPrice) is called, I get the output: 150

This works because the finalPrice variable is declared outside the loop using let, which gives it a scope that persists across all iterations of the loop. Unlike discountedPrice, which is scoped only within the loop block, finalPrice retains its value from the last iteration. After the loop finishes, finalPrice contains the discounted price of the last item in the array, which is 150 in this case. This is why console.log(finalPrice) prints 150.

8:
The function, as written, will not produce any output because there is no call to console.log() or anything that triggers the result to be printed. The function is correctly calculating the discounted prices and returning them, but unless the result is logged or explicitly returned in a way that gets printed, it will just run without showing anything.

9:
At line 11, where console.log(i) is called, I get an error: ReferenceError: i is not defined.

The reason for this is that the variable i is declared inside the for loop using let. In JS, variables declared with let have block scope, meaning they are only accessible within the block in which they are defined. Since i is defined inside the for loop, it is not accessible outside of the loop.

10:
At line 12, console.log(length) will successfully print 3, because the length variable holds the value of the prices array's length, which is 3 in this case.

11:
The function, as written, will not produce any output because there is no call to console.log() or anything that triggers the result to be printed. The function is correctly calculating the discounted prices and returning them, but unless the result is logged or explicitly returned in a way that gets printed, it will just run without showing anything

12: 
A, Accessing the value of the name property in the student object:
`student.name;`

B, Accessing the value of the Grad Year property in the student object:
`student['Grad Year'];`


C, Calling the function for the greeting property in the student object:
`student.greeting();`

D, Accessing the name property of the object in the Favorite Teacher property in student:
`student['Favorite Teacher'].name;`

E, Access index zero in the array of the courseLoad property of the student object:
`student.courseLoad[0];`


13: Arithmetic

a. '3' + 2  
Output: '32'  
Explanation: The number 2 is turned into a string and added to '3' as text.

b. '3' - 2  
Output: 1  
Explanation: The string '3' is converted to a number for subtraction.

c. 3 + null  
Output: 3  
Explanation: null becomes 0, so it is just 3 + 0.

d. '3' + null  
Output: '3null'  
Explanation: null is turned into a string and added to '3'.

e. true + 3  
Output: 4  
Explanation: true is treated like 1, so 1 + 3.

f. false + null  
Output: 0  
Explanation: false is 0, null is 0, so 0 + 0.

g. '3' + undefined  
Output: '3undefined'  
Explanation: undefined becomes a string and gets added as text.

h. '3' - undefined  
Output: NaN  
Explanation: You cannot subtract undefined, so it gives "Not a Number".


14: Comparison

a. '2' > 1  
Output: true  
Explanation: '2' turns into 2 for the comparison.

b. '2' < '12'  
Output: false  
Explanation: These are strings, so it checks alphabetically. '2' comes after '1'.

c. 2 == '2'  
Output: true  
Explanation: == allows type conversion so it matches.

d. 2 === '2'  
Output: false  
Explanation: === checks both value and type. One is a number and one is a string.

e. true == 2  
Output: false  
Explanation: true becomes 1, which is not equal to 2.

f. true === Boolean(2)  
Output: true  
Explanation: Boolean(2) is true, and both sides are the same type.


15: Difference between == and ===
== checks if values are equal but lets JavaScript convert the types if they are different.  
=== checks if the values and the types are both exactly the same with no conversions.

16: in a different file

17:
When we call `modifyArray([1, 2, 3], doSomething)`, we are passing an array and a callback function into modifyArray. The function then loops through each element of the array and applies the callback function to it. In this case, the callback doSomething simply multiplies each number by two. So, 1 becomes 2, 2 becomes 4, and 3 becomes 6. These new values are pushed into a new array, and once the loop is finished, the function returns `[2, 4, 6]`. At first, when I ran the code, I did not see any output in the terminal. That is because even though modifyArray returns a new array, I never actually logged the result to the console. After adding a console.log around the function call, I was able to see the output `[2, 4, 6]` displayed properly.

18: in diff file
It works because:
printTime is a function that gets the current time and logs it.
setInterval(printTime, 1000) calls printTime every 1000 milliseconds (which is every 1 second).

19:the output is:
```
amandhillon@MacBook-Pro Lab4_Starter % node scripts/lab4-part2.js
1
4
3
2

The function starts by printing 1 right away. Then it sets a timer to print 2 after 1000 milliseconds (1 second) and another one to print 3 after 0 milliseconds. Even though 3 is set with a delay of 0, it doesn’t run immediately—it gets placed in a queue to run after the current code finishes. So the next line, console.log(4), runs right away. After that, the program goes back and runs the 0-delay timeout, which prints 3, and finally, after one full second, it prints 2. That’s why the final output ends up in the order: 1, 4, 3, 2.




