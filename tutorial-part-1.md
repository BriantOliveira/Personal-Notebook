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

Notice that we are ignoring the **node\_modules** folder. The reason why we are ignoring this folder, is because all the dependencies that will be used in this project will be located in the folder, which is a lot of memory space to the repository, plus we want to ensure that whomever clones this code gets the most updated version of the dependencies. All the other files that are being ignored are IDE's default files, expect the **.env** file, which is being ignore because we **don't** want people to have our environment variables values.

In this project I will be using the [Airbnb style guide](https://github.com/airbnb/javascript) in order to make the codebase more readable. I extremely recommend that you go on your IDE settings and install the [ESLint](https://eslint.org/) plugging.

_**Warnings:** Initially the linter and the style guide might drive you a bit crazy, but trust me if you stick with it until the end, you will start noticing the these tools will turn you into a much organized developer._

In oder to make the style guide work in your codebase and to ensure that everyone working in the given repository is using the same style guide, we need to make do a few things. First let's install a few dependencies, go to you terminal again and type:

```
$ npm install eslint eslint-config-airbnb-base eslint-plugin-import --save-dev
```

Notice that we are** --save-dev** in the end. This command will create an devDependencies section in your package.json, this means that those given dependencies are only to be accessible to the development environment. So now your package.json should look like this:

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
  },
  "devDependencies": {
    "eslint": "^4.19.0",
    "eslint-config-airbnb-base": "^13.1.0",
    "eslint-plugin-import": "^2.14.0",
  }
}
```

Now that we've installed the dependencies needed, we need to create a file in the root directory called **.eslintrc.json**

```
$ touch .eslintrc.json
```

Now in let's add something to the **.eslintrc.json** file:

```
{
  "extends": "airbnb-base"
}
```

The **.eslintrc.json **is a configuration file that will enable the Airbnb style guide in your code. Now that we have the style guide up and running, let's create our server. Go to the **app.js** file, the first thing that we will need is to import all the dependencies that will be used:

```
/* eslint-disable no-console */
/*
*   Bookstore Tutorial
*   REST API Unit Test
*/

require('dotenv').config();
const cookieParser = require('cookie-parser');
const express = require('express');
const path = require('path');
const mongoose = require('mongoose');
const sanitizer = require('sanitize');
const expressSanitizer = require('express-sanitizer');
const bodyParser = require('body-parser');
```

The next step is to instantiate your server and add a listening PORT number that your server will be running on:

```
/** Instantiate the server */
const app = express();

/** Instantiate a PORT number */
const PORT = process.env.PORT || 3000;


app.listen(PORT, () => {
  console.log('Bookstore listening on port', PORT);
});
```

Now let's add the middlewares:

```
/** Set up static public directory */
app.use(express.static(path.join(__dirname, '..', 'public')));

/** Middleware */
app.use(cookieParser());
app.use(express.json());
app.use(express.urlencoded({ extended: true }));
app.use(sanitizer.middleware);
app.use(expressSanitizer());
app.use(bodyParser.text());
app.use(bodyParser.json({ type: 'application/json' }));
```

So far your **app.js** server file should look like this:

```
/* eslint-disable no-console */
/*
*   Bookstore Tutorial
*   REST API Unit Test
*/

require('dotenv').config();
const cookieParser = require('cookie-parser');
const express = require('express');
const path = require('path');
const mongoose = require('mongoose');
const sanitizer = require('sanitize');
const expressSanitizer = require('express-sanitizer');
const bodyParser = require('body-parser');

/** Instantiate the server */
const app = express();

/** Instantiate a PORT number */
const PORT = process.env.PORT || 3000;

/** Import Routes */


/** Set up static public directory */
app.use(express.static(path.join(__dirname, '..', 'public')));

/** Middleware */
app.use(cookieParser());
app.use(express.json());
app.use(express.urlencoded({ extended: true }));
app.use(sanitizer.middleware);
app.use(expressSanitizer());
app.use(bodyParser.text());
app.use(bodyParser.json({ type: 'application/json' }));


