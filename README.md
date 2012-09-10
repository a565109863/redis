# phpish/redis

Simple PHP client library for the [Redis protocol](http://redis.io/topics/protocol).


## Requirements

* PHP 5.3+


## Getting Started

### Download via [Composer](http://getcomposer.org/)

Create a `composer.json` file if you don't already have one in your projects root directory and require phpish/redis:

```
{
	"require": {
		"phpish/redis": "dev-master"
	}
}
```

Install Composer:
```
$ curl -s http://getcomposer.org/installer | php
```

Run the install command:
```
$ php composer.phar install
```

This will download phpish/redis into the `vendor/phpish/redis` directory.

To learn more about Composer visit http://getcomposer.org/


### Description

callable __redis\client__( [string _$host = '127.0.0.1'_ [, int _$port = 6379_]] )

The returned function accepts a Redis command as a string.


### Usage

```php
<?php

	require 'vendor/phpish/redis/redis.php';
	use phpish\redis;


	$redis = redis\client();

	var_dump($redis('SET foo "bar baz"')); // bool(true)
	var_dump($redis('GET foo'));           // string(7) "bar baz"

	$redis('QUIT');


?>
```

## TODO
Support for Pipelining and Clustering.