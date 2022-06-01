# Day 33 Reading Notes --> Authentication & Production Server

## Reading
* [JSON Web Tokens](https://jwt.io/introduction/)
* [DRF JWT Authentication](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html)
* [Django Runserver Is Not Your Production Server](https://vsupalov.com/django-runserver-in-production/)
<hr/>

* JWT aka `JSON Web Token` is an open standard that defines a compact and self-contained way for securely 
  transmitting information between parties as a JSON object.
* Can be signed with either a secret or a public/private key pair using RSA or ECDSA
* Use for:
  * Authorization, or 
  * Information Exchange
* Token structure -> consists of 3 parts seperated by a `.`
  * Header:
    * the type of token it is, in this case, JWT
    * the signing algorithm used, such as, RSA
  * Payload:
    * 3 types of claims:
      * Registered -> a set of predefined claims that are not mandatory but, are definitely recommended
        * `iss` issuer
        * `sub` subject
        * `aud` audience
        * etc...
      * Public -> can be defined at will, however, to avoid collisions, they should be defined in the:
        * IANA JSON Web Token Registry
        * defined as a URI that contains a collision resistant namespace
      * Private -> custom claims that are created to share information between parties that agree on using them and 
        are neither registered nor public
* Signature -> is used to verify that the message wasn't changed. To create this part
  * encoded header + encoded payload + a secret (the algorithm specified in the header) -> sign that
```
    HMACSHA256(
      base64UrlEncode(header) + '.' +
      base64UrlEncode(payload),
      secret)
```
* ***NOTE:*** For signed tokens this information, though protected against tampering, is readable by anyone. **DO 
  NOT** put secret information in the payload or header unless it is encrypted.
* To play with these concepts and to put them into practice go to [jwt.io Debugger](https://jwt.io/#debugger-io)

## Videos
* [JWT with DRF (https://www.youtube.com/watch?v=Fhcn2qx-4VQ)]

### Bookmark & Review
* [Gunicorn](https://gunicorn.org/)
* [Django Migrations: A Primer](https://realpython.com/django-migrations-a-primer/)
