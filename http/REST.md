## get mehod
GET is used to request data from a specified resource.
* get request can be cached
* get request remain in the browser history
* get request can be bookmarked
* get request should never be used when dealing with sensitive data
* get request have length restrictions
* get request is only used to request data (not modify)
  
## post method
POST is used to send data to a server to create/update a resource.  
* post request are never cached
* post request do not remain in the browser history
* post request cannot be bookmarked
* post request have no restrictions on data length

## put method
PUT is used to send data to a server to create/update a resource.    
* calling the same PUT request multiple times will always produce the same result, POST not.

## head method    
HEAD is almost identical to GET, but without the response body.           
HEAD requests are useful for checking what a GET request will return before actually making a GET request - like before downloading a large file or response body



