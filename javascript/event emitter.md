
#### event 
   * on:  bind a function with the event
   * emit: fire an event.

### Node JS
from server listen to event emmiter
* listen()  
  
  Whenever an request is received,it handles the request and returns some response. 

      server.listen( {
          handleRequest: function( request, response ) {
              // handle the request...
              // handle the response...
          },
          handleError: function( err ) {
              // handle the error...
          }
      } );

  http server will call this function every time it receives an HTTP request

* event emitter  
  use multiple handlers for the same event 
  
      const EventEmitter = require( 'events' );
      class MyClass extends EventEmitter {
          doSomething() {
              // do something...
              if ( !err )
                  this.emit( 'success', result );
              else
                  this.emit( 'error', err );
          }
      }
      
   


