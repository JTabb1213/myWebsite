## Project Description
This project was created to learn and apply industry standard software engineering concepts, technology, and design. I did this by building a website using react.js and node/express that displays city information. To build this website I used:

[Rest Apis](#RestAPI)
* My backend is built as a rest api. I did this to make clients such as the front end web pages easily retrieve, modify, or delete data from various resources.

[User authentication and shared caching](#UserA)
* I have user authentication for this website, so if a user wants to gain access to the protected parts of this website, they must either create an account or give a valid username and password 

 [Databases](#db)
* I use a postgreSQL database to store user information as well as be a source of weather info. 

 [Good design practice](#design)
* Through building this website, I realized just how important it is to follow good design practice to make the final  product run smoothly and to aid the development process. 


## Rest apis:
<details>
	<summary>Click here to see more about rest api</summary>


* My backend is built as a rest api, using node.js and express.js. This involved creating various endpoints to handle different types of requests.
* I have done this to provide a standardized interface for clients such as my frontend to use http requests to communicate with components in my backend. 
* I have implemented 5 http methods: get, put, post, delete, and patch. Each endpoint, when called upon, will handle the request accordingly, performing operations such as updating a database with user/weather information, or getting real time weather information. 
* I have added OAS (open api spec) support to the api, the official contract can be viewed here: [https://jtabb1213.github.io/weather/#/](https://jtabb1213.github.io/weather/#/)
* I have a variety of providers set up to get information from, including a google map api, two real time weather apis, and a personal database. 

</details>

<a id="RestAPI"></a>

## User authentication and shared caching:

<details>



* I use a postgre SQL database to store user information. 
* The reason I added this feature was purely for practice with user authentication.
* When the user attempts to login, an http request is sent to the database to confirm that the user is found, which if successful, will make a 10 minute session for the user. This allows the user to access the protected endpoints of the website
* I have also a create account endpoint, which will add user information to the database.
* Additionally, I have added shared caching, which stores the user session in a redis store. Now, if I wish to scale up my web application, users will not have any authentication issues when switching between instances of my app.

</details>

<a id="UserA"></a> 

## Databases:

<details>



* As mentioned earlier, I have implemented a postgre sql database in this application.
* The reason I did this was to store user and weather information, which I do so in two different tables. 
* I can update the weather table by using postman to issue api calls to an endpoint in my api.
* I use the ORM library sequelize to interact with the database, and I have created models for the city and the user. 

</details>

<a id="db"></a>

## Good organization:

<details>



* One organization concept I tried my best to follow is the single responsibility principle.
* I have designed my backend so that each module is responsible for one thing.
* This makes it very easy to switch or add providers for the information, all you have to do is specify it in the ‘config’ file. 
* I also followed this principle to help me build a good front end. I have different components spread across multiple files, and I combine them to build a good web page. 

</details>

<a id="designs"></a>
