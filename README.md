### HelloChef PHP Code Styles

Shared PHP style rules for PHP-CS-Fixer

[![Latest Version on Packagist](https://img.shields.io/packagist/v/hellochef-me/php-styles.svg?style=flat-square)](https://packagist.org/packages/hellochef-me/php-styles)
[![Total Downloads](https://img.shields.io/packagist/dt/hellochef-me/php-styles.svg?style=flat-square)](https://packagist.org/packages/hellochef-me/php-styles)
[![MIT Licensed](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)

Install the package

```bash
composer require hellochef-me/php-styles
```

Create and setup config file in project root `.php-cs-fixer.php`

```php
<?php

return HelloChef\CodeStyles\PhpStyles::style();
```

Optionally, you may add php-cs-fixer cache file to your `.gitignore`
```
// .gitignore
.php-cs-fixer.cache
```

### Format code on demand

- Format the whole project

```bash
vendor/bin/php-cs-fixer fix .
```

- Format specific file

```bash
vendor/bin/php-cs-fixer fix Path/To/ExampleFileToFormat.php
```

### Format code on commit

Add the following scripts to your `composer.json`

```json
"scripts": {
    "post-update-cmd": [
      "cp vendor/hellochef-me/php-styles/pre-commit .git/hooks/pre-commit",
      "chmod a+x .git/hooks/pre-commit"
    ],
    "post-install-cmd": [
      "cp vendor/hellochef-me/php-styles/pre-commit .git/hooks/pre-commit",
      "chmod a+x .git/hooks/pre-commit"
    ],
},
```
