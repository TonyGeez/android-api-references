Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RoundedRectBlurRegion

```
class RoundedRectBlurRegion : BlurRegion
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.BlurRegion](../android/view/BlurRegion.md) ||
| | ↳ | [android.view.RoundedRectBlurRegion](RoundedRectBlurRegion.md) |

Defines a rounded rectangular blur region on the SurfaceView.

## Summary

| Public constructors ||
|---|---|
| RoundedRectBlurRegion Constructs a new `RoundedRectBlurRegion` with the default parameters. |
| RoundedRectBlurRegion Constructs a new `RoundedRectBlurRegion` with the specified rounded rectangle coordinates and corner radii. |

| Public methods ||
|---|---|
| [RoundedRectBlurRegion](RoundedRectBlurRegion.md) | copy Returns a deep copy of this blur region. |
| [RectF](../android.graphics/RectF.md) | getBounds Returns the bounds of the blur region. |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | getCornerRadii Returns the corner radii for the blur region. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBounds Sets the bounds of the blur region. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCornerRadii Sets the corner radius for all corners of the blur region. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCornerRadii Sets the corner radii for the blur region. |
| --- | --- |

Inherited functions From class BlurRegion `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` equals

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getAlpha

Returns the alpha for this region.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getBlurRadius

Returns the blur radius for this region.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` hashCode

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAlpha

Sets the alpha for this region.

The default value for alpha is 1.0f.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBlurRadius

Sets the blur radius for this region.

The default value for blur radius is 0.0f.

<br />

## Public constructors

### RoundedRectBlurRegion

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RoundedRectBlurRegion()
```

Constructs a new `RoundedRectBlurRegion` with the default parameters.

The default bounds and all corner radii are 0.0f.

The default alpha is 1.0f and the default blur radius is 0.0f.

### RoundedRectBlurRegion

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RoundedRectBlurRegion(
    rect: RectF, 
    cornerRadii: FloatArray, 
    alpha: Float, 
    blurRadius: Float)
```

Constructs a new `RoundedRectBlurRegion` with the specified rounded rectangle coordinates and corner radii.

The `cornerRadii` values are ordered \[topLeftX, topLeftY, topRightX, topRightY, bottomLeftX, bottomLeftY, bottomRightX, bottomRightY\].

| Parameters ||
|---|---|
| `rect` | [RectF](../android.graphics/RectF.md): bounds of the blur region. This value cannot be `null`. |
| `cornerRadii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): array of 8 floats representing the corner radii. This value cannot be `null`. |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): alpha value of the region \[0.0 - 1.0\]. Value is between 0.0f and 1.0f inclusive |
| --- | --- |
| `blurRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the blur radius in pixels |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `cornerRadii` is `null` or its length is not 8 or `rect` is `null` |

## Public methods

### copy

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copy(): RoundedRectBlurRegion
```

Returns a deep copy of this blur region.

| Return ||
|---|---|
| RoundedRectBlurRegion | This value cannot be `null`. |

### getBounds

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBounds(): RectF
```

Returns the bounds of the blur region.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` | `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` containing the bounds. This value cannot be `null`. |

### getCornerRadii

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCornerRadii(): FloatArray
```

Returns the corner radii for the blur region.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | array of 8 floats representing the corner radii. This value cannot be `null`. |

### setBounds

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setBounds(rect: RectF): Unit
```

Sets the bounds of the blur region.

The default value is an empty rectangle.

| Parameters ||
|---|---|
| `rect` | [RectF](../android.graphics/RectF.md): the bounds of the blur region. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `rect` is `null` |

### setCornerRadii

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCornerRadii(cornerRadius: Float): Unit
```

Sets the corner radius for all corners of the blur region.

| Parameters ||
|---|---|
| `cornerRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): radius in pixels. |

### setCornerRadii

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCornerRadii(cornerRadii: FloatArray): Unit
```

Sets the corner radii for the blur region.

The `cornerRadii` values are ordered \[topLeftX, topLeftY, topRightX, topRightY, bottomLeftX, bottomLeftY, bottomRightX, bottomRightY\].

The default value is all zeros.

| Parameters ||
|---|---|
| `cornerRadii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): array of 8 floats representing the corner radii. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `cornerRadii` is `null` or its length is not 8 |
