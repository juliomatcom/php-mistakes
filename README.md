![PHP MISTAKES](http://i.memecaptain.com/gend_images/H1oGGQ.gif)
###Biggest PHP developers mistakes


####- http://php.com/ 
  *no explanation*
####- Turn OFF all error reporting
```php
error_reporting(0);
```
*thats why errors or warnings appears randomly later!*
####- Use @ intentionally to silence errors or exceptions
```php
$result = @$my_lib->process($data);
```
 *a secure library will validate the external data and return false or an Exception if something fail so we can handle that* properly 
```php
try {
$result = $my_lib->process($data);
} catch (Exception $e) {
   //handler the error
}
``` 
*Read more about  [Error Control Operators](http://php.net/manual/en/language.operators.errorcontrol.php)*
	 
 
####- Not use [isset()](http://php.net/manual/en/function.isset.php) or [array_key_exists](http://php.net/manual/en/function.array-key-exists.php)
```php
if ($_POST['email']) {
    $email = $_POST['email'];
}
```
*sure this will throw an Exception if email key is not found*
####- [Wrong Comparison Operators](http://php.net/manual/en/language.operators.comparison.php "http://php.net/manual/en/language.operators.comparison.php")
```php
if ($a = value) { /* really what you want?*/ }
//Equal
if (1 == true) { /*true*/ }
//Identical
if( 1 === true) { /*false*/ }
```
-- Is all in the link
####-  Security: [SQL injection](http://en.wikipedia.org/wiki/SQL_injection "http://en.wikipedia.org/wiki/SQL_injection") or [XSS attacks](http://en.wikipedia.org/wiki/Cross-site_scripting "http://en.wikipedia.org/wiki/Cross-site_scripting") and others
*you must use statments and properly encode all external data*

####- Not read php-fig [(Basic Coding Standard & Coding Style Guide )](http://www.php-fig.org/)
*nowadays we work for others people too, we share code and contribute with others developers, so this is a must guide*
####- Learn [PHP Frameworks](https://github.com/ziadoz/awesome-php#frameworks) like [Symfony](http://symfony.com/) before learn PHP 	
*If you don't dominate OOP, ORM, interfaces, abstract classes,  annotations and other basics in PHP  you can not expect to  really understand what are you winning with this Framework*
###Contribute
#####Miss some others common mistake ? Make Edit and make a [Pull Request](https://github.com/juliomatcom/php-mistakes/compare "Pull request")

