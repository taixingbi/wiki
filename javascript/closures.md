### closures

---
A closure is the **combination** of a function and the _lexical_ environment within which that function was declared.      

To use a closure, simply define a function inside another function and expose it

* closures for data privacy.    
`.get()` method is defined inside the scope of `getSecret()`, which gives it access to any variables from `getSecret()`, and makes it a privileged method. In this case, the parameter, `secret`.

        const getSecret = (secret) => {
          return {
            get: () => secret
          };
        };

        test('Closure for object privacy.', assert => {
          const msg = '.get() should have access to the closure.';
          const expected = 1;
          const obj = getSecret(1);

          const actual = obj.get();

          try {
            assert.ok(secret, 'This throws an error.');
          } catch (e) {
            assert.ok(true, `The secret var is only available
              to privileged methods.`);
          }

          assert.equal(actual, expected, msg);
          assert.end();
        });


* closures with self-invoking functions

    var add = (function () {
      var counter = 0;
      return function () {counter += 1; return counter}
    })();

    add(); //1
    add(); //2
    add(); //3

---

#### 
lexical environment

* environment record



* out reference



