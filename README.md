# Useful / fun bash alias

## Laravel

### Laravel doc
```bash
alias ldoc=/path-to-your/laravel-doc.sh
```

... and the laravel-doc.sh file
```bash
#!/bin/bash
echo "doc $1"| php artisan tinker
```

Then you can type something like:

```bash
$ ldoc array_wrap
```

And the output would be:
```php
Psy Shell v0.8.8 (PHP 7.0.18-0ubuntu0.17.04.1 — cli) by Justin Hileman
function array_wrap($value)

Description:
  If the given value is not an array, wrap it in one.

Param:
  mixed  $value

Return:
  array

Exit:  Ctrl+D
```

You can also use a full namespace of a class

```php
$ ldoc \\Carbon\\Carbon::createFromFormat

Psy Shell v0.8.8 (PHP 7.0.18-0ubuntu0.17.04.1 — cli) by Justin Hileman
public static function createFromFormat($format, $time, $tz = null)

Description:
  Create a Carbon instance from a specific format.

Throws:
  \InvalidArgumentException

Param:
  string                     $format
  string                     $time
  \DateTimeZone|string|null  $tz

Return:
  static

Exit:  Ctrl+D

```

### Laravel tinker
alias tinker="php artisan tinker"

---

## Git

### Discard changes
If you don't like what you are doing just type:
```bash
$ nah
```

Add the alias in your bash profile file
```bash
alias nah="git clean -df; git checkout -- ."
```

# Contribute

You can create a pull request to this repository or send me your bash alias to [@jeffer_8a](http://twitter.com/jeffer_8a) :)

### Thanks!
This repository was inspired by [@paulredmond](https://twitter.com/paulredmond)
