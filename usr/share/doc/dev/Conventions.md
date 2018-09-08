# Conventions

## Includes

Includes are wrapped in an `if` block which always fails, but the `#include` directive is still run.

```c
if (0) {
  #include "mark_iii/lib/drv"
}
```

## Variable Types

Variable types/function arguments are always given a type, even if they are a number.
