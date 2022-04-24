# CS-465
SNHU
Full Stack Development


-Main Branch-
Currently contains 7 Branches with their respective Modules.



Architecture
Compare and contrast the types of frontend development you used in your full stack project, including Express HTML, JavaScript, and the single-page application (SPA).

- We started with an Express/Node.js application which used Handlebars templating engine to retrieve and display JSON files. This allowed for quick changes/prototyping.
- after this we setup a MongoDB server and an Express/Node.js RESTful back-end within the encapsulating express application. This used HTTP calls and perform Create, Read, Update, Delete by creating request URL paths and parameters
- Seperating requests with MVC (Model, View, Controller) architecture. Routes forward incoming requests to their respective controllers. The controller can accept a parsed request and generate a response such as 404 for not found or 200 for success.
- The API can be called to pull lists of data and render it on the page. The API and the application logic are both wrapped in the same Express logic. This in turn will make it easier to call between the Express/NodeJS RESTful API and the front-end Express/NodeJs/Handlebars express app
- The structure consists of app_api/controllers, app_api/models, app_api/routes and app_server/controllers, app_server/routes, and app_server/views.
- Last implementation was SPA interacting with the REST API to create and read trip listings

Why did the backend use a NoSQL MongoDB database?
-scalability is cheaper than relational databases and better performance can be achieved by simply adding a shard to the server, rather than buying better hardware.
This scaling is horizontal.




Functionality
How is JSON different from Javascript and how does JSON tie together the frontend and backend development pieces?
Provide instances in the full stack process when you refactored code to improve functionality and efficiencies, and name the benefits that come from reusable user interface (UI) components.
-Javascript objects values can be any datatype, including functions, which is not possible with JSON.
-JSON supports Strings, Numbers, Objects, Arrays, Booleans, and null value. 
-Key names and strings must be double quoted. 


Testing
Methods for request and retrieval necessitate various types of API testing of endpoints, in addition to the difficulties of testing with added layers of security. Explain your understanding of methods, endpoints, and security in a full stack application.

-Within our app, when a user posts their credentials to the server via an API, the server validates these credentials by using the database and returning a JSON web token to the browser. The browser can then save this token for reuse later.
-Between the mean stack approach and traditional server application, is that instead of storing a user session data on the server the data is instead stored in the browser client side
- The token is used by the server that generated the token to authenticate a user when it's returned in a subsequent request
-The JSON web token helps pass data around between the API on the server and the SPA in the browser
- We can track user sessions for user logins by using JSON web tokens to securely call API endpoints
- 




Reflection
How has this course helped you in reaching your professional goals? What skills have you learned, developed, or mastered in this course to help you become a more marketable candidate in your career field?
