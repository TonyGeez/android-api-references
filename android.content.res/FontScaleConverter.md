Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FontScaleConverter

```
interface FontScaleConverter
```

| [android.content.res.FontScaleConverter](https://developer.android.com/reference/kotlin/android/content/res/FontScaleConverter#) |

A converter for non-linear font scaling. Converts font sizes given in "sp" dimensions to a "dp" dimension according to a non-linear curve.

This is meant to improve readability at larger font scales: larger fonts will scale up more slowly than smaller fonts, so we don't get ridiculously huge fonts that don't fit on the screen.

The thinking here is that large fonts are already big enough to read, but we still want to scale them slightly to preserve the visual hierarchy when compared to smaller fonts.

## Summary

| Public methods ||
|---|---|
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/FontScaleConverter#convertDpToSp(kotlin.Float)(dp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Converts a dimension in "dp" back to "sp". |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/FontScaleConverter#convertSpToDp(kotlin.Float)(sp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Converts a dimension in "sp" to "dp". |
| open static [FontScaleConverter](https://developer.android.com/reference/kotlin/android/content/res/FontScaleConverter#)? | `https://developer.android.com/reference/kotlin/android/content/res/FontScaleConverter#forScale(kotlin.Float)(fontScale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Finds a matching FontScaleConverter for the given fontScale factor. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/FontScaleConverter#isNonLinearFontScalingActive(kotlin.Float)(fontScale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns true if non-linear font scaling curves would be in effect for the given scale, false if the scaling would follow a linear curve or for no scaling. |

## Public methods

### convertDpToSp

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun convertDpToSp(dp: Float): Float
```

Converts a dimension in "dp" back to "sp".

### convertSpToDp

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun convertSpToDp(sp: Float): Float
```

Converts a dimension in "sp" to "dp".

### forScale

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun forScale(fontScale: Float): FontScaleConverter?
```

Finds a matching FontScaleConverter for the given fontScale factor. Generally you shouldn't need this; you can use `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#applyDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics)` directly and it will do the scaling conversion for you. Dimens and resources loaded from XML will also be automatically converted. But for UI frameworks or other situations where you need to do the conversion without an Android Context, you can use this method. 
This method is safe to call from any thread.

| Parameters ||
|---|---|
| `fontScale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the scale factor, usually from `https://developer.android.com/reference/kotlin/android/content/res/Configuration#fontScale:kotlin.Float`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/FontScaleConverter#?` | a converter for the given scale, or null if non-linear scaling should not be used. |

### isNonLinearFontScalingActive

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isNonLinearFontScalingActive(fontScale: Float): Boolean
```

Returns true if non-linear font scaling curves would be in effect for the given scale, false if the scaling would follow a linear curve or for no scaling.

Example usage: `isNonLinearFontScalingActive(getResources().getConfiguration().fontScale)` 
This method is safe to call from any thread.
