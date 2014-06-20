# Groundwork

A WordPress starter kit, based on the excellent work of [Roots.io]. 

Rather than just use [bedrock], I have pieced this together from [@swalkinshaw]’s thorough [screencast], to increase the size of my brain.

Hopefully this may be useful to web developers who want a well organised, easy to deploy WordPress installation.

**NB: still very much in early stages**

## Instructions

* `composer install`
* Copy `index.php` to root
* Change `index.php` to correct path:
```
require( dirname( __FILE__ ) . '/wp/wp-blog-header.php' );
```
* Copy `wp-config-sample.php` to `/wp-config.php`
* Change absolute path to WordPress directory:
```
define('ABSPATH', dirname(__FILE__) . '/wp');
```
* Add autoload to `wp-config.php` at end of file:
```
require 'vendor/autoload.php';
```
* Create `.env` file from `.env.example`
* Set environment variables
* Create custom content directory in `wp-config.php` after database details, to use `/app` directory:
```
define('CONTENT_DIR', '/app');
define( 'WP_CONTENT_DIR', dirname( __FILE__ ) . CONTENT_DIR);
define( 'WP_CONTENT_URL', 'http://' . $_SERVER['HTTP_HOST'] . CONTENT_DIR);
```
* Set [WordPress file permissions]
* Run the WordPress install in a browser
* Change `Site address (URL)` in `Settings > General`
* Enable permalinks in `Settings > Permalinks`

---

* Setup dotenv
* Use provisioning software to re-create above steps. Ansible? Puppet?
* Add required plugins to `composer.json` `"require": {` and run `composer update`. Eg
```
"wpackagist/advanced-custom-fields": "4.3.8"
```
## Further reading

* [Twelve Factor WordPress] 
* [Using Composer with WordPress].


[Roots.io]: http://roots.io/
[bedrock]: https://github.com/roots/bedrock
[Twelve Factor WordPress]: http://roots.io/twelve-factor-wordpress/
[screencast]: http://roots.io/screencasts/using-composer-with-wordpress/
[@swalkinshaw]: https://twitter.com/swalkinshaw
[Using Composer with WordPress]: http://roots.io/using-composer-with-wordpress/
[WordPress file permissions]: https://gist.github.com/growdigital/a98d3fb9efe575159151