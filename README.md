# angularjs-udemy-1
Anthony Alicea - Learn and Understand AngularJS  
https://www.udemy.com/learn-angularjs/learn/#/

# Git: How to create Repositary from Existing Folder
- cd <localdir>
- git init
- git add .
- git commit -m 'message'
- git remote add origin <url>
- git push -u origin master


# Initializing
- npm init
- npm install express -save
- npm install bower --save

- bower install angular --save
- bower install bootstrap --save
- add .gitignore
    - add node_components
    - add bower_components
- create [server.js](http://expressjs.com/starter/hello-world.html)
- update server.js 
	```javascript
	var express = require('express');
	var serveIndex = require('serve-index')
	var app = express();

	//this will allow serving files in /bower_components at /bower_components
	app.use('/bower_components', express.static(__dirname + '/bower_components'));

	app.use(express.static('views')); //this will allow serving files in /views at /
	app.use('/views', express.static('views')); //this will allow serving files in /views at /views

	// Directory Listing 
	app.use('/views', serveIndex('views', {'icons': true}))


	// respond with "Hello World!" on the homepage
	app.get('/', function (req, res) {
	  res.send('Hello World!');
	});


	var server = app.listen(3000, function () {
	  var host = server.address().address;
	  var port = server.address().port;

	  console.log('Example app listening at http://%s:%s', host, port);
	});
	```

