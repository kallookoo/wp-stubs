# WordPress and WooCommerce stubs for PHP

This repository uses the [php-stubs](https://github.com/php-stubs) to:

1. Have all stubs registered within the stubs folder
2. Have a single file with all stubs

Stub packages:

- [php-stubs/wordpress-stubs](https://github.com/php-stubs/wordpress-stubs)
- [php-stubs/wordpress-globals](https://github.com/php-stubs/wordpress-globals)
- [php-stubs/woocommerce-stubs](https://github.com/php-stubs/woocommerce-stubs)
- [php-stubs/wp-cli-stubs](https://github.com/php-stubs/wp-cli-stubs)

Usage in phpantom (until it supports custom stubs):

- Install

```sh
composer require --dev kallookoo/wp-stubs
```

- Configure it so phpantom detects it

```json
{
  "autoload-dev": {
    "files": ["vendor/kallookoo/wp-stubs/stubs.php"]
  }
}
```

Or load only what you need

```json
{
  "autoload-dev": {
    "files": [
      "vendor/kallookoo/wp-stubs/stubs/wordpress-globals.php",
      "vendor/kallookoo/wp-stubs/stubs/wordpress-stubs.php"
    ]
  }
}
```

- Update

Run `composer update` to refresh the stub package
