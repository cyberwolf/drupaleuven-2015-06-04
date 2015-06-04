##  How we used to build stuff (2/2)

```php
function twitter_connect($account) {
  $auth = $account->get_auth();
    
  return new Twitter(
    variable_get('twitter_consumer_key'),
    variable_get('twitter_consumer_secret'),
    $auth['oauth_token'],
    $auth['oauth_token_secret']
  );
}
```
