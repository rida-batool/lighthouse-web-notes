## Recursion

Recursion is an alternative to traditional looping that allows you to do the same thing, just in a slightly different way. Recursion isn't necessarily a better way of doing this, it's just a different way of doing this.

```javascript
1.| function countEvenToTwelve(number) {
2.|   if (number <= 12) {
3.|     console.log(number);
4.|     countEvenToTwelve(number+2);
5.|   }
6.| }
7.| countEvenToTwelve(0);
```

A recursive function will call itself to execute code over and over again, kind of like a loop. And like a loop, it has to stop calling itself at some point so that it doesn't keep repeating forever.

- We refer to number <= 12 as a recursive case, because as long as this is true, the function will continue to call itself.

- We refer to number > 12 as a base case. If this is true, the function will not call itself.

The recursive case is when the function will continue to call itself. Every time the function calls itself, the input gets closer and closer to the base case. 

The base case is when the function no longer calls itself. In a properly designed recursive function, with each recursive call, the input must gradually resolve toward the base case.

### A function must have at least one recursive case and at least one base case in order to be recursive.