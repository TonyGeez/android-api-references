# PorterDuffColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PorterDuffColorFilter

Kotlin| [Java](../android/graphics/PorterDuffColorFilter.md) 
| --- | --- |

```
open class PorterDuffColorFilter : ColorFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.ColorFilter](../android/graphics/ColorFilter.md) ||
| | ↳ | [android.graphics.PorterDuffColorFilter](../android/graphics/PorterDuffColorFilter.md) |

A color filter that can be used to tint the source pixels using a single color and a specific [Porter-Duff composite mode](../android/graphics/PorterDuff.md).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PorterDuffColorFilter](../android/graphics/PorterDuffColorFilter.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` Create a color filter that uses the specified color and Porter-Duff mode. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/PorterDuffColorFilter.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/PorterDuffColorFilter.md))`()` <br /> |

## Public constructors

### PorterDuffColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PorterDuffColorFilter(
    color: Int, 
    mode: PorterDuff.Mode)
```

Create a color filter that uses the specified color and Porter-Duff mode.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ARGB source color used with the specified Porter-Duff mode |
| `mode` | [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md):The porter-duff mode that is applied This value cannot be`null`. |

**See Also**

- [android.graphics.Color](../android/graphics/Color.md)

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
