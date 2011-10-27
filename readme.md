# Redavel

## A Minimalistic Redis Client For PHP

### Connecting to Redis

    $redis = new Redavel('127.0.0.1', 6379);

### Executing Commands

	$redis->set('name', 'Taylor');

	$list = $redis->lrange('list', 5, 10);

If you don't want to use magic methods, you may use the "run" method:

	$redis->run('set', array('Taylor'));

	$list = $redis->run('lrange', array(5, 10));