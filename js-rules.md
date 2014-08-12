# Rules

## 1. Syntax

### 1.1. Always use semicolons (;)

***Bad:***

    var a = 5
    var myFunction1 = function(){...}
    
***Good:***
    
    var myVar1 = 5;
    var myFunction1 = function(){...};
 
 
## 2. Naming

### 2.1.	Use camel case names
   
   
***Bad:***

    var my-vovely_variable;
    var my-LovelyFunction = function(){...}
    var my-Lovely_obj = {
     dosometing:function(){...},
     "here-is-property":5
    }
    
***Good:***
    
    var myLovelyVariable;
    var myLovelyFunction = function(){}
    var myLovelyObj = {
     doSometing:function(){...}
     hereIsProperty:5
    }

 
<!--#### 2.2	Constructor function name should start with capital letter and named as a singular noun
***Bad:***

    function Apples() {...}
    function Apples() {...}

    
***Good:***

    function Apple() {...}
    -->
    
### 2.2. Use NAMES_LIKE_THIS only for constant values.


***Bad:***

    example.settings.animationFps = 60;

***Also Bad:***
    
    example.settings.ANIMATION_FPS = currentNumberOfFrames/currentDelay;
    
***Good:***

    example.settings.ANIMATION_FPS = 60;
## 3. Code
### 3.1. Avoid using global variables

***Bad:***

    mySettings = {...}
    myOptions = {...}
    myProperties = {...}
    mySomething = {...}

*** Also Bad: ***

    window.mySettings = {...}
    window.myOptions = {...}
    window.myProperties = {...}
    window.mySomething = {...}

    
***Good:***

    window.XBS = {
      mySettings: {...}
      myOptions: {...}
      myProperties: {...}
      mySomething: {...}
    }
    
### 3.2. Declare with `var`
 
*When you fail to specify var, the variable gets placed in the global context, potentially clobbering existing values. Also, if there's no declaration, it's hard to tell in what scope a variable lives (e.g., it could be in the Document or Window just as easily as in the local scope). So always declare with var.*
 
***Bad:***

    myVar1 = 'Hello';
    myFunction1 = function(a){...};
    myFunction2(b){...}
    
***Good:***
    
    var myVar1 = 'Hello';
    var myFunction1 = function(a){...};
    var myFunction2 = function(b){...};---------------------------------------------------------------------------