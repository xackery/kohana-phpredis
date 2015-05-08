# PHPRedis for Kohana

[Kohana](http://kohanaframework.org/) is an elegant, open source, and object oriented HMVC framework built using PHP5, by a team of volunteers. It aims to be swift, secure, and small.

[PHPRedis](https://github.com/phpredis/phpredis) is an extension providing an API for communicating with the Redis key-value store. It is compiled in C.

## Documentation
Kohana's documentation can be found at <http://kohanaframework.org/documentation> which also contains an API browser.

Installing PHPRedis can be found at <https://github.com/phpredis/phpredis>.

-----

# Installing/Configuring
-----
First, ensure you install PHPRedis and have a working Kohana environment.

Inside /application/bootstrap.php:
Add this line in the modules listing (There will be similar entries near it):

'redis'		=> MODPATH . 'redis',

Add this line around where the Cookie::salt area is:
~~~
Session::$default = 'redis';
~~~

Much like Kohana's database configuration, create a file inside /application/config/ called redis.php
Change this file to reflect the settings your redis is using (by default, it connects locally).
