# JavaScript Functions as First Class Data: Array of Functions

### Create a JavaScript Function That Loops Through a Function `Array`

Let's create an `Array` of dog-care functions so that we can report on the
activities we take in caring for Byron the Poodle.

When this program runs, it should print out:

```txt
console.log("Wake Byron the poodle");
console.log("Leash Byron the poodle");
console.log("Walk to the park with Byron the poodle");
console.log("Throw the frisbee for Byron the poodle");
console.log("Walk home with Byron the poodle");
console.log("Unleash Byron the poodle");
```

Start by creating a function for every activity that you see listed above:

```js
function wakeDog(dogName, dogBreed) {
  console.log(`Wake ${dogName} the ${dogBreed}`);
}
...
```

**Additionally**: Each function should **return** the string that it creates.
That is, we should create a `String`, log it to the console (using
`console.log()`), and return that `String`.

Continue writing _"generalized"_ functions for:

-   `wakeDog`
-   `leashDog`
-   `walkToPark`
-   `throwFrisbee`
-   `walkHome`
-   `unleashDog`

Each function's implementation will be a generalized invocation of
`console.log()`.

## Create the Array o' Functions

Next, create our "Array o' Functions!"

Create a variable called `routine`. This variable will be an `Array` all of the
functions we've just defined.

Note that this array should hold _references_ to each of the functions.

## Create a Function to Process the Array o' Functions

Lastly, create the function called `exerciseDog` that will take in two
arguments:

-   `dogName`
-   `dogBreed`

In the `exerciseDog` function, your goal is to call every function in the
`routine` array with the `dogName` and `dogBreed`,
and return a **new array** with the return values from each of those calls.

To break that down into steps, `exerciseDog` should:

-   **Iterate** over the `routine` array to get access to each function in the array
-   **Call** each function in the array, passing the `dogName` and `dogBreed`
    received by `exerciseDog()` to each function when calling it
-   Store the return value of each function's call in a **new array**
-   Return that **new array** from `exerciseDog`
