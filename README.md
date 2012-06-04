minify-redis
------------
Redis cache engine for Minify

Requirements
------------
* PHP 5
* [Minify](https://github.com/mrclay/minify)
* [PHPRedis](https://github.com/nicolasff/phpredis)

Installation
------------
Place Redis.php to min/lib/Minify/Cache/Redis.php

Usage
-----
Edit min/config.php
<pre>
require 'lib/Minify/Cache/Redis.php';
$redis = new Redis;
$redis->connect('localhost', 6379);
$redis->auth('mypassword'); // If you need password to connect
$redis->select(1); // If you want to select DB
$min_cachePath = new Minify_Cache_Redis($redis);
</pre>

License
-------
( Same as Minify )

Copyright (c) 2012 Indra BW
