##  How we used to build stuff (1/2)

```php
function twitter_fetch_user_timeline($id) {
  $account = twitter_account_load($id);
  $since = db_query("...", array(':screen_name' => $account->screen_name))
    ->fetchField();

  $twitter = twitter_connect($account);
  $params = $since ? array('since_id' => $since) : array();

  $statuses = $twitter->user_timeline($id, $params);
  foreach ($statuses as $status) {
    twitter_status_save($status);
  }

  if (count($statuses) > 0) {
    twitter_account_save($statuses[0]->user);
  }
}
```
