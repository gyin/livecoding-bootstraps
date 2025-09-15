Can be used for live coding exercises during job interviews, or for a quick bootstrap during a coding dojo.
It was created by running `composer init`, adding PHPUnit as a dev dependency, and creating a small lightweight test case.

# Prerequisites

## With GitHub Codespaces

One easy way to run  is meant to be run inside of GitHub Codespace for job interview. See the home README for instructions on 
Can also be used for coding dojos.

## On local PC

This can be run simply by installing 

# Execute

Run, on MacOS and Linux:

```
cd php-composer
php src/app.php
```

And in Windows

```
cd php-composer
php src\app.php
```


# Run Unit Tests

Run, on MacOS and Linux:

```
cd php-composer
vendor/bin/phpunit --testdox tests
```

And in Windows:

```
cd php-composer
vendor\bin\phpunit --testdox tests
```
## PHP Composer Bootstrap

This is a minimal PHP console application project created with Composer. Use it for live coding exercises, technical interviews, or as a quick bootstrap for coding dojos.

It demonstrates best practices for a modern PHP CLI app: Composer-based dependency management, PSR-4 autoloading, and PHPUnit for testing.

Created by running `composer init`, adding PHPUnit as a dev dependency, and creating a lightweight test case.

## Prerequisites

### GitHub Codespaces
Recommended for interviews and dojos. See the [main README](../README.md) for Codespaces setup instructions.

### Local PC
To run locally, install [PHP](https://www.php.net/downloads.php) and [Composer](https://getcomposer.org/download/).

**First time setup:**
After cloning, run the following command to install dependencies:
```sh
composer install
```

This will create the `vendor/` directory, which should not be committed to git. Make sure `vendor/` is listed in `.gitignore`.

## Project Structure
- `src/app.php`: Main application file
- `tests/UnitTest.php`: Example PHPUnit test
- `vendor/`: Composer dependencies

## Execute

On MacOS and Linux:
```sh
cd php-composer
php src/app.php
```

On Windows:
```pwsh
cd php-composer
php src\app.php
```

## Run Unit Tests

On MacOS and Linux:
```sh
cd php-composer
vendor/bin/phpunit --testdox tests
```

On Windows:
```pwsh
cd php-composer
vendor\bin\phpunit --testdox tests
```

## Troubleshooting
- Make sure PHP and Composer are installed and available in your PATH.
- If dependencies are missing, run `composer install` in the `php-composer` folder.