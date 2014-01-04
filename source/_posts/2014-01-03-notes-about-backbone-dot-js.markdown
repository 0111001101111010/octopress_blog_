---
layout: post
title: "Notes About Backbone.JS"
date: 2014-01-03 19:34
comments: true
categories: 
---

Reading addyosmani guide on backbone js from the following source. Its on the Web For free. 

http://addyosmani.github.io/backbone-fundamentals/#memory-management

Notable Exerpts or section's I'd want to revist later on. 

Chapter CribNotes

1. MVC Patterns 	
================ 
* (The GoF (Gang of Four) do not refer to MVC as a design pattern, but rather consider it a set of classes to build a user interface. In their view, it’s actually a variation of three other classical design patterns: the Observer (Publish/Subscribe), Strategy, and Composite patterns. Depending on how MVC has been implemented in a framework, it may also use the Factory and Decorator patterns. I’ve covered some of these patterns in my other free book, JavaScript Design Patterns For Beginners if you would like to read about them further.

2. Models
================ 
* Initializations with default values using initialize: function
* Getters and Setters using this synthax Model.get('ATTRIBUTE_NAME') & All Model.set({ATTRIBUTE:"PROPERTY"}) or single Model.set("Attribute","property") 
* Direct Access ... to attributes .. event view based model change.
* Validate Models - uses model.validate() to produce -> {validate:true} 
* What is El? - el is basically a reference to a DOM element and all views must have one. Views can use el to compose their element’s content and then insert it into the DOM all at once, which makes for faster rendering because the browser performs the minimum required number of reflows and repaints.
```javascript

var TodosView = Backbone.View.extend({
  tagName: 'ul', // required, but defaults to 'div' if not set
  className: 'container', // optional, you can assign multiple classes to 
                          // this property like so: 'container homepage'
  id: 'todos', // optional
});

var todosView = new TodosView();
console.log(todosView.el); // logs <ul id="todos" class="container"></ul>
//The above code creates the DOM element below but doesn’t append it to the DOM.

//to this

<ul id="todos" class="container"></ul>
```
* some stuff about _. templates...
* Collections are groups of models
*underscore fully supported methods -> forEach, map, sortBy, reduce
* use attributes of collections->url to communicate to datastore and use 
   *COLLECTION.fetch()
   *COLLECTION.save()
   *COLLECTION.create()
   *COLLECTION.remove()

3. Persistant data
=================  
``` javascript

var Todo = Backbone.Model.extend({
  defaults: {
    title: '',
    completed: false
  }
});

var TodosCollection = Backbone.Collection.extend({
  model: Todo,
  url: 'localhost:27017s'
});

var todos = new TodosCollection();
todos.fetch();

var todo2 = todos.get(2);
todo2.set('title', 'go fishing');
todo2.save(); // sends HTTP PUT to /todos/2

todos.create({title: 'Try out code samples'}); // sends HTTP POST to /todos and adds to collection

''''
4. Event based
*Backbone.Events is mixed into the other *Backbone classes, including:	
	*Backbone
	*Backbone.Model
	*Backbone.Collection
	*Backbone.Router
	*Backbone.History
	*Backbone.View
*Example apps

5. Good App examples
* ToDoAPP http://todomvc.com
* ToDoModularApp 
* http://jsbin.com/afetez/2/edit
6. Plugins 
* Backbone Marionette 
* Super
* Understanding the similarities and differences between an event aggregator and mediator is important for semantic reasons. It’s equally as important to understand when to use which pattern, though. 
* Event Aggregator Use
In general, an event aggregator is used when you either have too many objects to listen to directly, or you have objects that are entirely unrelated.
* Mediator Use
A mediator is best applied when two or more objects have an indirect working relationship, and business logic or workflow needs to dictate the interactions and coordination of these objects.
* What tools like RequireJS do is load scripts asynchronously. This means we have to adjust our code slightly, you can’t just swap out <script> elements for a small piece of RequireJS code, but the benefits are very worthwhile:

* Loading the scripts asynchronously means the load process is non-blocking. The browser can continue to render the rest of the page as the scripts are being loaded, speeding up the initial load time.
* We can load modules in more intelligently, having more control over when they are loaded and ensuring that modules which have dependencies are loaded in the right order.


