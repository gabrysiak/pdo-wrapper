# This is a PDO Wrapper Class

Example Usage:

CONNECT:
```php
$db = new DB("mysql:host=localhost;dbname=db", "dbuser", "dbpass");
```
ERROR HANDLING:
```php
$db->setErrorCallbackFunction("myErrorHandler");
```
SELECT:
```php
$result = $db->select('tablename', 'foo = "bar"');
foreach($result as $row) {
    echo $row['foo'];
}
```
PREPARED SELECT:
```php
$foo = "bar";
$bind = array(
  ":name"	=>	"$foo"
);
$results = $db->select("mytable", "name = :name", $bind, 'first_name, last_name');
```

