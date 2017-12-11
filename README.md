# Stateless vs stateful authentication

## What is session based authentication (stateful) vs token based authentication (stateless)?
Both authentications use cookies to identify the user.

you can also hash a normal cookie, but jwt is an established cookie-signing standard.

**1. Session based authentication**\
After authentication, a session id is stored in the cookie, and that id is cross referenced with a database which contains all the user information, such as username, access privileges(claims), etc


**2. Token based authentication**\
With token based authentication, claims of the user are stored in a jwt, and there is no need to cross reference a database which stored details about the user's session, as its all in the jwt.

N.B. sensitive information should still not be stored in a jwt.



## Draw flow diagrams to show the steps involved in each process

**1. Session based authentication**\
![session_based](https://i.imgur.com/cGa7eQn.png)


**2. Token based authentication**\
![token_based](https://i.imgur.com/OCD5AJB.png)




## What are the advantages and disadvantages of each?
**1. Session based authentication**
advantages : 
* More detailed data can be referenced to a session ID in a cookie.
disadvantages :
* Requires big database.
* Difficult to scale when more than one server.

**2. Token based authentication**
advantages :
* Light-weight
* Do not need database of session IDs.
* You do not need to append database 
disadvantages :
* Header and payload are only encoded, not encrypted.


