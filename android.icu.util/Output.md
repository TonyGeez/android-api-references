# Output

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Output

Kotlin | [Java](Output.md) 
| --- | --- |

```
open class Output<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.Output](Output.md) |

Simple struct-like class for output parameters.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Output](Output.md))`()` Constructs an empty `Output` |
| [Output](Output.md))`(`value:` `T`)` Constructs an `Output` with the given value. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Output.md))`()` Returns a string representation of the object. |

| Properties ||
|---|---------------------------------------------------------------------------------------------------------------------------------|
| T | [value](Output.md) The value field |

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
