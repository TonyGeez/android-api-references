Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongObjFunction

```
@FunctionalInterface interface LongObjFunction<T : Any!, R : Any!>
```

| [android.util.function.LongObjFunction](LongObjFunction.md) |

Represents a function that accepts a `long`-valued argument and an object-valued argument, and produces a result.

## Summary

| Public methods ||
|---|---|
| abstract R | apply Performs this operation on the given arguments. |

## Public methods

### apply

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun apply(
    value: Long, 
    t: T
): R
```

Performs this operation on the given arguments.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first input argument |
| `t` | T: the second input argument |

| Return ||
|---|---|
| `R` | the operation result |
