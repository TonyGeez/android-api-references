# SystemFonts

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemFonts

Kotlin| [Java](../android/graphics/fonts/SystemFonts.md) 
| --- | --- |

```
class SystemFonts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.fonts.SystemFonts](../android/graphics/fonts/SystemFonts.md) |

Provides the system font configurations.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Font](../android/graphics/fonts/Font.md)!\> | [getAvailableFonts](../android/graphics/fonts/SystemFonts.md))`()` Returns all available font files in the system. |

## Public methods

### getAvailableFonts

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAvailableFonts(): MutableSet<Font!>
```

Returns all available font files in the system.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Font](../android/graphics/fonts/Font.md)!> | a set of system fonts This value cannot be`null`. |
