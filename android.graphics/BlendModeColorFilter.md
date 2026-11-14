Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlendModeColorFilter

Kotlin | [Java](BlendModeColorFilter.md)
| --- | --- |

```
class BlendModeColorFilter : ColorFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.ColorFilter](ColorFilter.md) ||
| | ↳ | [android.graphics.BlendModeColorFilter](BlendModeColorFilter.md) |

A color filter that can be used to tint the source pixels using a single color and a specific `https://developer.android.com/reference/kotlin/android/graphics/BlendMode`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter#BlendModeColorFilter(kotlin.Int,%20android.graphics.BlendMode)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode)` <br /> |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter#getColor()()` Returns the ARGB color used to tint the source pixels when this filter is applied. |
| [BlendMode](BlendMode.md)! | `https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter#getMode()()` Returns the Porter-Duff mode used to composite this color filter's color with the source pixel when this filter is applied. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter#hashCode()()` Returns a hash code value for the object. |

## Public constructors

### BlendModeColorFilter

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BlendModeColorFilter(
    color: Int, 
    mode: BlendMode)
```

| Parameters ||
|---|---|
| `mode` | [BlendMode](BlendMode.md): This value cannot be `null`. |

## Public methods

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColor(): Int
```

Returns the ARGB color used to tint the source pixels when this filter is applied.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Color`

### getMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMode(): BlendMode!
```

Returns the Porter-Duff mode used to composite this color filter's color with the source pixel when this filter is applied.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/BlendMode`

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
