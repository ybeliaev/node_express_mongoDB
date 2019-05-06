# Создание сайта на Node.js, Express, MongoDB

## 1. Настраиваем окружение
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

```Node.js
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
> Ввести в консоли  ```npm run dev``` и перейти по http://localhost:3000/

## 2. Работа с POST/GET запросами в Express

> подкл. шаблонизатор https://ejs.co/
```npm install ejs```
> Далее добавляю ```app.set('view engine', 'ejs');``` в index.js  - подкл. шаблонизатор и создаю папку ```views``` т.к в ней по-умолчанию шаблонизатор ищет файлы. В ней файл index.ejs.
> ```.res.send('Hello World!')``` меняем на ```res.render(index)```

