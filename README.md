### HelloChef PHP Code Styles

Shared PHP style rules for PHP-CS-Fixer

Install the package

```bash
composer require hellochef-me/php-styles
```

Create and setup config file in project root `.php-cs-fixer.php`

```php
<?php

return HelloChef\CodeStyles\PhpStyles::style();
```

### Format code on demand

- Format the whole project

```bash
vendor/bin/php-cs-fixer fix .
```

- Format specific file

```bash
vendor/bin/php-cs-fixer fix `FILE-TO-FORMAT.php`
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
