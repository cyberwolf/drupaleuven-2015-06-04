##  Example: Block (1/2)

```php
/**
 * Provides a 'Language switcher' block.
 * ...
 */
class LanguageBlock
    extends BlockBase
    implements ContainerFactoryPluginInterface
{
  public function __construct(
      array $configuration,
      $plugin_id,
      $plugin_definition,
      LanguageManagerInterface $language_manager,
      PathMatcherInterface $path_matcher
    ) {
    ...
  }
```
