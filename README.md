# JS-CONCEPTS

## my documentation for [33-js-concepts](https://github.com/leonardomso/33-js-concepts)

check the diff branches for the docs

# This, Call, Apply and Bind

## Call

The call() method calls the function with a given this value and arguments provided individually.

    let obj = {num: 2}

    function addToThis (a){
      return this.num + a;
    }
    console.log(addToThis.call(obj, 2)) //4

The obj variable provides the `this` value and the second argument of the call function provides the `addToThis` function its `a` argument.

## Apply

The apply() method calls the specified function with a given this value, and arguments provided as an array

It is the same as `call()`, just that you pass it an array and it will pass those values in the array into the function

    let obj = {num: 2}

    function addToThis (a, b, c){
      return this.num + a;
    }
    console.log(addToThis.apply(obj, [1,2,3])) //8

## Bind

The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

    const module = {
      x: 42,
      getX: function() {
        return this.x;
      }
    };

    const unboundGetX = module.getX;
    console.log(unboundGetX()); // The function gets invoked at the global scope
    // Expected output: undefined

    const boundGetX = unboundGetX.bind(module);
    console.log(boundGetX());
    // Expected output: 42
