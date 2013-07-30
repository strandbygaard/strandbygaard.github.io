---
author: strandbygaard
comments: true
date: 2011-06-09 11:51:31+00:00
layout: post
slug: insert-document-in-mongodb-from-node
title: Insert document into MongoDB from Node.js
wordpress_id: 139
categories:
- Development
tags:
- Javascript
- MongoDB
- Node.js
---

This is a very simple example of how to insert a document in MongoDB from Node.js

I recently needed to use MongoDB with Node.js on a project, and finding a barebones example of how to make them work together was more difficult than anticipated.

It's nothing more than what's in the excellent [Getting Started with MongoDB and Node.js](http://www.slideshare.net/ggoodale/getting-started-with-mongodb-and-nodejs) presentation, but it's kind of hard to copy-paste from an image :-)

``` javascript
var mongo = require('mongodb');

db = new mongo.Db('mydb', new mongo.Server("127.0.0.1", 27017, {}), {});

db.open(function(err, db) {
	db.collection('sample', function(err, collection) {
		doc = {
			"prop1" : "val",
			"prop2" : {
				a : 1,
				b : 2
			}
		};
		collection.insert(doc, function() {
			db.close();
		});
	});
});
```

For this example to work, you need to have MongoDB installed, started and listening on the default port. You also need to add the mongodb module to your node installation (`npm install mongodb` worked for me).

Another good simple example of using MongoDB with Node.js can be found [here](http://christiankvalheim.com/post/596160094/a-simple-insert-and-query-using-node-js-mongodb-driver). I don't find the notation quite as clear, but that's just my personal preference. It works just fine. 
