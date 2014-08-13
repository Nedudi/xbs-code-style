# Rules

## 1. Syntax

### 1.1. Always use semicolons (;)

***Bad:***

```js
    var a = 5
    var myFunction1 = function(){...}
```  

***Good:***
```js    
    var myVar1 = 5;
    var myFunction1 = function(){...};
``` 
 
## 2. Naming

### 2.1.	Use camel case names
   
   
***Bad:***

```js
    var my-vovely_variable;
    var my-LovelyFunction = function(){...}
    var my-Lovely_obj = {
     dosometing:function(){...},
     "here-is-property":5
    }
```  

***Good:***

```js    
    var myLovelyVariable;
    var myLovelyFunction = function(){}
    var myLovelyObj = {
     doSometing:function(){...}
     hereIsProperty:5
    }
```  

 
<!--#### 2.2	Constructor function name should start with capital letter and named as a singular noun

***Bad:***

```js
    function Apples() {...}
    function Apples() {...}

    
***Good:***

```js
    function Apple() {...}
    -->
    
### 2.2. Use NAMES_LIKE_THIS only for constant values.


***Bad:***

```js
    example.settings.animationFps = 60;
```  

***Also Bad:***

```js    
    example.settings.ANIMATION_FPS = currentNumberOfFrames/currentDelay;
```  
    
***Good:***

```js
    example.settings.ANIMATION_FPS = 60;
```  



## 3. Code


### 3.1. Avoid using global variables

***Bad:***

```js
    mySettings = {...}
    myOptions = {...}
    myProperties = {...}
    mySomething = {...}
```  

*** Also Bad: ***

```js
    window.mySettings = {...}
    window.myOptions = {...}
    window.myProperties = {...}
    window.mySomething = {...}
```  

    
***Good:***

```js
    window.XBS = {
      mySettings: {...}
      myOptions: {...}
      myProperties: {...}
      mySomething: {...}
    }
```  

    
### 3.2. Declare with `var`
 
*When you fail to specify var, the variable gets placed in the global context, potentially clobbering existing values. Also, if there's no declaration, it's hard to tell in what scope a variable lives (e.g., it could be in the Document or Window just as easily as in the local scope). So always declare with var.*
 
***Bad:***

```js
    myVar1 = 'Hello';
    myFunction1 = function(a){...};
    myFunction2(b){...}
```  

    
***Good:***

```js    
    var myVar1 = 'Hello';
    var myFunction1 = function(a){...};
    var myFunction2 = function(b){...};
```  


---------------------------------------------------------------------------
