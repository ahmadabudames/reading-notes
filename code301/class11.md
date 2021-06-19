# What is OAuth
***Auth doesn’t share password data but instead uses authorization tokens to prove an identity between consumers and service providers. OAuth is an authentication protocol that allows you to approve one application interacting with another on your behalf without giving away your password.***
> Give an example of what using OAuth would look like.
- when we want to login with a new using another account just like when we login into Netlify using GitHub.

> How does OAuth work? 
> What are the steps that it takes to authenticate the user?
***OAuth is not authentication. It’s an authorization protocol, or, better yet, a delegation protocol. It’s for this reason that identity protocols such as OpenID Connect exist and legacy protocols such as SAML use extension grants to link authentication and delegation.***
# What is OpenID?
- OpenID allows you to use an existing account to sign in to multiple websites, without needing to create new passwords
> What is the difference between authorization and authentication?
***In simple terms, it’s like giving someone official permission to do something or anything. For example, the process of verifying and confirming employees ID and passwords in an organization is called authentication, but determining which employee has access to which floor is called authorization.***
> What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
- The Authorization Code Flow + PKCE is an OpenId Connect flow specifically designed to authenticate native or mobile application users.
>What is Client Credentials Flow?
***In the client credentials flow, permissions are granted directly to the application itself by an administrator. When the app presents a token to a resource, the resource enforces that the app itself has authorization to perform an action since there is no user involved in the authentication.***

# PKCE
> What is Resource Owner Password Flow?
- The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token and, optionally, a refresh token. … The primary difference is that the user’s password is accessible to the application. This requires strong trust of the application by the user.