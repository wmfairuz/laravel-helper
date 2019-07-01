## laravel-helper

Bash script helper for common Laravel related tasks on server

## Installation

Clone this repository and make symlink:

```
$ git clone https://github.com/wmfairuz/laravel-helper.git
$ cd laravel-helper
$ ln -s laravel-helper /usr/bin/laravel-helper
```

Set DEPLOY_DIR in your shell (eg. .bashrc) or directly define when invoking the script.

## Update laravel-helper

```
$ cd laravel-helper
$ git pull
```


## Usage

```
$ laravel-helper -d /opt/my-laravel -uir
```

or with a server that only has one laravel instance, we can put the target directory in DEPLOY_DIR

```
$ export DEPLOY_DIR=/opt/my-laravel
$ laravel-helper -uir
```

or you can use current directory by omitting both -d argument and DEPLOY_DIR env variable

## Arguments

- d - Target directory (eg: -d /opt/my-laravel)
- u - Update code using git pull (defaults to master branch)
- i - Install dependencies using composer
- r - Refresh laravel instance and fix folder permission / ownership
- t - Output Laravel log file with specified line number  (eg: -t 100 to output last 100 line)
- l - Output Laravel log file and append output as log file grow

## License

This package is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
