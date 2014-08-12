# Good practices
### 1.1. We use **$**something for variables that represent jQuery wrapped dom node(s)
   
   
***Bad:***

    var myNode = $('#abc');

***Good:***
    
    var $myNode = $('#abc');
    
### 1.2. We use `that` to transfer `this` from outside context into the closure

***Bad:***

    var _this = this; 
    var self = this; 
    var $that = this;  
    
***Good:***
    
    var that = this; 
### 1.3. We don't use style classes for binding js events. Good practice to use id, or additional class starting with `js-` 
**example:** 
    class="btn btn-success btn-red js-class-to-attach-events"

***Bad:***

	<a class="red-button">hello</a>
	
	$('.red-button').on('click', function(){
	  // do something
	})

***Good:***

	<a class="js-submit-button red-button">hello</a>
	
	$('.js-submit-button').on('click', function(){
	  // do something
	})
