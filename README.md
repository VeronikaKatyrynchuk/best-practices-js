# JavaScript Best Practices
---

## Let's start:bomb:

- Avoid `global` variables
> Because global variables and functions can be overwritten by other scripts.
- Always declare `local` variables
> All variables used in a function should be declared as local variables. Local variables must be declared with the `var keyword` or the `let` or the `const` keywords, otherwise they will become global variables.
- Comment as much as needed but not more
> Comments are your messages to other developers (and yourself, if you come back to your code after several months working on something else). There’s been numerous battles raging over the years about whether to use comments at all, the main argument being that good code should explain itself.
- Use `===` Comparison
> The `==` comparison operator always converts (to matching types) before comparison. The `===` operator forces comparison of values and type: 
```js
0 == "";        // true
1 == "1";       // true
1 == true;      // true

0 === "";       // false
1 === "1";      // false
1 === true;     // false
```
- Utilize JS Lint
> JSLint is a debugger written by Douglas Crockford. Simply paste in your script, and it'll quickly scan for any noticeable issues and errors in your code.
- Don't Pass a String to "SetInterval" or "SetTimeOut"
> Never pass a string to SetInterval and SetTimeOut. Instead, pass a function name.
- Use `{}` Instead of New Object()
> This method receives the "bad practice" stamp without actually being so. Instead, I recommend that you use the much more robust object literal method:
```js
var o = {
   name: 'Jeffrey',
   lastName = 'Way',
   someFunction : function() {
      console.log(this.name);
   }
};
```
- Use `[]` Instead of New Array()
> A common error in JavaScript programs is to use an object when an array is required or an array when an object is required. The rule is simple: when the property names are small sequential integers, you should use an array. Otherwise, use an object
```js
var a = ['Joe','Plumber'];
```
- Always use semicolons
> Technically, most browsers will allow you to get away with omitting semi-colons, but this is a very bad practice that can potentially lead to much bigger, and harder to find, issues.
- Strictly ‘use strict’
> Strict mode makes a lot of changes to how JavaScript runs, from obvious to subtle (these ones you’ll be most grateful for). With ‘use strict’ silent errors will now throw errors. Mistakes that would make that are difficult for Javascript engine optimization will now be relieved. Your code might even work faster.
- Make it Understandable
```js
let i1, pio, rialtv;
let  newOrderIfItemIsOnStockAndCustomerFromAustralia;
```
> i1, pio, rialt vwould be bad variable names. Also newOrderIfItemIsOnStockAndCustomerFromAustralia is a not really readable. Imagine reading code with these variables. You want to make your code understandable with short and meaningful names. A variable name should make sense.

- Don’t Do Too Much Nesting
> Nesting too far can make your code super unreadable. The coder after you should not suffer when their code editors wrap long lines.
```js
firstFunction(args, function() {
    secondFunction(args, function() {
        thirdFunction(args, function() {
            // And so on…
        });
    });
});
```
- Use the Power of ES6 Arrow Functions
> To avoid some of the edge cases and trauma associated with `this`, ES6 gives us the arrow function. Arrow functions bind this.
- Use the operator Spread
> Spread allows an array to expand in places where 0+ arguments are expected.
```js
function sum(x, y, z) {
    return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers)); //6
```
