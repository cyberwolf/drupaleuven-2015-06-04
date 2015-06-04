##  Construction by a factory (2/2)

OR by a _factory service_

```sql
services:
  cache_factory:
    ...
 
  cache.menu:
    class: Drupal\Core\Cache\CacheBackendInterface
    factory_method: get
    factory_service: cache_factory
    arguments: [menu]
```

Equivalent to:

```php
$cacheFactory = ...;
$menuCache = $cacheFactory::get('menu');
```
