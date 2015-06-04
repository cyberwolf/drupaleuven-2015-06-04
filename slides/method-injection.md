##  Setter injection

```sql
theme.manager:
  class: Drupal\Core\Theme\ThemeManager
  arguments: ...
  calls:
    - [setThemeRegistry, ['@theme.registry']]

theme.registry:
  class: Drupal\Core\Theme\Registry
  arguments: ...
  calls:
    - [setThemeManager, ['@theme.manager']]
```

Equivalent to:

```php
  $themeManager = new \Drupal\Core\Theme\ThemeManager(...);
  
  $themeRegistry = new \Drupal\Core\Theme\Registry(...);
  $themeRegistry->setThemeManager($themeManager);
  
  $themeManager->setThemeRegistry($themeRegistry);
```

Code smell!
