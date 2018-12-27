# Let's Get Started

In this tutorial we building a simple RESTful API.

### Part 1 - Setting up

Let's set up our server structure, for this project we will be using MVC architecture.

##### Step 1

Let's create our files and folder structures we need for this project. It should look like this:

```
  ├── config
  ├── controllers
  |     ├─ book.js
  ├── public
  |     ├── css
  |     ├── js
  |     └── img
  ├── models
  |     ├─ books.js
  ├── views
  ├── test
  ├── utils
  ├── app.js
  ├── .env
  ├── .gitignore
  └── ...
```

Now that we have all the folder structures, let's import the dependencies we will be using on this project. In order to manage all the dependencies, we need to create a package.json file.

```
$ npm init
```

This command should create your **package.json** file, it will request a few information about your project and in the end it should look like this:

```
{
  "name": "bookstore-api",
  "version": "1.0.0",
  "description": "This is a simple rest api tutorial",
  "main": "app.js",
  "scripts": {
    "start": "node app.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": ""
  },
  "author": "Elliot Briant",
  "license": "MIT",
  "bugs": {
    "url": ""
  },
  "homepage": "",
  "dependencies": {
    "bcrypt": "^3.0.1",
    "compression": "^1.7.3",
    "cookie-parser": "^1.4.3",
    "dotenv": "^6.2.0",
    "express": "^4.16.4",
    "express-sanitizer": "^1.0.4",
    "express-session": "^1.15.6",
    "jsonwebtoken": "^8.3.0",
    "mongo-to-knex": "^0.5.0",
    "mongoose": "^4.13.17",
    "morgan": "^1.7.0",
    "nodemon": "^1.18.4",
    "path": "^0.12.7",
    "sanitize": "^2.1.0",
    "winston": "^3.1.0"
  }
}
```

Now that we have our **package.json** and **package-lock.json**, we need to install all dependencies listed in the package.json:

```
$ npm install
```

or if you prefer, you can also install each dependency individually with:

```
$ npm install <dependency name> --save
```

So far we structure all the files and folders and installed the main dependencies needed. But before we move on, let's edit our **.gitignore** file. This file tells git what needs to be ignored and not commited along with everything else in the repository.

```
node_modules
.DS_Store
.idea
.vscode
.env
```

Notice that we are ignoring the **node\_modules** folder. The reason why we are ignoring this folder, is because all the dependencies that will be used in this project will be located in the folder, which is a lot of memory space to the repository, plus we want to ensure that whomever clones this code gets the most updated version of the dependencies. 



