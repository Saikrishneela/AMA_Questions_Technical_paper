
# Advanced JavaScript AMA Questions & Answers

## 1.How would you implement your own version of Array.map() or Array.filter()?

**Array.map():** Iterates over each element, applies a function, and returns a new array with transformed values.  

**Array.filter():** Iterates over each element, applies a condition, and returns a new array with only values that pass.  

👉 **Example:**  
- `map` → `[1,2,3]` → `[2,4,6]` (double each number).  
- `filter` → `[1,2,3,4]` → `[2,4]` (keep only evens).  

---

## 2.What problem does async/await solve compared to plain promises or callbacks?

`async/await` makes asynchronous code look like synchronous code, improving **readability** and **maintainability**.  

- With **callbacks** → nested “callback hell.”  
- With **promises** → long `.then().catch()` chains.  
- With **async/await** → simpler, linear flow using `try/catch`.  

---

## 3.Can you explain the difference between Promise.all, Promise.any, and Promise.race with examples?

- **Promise.all**: Waits for all promises to succeed, rejects if one fails.  
- **Promise.any**: Returns the first successful promise, ignores rejections.  
- **Promise.race**: Returns the result of the first settled promise (fulfilled or rejected).  

👉 **Example:**  
- Loading multiple images → `Promise.all`.  
- Fetching from multiple servers, use the first good response → `Promise.any`.  
- Timeout mechanism → `Promise.race`.  

---

## 4.What are the possible states of a promise, and how do they transition?

A promise has three states:  

1. **Pending** → initial state.  
2. **Fulfilled** → operation completed successfully.  
3. **Rejected** → operation failed with an error.  

Once a promise is fulfilled or rejected, it becomes **settled** and cannot change state again.  

---

## 5.Can you give an example of how closures are used to implement data privacy or encapsulation?

Closures allow variables to remain private inside a function scope while exposing controlled access.  

👉 **Example:**  
A “password manager” function can hide the actual password variable but expose `getPassword` and `setPassword` methods.  
This prevents direct modification while still allowing controlled interaction.  

---

## 6.What is a closure in JavaScript, and why are they useful?

A closure is when an inner function “remembers” variables from its outer scope, even after the outer function has finished execution.  

👉 **Useful for:**  
- Data privacy (private variables).  
- State management (like counters).  
- Function factories (customized behavior).  

---

## 7.How would you handle errors inside an async/await function?

By wrapping `await` calls in a **try/catch** block.  

- `try` → contains the awaited operations.  
- `catch` → handles errors like network failures.  

This avoids chaining `.catch()` and makes error handling cleaner.  

---

## 8.What is the difference between call, apply, and bind in JavaScript?

All three are used to control the value of `this` when invoking functions.  

- **call**: Invokes immediately, arguments passed individually.  
- **apply**: Invokes immediately, arguments passed as an array.  
- **bind**: Returns a new function with `this` permanently bound, does not invoke immediately.  

👉 **Example:** Borrowing a method from one object and using it on another.  