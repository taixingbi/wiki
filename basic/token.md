### JSON Web Token (JWT) 
---
It is a JSON object as a safe way to represent a set of information between two parties. 
The token is composed of a header, a payload, and a signature.

* header
it contains information about how the JWT signature should be computed

    {
        "typ": "JWT",
        "alg": "HS256"
    }
    
* payload
“claims” of the JWT
 
    {
        "userId": "b08f86af-35da-48f2-8fab-cef3904660bd"
    }
    
* signature
signature is computed based on hashing algorithm

    data = base64urlEncode( header ) + “.” + base64urlEncode( payload )
    hashedData = hash( data, secret )
    signature = base64urlEncode( hashedData )
    
##### csrf token
a simple GET request to a state-changing URL X will not work unless an csrf token is included
 