/** Set up routes */


/** Listening PORT */
app.listen(PORT, () => {
  console.log('Bookstore listening on port', PORT);
});
```

---

## Step 2 - Connecting Database

On this project we will be using MongoDB. The way that we will be connecting the database will be a little different from the conventional way. We are going to connect to the database accordantly to the environment that the server is running on, that way you can switch between environments easily.

On the config folder, create another folder called **env**. Now inside the environment folder, create these 4 files:

```
├── config
| ├── env
|     ├─ development.js
|     ├─ index.js
|     ├─ production.js
|     └─ test.js
└── ...
```

Inside **development.js** we are going to this:

```
module.exports = {
  env: 'development',
  db: 'mongodb://localhost/bookstore',
};
```

Inside **production.js** we are going to this:

```
module.exports = {
  env: 'development',
  db: process.env.DBURI,
};
```

Inside** test.js** we are going to this:

```
module.exports =  {
  env: 'test',
  db: 'mongodb://localhost/test-bookstore',
};
```

Notice that we are creating environment variables. These variables will allow us to connect to a specific database according to the environment that the server is running on. That way if you run **npm test** on your terminal, it will only connect to you test database.

If you have already a live database on MLab or Mongo Atlas, don't forget to add the database URL to your **.env** file. In case if you don't, no worries, I will teach you further down in the tutorial.

```
DBURI='mongodb://<db user>:<db password>.mlab.com:56789/mydb
```

On the **index.js **file, we are going to add this:

    // This sipped of code is just telling the server that if there isn't a environment
    // being declared already, to connect to the development database.

    const env = process.env.NODE_ENV || 'development';
    // eslint-disable-next-line import/no-dynamic-require
    const config = require(`./${env}`);

    module.exports = config;

Now that we have the database configuration files all set up, let's import the database configuration and add the database connection to the **app.js** file. 

```
const config = require('./config/env');
```

    /** MongoDB connection */
    mongoose.Promise = global.Promise;

    mongoose.connect(config.db, { useMongoClient: true });
    mongoose.connection.on('error', () => {
      throw new Error(`unable to connect to database: ${config.db}`);
    });
    mongoose.connection.on('connected', () => {
      console.log(`Connected to database: ${config.db}`);
    });

    if (config.env === 'development') {
      mongoose.set('debug', true);
    }

Your **app.js** file should look like this:

    /* eslint-disable no-console */
    /*
    *   Bookstore Tutorial
    *   REST API Unit Test
    */

    require('dotenv').config();
    const cookieParser = require('cookie-parser');
    const express = require('express');
    const path = require('path');
    const mongoose = require('mongoose');
    const sanitizer = require('sanitize');
    const expressSanitizer = require('express-sanitizer');
    const bodyParser = require('body-parser');
    const config = require('./config/env');

    /** Instantiate the server */
    const app = express();

    /** Instantiate a PORT number */
    const PORT = process.env.PORT || 3000;

    /** Import Routes */


    /** Set up static public directory */
    app.use(express.static(path.join(__dirname, '..', 'public')));

    /** Middleware */
    app.use(cookieParser());
    app.use(express.json());
    app.use(express.urlencoded({ extended: true }));
    app.use(sanitizer.middleware);
    app.use(expressSanitizer());
    app.use(bodyParser.text());
    app.use(bodyParser.json({ type: 'application/json' }));


    /** MongoDB connection */
    mongoose.Promise = global.Promise;

    mongoose.connect(config.db, { useMongoClient: true });
    mongoose.connection.on('error', () => {
      throw new Error(`unable to connect to database: ${config.db}`);
    });
    mongoose.connection.on('connected', () => {
      console.log(`Connected to database: ${config.db}`);
    });

    if (config.env === 'development') {
      mongoose.set('debug', true);
    }

    /** Set up routes */

    /** Listening PORT */
    app.listen(PORT, () => {
      console.log('Bookstore listening on port', PORT);
    });




