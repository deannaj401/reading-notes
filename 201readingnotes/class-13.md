# The Past Present & Future of Local Storage for Web Applications

Web applications do not have the same storage capabilities as native applications. For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be stored in the registry, INI files, XML files, or some other place according to platform convention. If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions.

Web applications can use cookies but they are slower, smaller and not as secure.

All of the other solutions were specific to a single browser or reliant on a third party plugin

## HTML5 storage

**HTML5 Storage** - a way for web pages to store named key/value pairs locally, within the client web browser	

* Like cookies this data persists even after you navigate away from the web site or close your browser
	*Unlike cookies this data is never transmitted to the remote web server unless it is sent manually

	* It is implemented natively in web browsers and is available even when third party browser plugins are not
	
HTML5 Storage is accessed through the ```localStorage``` object on the global window object


## Using HTML5 Storage

* HTML5 Storage is based on named key/value pairs
	* dated is stored based on a named key, and then data is retrieved with the same key. 
	* The named key is a string
	* The data is supported by any type of JavaScript including strings, Booleans, integers or floats.
	* If you are storing and retrieving anything other than strings, you will need to use functions like ```parseInt()``` or ```parseFloat()``` to coerce your retrieved data into the expected JavaScript datatype.

```setItem()``` - overwrites a named key with the previous value

```getItem()``` - returns null when calling a non existent key instead of throwing an exception

*you can replace the above methods with square brackets*

The following code removes the value for a given named key and clears the entire storage area by deleting all the keys and values at once.

```interface Storage```  {
  
  ```deleter void removeItem(in DOMString``` ``` key);
  void clear();```

};

The following code gets the total number of values in the storage area and interates through all of the keys by index.

```interface Storage``` {
  ```readonly attribute unsigned long``` ```length;```

  ```getter DOMString key(in unsigned long``` ```index);```
};

If you call ```key()``` with an index that is not between ```0-(lenth-1)``` the function will return ```null```

## Tracking changes to the HTML5 storage area

If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever ```setItem()```, ```removeItem()```, or ```clear()``` is called and actually changes something. For example, if you set an item to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.

























https://deannaj401.github.io/reading-notes/)