Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntObjFunction

```
@FunctionalInterface interface IntObjFunction<T : Any!, R : Any!>
```

| [android.util.function.IntObjFunction](IntObjFunction.md) |

Represents a function that accepts an `int`-valued argument and an object-valued argument, and produces a result.

## Summary

| Public methods ||
|---|---|
| abstract R | `https://developer.android.com/reference/kotlin/android/util/function/IntObjFunction#apply(kotlin.Int,%20android.util.function.IntObjFunction.T)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: T)` Performs this operation on the given arguments. |

## Public methods

### apply

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun apply(
    value: Int, 
    t: T
): R
```

Performs this operation on the given arguments.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first input argument |
| `t` | T: the second input argument |

| Return ||
|---|---|
| `R` | the operation result |
