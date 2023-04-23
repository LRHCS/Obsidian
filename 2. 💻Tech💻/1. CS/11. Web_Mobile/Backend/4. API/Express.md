#javascript #backend

- Inition
```javascript
const express = require("express");

// start the server at port 3000
app.listen(3000, function () {
  console.log("Start...");
});
```


- Create Response for different router
```javascript
// user Router
const user = express.Router();
  
user.get("/list", function (req, res) {
  res.send("/user/list");
});
  
user.get("/detail", function (req, res) {
  str = JSON.stringify(req.query);
  prop = str.slice(7, 10);
  res.send(`user ${prop}`);
});
  
app.use("/user", user);
```

- View Engine(Handelbars)
```javascript
// Inition
app.set("views", "views");

app.set("view engine", "hbs");

// renders about.hbs to the /about route 
app.get("/about", function (req, res) {
  res.render("about"); // about is name of the file
});

```

- 404 & 500
```javascript
// 404
app.use("*", (req, res) => {
  res.status(404).render("404", { url: req.originalUrl });
});

// Throw error
app.use((err, req, res, next) => {
  res.status(500).render("500");
});
```
```html
<h1>404</h1>
<p>{{url}} not found</p> 
<!-- this url is danamic here -->
```

```js
app.get("/", function (req, res) {
  res.render("index", {
    name: "jack",
    age: 11,
  });
});
```
```html
<link rel="stylesheet" href="css/style.css">
<h1>Express</h1>
  
<p>{{name}}</p> <!-- this name is danamic too, it takes the value from the current route(or javascript files) -->
<p>{{age}}</p> <!-- this is danamic too -->
  
<a href="about">about</a>
```

- middleware
```javascript
// Global Middelware
function logger(req, res, next) {
  const time = new Date();
  console.log(`[${time.toLocaleString()} ${req.method} ${req.url}] `);

  next();
}
  
app.use(logger);


// Local Middleware
function someMiddleware(req, res, next){
	console.log("this is local Middleware");
	next()
}

user.get("/list", someMiddleware(), function (req, res) { // this local Middleware is only functions here
  res.send("/user/list");
});
```

- use Static
```javascript
app.use(express.static("public")); // Load Static
```