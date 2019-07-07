# DSA Practice

## Question 1

### Can you explain big O notation and why it's important?

When writing a piece of code, it's important to consider how long it takes for it to run in the worst case scenario. We approximate the overall time complexity according to what the size of the expected inputs. This helps us measure how efficient our code is, especially when scaling applications, and helps us decide what tradeoffs we should or shouldn't be making.

## Question 2

### Please rank the following Big-O functions from fastest to slowest:
```
O(n), O(n log n), O(1), O(n^2), O(2^n)
```

Answer:

Fastest
```
O(1),
O(n),
O(n log n),
O(n^2),
O(2^n)
```
Slowest

## Question 3

### What's the time complexity of the following function?

What is the time complexity, expressed in big O notation, of the below function? This function, scrambleString, accepts a string as an argument and returns that a string with the letters randomly rearranged.

```javascript
function scrambleString(str) {
  let split = str.split("");    

  split.forEach((char, idx) => {
    let randInd = Math.floor(Math.random() * split.length);
    split[idx] = split[randInd];
    split[randInd] = char;
  });

  return split.join("");
}
```