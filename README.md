### HelloChef PHP Code Styles

Shared PHP style rules for PHP-CS-Fixer

Install 
> composer require hellochef-me/php-styles
 
Create and setup config file `.php-cs-fixer`

```php
<?php

return HelloChef\CodeStyles\PhpStyles::style();
```

Enable pre-commit
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
