WAMPush
-------

The [WAMP](http://wamp.ws) acronym stands for Web Application Messaging Protocol. 
It **IS** a subprotocol for web app JSON RPC.
It **IS NOT** a Windows, Apache, Mysql, PHP stack.

WAMPush is a library to connect your Angular app to a websocket [WAMP](http://wamp.ws) server. It uses the Autobahn JS (WAMP impl) library from Tavendo to facilitate JSON PubSub/RPC over Websockets as an Angular service.

About
-----

I created this library out of need. I couldn't find any existence of a library like this, only [hints](http://stackoverflow.com/questions/23223619/angularjs-and-autobahn-js-wamp-implementation) on how to do it through Stack Overflow. 

Include/Install
---------------

This library can be included or installed in multiple ways:

* wampush on Bower (preferred method)
* Clone this repo locally
* Copy/paste it like some sort of animal

Example
-------

Roadmap
-------

This first started before the WAMP2 implementation was even specified, so it will first deal with WAMP1. Eventually, I would like to use WAMP2 but support backward compatibility with WAMP1 (it's simpler/easier to get started with).

* Tests/test suite
* -WAMP1 Connectivity-
* Put it on Bower
* PubSub/RPC Wrapper
* Allow users of lib to hook in their custom JS API for PubSub and RPC
* WAMP2 Connectivity
* Replicate features in WAMP1 for WAMP2

Contributing
------------

Feel free to contact me over Github. Pull requests and documentation contributions are more than welcome! If you have an issue, please use the Github issue system. 

There is currently no mailing list or IRC channel (no need at the moment).

