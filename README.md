# MEAN-Website-Backend
Experimental Backend application written using MEAN stack.

Frontend application is written in [MEAN-Website-Frontend](https://github.com/GoyalYatin/MEAN-Website-Frontend) repo.

## Index
- [Todo API](#todo)
- [Architecture](#arch)
- [Setup](#setup)
    - [Environment Setup](#env)
    - [Database Setup](#db)
    - [Project Setup](#project)
- [Testing the API](#test)
    - [Insert API](#insert)
    - [Get API](#get)
    - [Update API](#update)
    - [Delete API](#delete)
- [Reference](#ref)
- [License](#license)

## <a name="todo"></a>Todo Api
A simple todo API made with NodeJS, ExpressJS and MongoDB. Can be used as a back-end for learning front-end technologies without making a standalone API for that purpose.

## <a name="arch"></a>Architecture
![Highlevel](doc/highlevel.png)

Above picture describes how the applications are positioned. This is high level flow.

Testing is done manually using postman for backend application and manually via UI for frontend application. Postman is used to trigger webservice calls. The tests can be automated using Robot framework's requests and ui testing libraries.

![Lowlevel](doc/lowlevel.png)

This picture describes the sequence of the calls, this is low level design for this complete application, this repo only consist of backend side, along with mongoDb setup scipts. 


## <a name="setup"></a>Setup
#### <a name="env"></a>Environment Setup
- First go here — https://nodejs.org/en/download/ and Install NodeJS.
- Download and Install MongoDB — https://www.mongodb.com/download-center#community
- Download a good Text Editor or IDE. I Personally prefer Visual Studio Code — https://code.visualstudio.com/download


Now the environment Setup is done. Let’s get into the command line.

First we need to install ExpressJS. The most popular NodeJS Framework.

```
npm install -g express express-generator
```

This will install ExpressJS and the ExpressJS Official generator packages. Now let’s generate the Application using the Express Generator.

```
express --view=ejs todoapp
```

Now the express App is generated. Go inside the directory.

````
cd todoapp
npm install
````
All the necessary packages will be installed.
At first let’s install all the necessary packages we will be using throughout this app.

````
npm install --save bluebird mongoose mongoose-paginate nodemon
````

#### <a name="db"></a>Database Setup

Download and install MogoDB.
Make sure that the database is running at `127.0.0.1:27017`
DB name `todoapp` should be available


#### <a name="project"></a>Project Setup

Now run `cd todo-api` to go inside the directory

Run `npm install` to install all the dependencies.

Run `npm install -g nodemon` to install Nodemon Globally.

Run `npm start` to run the NodeJS Server.

## <a name="test"></a>Testing the API 

#### <a name="insert"></a>Insert API
This is a POST call

URL - `http://localhost:3000/api/todos`

Call Parameters
- title
- description
- status

URL with parameters - `http://localhost:3000/api/todos?title=Test1&description=Testing the insert api&status=pending`

#### <a name="get"></a>Get API
This is a Get call

URL - `http://localhost:3000/api/todos`

#### <a name="update"></a>Update API
This is a Put call

URL - `http://localhost:3000/api/todos`

URL with parameters - `http://localhost:3000/api/todos?title=Test1&description=Testing the insert api&status=pending&_id=5d5926c8356670fb053ee5ea`

#### <a name="delete"></a>Delete API
This is a Delete call

URL - `http://localhost:3000/api/todos`

URL with parameters - `http://localhost:3000/api/todos/5d5926c8356670fb053ee5ea`

## <a name="ref"></a>Reference
This is learning project inspired from
https://medium.com/netscape/mean-app-tutorial-with-angular-4-part-1-18691663ea96

## <a name="license"></a>License
[MIT](LICENSE) License