### closures
A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment)       

To use a closure, simply define a function inside another function and expose it

    var add = (function () {
      var counter = 0;
      return function () {counter += 1; return counter}
    })();

    add(); //1
    add(); //2
    add(); //3



