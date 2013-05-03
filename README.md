# Akismet for the Laravel framework #

This is a bundle of the Akismet PHP library found [here](https://github.com/achingbrain/php5-akismet).

## Installation

Install akismet via Artisan:

```
php artisan bundle:install akismet
```

Add the following to your **application/bundles.php** file:

```
'akismet' => array('auto' => true),
```

## Usage

You can use the Aksimet class just as you normally would.

```php
$akismet = new Akismet("http://www.example.com" ,'aoeu1aoue');
$akismet->setCommentAuthor( Input::get('name') );
$akismet->setCommentAuthorEmail( Input::get('email') );
$akismet->setCommentContent( Input::get('message') );
if($akismet->isCommentSpam())
	echo "You sent spam!";
else
	echo "Thank you!";
```

## More Information

If you need to learn more about the PHP Akismet library used [try the GitHub page](https://github.com/achingbrain/php5-akismet). If you want to learn more about Akismet, or get a key, go to [Akismet's site](https://akismet.com/).
