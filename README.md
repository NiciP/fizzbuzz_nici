## Project: FizzBuzz Game

#### Deployed: https://fizzbuzzgame.netlify.com/

### Game Rules:
FizzBuzz is a numbers game that allows a user to input a random number where in turn the player receives feedback based on that number.

- For numbers divisible by 3 the application should return 'Fizz' 
- For numbers divisible by 5 the application should return 'Buzz' 
- For numbers divisible by 15 the application should return 'FizzBuzz'

For any number not the app should return the number. 

### Languages used:
- Javascript
- HTML
- Tailwind

### Goal:

To build an application with Javascript, perform unit and feature testing of the web app, set up of HTML, styling with Tailwind as well as web deployment of the project.

### Author:
Nici Putter



## Questions:

### Question 1 
#### To the best of your knowledge please explain what the following lines of code do:

let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)

Setting the constant fizzBuzz to read the contents of 'fizz-buzz.js' in the specified path and eval() executes the string of javascript code


### Question 2
#### Please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

To be able to create and use other instances of fizzbuzz in other it blocks, without the need to duplicate code unnecessarily


### Question 3 
#### Please explain the difference between using === and == in JS?

== allows you to compare a number with a string to return a boolean, where the === compares both the value and the data type


### Question 4  
#### Please explain why we are moving (number % 5 === 0) to the top?

We would like to test the higher number of 5 first in the sequence before the other option/s are evaluated. As we know that the code is executed chronologically, this will avoid lower numbers (eg. 3) fulfilling the requirements first.


### Question 5  
#### Please explain the difference between feature and unit test

- Unit testing is where we test the logic of the software in its smallest parts and evaluate if the individual functionality of each component is working as designed. 
- Feature tests are used to test if all parts of our software are working together as intended according to the product owner specifications and/or the client needs. This is where we ensure that the software performs correctly from a users perspective.


### Question 6 
#### To the best of your knowledge please explain what this following code does:

describe('User can input a value and get FizzBuzz results', () => {
    before(async () => {
        await  browser.init()
        await  browser.visitPage('http://localhost:8080/')
    });

    beforeEach(async () => {
        await  browser.page.reload();
    })

    after(async ()=> {
        await  browser.close();
    })
})

For feature testing to be done, the browser must be initialized and load the address of the specified server. The browser must be reloaded before each new test and after each test the browser should close again. The async function means that the processes are asynchronous and that they can run simultaneously without the need to wait for another to be completed.


### Question 7 
#### Please explain what expectations in the context of testing are?

Expectations are the intended results/output that is expected from the implementation code. When the expectations are met, the test is regarded successful. Collectively the desired outcome and goals of the application are that all the software expectations are fulfilled according to specified requirements.


### Question 8 
#### Please write a line to line explanation of what is happening in this code

 <script src="./js/fizz-buzz.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            let button = document.getElementById('button')
            let displayDiv = document.getElementById('display_answer')
            button.addEventListener('click', () =>{
                let value = document.getElementById('value').value
                let fizzBuzz = new FizzBuzz
                let result = fizzBuzz.check(value)
                displayDiv.innerHTML = result;
            })
        })
    </script>

- The script file is called upon as source to be used when the page loads
- A script block is inserted so that we are able to write code in this file
- A listener is set up to identify when the HTML has been loaded and parsed
- Store element with the id 'button' in the variable "button"
- Store element with the id 'display_answer' in the variable "displayDiv"
- An event listener is set up to monitor for a mouse click, and in the event then performs the following actions:
- Store element with the id 'value' in the new variable "value"
- A new fizzbuzz instance is created
- The "result" variable is set up so that the value entered by the user be used in the fizzBuzz check function
- This result is to be displayed in the browser
- End of script block


### Question 9 
#### Explain what a CDN (Content Delivery Network) is?

A system of distributed servers that deliver information and other Web content to a user, as opposed to storing it locally. This makes content available to users more reliably and without the need for the origin pc to be available in order to do so. 
