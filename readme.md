WAMPush
-------

The [WAMP](http://wamp.ws) acronym stands for Web Application Messaging Protocol. 
It **IS** a subprotocol for web app JSON RPC.
It **IS NOT** a Windows, Apache, Mysql, PHP stack.

WAMPush is a library to connect your Angular app to a websocket [WAMP](http://wamp.ws) server. It uses the Autobahn JS (WAMP impl) library from Tavendo to facilitate JSON PubSub/RPC over Websockets as an Angular service.

About
-----

I created this library out of need since I couldn't find anything like this for Angular already out there, only [hints](http://stackoverflow.com/questions/23223619/angularjs-and-autobahn-js-wamp-implementation) on how to do it through Stack Overflow. It's useful for connecting your app to a back-end WAMP server. WAMP has proven to be incredibly useful for remote procedure invocation and the pub-sub paradigms. I used it in many apps before I started learning Angular.

Dependencies
------------

Currently WAMPush only supports WAMPv1; AutobahnJS-wamp1 is already included in the project's ``include`` directory. Keep in mind that it's a legacy version while compatibility with the newest version is built in.

* [AngularJS latest](http://angularjs.org)
* [AutobahnJS latest (for eventual compatibility)](http://autobahn.ws/js/)


Include/Install
---------------

This library can be included or installed in multiple ways:

* ``bower install wampush``
* Clone this repo locally
* Copy/paste it like some sort of animal

Example
-------

Example of a useless app.js to get started. Examples forthcoming.

```javascript

var app = angular.module('app', [
	'wampush'
])
.config([, function() {
	// Routes and stuff
}]);

app.run(['$push', function($push) {
	// Assuming the #getTime route has been setup on the WAMP back-end
	// Call a remote procedure referenced by #getTime
	$push.rpc(
		'#getTime', 
		null, 
		function(data) {
			console.log('callback!');
			console.log(cb);
		}, 
		function(err) {
			console.log('error!');
			console.log(err);
		}
	);
}]);
```


Roadmap
-------

This first started before the WAMP2 implementation was even specified, so it will first deal with WAMP1. Eventually, I would like to use WAMP2 but support backward compatibility with WAMP1 (it's simpler/easier to get started with).

* Tests/test suite
* WAMP1 Connectivity
* Put it on Bower
* PubSub/RPC Wrapper
* Ability to hook in your own custom JS API for PubSub and RPC
* WAMP2 Connectivity
* Replicate features in WAMP1 for WAMP2

Contributing
------------

Feel free to contact me over Github. Pull requests and documentation contributions are more than welcome! If you have an issue, please use the Github issue system. 

There is currently no mailing list or IRC channel (no need at the moment).

