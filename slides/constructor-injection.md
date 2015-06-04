##  Constructor injection

```sql
services:
  database:
   ...

  config.storage.active:
    class: Drupal\Core\Config\DatabaseStorage
    arguments: ['@database', config]
    
  config.storage.snapshot:
    class: Drupal\Core\Config\DatabaseStorage
    arguments: ['@database', config_snapshot]
```

Equivalent to:

```php
$database = ...

$activeConfigStorage = new \Drupal\Core\Config\DatabaseStorage(
  $database,
  'config'
);

$snapshotConfigStorage = new \Drupal\Core\Config\DatabaseStorage(
  $database,
  'config_snapshot'
);

```
