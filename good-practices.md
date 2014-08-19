

# Good practices

### 1.1. We use $something for variables that represent jQuery wrapped dom node(s)
   
   
***Bad:***

```js
    var myNode = $('#abc');
```

***Good:***

```js    
    var $myNode = $('#abc');
```

### 1.2. We use `that` to transfer `this` from outside context into the closure

***Bad:***

```js
    var _this = this; 
    var self = this; 
    var $that = this;  
```   

***Good:***

```js    
    var that = this; 
```

### 1.3. We don't use style classes for binding js events. Good practice to use id, or additional class starting with `js-` 

**example:** 

```html
    class="btn btn-success btn-red js-class-to-attach-events"
```

***Bad:***

```html
	<a class="red-button">hello</a>
```

```js
	$('.red-button').on('click', function(){
	  // do something
	})
```

***Good:***

```html
	<a class="js-submit-button red-button">hello</a>
```

```js	
	$('.js-submit-button').on('click', function(){
	  // do something
	})
```
