# NotEmpty

- `NotEmpty()`

Validates wether the given input is not empty. This function also takes whitespace
into account, use `noWhitespace()` if no spaces or linebreaks and other
whitespace anywhere in the input is desired.

```php
v::stringType()->notEmpty()->validate(''); // false
```

Null values are empty:

```php
v::notEmpty()->validate(null); // false
```

Numbers:

```php
v::intVal()->notEmpty()->validate(0); // false
```

Empty arrays:

```php
v::arrayVal()->notEmpty()->validate([]); // false
```

Whitespace:

```php
v::stringType()->notEmpty()->validate('        ');  //false
v::stringType()->notEmpty()->validate("\t \n \r");  //false
```

## Categorization

- Miscellaneous

## Changelog

Version | Description
--------|-------------
  0.3.9 | Created

***
See also:

- [Each](Each.md)
- [Max](Max.md)
- [Min](Min.md)
- [NoWhitespace](NoWhitespace.md)
- [NotBlank](NotBlank.md)
- [NotUndef](NotUndef.md)
- [NullType](NullType.md)
- [Number](Number.md)
- [UndefOr](UndefOr.md)
