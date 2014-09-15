# Groundwork

## Status: it works, just about  
Version: 0.1.0

A WordPress starter kit, based on the excellent work of [Roots.io]. 

Rather than just use [bedrock], I have pieced this together from [@swalkinshaw]’s thorough [screencast], to increase the size of my brain.

Hopefully this may be useful to web developers who want a well organised, easy to deploy WordPress installation.

## Instructions

* `composer install`
* Create `.env` file from `.env.example`
* Set environment variables
* Set [WordPress file permissions]
* Run the WordPress install in a browser
* Change `Site address (URL)` in `Settings > General`
* Enable permalinks in `Settings > Permalinks`

---

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
