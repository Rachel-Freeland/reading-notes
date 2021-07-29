# Reading for Day 11:

- [What is OAuth](<https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html>)

1. What is OAuth?
    - OAuth is an open-standard authoriztion protocol or framework that allows for servers and services to safely allow authenticated access to their assets.

2. Give an example of what using OAuth would look like.
    - An example of OAuth would be like when you go to a new site and you are given the option to login using another service such as Google or Facebook
3. How does OAuth work? What are the steps that it takes to authenticate a user?
    - If youare already signed into a site, such as, Facebook and you need to sign into another site or service, you are presented with the option to use the previous site's login to access the new site. There are 10 steps:
    1. The 1st site connects to the 2nd site on behalf of the user, using OAuth, providing the user's verified identity.
    2. The 2nd site generates a 1-time token and a 1-time secret unique to the transaction and parties involved.
    3. The 1st site gives this token and secret to the initiating user's client software.
    4. the client's software presents the request token and secret to their authoriztion provider.
    5. If not already authenticated to the authorization provider, the client may be asked to authenticate. Afterwards, the client is then asked to approve the authorization to the 2nd site.
    6. The user approves (or the software silently approves) the transaction at the 1st site.
    7. The user is given an approved access token.
    8. The user gives the approved access token to the 1st site.
    9. Then, the 1st site gives the access token to the 2nd site as proof of authentication on behalf of the user.
    10. The 2nd site then allows the 1st site access on behalf of the user.
  
4. What is an OpenID?
    - OpenID is an authentication service. To sum up the difference between OAuth and OpenID: OpenID is for humans logging into machines and OAuth is for machines that log into other machines.

-[Authorization and Authentication Flows](<https://auth0.com/docs/flows>)

1. What is the difference between authorization and authentication?
    - Authentication is confirming the user is who they say they are.
    - Authoriztion is confirmation that the user has permission to access the resource(s).
2. What is Authorization Code Flow?
    - It is the exchange of an Authoriztion Code for a token.
3. What is Authoriztion Code Flow with Proof Key for Code Exchange (PKCE)?
    - It is similar to Authoriztion Code Flow but it adds a secret
4. What is Implicit Flow with Form Post?
    - Using OpenID Connect a.k.a OIDC, the web app requests and obtains tokens throught the frontend without the need for secrets or extra backend calls.
5. What is Client Credentials Flow?
    - Used in machine-to-machine applications, the app is authenticated and authorized instead of the user.
6. What is Device Authoriztion Flow?
    - Instead of authenticating a user directly, a device can ask the user to go to a link on their computer or smartphone and authorize the device.
7. What is Resource Owner Password Flow?
    - This is where the user provides credentials typically via an interactive form. This is then sent to the backend and stored before exchanging a token.

## Additional Resources

- [AuthO for single page apps](<https://auth0.com/docs/libraries/auth0-react>)