1:
`let result = num1 + num2;`
num1 and num2 were string values (from input fields), so the + operator concatenated them instead of performing numerical addition.

For example:

"1" + "2" results in "12" instead of 3.


2:
`let result = Number(num1) + Number(num2);`
This is how I would fix it, ensuring that we are adding numeric values,  not strings. (check fix.png for full code snippet)
