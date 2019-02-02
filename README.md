
Question 1. In your README to the best of your knowledge please explain what the following lines of code do

let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)

Setting the constant fizzBuzz to read the contents of 'fizz-buzz.js' in a synchronized manner 


Question 2. In your README to the best of your knowledge please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

To be able to create and use other instances of fizzbuzz in other it blocks as well



