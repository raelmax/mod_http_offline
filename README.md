mod_http_offline_
================

Ejabberd module to send a post if users was offline.


This module is based on Adam Duke mod__interact, Jason Rowe's post and a lot
of pieces of code and tips from the web to adapts to work with Ejabber 14.12.

Installing
----------

Clone this repository:

``` git clone git@github.com:raelmax/mod_http_offline.git```

Change the ```'[your-url-here]'``` string in ```mod_http_offline.erl``` file.

To compile this I downloaded the code at my home directory and run:

``` 
	erlc -I /lib/ejabberd/include/ -pa ~/ejabberd/deps/lager/ebin/ mod_http_offline.erl
```

Move the .beam file to ejabberd ebin folder:

``` 
	sudo mod_http_offline.beam /lib/ejabberd/ebin/ 
```

Add "mod_http_offline" to your ejabberd.yml config at "modules" section:

```
    mod_http_offline: {}
```

Restart ejabberd! \o/

This is tested with ejabberd 14.12 and ubuntu server 14.04.
