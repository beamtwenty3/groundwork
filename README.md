# Groundwork

A WordPress starter kit, based on the excellent work of [Roots.io]. 

Rather than just use [bedrock], I have pieced this together from [@swalkinshaw]’s thorough [screencast], to increase the size of my brain.

Hopefully this may be useful to web developers who want a well organised, easy to deploy WordPress installation.

**NB: still very much in early stages**

## Instructions

* `composer install`
* Copy `index.php` and `wp-config.php` to root
* Change `index.php` to correct path:
```
require( dirname( __FILE__ ) . '/wp/wp-blog-header.php' );
```
* Change absolute path to WordPress directory in `wp-config.php`
```
define('ABSPATH', dirname(__FILE__) . '/wp');
```
* Add autoload to `wp-config.php`:
```
require 'vendor/autoload.php';
```
* Create `.env` file from `.env.example`, set environment variables
* Add `.env`, `vendor` to `.gitignore` file
* Create `.htaccess` in root
* Copy `wp/wp-content` to `/app`
* Create custom content directories in `wp-config.php` after database details:
```
define( 'WP_CONTENT_DIR', dirname( __FILE__ ) . '/app' );  
define( 'WP_CONTENT_URL', 'http://' . $_SERVER['HTTP_HOST'] . '/app' );
```
* Set WordPress file permissions
* Run the WordPress install
* Change `Site address (URL)` in `Settings > General`
* Enable permalinks in `Settings > Permalinks`


* Setup dotenv
* Use provisioning software to re-create above steps

## Further reading

Read [Twelve Factor WordPress] and the [Using Composer with WordPress].


[Roots.io]: http://roots.io/
[bedrock]: https://github.com/roots/bedrock
[Twelve Factor WordPress]: http://roots.io/twelve-factor-wordpress/
[screencast]: http://roots.io/screencasts/using-composer-with-wordpress/
[@swalkinshaw]: https://twitter.com/swalkinshaw
[Using Composer with WordPress]: http://roots.io/using-composer-with-wordpress/
