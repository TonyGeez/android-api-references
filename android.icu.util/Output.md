# Output

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Output

Kotlin | [Java](https://developer.android.com/reference/android/icu/util/Output "View this page in Java") 
| --- | --- |

```
open class Output<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.Output](https://developer.android.com/reference/kotlin/android/icu/util/Output#) |

Simple struct-like class for output parameters.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Output](https://developer.android.com/reference/kotlin/android/icu/util/Output#Output())`()` Constructs an empty `Output` |
| [Output](https://developer.android.com/reference/kotlin/android/icu/util/Output#Output(android.icu.util.Output.T))`(`value:` `T`)` Constructs an `Output` with the given value. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/util/Output#toString())`()` Returns a string representation of the object. |

| Properties ||
|---|---------------------------------------------------------------------------------------------------------------------------------|
| T | [value](https://developer.android.com/reference/kotlin/android/icu/util/Output#value:android.icu.util.Output.T) The value field |

## Public constructors

### Output

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Output()
```

Constructs an empty `Output` 

### Output

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Output(value: T)
```

Constructs an `Output` with the given value.

| Parameters ||
|---------|----------------------|
| `value` | T: the initial value |

## Public methods

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### value

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var value: T
```

The value field
