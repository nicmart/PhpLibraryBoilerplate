# Php library template

This is the basic skeleton I use each time I create a new php library. It includes basic phpunit, travisci and composer configuration,
and a basic folder structure.

There are few template variables I substitute with a "find and replace" each time I initialize the library. This variables are
- {library-name} The name of the library
- {library-name-slug} The sluggified version of library name, used in composer configuration
- {library-desc} A brief descrption of what the library does
- {library-namespace} The main library namespace. I usually set this equal to the camelized library name

Other values like library author name and email are hardcoded in the files.

What follows is the skeleton README.md file.

# {library-name}
[![Build Status](https://travis-ci.org/nicmart/{library-name}.png?branch=master)](https://travis-ci.org/nicmart/{library-name})
[![Coverage Status](https://coveralls.io/repos/nicmart/{library-name}/badge.png?branch=master)](https://coveralls.io/r/nicmart/{library-name}?branch=master)
[![Scrutinizer Quality Score](https://scrutinizer-ci.com/g/nicmart/{library-name}/badges/quality-score.png?s=e06818508807c109a8c9354a73fc1a5227426c09)](https://scrutinizer-ci.com/g/nicmart/StringTemplate/)

{library-desc}.

## Install

The best way to install {library-name} is [through composer](http://getcomposer.org).

Just create a composer.json file for your project:

```JSON
{
    "require": {
        "nicmart/{library-name-slug}": "dev-master"
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