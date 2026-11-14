Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongObjFunction

```
@FunctionalInterface interface LongObjFunction<T : Any!, R : Any!>
```

| [android.util.function.LongObjFunction](https://developer.android.com/reference/kotlin/android/util/function/LongObjFunction#) |

Represents a function that accepts a `long`-valued argument and an object-valued argument, and produces a result.

## Summary

| Public methods ||
|---|---|
| abstract R | `https://developer.android.com/reference/kotlin/android/util/function/LongObjFunction#apply(kotlin.Long,%20android.util.function.LongObjFunction.T)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, t: T)` Performs this operation on the given arguments. |

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
