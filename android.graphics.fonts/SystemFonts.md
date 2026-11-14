# SystemFonts

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemFonts

Kotlin| [Java](SystemFonts.md) 
| --- | --- |

```
class SystemFonts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.fonts.SystemFonts](SystemFonts.md) |

Provides the system font configurations.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Font](Font.md)!\> | [getAvailableFonts](SystemFonts.md))`()` Returns all available font files in the system. |

## Public methods

### getAvailableFonts

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAvailableFonts(): MutableSet<Font!>
```

Returns all available font files in the system.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Font](Font.md)!> | a set of system fonts This value cannot be`null`. |
