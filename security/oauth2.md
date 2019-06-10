# Client Credentials    

![Screenshot](1.png)



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

#### 4 Authorization Response
The authorization server authenticates the client and validates
the authorization grant, and if valid, issues an access token.

#### 5 Authorization Request
The client requests the protected resource from the resource
server and authenticates by presenting the access token.

#### 6 Authorization Response
The resource server validates the access token, and if valid,
serves the request.
