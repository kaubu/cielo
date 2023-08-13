# Cielo Standard Library

## Prelude
Cielo files automatically include imports that are in `std::prelude`, by using
an implicit `import std::prelude::*`.

You can opt-out of this behaviour by typing the `#NO_PRELUDE` directive. These
should generally be placed at the top of the file (because the interpreter has
to search through the entire file, placing it near the bottom will simply make
load times increase), but can be placed anywhere in the main scope.

Here is a list of imports in the prelude:

```
import std::io::{
    print,
    input,
}
```