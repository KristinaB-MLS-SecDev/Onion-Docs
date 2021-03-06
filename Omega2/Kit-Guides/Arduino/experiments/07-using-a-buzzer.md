## Using a Buzzer

// description of what this experiment will accomplish and what we'll learn

## The Buzzer Element
// should be its own markdown file

// description of the buzzer: we apply current, it buzzes, have some photos


## Building the Circuit

// build a circuit with a push button input and a buzzer

### Hooking up the Components

// in depth wiring details on building the circuit
// should be pretty straight-forward for the buzzer, look it up online

// reuse the push button instructions from the push button article


## Writing the Code

// in the loop function, read the input value of the push button. if the button is pressed, activate the buzzer, when it is released, stop buzzing



### What to Expect

// explanation that pressing the button will make the buzzer sound

### A Closer Look at the Code

// we'll be looking at the difference between polling and interrupt based input

#### Polling a value

// talk about polling and how we continuously read the input value coming from the push button and then act on it
// make a note about how this is expensive/wasteful for the microcontroller since you can't do anything else during the polling

#### Interrupt Alternative

// an alternative to polling is interrupt-based inputs
// to implement the same functionality as we have above, we'll need to set an action - the interrupt - that will trigger a response - the interrupt service routine.
// in our case, the interrupt action will be a change in the signal coming from the push button (both rising and falling edges), and we will write a function that we will register as the interrupt service routine, ie it will run when the interrupt is triggered - nothing of interest happens in the loop() function

// new code:
// have an interrupt routine programmed to the button input, when an edge is detected, flip the value that controls the buzzer and write it to the output connected to the buzzer
// have an led blinking in the loop() function

##### What to Expect
// highlight that the loop function is able to do its thing - keep the LED blinking steadily AND take care of the button input
