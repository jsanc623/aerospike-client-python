
# aerospike.Client.lset.size

## Description

```
size = lset.size(policies)
```
**lset.size()** will get the current item count of the lset.    

## Parameters

**policies**, the dictionary of policies to be given while size.   

## Return Values
Returns the current item count of the lset. In case of error, appropriate exceptions will be raised.

## Examples

```python

# -*- coding: utf-8 -*-
import aerospike
config = {
            'hosts': [('127.0.0.1', 3000)]
         }
client = aerospike.client(config).connect()

key = ('test', 'demo', 1)

lset = client.lset( key, ldt_bin, module )

policy = {
    'timeout' : 2000
}

size = lset.size(policy)

print size


```

We expect to see:

```python
3
```



### See Also



- [Glossary](http://www.aerospike.com/docs/guide/glossary.html)

- [Aerospike Data Model](http://www.aerospike.com/docs/architecture/data-model.html)
