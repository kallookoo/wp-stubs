# PHP stubs for the WordPress ecosystem

This repository uses the [php-stubs](https://github.com/php-stubs) to:

1. Have all stubs registered within the stubs folder
2. Have a single file with all stubs

Stub packages:

- [php-stubs/wordpress-stubs](https://github.com/php-stubs/wordpress-stubs)
- [php-stubs/wordpress-globals](https://github.com/php-stubs/wordpress-globals)
- [php-stubs/woocommerce-stubs](https://github.com/php-stubs/woocommerce-stubs)
- [php-stubs/wp-cli-stubs](https://github.com/php-stubs/wp-cli-stubs)

> [!NOTE]
> `wordpress-globals` is **DEPRECATED** but is still being kept for the time being.

> [!WARNING]
> The combined `stubs.php` file will be removed in a future major release. It only exists for PHPantom `<=0.11.1`; use the individual files in the `stubs/` folder instead.

## Usage in PHPantom (<=0.11.1)

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
    "files": ["vendor/kallookoo/wp-stubs/stubs/wordpress-stubs.php"]
  }
}
```

- Update

Run `composer update` to refresh the stub package

## Usage in PHPantom (> 0.11.1)

More info at:

- https://phpantom-dev.github.io/phpantom_lsp/prerelease/configuration/#stubs
- https://phpantom-dev.github.io/phpantom_lsp/prerelease/configuration/#editor-supplied-stubs

My recommendation if you use it regularly:

- Install it globally

```sh
composer global require --dev kallookoo/wp-stubs
```

- Configure PHPantom globally

```toml
[stubs]
paths = ["COMPOSER_HOME/vendor/kallookoo/wp-stubs/stubs"]
```

Replace `COMPOSER_HOME` with the correct path.

```sh
composer config --global home
```

More info: https://getcomposer.org/doc/03-cli.md#composer_home
