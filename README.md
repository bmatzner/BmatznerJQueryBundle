jQuery Bundle for Symfony2
=======================

## Current Version

jQuery 3.1.1

jQuery Migrate Plugin 3.0.0

**NOTE: If you have not yet upgraded to 1.12.x or 2.2.x, first upgrade to them and use jQuery Migrate 1.x to resolve any compatibility issues before using jQuery Migrate 3.0 and upgrading to jQuery 3.0.**

## Installation

### Add bundle to your composer.json file

Set the version of the bundle to the corresponding jQuery version.
For IE6/7/8 support, use the 1.x branch

``` js
// composer.json

{
    "require": {
		// ...
        "bmatzner/jquery-bundle": "~3.1"
    }
}
```

### Add bundle to your application kernel

``` php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Bmatzner\JQueryBundle\BmatznerJQueryBundle(),
        // ...
    );
}
```

### Download the bundle using Composer

``` bash
$ php composer.phar update bmatzner/jquery-bundle
```

### Install assets

Given your server's public directory is named "web", install the public vendor resources

``` bash
$ php app/console assets:install web
```

Optionally, use the --symlink attribute to create links rather than copies of the resources 

``` bash
$ php app/console assets:install --symlink web
```

## Usage

Refer to the desired files in your HTML template, e.g.

``` html
<script type="text/javascript" src="{{ asset('bundles/bmatznerjquery/js/jquery.min.js') }}"></script>
```

## Licenses

Refer to the source code of the included files for license information

## References

1. http://jquery.com
2. http://symfony.com
