# php-mistakes
Biggest PHP code mistakes

1. ####http://php.com/  
 -- no words
2. ####Turn off all error reporting
```php
error_reporting(0);
```
-- thats why errors appears randomly later!
3. ####Use @ intentionally to silence errors
```php
$file = @fopen('...');
```
--  check if file exist first no ?  
4. ####Not use isset()
```php
if ($_POST['email']) {
    $email = $_POST['email'];
}
```
--sure this will throw an Exception if email key is not found
5. ####[Comparison Operators](http://php.net/manual/en/language.operators.comparison.php "http://php.net/manual/en/language.operators.comparison.php")
```php
if ($a = value) { ? }
if (1 == true) { 1;}
if( 1 === true) { 0 }
```
-- Is all in the book
6. #### Security: [SQL injection](http://en.wikipedia.org/wiki/SQL_injection "http://en.wikipedia.org/wiki/SQL_injection") or [XSS attacks](http://en.wikipedia.org/wiki/Cross-site_scripting "http://en.wikipedia.org/wiki/Cross-site_scripting") and others
-- You must use statments and properly validate all external data


###Contribute
#####Miss some others common mistake ? Make Edit and make a [Pull Request](https://github.com/juliomatcom/php-mistakes/compare "Pull request")

.
