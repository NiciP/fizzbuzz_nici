
Question 1. In your README to the best of your knowledge please explain what the following lines of code do
let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)

Setting the constant fizzBuzz to read the contents of 'fizz-buzz.js' in a synchronized manner 



Question 2. In your README to the best of your knowledge please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

To be able to create and use other instances of fizzbuzz in other it blocks as well



Question 3. Please explain the difference between using === and == in JS?

== allows you to compare a number with a string to return a boolean. Where the === compares both the value and the data type to return the same.



Read more: http://www.java67.com/2013/07/difference-between-equality-strict-vs-operator-in-JavaScript-Interview-Question.html#ixzz5eOBT8oIJ

Question 4. Please explain why we are moving (number % 5 === 0) to the top?



