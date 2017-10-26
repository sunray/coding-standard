# Sunray PHP Coding Standard

We basically follow the coding style related [PSR standards](http://www.php-fig.org/psr/) 
issued by the PHP Framework Interoperability Group:

* [PSR-1: Basic Coding Standard](http://www.php-fig.org/psr/psr-1/)
* [PSR-2: Coding Style Guide](http://www.php-fig.org/psr/psr-2/)
* [PSR-12: Extended Coding Style Guide](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md) (draft)

## Differences from PSR

#### Spaces around concatenation

The string concatenation operator MUST be preceded and followed by a space.

```php
// bad
$string = 'Hello '.$name;

// good
$string = 'Hello ' . $name;
```

#### Naming

About the names of identifiers like classes, functions, methods, variables:

* A name SHOULD be descriptive, distinctive, precise and readable.
* A name SHOULD NOT be abbreviated.
* A name SHOULD NOT be pre- or postfixed with Interface, Trait or Abstract.

A long name is not a problem, since our IDE has auto completion.

#### Inter-line alignment

Consecutive assignments or declarations SHOULD NOT be aligned. Adding one item may 
require you to re-align the other items, resulting in unnecessary changes in your commit.

```php
// bad
$short        = 1;
$veryLongItem = 2;

// good
$short = 1;
$veryLongItem = 2;