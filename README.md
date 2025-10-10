<div align="center">

# TYPO3 PHPStan Preset

</div>

This package provides a basic TYPO3 [PHPStan](https://phpstan.org/) configuration.

> [!IMPORTANT]
> This package is intended for use in my personal projects only. It is not designed for general use.

## 🔥 Installation

[![Packagist](https://img.shields.io/packagist/v/konradmichalik/php-cs-fixer-preset?label=version&logo=packagist)](https://packagist.org/packages/konradmichalik/php-cs-fixer-preset)
[![Packagist Downloads](https://img.shields.io/packagist/dt/konradmichalik/php-cs-fixer-preset?color=brightgreen)](https://packagist.org/packages/konradmichalik/php-cs-fixer-preset)

```bash
composer require konradmichalik/phpstan-typo3-preset --dev
```

## ⚡ Usage

If you have the [`phpstan/extension-installer`](https://github.com/phpstan/extension-installer)
package installed, there's nothing more to do. The [base configuration](extension.neon)
is automatically included.

### Manual Setup

```yaml
# phpstan.neon

includes:
  - %rootDir%/../../konradmichalik/phpstan-typo3-preset/phpstan.neon.dist

parameters:
  level: 7

  paths:
    - Classes
    - Configuration
    - Resources
    - Tests/Unit

  excludePaths:
    - .Build (?)

  type_coverage:
    constant: 0 # TODO: Set to 100, when PHP 8.3 is minimum requirement
```

## ⭐ License

This project is licensed under [GNU General Public License 3.0 (or later)](LICENSE).
