# Client Credentials    




#### 1 Authorization Request
requests authorization from the resource owner .   

* grant_type: authorization_code (vs token) . 
* client_id: username   
* client_secret: password    
* code: The Authorization Code received from the initial authorize call.    
* redirect_uri: The URL must match exactly the redirect_uri passed to /authorize.    
    
#### 2 Authorization Response . 
The client receives an authorization code 

#### 3 Authorization Request
The client requests an access token by authenticating with the
authorization server and presenting the authorization grant.

#### 4 Authorization Request
The authorization server authenticates the client and validates
the authorization grant, and if valid, issues an access token.
