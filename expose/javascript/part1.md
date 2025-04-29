1:
At line 9, if add is true, it prints:
values added: 20
This happens because the function adds num1 and num2 together and then logs the result.

2:
At line 13, it prints:
final result: 20
This is because after adding the numbers, the result variable now holds the value 20, and the code logs it right after.

3:
We should avoid using var because it has strange behavior with something called hoisting. Variables declared with var are lifted to the top of their scope, which can lead to bugs where variables seem to exist before we define them. var is also function-scoped, not block-scoped, so if we define it inside an if block or loop, it still behaves like it was declared at the top of the function. Using let or const instead makes it easier to manage where variables actually live and change.

4: 
At line 9, if add is true, it prints:
values added: 20
This happens because the function adds num1 and num2 together and then logs the result.

5:
At line 13, it prints:
final result: 20
After the addition happens and the result is saved, the function logs the final value of the result variable. Since it was already calculated and stored, the print works with no issues.

6:
/Users/amandhillon/Lab4_Starter/scripts/lab4.js:17
        result = num1 + num2;
               ^

TypeError: Assignment to constant variable.
    at sumValues (/Users/amandhillon/Lab4_Starter/scripts/lab4.js:17:16)
    at Object.<anonymous> (/Users/amandhillon/Lab4_Starter/scripts/lab4.js:28:1)
    at Module._compile (node:internal/modules/cjs/loader:1730:14)
    at Object..js (node:internal/modules/cjs/loader:1895:10)
    at Module.load (node:internal/modules/cjs/loader:1465:32)
    at Function._load (node:internal/modules/cjs/loader:1282:12)
    at TracingChannel.traceSync (node:diagnostics_channel:322:14)
    at wrapModuleLoad (node:internal/modules/cjs/loader:235:24)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:170:5)
    at node:internal/main/run_main_module:36:49

Node.js v22.15.0

Nothing is printed by line 9 because the code throws an error before it can get there. The line result = num1 + num2 tries to change the value of a variable that was declared using const, which is not allowed. Since const means the variable can’t be reassigned, the program stops and throws an error before it can reach that console log.

7:
Nothing is printed at line 13  because the error from line 9 causes the function to exit early. Since the program crashes when trying to reassign a constant variable, it never makes it to line 13.






