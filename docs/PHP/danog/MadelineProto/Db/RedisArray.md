---
title: "danog\\MadelineProto\\Db\\RedisArray: Redis database backend."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\Db\RedisArray`
[Back to index](../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Redis database backend.  




## Method list:
* `initStartup()`
* `initConnection(\danog\MadelineProto\Settings\Database\Redis $settings)`
* `set(string $index)`
* `getArrayCopy(): \Amp\Promise<array>`
* `count(): \Promise<int> The number of elements or public properties in the associated
array or object, respectively.`
* `clear()`
* `getTable()`
* `setTable()`
* `isset(mixed $key): \Promise<bool> true if the offset exists, otherwise false`
* `getInstance(\danog\MadelineProto\Db\DbArray|array|null $previous, \danog\MadelineProto\Settings\Database\DatabaseAbstract $settings)`

## Methods:
### `initStartup()`

Initialize on startup.



### `initConnection(\danog\MadelineProto\Settings\Database\Redis $settings)`

Initialize connection.


Parameters:

* `$settings`: `\danog\MadelineProto\Settings\Database\Redis`   


#### See also: 
* [`\danog\MadelineProto\Settings\Database\Redis`: Redis backend settings.](../../../danog/MadelineProto/Settings/Database/Redis.html)




### `set(string $index)`

Set value for an offset.


Parameters:

* `$index`: `string` <p>
The index to set for.
</p>  



### `getArrayCopy(): \Amp\Promise<array>`

Get array copy.


#### See also: 
* `\Amp\Promise`




### `count(): \Promise<int> The number of elements or public properties in the associated
array or object, respectively.`

Count elements.


Return value: The number of elements or public properties in the associated
array or object, respectively.


### `clear()`

Clear all elements.



### `getTable()`

Get the value of table.



### `setTable()`

Set the value of table.



### `isset(mixed $key): \Promise<bool> true if the offset exists, otherwise false`

Check if key isset.


Parameters:

* `$key`: `mixed`   


Return value: true if the offset exists, otherwise false


### `getInstance(\danog\MadelineProto\Db\DbArray|array|null $previous, \danog\MadelineProto\Settings\Database\DatabaseAbstract $settings)`




Parameters:

* `$previous`: `\danog\MadelineProto\Db\DbArray|array|null`   
* `$settings`: `\danog\MadelineProto\Settings\Database\DatabaseAbstract`   


Fully typed return value:
```
\Amp\Promise<static>
```
#### See also: 
* [`\danog\MadelineProto\Db\DbArray`: DB array interface.](../../../danog/MadelineProto/Db/DbArray.html)
* [`\danog\MadelineProto\Settings\Database\DatabaseAbstract`: Base class for database backends.](../../../danog/MadelineProto/Settings/Database/DatabaseAbstract.html)
* `\Amp\Promise`




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
