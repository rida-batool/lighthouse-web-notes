## Global vs Local Scopes

A **globally-scoped** variable is available everywhere in the code, whereas a **locally-scoped** variable would only be available within the function in which it's defined.

## Functions rules
1. Give your functions precise verb/action based names
2. Use camelCasedNames (like this one)
Properly indent the function code
3. Functions should focus on a single task: returning a value or causing a side effect. Break your function into additional smaller functions if you find it doing two or more things

- One single task could be to compute and return a value (eg: zeroPad)
- Another single task could be to perform a side effect such as logging a message to the screen (eg: printFarmInventory)

### Rule 5:

It is ideal if functions try to avoid reading outer scope variables. If a function needs some information / data, then that data should instead be passed in as a parameter, making it available within the function's inner scope.