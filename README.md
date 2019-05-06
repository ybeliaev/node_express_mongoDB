# Создание сайта на Node.js, Express, MongoDB

> подключаю Express https://expressjs.com/ru/starter/installing.html

```JavaScript
const express = require('express');
const app = express();

app.get('/', function (req, res) {
  res.send('Hello World!');
});

app.listen(3000, function () {
  console.log('Example app listening on port 3000!');
});
```
> package.json:

```JavaScript
{
  "name": "node_block",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "node index.js",    
    "dev": "nodemon -L ./index.js " 

  },
  "author": "Yura",
  "license": "ISC",
  "dependencies": {
    "express": "^4.16.4"
  },
  "devDependencies": {
    "nodemon": "^1.19.0"
  }
}
```
