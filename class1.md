# Class Notes
### Github Notes
`git status` - checks if files are tracked/changed

`git clone` - clones a repo

`git add -A` adds changes to repo

`git commit -m "string"` commits changes

`git push origin master` pushes changes to master branch

`git pull origin master` grabs the up to date master branch

`git checkout -b NameOfBranch` creates a new branch

`git checkout NameOfBranch` switch to new branch

`git push origin NameOfBranch` pushes branch to Github

`git clean -df` destroys changes

`git reset --hard origin/master` super destroys changes

`git clone url name(optional)` pulls a repository from github placing a name after the url renames the directory

`git init` turns a directory into a local repository

`git remote add origin url` url is clone url adds a origin repo to local repository

create .gitignore file when making new local repository

`echo >> .gitignore "node_modules"`



### Atom Commands
`control shift m` shows markdown

`"devstart": "./node_modules/nodemon/bin/nodemon.js server.js"` place in package.json under scripts for devstart

### Command Line Commands/node
`mkdir` - makes a new directory

GREP - a command line utility for searching plain text data looking for lines that match a reg. expression

`cat` turns files into a string

`touch` creates files

`pwd` prints working directory

`npm` node package manager

`apm` atom package manager

`echo >> .gitignore "some string"` writes to a file

`history` gives you a list of commands you've recently inputed

`npm install` installs dependencies from package.json

`npm run devstart` runs server locally

`npm install nodemon --save` sets ups nodemon which leads to devstart

`npm install --save-dev` more legit way to install

`mv fileName newFileName` renames a file

`npm install eslint` do this first before next step

`npm install eslint-plugin-import --save-dev` eslint for new project

### Heroku
`heroku create` creates a server on Heroku

`git push heroku master` pushes changes to heroku master

`npm install --save-dev eslint` installs a lot of necessary packages

`apm install linter-eslint` installs eslint for atom


### CSS & html
html - tag oriented language

CSS - uses selectors and key value pairs to change properties

`<img src= "link">` links an image

`<a href="link">link text</a>` makes a link

### Javascript

`document.createElement('button')` creates an html button I believe

Importing Files:
  1. on top of code import another js file
  2. run webpack which compresses your imported files
  3. `import'rootVeg'from'../rootVeg'`




### JSON
javascript object notation

Keys are quoted in json objects!

strings are double quoted!

`{
  "title": "Dark Side of the Moon",
  "artist": "Pink Floyd",
  "genre":, "Classic Rock",
  "songs": [""]
  }`

### jquery
`<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>` post in head to link jquery

`$(document),ready(function(){
  stuff in here
  });\` this needs to be the frame for your js file

### SQL
  Structured Query language

  allows you to connect data

  ### NoSQL

  Mongo db

### Agile
- Not waterfall development

- Mob Programming

- Sticky notes

- focus is not processes and tools

- The Power of Habit

- 4 tenants:
  1. Make people awesome
  2. Safety
  3. Value (continuously)
  4. learning and experimenting

### APIs
API = appplication program interface

API commands:
1. GET  (Read)
2. POST  (Create)
3. PUT  (Update)
4. DELETE (Delete)

### ES6
Ecma Script 6 = newest version of Javascript

function declaration `(name)=>console.log(name)` or `function(){}`

data type decorators = `@somename`


### Creating a test
1. create a directory
2. npm init
3. create matching .js and test.js files
4. npm install chai mocha --save
5. within .test.js file:
  - `const chai = require('chai');`
  - `var nameoftest = require('file location');` use the name of your test and link to file location ie. var addEnd = require('../../arrays/addEnd.js') ;
  - `var expect = chai.expect;`
  - create a describe function ie. `describe('Array Exercise - addEnd()', function () {
  it('should add a number to the end of an array', function () {
    var arr = [1, 2, 3]
    var pushedArray = addEnd(arr, 4)
    expect(pushedArray.length).to.eql(4)
    expect(pushedArray[3]).to.eql(4)
  })
})`
6. in .js file modules.export test function ie `module.exports = addEnd;`
7. npm test and pray

### Creating a Server
1. Pull directory from Github
2. use `git clone url`
3. create a directory called 'Public'
4. within Public `touch index.html index.js style.css`
5. cd out and `npm init`
5. `touch server.js`
6. `npm install express path --save`
7. `atom . `
8. Within index.html call html
9. add title and make `<h1>`
10. in `<body>` create `<script src="index.js" charset="utf-8"></script>`
11. in `<head>` add `  <link rel="stylesheet" href="style.css">`
12. in server.js create:
  - `const express = require("express");`
  - `const path = require("path");`
  - `const app = express();`
  - for heroku: `const port= process.env.PORT || 3000;` then change your port in app.listen to `port`
  - `app.use('/', express.static(path.join(__dirname, 'public')));`
  - `app.listen(3000, ()=>console.log("it works =>3000"));`
14. for heroku: `heroku create`
15. for devstart `npm install nodemon`
16. in scripts add `"devstart": "node node_modules/nodemon/bin/nodemon server.js"`
