# DataOrigin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataOrigin

Kotlin| [Java](DataOrigin.md) 
| --- | --- |

```
class DataOrigin
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.DataOrigin](DataOrigin.md) |

Specifies the contributing source/application of any [Record](Record.md)

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/datatypes/DataOrigin.Builder.md) <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](DataOrigin.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](DataOrigin.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](DataOrigin.md))`()` Returns a hash code value for the object. |
| --- | --- |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|----------|----------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj |

### getPackageName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String
```

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the corresponding package name. This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
