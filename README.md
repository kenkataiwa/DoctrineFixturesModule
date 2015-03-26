# Doctrine Fixtures Module for Zend Framework 2

## Introduction

This module integrates the [Doctrine Data Fixtures library](https://github.com/doctrine/data-fixtures).
into Zend Framework 2 so that you can load data fixtures programmatically into the Doctrine ORM or ODM.

## Installation

Installation of this module uses composer. For composer documentation, please refer to
[getcomposer.org](http://getcomposer.org/).

```sh
$ composer require kenkataiwa/doctrine-fixtures-module
```

Then open `config/application.config.php` and add `DoctrineModule`, `DoctrineORMModule` and 
`DoctrineFixturesModule` to your `modules`

#### Registering Fixtures

To register fixtures with Doctrine module add the fixtures in your configuration.

```php
<?php
return array(
      'doctrine' => array(
            'fixtures' => array(
                  __NAMESPACE__.'_fixture' => __DIR__ . '/../src/'.__NAMESPACE__.'/Fixture',
            )
      )
);
```

## Usage

### Command Line
Access the Doctrine command line as following

#### Load
```sh
./vendor/bin/doctrine-module fixtures:load 
```
