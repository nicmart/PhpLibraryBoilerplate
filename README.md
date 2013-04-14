# Php library template

This is the basic skeleton I use each time I create a new php library. It includes basic phpunit, travisci and composer configuration,
and a basic folder structure.

There are few template variables I substitute with a "find and replace" each time I initialize the library. This variables are
- {library-name} The name of the library
- {library-desc} A brief descrption of what the library does
- {library-namespace} The main library namespace. I usually set this equal to the camelized library name

Other values like library author name and email are hardcoded in the files.

What follows is the skeleton README.md file.

# {library-name}

{library-desc}.

[![Build Status](https://secure.travis-ci.org/nicmart/{library-name}.png?branch=master)](http://travis-ci.org/nicmart/{library-name})

## Install

The best way to install {library-name} is [through composer](http://getcomposer.org).

Just create a composer.json file for your project:

```JSON
{
    "require": {
        "nicmart/{library-name}": "dev-master"
    }
}
```

Then you can run these two commands to install it:

    $ curl -s http://getcomposer.org/installer | php
    $ php composer.phar install

or simply run `composer install` if you have have already [installed the composer globally](http://getcomposer.org/doc/00-intro.md#globally).

Then you can include the autoloader, and you will have access to the library classes:

```php
<?php
require 'vendor/autoload.php';
```