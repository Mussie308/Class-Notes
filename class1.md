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



### Atom Commands
`control shift m` shows markdown

`"devstart": "./node_modules/nodemon/bin/nodemon.js server.js"` place in package.json under scripts for devstart

### Command Line Commands
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
### Heroku
`heroku create` creates a server on Heroku

`git push heroku master` pushes changes to heroku master

### CSS & html
html - tag oriented language

CSS - uses selectors and key value pairs to change properties

`<img src= "link">` links an image

`<a href="link">link text</a>` makes a link

### Javascript


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
