# ORM & Sequelize.js

---

**What is sequelize.js?**

Sequelize is a module that enables js developers to work with relational data more easily.

##### Benefits:

* You write less code
* You will write more consistent code
* You can mostly avoid SQL queries
* It abstracts the db engine
* Id does a lot of things automatically
* Migrations

**Limitations:**

* Complicated queries can be slow
* Additional learning curve
* Documentation isn't the best
* Loss of flexibility
* Which can hurt in the long run, according to some

Get Started:

```
$ npm install --save sequelize 

# And of the following 
$npm install --save pg pg-hstore
$npm install --save mysql
$npm install --save sqlite3
$npm install --save tedious
```

```
app.js

const Sequelize = require("sequelize"); 

const connection = new Sequelize("db name", "username", "password", {
//If using a database engine, you have to specify 
dialect: postgras
);

//Article = Table name

const Article = connection.define("article", {
    title: Sequelize.STRING, 
    content: Sequelize.STRING
});
connection.sync();

Article.findById(5).then(function(article) {
console.log(article);
});
```

**Define a model **

```
var Article = connection.define('article', {
    title: Sequelize.STRING,
    //to make sure that the title will always be unique  
    unique: true,
    //to require a title in the Article table
    allowNull: false

     //body: Sequilize.TEXT
    //code self documenting and extensible 

     body: {
    type: Sequelize.TEXT
    //defaltValue: 'coming soon...'
    }
}, {
    //to disable the timestamp
    timestamps: false,
    //to prevent Sequelize to pluralize the tables
   freezeTableName: true

    });
});
```

**To synchronize the database **

**Inserting records **

```
connection.sync().then(function () {
    Article.create({
        title:'<title name>'
        body: '<body text>'

    })
});
```

**To make an Article to be approved add:**

```
approved: {
    type: Sequelize.BOOLEAN,
    defaultValue: false
    }
})
```

**Ex:**

```
var Sequelize = require('sequelize');

var connection = new Sequilize('demo_schema', 'root', 'password')

var Article = connection.define('article', { 
  title: Sequelize.BOOLEAN, 
  defaultValue:false
  }
})

connection 
  .sync({
  force: true 
  })
  .then(function(){
  var req = { 
    body: {
    approve: true, 
      title: 'Some title', 
      body:  'Some body'
      }
    }
    Article.create(req.body).then(function(insertArticle){
      // name of the attributes that allow setting
      fiels: ['title', 'body'] 
      }).the(function(insertArtile) {
      console.log(insertedArticle.dataValues); 
    })
```

**To insert multiple records at once:**

```
.then(funtion(){
    Article.bulkCreate([
    {
        title: 'Article 1',
        body: 'Article 1',
    }, 
    {
        title: 'Article 2', 
        body: 'Article 2'
    }
])
```



**To retrieve**

In case if you don't know the id number of the table that you are looking for, you can use the **find all method.**

```
Article.findById(id#).then(function(article) {
console.log(article.dataValues);
    });
});

Article.findAll().then(function(article) {
console.log(article.lenght);
    });
}):
```

The** object** called dataValues contain metadata.

The _**sync**_ method cannot update objects, only can create if it does not exist already.

To force a change that made to the table, you can use the force method, which you don't usually want to do it because it will erases the entire  table

```
connection.sync({
    force: true, 
    logging: console.log
}).then(function() {

}).catch(function(error) {
console.log(error);
});
```

**Validation**

```
validade: {
//specify the attribute that you want to valide
    len: 
    args: [10,150]
     //min len/ max len
    msg: 'Please enter a title with at least 10 chars but no more then 150'

}
```

**Hooks **

Sequelize hooks enable your grogram to react when internal squel eyes evens occur.

```
 hooks: {
 // It will be performed before the validate function
  beforeValidate: function() {
  },
  //It will be performed after the validation function 
  afterValidate: function() {

    }
  }
```



 **The best way to store a password in a data base is to hash an adaptive function like bcrypt.**

```
hooks: {
    afterValidate: function(user) {
    user.password = bcrypt.hashSync(user.password, 8); 
    }
}
```



