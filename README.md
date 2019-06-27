## laravel-helper

Helper for common Laravel related tasks on server

## Installation

Clone this repository and make symlink:

```
$ git clone https://github.com/wmfairuz/laravel-helper.git
$ cd laravel-helper
$ ln -s laravel-helper /usr/bin/laravel-helper
```

## Usage

```
$ laravel-helper -dir
```

## Arguments

- d - Update code using git pull
- i - Update dependencies using composer
- r - Refresh laravel instance and fix folder permission / ownership
- l - Output Laravel log file and append output as log file grow
- t - Output Laravel log file with specified line number  (eg: -t 100 to output last 100 line)

## License

This package is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
