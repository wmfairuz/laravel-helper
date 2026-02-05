## laravel-helper

Bash script helper for common Laravel related tasks on server

## Installation

Clone this repository and make symlink:

```
$ git clone https://github.com/wmfairuz/laravel-helper.git
$ cd laravel-helper
$ ln -s ${PWD}/laravel-helper /usr/bin/laravel-helper
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

or you can use current directory by omitting both -d argument and DEPLOY_DIR env variable.

You can set a specific php cli version that will be used throughout the script. The php version will be reverted to the 
original version at the end of the script run.

```
$ laravel-helper -p 8.4 -d /opt/my-laravel -uir
```

By default will use current cli php version.

## Arguments

- d - Target directory (eg: -d /opt/my-laravel)
- u - Update code using git pull (defaults to master branch)
- i - Install dependencies using composer
- r - Refresh laravel instance and fix folder permission / ownership
- t - Output Laravel log file with specified line number  (eg: -t 100 to output last 100 line)
- l - Output Laravel log file and append output as log file grow
- p - Set php cli version. php version will be reverted to original before exiting (eg: -p 8.4)

## License

This package is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
