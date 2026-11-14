# SystemFonts

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemFonts

Kotlin| [Java](https://developer.android.com/reference/android/graphics/fonts/SystemFonts "View this page in Java") 
| --- | --- |

```
class SystemFonts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.fonts.SystemFonts](https://developer.android.com/reference/kotlin/android/graphics/fonts/SystemFonts#) |

Provides the system font configurations.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Font](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font)!\> | [getAvailableFonts](https://developer.android.com/reference/kotlin/android/graphics/fonts/SystemFonts#getAvailableFonts())`()` Returns all available font files in the system. |

## Public methods

### getAvailableFonts

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAvailableFonts(): MutableSet<Font!>
```

Returns all available font files in the system.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Font](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font)!> | a set of system fonts This value cannot be`null`. |
