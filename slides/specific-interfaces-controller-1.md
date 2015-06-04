##  Example: controller (1/2)

```php
class UserController extends ControllerBase {

  public function __construct(
    DateFormatter $date_formatter,
    UserStorageInterface $user_storage,
    UserDataInterface $user_data
  ) {
    $this->dateFormatter = $date_formatter;
    $this->userStorage = $user_storage;
    $this->userData = $user_data;
  }

```
