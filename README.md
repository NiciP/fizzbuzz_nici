
FIZZBUZZ CHALLENGE


HOW THE GAME WORKS:

FizzBuzz is a numbers game that allows user to input a random number where in turn he/she receives feedback. 
When the number is divisible by 3, the program returns "Fizz", when divisible by 5 "Buzz" and when divisible by 15 it will return "FizzBuzz". 
For any other number the program returns the eact number

REASON FOR BUILDING PROGRAM:

To practise building programs via Javascript, its unit and feature testing, set up and styling of HTML as well as web deployment of the project.

DEPLOYED SITE:
https://inspiring-sinoussi-f48baf.netlify.com/

COMPLETED BY:
Nici Putter


COURSE QUESTIONS:

Question 1. In your README to the best of your knowledge please explain what the following lines of code do
let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)

Setting the constant fizzBuzz to read the contents of 'fizz-buzz.js' in a synchronized manner, and do an evaluation of sorts 

.............



Question 2. Please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

To be able to create and use other instances of fizzbuzz in other it blocks, thus being available globally

.............



Question 3. Please explain the difference between using === and == in JS?

== allows you to compare a number with a string to return a boolean, where the === compares both the value and the data type

.............



Question 4. Please explain why we are moving (number % 5 === 0) to the top?

The higher number scenarios need to be at the top, as the highest number being 15 will be tested first in the sequence. This will avoid lower numbers fulfilling their requirements first, and thereby giving a more accurate portrayal of the game 

.............



Question 5. Please explain the difference between feature and unit test

Unit testing is where we test whether the logic of the software is correct, and with feature we test whether the functionality works as intended within the chosen framework.

.............



Question 6. In your README to the best of your knowledge please explain what this following code does:

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

This describes the sequence of events that need to happen in order for application to work as intended:
Before a user can initially start the game, the browser must complete loading. This is to be done for every new instance and afterwards the browser should close again.   

.............



Question 7. What expectations in the context of testing are?

Expectations are the intended results to be generated from the implementation code/setup created. Collectively this is the desired outcome and goal of the application.

.............



Question 8. Please write a line to line explanation of what is happening in this code

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

Fizz buzz javascript file is called upon as source to be used in the file 
Start of script
A listener is set up to react on when DOM is being loaded
Create a button from document that will be searched by its ID
Variable is set that will display the answer of the calculation
An event listener is set up to monitor for a mouse click
Variable is set to fetch a value
A new fizzbuzz instance is created
Variable is set up that is stored as the value entered by the user
This result variable is to be displayed within the browser
End of script

.............



Question 9. Explain what a CDN (Content Delivery Network) is?

A system of distributed servers that deliver pages and other Web content to a user, as opposed to storing it locally. This makes content available to users more reliably and without the need for the origin pc to be available in order to do so. 
