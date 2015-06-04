##  How to access a service?

```php
$container = \Drupal::getContainer();
$languageManager = $container->get('language_manager');
```

However, avoid using \Drupal::getContainer(), use dependency injection instead!
