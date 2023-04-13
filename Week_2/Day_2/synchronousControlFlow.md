## Blocking code

When program has to wait for one thing to finish before executing the rest of the code. e.g. Call to an API or readfile

Solution: Asynch code

JavaScript has a few parts that work together to facilitate multitasking: the Call Stack, the Web APIs, the Callback Queue, and then the Event Loop.

## Order of Execution

1. main thread
2. event loop

The main thread has to finish first before the event loop can even start!

```javascript
//main thread
const startWashingMachine = function(){
console.log("washing starts");
setTimeout(callback => {console.log("washing finished")} , 5000);
}

const startDishwasher = function(){
console.log("dishes starts");
setTimeout(callback => {console.log("dishes finish")} , 8000);
}

const dusting = function(){
  console.log('i am dusting');
}

startDishwasher()
startWashingMachine()
dusting()

```
In above example:
Mian thread executes
1. defines startWashingMachine and save the function in memory
2. defines startDishwasher and saved in memory
3. defined dusting function and saved

4. Now functions are invoked:

  i) startDishwasher prints "dishes starts" and adds the call back function to callback queue.

  ii) startWashingMachine prints "washing starts" and adds the callback fuction to queue.

  iii) dusting funcction invoked and prints "i am dusting" and finishes. It has no call back function.

  Over here Main thread ends. 

  Event loop starts. 

  It goes to callback queue and executes functins in queue. Prints "washing finished" and then "dishes finish". 

  End. 

  Output would look like:
  ```
  washing starts
  dishes starts
  i am dusting
  washing finished (its delay is 5s so prints first)
  dishes finish (delay is 8s so last)

