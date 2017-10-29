# ORM & Sequelize.js

---

What is sequelize.js?

Sequelize is a module that enables js developers to work with relational data more easily. 



```
app.js

const Sequelize = require("sequelize"); 

const connection = new Sequelize("db name", "username", "password");
const Article = connection.define("article", {
    title: Sequelize.STRING, 
    content: Sequelize.STRING
});
connection.sync();

Article.findById(5).then(function(article) {
console.log(article);
});
```



