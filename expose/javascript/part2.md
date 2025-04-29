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

When the code reaches console.log(i) after the loop, it tries to access i, but i is not in scope anymore, so you get the ReferenceError.

6:
At line 13, where console.log(discountedPrice) is called, I get an error: ReferenceError: discountedPrice is not defined.

The reason for this is that discountedPrice is declared inside the for loop with let. In JS, variables declared with let inside a block are only available within that block. Once the loop iteration is over, discountedPrice is no longer accessible outside of the loop.

Since I am trying to log discountedPrice outside of the loop, it isn't in scope anymore, so JS will throw a ReferenceError.

7:
At line 14, where console.log(finalPrice) is called, I get the output: 150

This works because the finalPrice variable is declared outside the loop using let, which gives it a scope that persists across all iterations of the loop. Unlike discountedPrice, which is scoped only within the loop block, finalPrice retains its value from the last iteration. After the loop finishes, finalPrice contains the discounted price of the last item in the array, which is 150 in this case. This is why console.log(finalPrice) prints 150.

8:

