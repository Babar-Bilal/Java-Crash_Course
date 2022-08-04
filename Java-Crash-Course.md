Source:
https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics

Try entering the example code lines into your JavaScript console to see what happens.

==================================================================================================================================================================================================
Variables:
Variables are containers that store values. You start by declaring a variable with the let keyword, followed by the name you give to the variable:

        let myVariable;

A semicolon at the end of a line indicates where a statement ends. It is only required when you need to separate statements on a single line. However, some people believe it's good practice to have semicolons at the end of each statement. There are other rules for when you should and shouldn't use semicolons.
You can name a variable nearly anything, but there are some restrictions.
    You use variables as symbolic names for values in your application. The names of variables, called identifiers, conform to certain rules.
    A JavaScript identifier must start with a letter, underscore (_), or dollar sign ($). Subsequent characters can also be digits (0–9).
    Because JavaScript is case sensitive, letters include the characters "A" through "Z" (uppercase) as well as "a" through "z" (lowercase).
    You can use most of ISO 8859-1 or Unicode letters such as å and ü in identifiers.
    Some examples of legal names are Number_hits, temp99, $credit, and _name.

JavaScript is case sensitive. This means myVariable is not the same as myvariable. If you have problems in your code, check the case!
After declaring a variable, you can give it a value:

        let myVariable = 'Bob';

You retrieve the value by calling the variable name:

        myVariable;

After assigning a value to a variable, you can change it later in the code:

        let myVariable = 'Bob';
        myVariable = 'Steve';

Note that variables may hold values that have different data types:

Variable         Explanation                                             Example
String           This is a sequence of text known as a string.           let myVariable = 'Bob';
                 To signify that the value is a string,
                 enclose it in single quote marks.	

Number           This is a number. Numbers don't have                    let myVariable = 10;
                 quotes around them.

Boolean          This is a True/False value. The words true              let myVariable = true;
                 and false are special keywords that don't need
                 quote marks.

Array            This is a structure that allows you to store            let myVariable = [ 1,'Bob','Steve',10];
                 multiple values in a single reference.                  myVariable[0], myVariable[1], etc.
                 Refer to each member of the array like this:                                                       

Object           This can be anything. Everything in JavaScript is       let myVariable = myVariable = document.querySelector('h1');
                 an object and can be stored in a variable.              All of the above examples too.
                 Keep this in mind as you learn.


So why do we need variables? Variables are necessary to do anything interesting in programming. If values couldn't change, then you couldn't do anything dynamic, like personalize a greeting message or change an image displayed in an image gallery.
==================================================================================================================================================================================================

==================================================================================================================================================================================================
Comments:
Comments are snippets of text that can be added along with code. The browser ignores text marked as comments. You can write comments in JavaScript just as you can in CSS:

        /*
        Everything in between is a comment.
        */

If your comment contains no line breaks, it's an option to put it behind two slashes like this:

        // This is a comment
==================================================================================================================================================================================================

==================================================================================================================================================================================================
Operators:
An operator is a mathematical symbol that produces a result based on two values (or variables). In the following table, you can see some of the simplest operators, along with some examples to try in the JavaScript console.

Addition	            Add two numbers together or combine two strings.	                +	                     6 + 9; 
                                                                                                                     'Hello ' + 'world!';

Subtraction,            These do what you'd expect them to do in basic math.                -, *, /                  9 - 3;
Multiplication,                                                                                                      8 * 2; // multiply in JS is an asterisk
Division			                                                                                                 9 / 3;

Assignment             	As you've seen already: this assigns a value to a variable. 	    =                        let myVariable = 'Bob';

Strict equality	        This performs a test to see if two values are equal.                ===                      let myVariable = 3;
                        It returns a true/false (Boolean) result.		                                             myVariable === 4;

Not, Does-not-equal	    This returns the logically opposite value of what it precedes.      !, !==                   For "Not", the basic expression is true, 
                        It turns a true into a false, etc.. When it is used alongside                                but the comparison returns false because we negate it:
                        the Equality operator, the negation operator tests                                           let myVariable = 3; 
                        whether two values are not equal.                                                            !(myVariable === 3);

                                                                                                                     "Does-not-equal" gives basically the same result with different syntax.
                                                                                                                     Here we are testing "is myVariable NOT equal to 3".
                                                                                                                     This returns false because myVariable IS equal to 3:
                                                                                                                     let myVariable = 3;
                                                                                                                     myVariable !== 3;

There are a lot more operators to explore, but this is enough for now.
==================================================================================================================================================================================================

==================================================================================================================================================================================================
Conditionals:
Conditionals are code structures used to test if an expression returns true or not. A very common form of conditionals is the if...else statement. For example:

        let iceCream = 'chocolate';
        if(iceCream === 'chocolate') {
          alert('Yay, I love chocolate ice cream!');
        } else {
          alert('Awwww, but chocolate is my favorite…');
        }

The expression inside the if() is the test. This uses the strict equality operator (as described above) to compare the variable iceCream with the string chocolate to see if the two are equal. If this comparison returns true, the first block of code runs. If the comparison is not true, the second block of code—after the else statement—runs instead.
==================================================================================================================================================================================================

==================================================================================================================================================================================================
  
Functions:
Functions are a way of packaging functionality that you wish to reuse. It's possible to define a body of code as a function that executes when you call the function name in your code. This is a good alternative to repeatedly writing the same code. You have already seen some uses of functions. For example:

        let myVariable = document.querySelector('h1');
        alert('hello!');

These functions, document.querySelector and alert, are built into the browser.

If you see something which looks like a variable name, but it's followed by parentheses— () —it is likely a function. Functions often take arguments: bits of data they need to do their job. Arguments go inside the parentheses, separated by commas if there is more than one argument.

For example, the alert() function makes a pop-up box appear inside the browser window, but we need to give it a string as an argument to tell the function what message to display.

You can also define your own functions. In the next example, we create a simple function which takes two numbers as arguments and multiplies them:

        function multiply(num1,num2) {
            let result = num1 * num2;
            return result;
        }

Try running this in the console; then test with several arguments. For example:

        multiply(4, 7);
        multiply(20, 20);
        multiply(0.5, 3);

The return statement tells the browser to return the result variable out of the function so it is available to use. This is necessary because variables defined inside functions are only available inside those functions. This is called variable scoping.
==================================================================================================================================================================================================

==================================================================================================================================================================================================

Events:
Real interactivity on a website requires event handlers. These are code structures that listen for activity in the browser, and run code in response. The most obvious example is handling the click event, which is fired by the browser when you click on something with your mouse. To demonstrate this, enter the following into your console, then click on the current webpage:

        document.querySelector('html').addEventListener('click', function()
         {
            alert('Ouch! Stop poking me!');
         });

There are many ways to attach an event handler to an element. Here we select the <html> element. We then call its addEventListener() function, passing in the name of the event to listen to ('click') and a function to run when the event happens.

Note that

        document.querySelector('html').addEventListener('click', function() 
         {
            alert('Ouch! Stop poking me!');
         });

is equivalent to

        let myHTML = document.querySelector('html');
        myHTML.addEventListener('click', function() {
            alert('Ouch! Stop poking me!');
        });

It's just shorter

The functions we just passed to addEventListener() here are called anonymous functions, because they don't have a name. There's an alternative way of writing anonymous functions, which we call an arrow function. An arrow function uses () => instead of function ():

        document.querySelector('html').addEventListener('click', () => {
            alert('Ouch! Stop poking me!');
        });
==================================================================================================================================================================================================




