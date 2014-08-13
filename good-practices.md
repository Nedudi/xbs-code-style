

   
   
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