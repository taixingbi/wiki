### ajax
AJAX is a misleading name. AJAX applications might use XML to transport data, but it is equally common to transport data as plain text or JSON text.

Update a web page without reloading the page  
* Request data from a server - after the page has loaded  
* Receive data from a server - after the page has loaded  
* Send data to a server - in the background  


### process 
when an event happen     
step 1 in browse(client server), create request object and send request   
* XMLHttpRequest
  * status
    * 200: OK. The request has succeeded
    * 403: Forbidden
    * 404: Not Found
  * readyState    
    * 0: request not initialized 
    * 1: server connection established
    * 2: request received 
    * 3: processing request 
    * 4: request finished and response is ready
    


step 2 in server, process request, and create a reqonse and send back to a browse     
step 3 in browse, process returned data using js and update page content.      

![alt tag](https://www.w3schools.com/xml/ajax.gif)


### all types
* jquery  
* xml  







