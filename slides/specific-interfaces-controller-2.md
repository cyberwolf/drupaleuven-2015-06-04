##  Example: controller (2/2)

```php
  public static function create(
    ContainerInterface $container
  ) {
    return new static(
      $container->get('date.formatter'),
      $container->get('entity.manager')->getStorage('user'),
      $container->get('user.data')
    );
  }
}
```
