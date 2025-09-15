PHP (Composer) Console Bootstrap

This is a minimal PHP console application created with Composer. Use it for live coding exercises, technical interviews, or as a quick bootstrap for coding dojos.

It demonstrates best practices for a modern PHP CLI app: Composer-based dependency management, PSR-4 autoloading, and PHPUnit for testing.

## Project origin
Created by running `composer init`, adding PHPUnit as a dev dependency, and creating a lightweight test case.

## Prerequisites

- PHP (https://www.php.net/downloads.php)
- Composer (https://getcomposer.org/download/)

### GitHub Codespaces
Recommended for interviews and dojos. See the [main README](../README.md) for Codespaces setup instructions.

### First-time setup (local)
After cloning, in the `php-composer` folder run:

```sh
composer install
```

This will create the `vendor/` directory. Do not commit `vendor/`; ensure it's listed in `.gitignore`.

## Project Structure
- `src/app.php`: Main application file
- `tests/UnitTest.php`: Example PHPUnit test
- `vendor/`: Composer dependencies (generated)

## Run the app
On macOS / Linux:

```sh
cd php-composer
php src/app.php
```

On Windows (PowerShell):

```pwsh
cd php-composer
php src/app.php
```

## Run tests
Preferred (cross-platform, uses Composer scripts):

```sh
cd php-composer
composer test
```

Optional: run PHPUnit directly from the vendor folder (useful for debugging):

On macOS / Linux:

```sh
cd php-composer
vendor/bin/phpunit --testdox tests
```

On Windows (PowerShell):

```pwsh
cd php-composer
vendor\bin\phpunit --testdox tests
```

## Troubleshooting
- Ensure PHP and Composer are installed and on your PATH.
- If dependencies are missing, run `composer install` in the `php-composer` folder.

## Maintenance
For contributors and maintainers only: to update dependencies to newer versions run:

```sh
composer update
```

This updates `composer.lock` and installed packages. If you run `composer update`, review and commit the updated `composer.lock` so other users get the same dependency versions when they run `composer install`.

Regular users and interview participants should not run `composer update` — they should use `composer install` to reproduce the versions in `composer.lock`.

## Notes
- This is intentionally minimal to keep the barrier to entry low during interviews and dojos.
- If you want a web app example, consider adding a separate folder (e.g., `php-laravel`).