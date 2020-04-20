# EinoServer
Back-end server for the android-application Eino 


# Running the server

```shell

    git clone https://github.com/Poufy/EinoServer.git
    cd EinoServer
    npm install
```
You also need to create a config folder in the root directory with a config.js file with a json object that has
a hostURL attribute that specifies the IP you're hosting on. I suggest http://localhost:3000, and you also need dbConnectionString attribute to store your connection string to your mongodb database.

Follow that by

```shell

    npm run build
    node transpiled-server/app.js
```
and then the server is ready to go!

# Routes

**User**
----

* **End-Points**

  `GET` /users/ To return all users

  `GET` /users/:id To return a specific user

  `POST` /users/ To add a user

* **Success Response:**

  * **message:** Created user successfully <br />
    **createdUser:** `createdUser: {
          _id: 1,
          email: noor@yahoo.com,
          password: #dsadsadg323,
          displayName: noor,
          image: img.png,
          skills: array,
          available: true,
          request: {
            type: "GET",
            url: localhost:3000/users/1
          },
        }`
 
* **Error Response:**

  * **error:** `{ error : "No such user exists with this ID" }`