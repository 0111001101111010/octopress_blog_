---
layout: post
title: "Rails:restart your app"
date: 2013-09-10 01:16
comments: true
categories: 
---



Rails tips: 


If you migrated your database or changed your schema. Before flipping out about errors like and why it doesn't work. Restart your app  
```
ActiveRecord::PendingMigrationError 
```

Also if you generated the wrong named controller try to keep it clean..


Also.. SQLITE3 -_-;--  	


***deploying to heroku*** 

Do not forget to commit your changes to your branch before pushing your branch to heroku..

Do not 

```
git push heroku master

#until you do this on your deployment/master branch

git add . 
git commit -m "my commit"

```	
