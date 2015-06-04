##  Construction by a factory (1/2)

Creation by a _static factory method_

```sql
services:
  database:
    class: Drupal\Core\Database\Connection
    factory_class: Drupal\Core\Database\Database
    factory_method: getConnection
    arguments: [default]
```

Equivalent to:
```php
$database = \Drupal\Core\Database\Database::getConnection('default');
```
