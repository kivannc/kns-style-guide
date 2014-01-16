# KNS Javascript Guide

*Based on Airbnb and other best practises.*


## <a name='TOC'>Table of Contents</a>

  1. [General - Introducton](#general-introduction)
  1. [Types - Arrays - Objects - Functions](#types-arrays-objects-functions)

## <a name='general-introduction'>General - Introduction</a>

- **GIT** ; use it for all projects, includes any web or small iOS projects. 
	+ `commits` : use meaningful messages, commit every step of your project. So other member can be easily track you.
	
	```
	git commit -m "Scrolling feature added."
	git commit -m "Event page added."
	
	// Never ever do not do it : 
	git commit -m "*"
	```
	    
	+ `branch` : use branches if necessary, for big changes.

- **.gitignore** ; use this repo's ``.gitignore`` file in any future project 

- **.gitconfig** ; use this repo's ``.gitconfig`` for coloring and syntatic sugars. 
  ``Append this file your ~/.gitconfig file.``

- **Indentation / General Settings**
	+ ``indentation``: 4 spaces always, dont use TABS!
	+ ``line-endings``: Always use unix style line-ending i.e "\n"
	+ ``encoding``: UTF-8
	
    ```
    // If you dont know hot to set these, GOOGLE it !
    // Encoding settings in Webstorm / XCode
    // Indentation settings in Webstorm / XCode
    ```
    

## <a name='types-arrays-objects-functions'>Types - Arrays - Objects - Functions</a>

  - **Variable Naming**: Always start with lowercase and use meaningul names.
  
  ```
  // bad
  var x;
  var Zrrrr;
  
  // good
  var relativeWindowHeight; 
  var storeList; 
  ```
  
  - **Global Declaration**: Avoid always! If you necessary to do that; explain why it must be global.
  
  ```
    // indexPageTiming must be accessible globally, 
    // since it's a ...EXPLANATION...
    var indexPageTiming = 0;
    
    ...
    function() reloadIndexPage {
    
    }
    ...
  ```   
  
  - **Local Declaration**: Declare your variables at top of the function.
  
   
  ```
    ...
    @params: void
    @porpuse: 
    @
    function() reloadIndexPage {
	    var indexPageTiming = 0;
	    var storeList = [];
    }
    ...
  ```  
    
    
  - ** Objects **: 
 
 	```
 	// bad
 	var storeDictionary = new Object();
 	// good
 	var storeDictionary = {};
    ```
    
  - ** Arrays **:
    
    ```
 	// bad
 	var storeList = new Array();
 	// good
 	var storeList = [];
 	
 	// To iterate over array use forEach, never use for..in syntax
 	// bad
	for (store in storeList) {
		
	}
	// good
	storeList.forEach(function(store, index) {
		
	});
    ```
    
  
**[[⬆]](#TOC)**
