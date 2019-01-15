

### states
* pending: initial state, neither fulfilled nor rejected.
* fulfilled: meaning that the operation completed successfully.
* rejected: meaning that the operation failed.


### examples
* constructor

        const promise = new Promise((resolve, reject) => {
          //asynchronous code goes here
        });

* simple promise     

        var promise1 = new Promise(function(resolve, reject) {
          setTimeout(function() {
            resolve('foo');
          }, 300);
        });

        promise1.then(function(value) {
          console.log(value);
          // expected output: "foo"
        });

        console.log(promise1);
        // expected output: [object Promise]

* promise with ajax

        const promise = new Promise((resolve, reject) => {
          const request = new XMLHttpRequest();

          request.open('GET', 'https://api.icndb.com/jokes/random');
          request.onload = () => {
            if (request.status === 200) {
              resolve(request.response); // we got data here, so resolve the Promise
            } else {
              reject(Error(request.statusText)); // status is not 200 OK, so reject
            }
          };

          request.onerror = () => {
            reject(Error('Error fetching data.')); // error occurred, reject the  Promise
          };

          request.send(); // send the request
        });

        console.log('Asynchronous request made.');

        promise.then((data) => {
          console.log('Got data! Promise fulfilled.');
          document.body.textContent = JSON.parse(data).value.joke;
        }, (error) => {
          console.log('Promise rejected.');
          console.log(error.message);
        });



