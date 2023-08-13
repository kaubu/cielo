# Cielo Specification

## Variables
### Names
There is no set format, though it is recommended that you keep it in
`snake_case`.

Limitations include:

* Variables must not start with a number
* Variables must not contain any operators like `(`, `)`, `+`, etc
* Variables must not have spaces

### Declaration
Variables can be declared like so:

```
let age
```

With explicit type declaration:

```
let i32 age
```

### Assigning values
You can assign values to variables using:

```
age = 42
```

### Initialization
Variables can be declared and assigned in one go using initialization:

```
let age = 42
```

The interpreter will automatically figure out which type it is, though it can
be manually stated:

```
let age i32 = 42
```

You can also use a shorthand syntax with the initialization operator `:=`:

```
age := 42
birth_year i32 := 1907
```

## Arithmetic Expressions
You can use the following arithmetic operators:

* `+` – The addition operator | `5 + 5` returns `10`
* `-` – The subtraction operator | `7 - 2` returns `5`
* `*` – The multiplication operator | `2 * 4` returns `8`
* `/` – The division operator
    * `10 / 3` returns `3` if they are both integers, and `2.0` if one or both
      are floats
    * `9