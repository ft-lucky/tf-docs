# Registration


## Case 1: When user registers from registration modal



### __1:__
- Call to endpoint - __/oauth/register-rn__ - POST request
- Request body - user filled credentials 
- Response gives us :&nbsp; __x-tf-ecommerce__ from response header,&nbsp; user attributes - __firstname__, &nbsp; __lastname__, __email__  from response body


### __2:__
- Set __x-tf-ecommerce__ value inside first-party cookies and include __x-tf-ecommerce__ inside every request header to verify that the user is logged in

 ### __3:__
 - Call to endpoint - **/profile** - GET request <br>
 - Via __x-tf-ecommerce__ value inside request header back-end will verify that user is authentificated and will return user full information


  ***Important Note - after authentification every time we make a call to the endpoint we will get newly generated __x-tf-ecommerce__ cookie value from the request response header and we need to update our first-party cookie with this new value***