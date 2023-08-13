# Cielo Specification

## Inspirations

* Rust
* Python
* Haskell
* C

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

### Types

#### Integers
Integers can be represented by the following types:

* `int` – type alias for `i32`

Unsigned:

* u8
* u16
* u32
* u64
* u128

Signed:

#### Strings
Strings are UTF8 encoded by default.

##### Concatenation
Strings can be concatenated as is with the `+` operator:

```
print("Hello " + "World!")
```

outputs:

```
Hello World!
```

Strings can also be concatenated with a space in the middle by using the `++`
operator:

```
print("Hello" ++ "World!")
```

outputs:

```
Hello World!
```

## Arithmetic Expressions
You can use the following arithmetic operators:

* `+` – The addition operator | `5 + 5` returns `10`
* `-` – The subtraction operator | `7 - 2` returns `5`
* `*` – The multiplication operator | `2 * 4` returns `8`
* `/` – The division operator
    * `10 / 5` returns `2` if they are both integers, and `2.0` if one or both
      are floats
    * `1 / 3` returns `0` if they are both integers, and `0.333333 (etc)` if
      one or both are floats



<!-- ## Precedence -->

## Loops

### Infinite loop
This loop will loop indefinitely by default, but can be broken out of with
`break`.

```
loop {
    print("I loop forever!")
}
```

### for loop
This loop will iterate over any iterable type:

```
names = ["John", "Kerry", "Sophia", "Delilah"]
for name in names {
    print(name)
}
```

prints:

```
John
Kerry
Sophia
Delilah
```

### while loop
This loop will execute only if the expression give is true:

```
i = 0
while (i < 10) {
    print("i = " ++ i)
    i++
}
print("done!")
```

prints:

```
0
1
2
3
4
5
6
7
8
9
done!
```

### do while loop
This loop will execute once, then only execute the following times if a
condition is met:

```
i := 1
do while (false) {
    print(i)
    i++
}
```

prints:

```
1
```

### with expression
You can use a `with` expression to do some functionality only **once** before a
loop starts, even if the loop doesn't execute due to conditions failing.

Variables declared within this expression are available only within the `with`
expression, the `while` expression, and the main loop body.

This is mostly used to emulate the `for` loops of other languages, wherein
there exists a variable.

### for loops from other languages
To emulate `for` loops from other languages, by chaining a `with` expression
for the initialization of variables, a `while` or `do while` loop (for the
condition checking), 