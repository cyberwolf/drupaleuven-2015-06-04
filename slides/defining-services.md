##  Defining services in Drupal 8

Definition in YAML inside your module named _example_:
 
  _example.services.yml_

Simplest form:
```sql
services:
  asset.css.optimizer:
      class: Drupal\Core\Asset\CssOptimizer
```

Equivalent to:
```php
new \Drupal\Core\Asset\CssOptimizer();
```
