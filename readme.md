# Redavel

## A Minimalistic Redis Client For PHP

### Connecting to Redis

    $redis = new Redavel('127.0.0.1', 6379);

### Executing Commands

Redavel uses magic methods to interact with Redis. Just call the Redis command you
want to execute, and pass the arguments into the method.

	$redis->set('name', 'Taylor');

	$list = $redis->lrange('list', 5, 10);

If you don't want to use magic methods, you may use the "run" method. Just pass the
Redis command as the first parameter, and an array of arguments as the second.

	$redis->run('set', array('Taylor'));

	$list = $redis->run('lrange', array(5, 10));