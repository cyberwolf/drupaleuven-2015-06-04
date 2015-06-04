##  Why is there so much service configuration code needed?

Faster to write it like in the old days?

```php
$database = \Drupal\Core\Database\Database::getConnection('default');
```

```sql
services:
  database:
    class: Drupal\Core\Database\Connection
    factory_class: Drupal\Core\Database\Database
    factory_method: getConnection
    arguments: [default]
```

Remember:

- S & D of SOLID
- ++Testability
