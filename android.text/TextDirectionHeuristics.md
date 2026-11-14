# TextDirectionHeuristics

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextDirectionHeuristics

Kotlin| [Java](TextDirectionHeuristics.md) 
| --- | --- |

```
open class TextDirectionHeuristics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.TextDirectionHeuristics](TextDirectionHeuristics.md) |

Some objects that implement [TextDirectionHeuristic](TextDirectionHeuristic.md). Use these with the android.text.BidiFormatter#unicodeWrap methods in [BidiFormatter](BidiFormatter.md). Also notice that these direction heuristics correspond to the same types of constants provided in the [android.view.View](../android.view/View.md) class for [setTextDirection()](../android.view/View.md)), such as [android.view.View#TEXT_DIRECTION_RTL](../android.view/View.md).

To support versions lower than [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), you can use the support library's androidx.core.text.TextDirectionHeuristicsCompat class.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextDirectionHeuristics](TextDirectionHeuristics.md))`()` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [TextDirectionHeuristic](TextDirectionHeuristic.md)! | [ANYRTL_LTR](TextDirectionHeuristics.md) If the text contains any strong right to left non-format character, determines that the direction is right to left, falling back to left to right if it finds none. |
| static [TextDirectionHeuristic](TextDirectionHeuristic.md)! | [FIRSTSTRONG_LTR](TextDirectionHeuristics.md) Determines the direction based on the first strong directional character, including bidi format chars, falling back to left to right if it finds none. |
| static [TextDirectionHeuristic](TextDirectionHeuristic.md)! | [FIRSTSTRONG_RTL](TextDirectionHeuristics.md) Determines the direction based on the first strong directional character, including bidi format chars, falling back to right to left if it finds none. |
| --- | --- |
| static [TextDirectionHeuristic](TextDirectionHeuristic.md)! | [LOCALE](TextDirectionHeuristics.md) Force the paragraph direction to the Locale direction. |
| static [TextDirectionHeuristic](TextDirectionHeuristic.md)! | [LTR](TextDirectionHeuristics.md) Always decides that the direction is left to right. |
| static [TextDirectionHeuristic](TextDirectionHeuristic.md)! | [RTL](TextDirectionHeuristics.md) Always decides that the direction is right to left. |
| --- | --- |

## Public constructors

### TextDirectionHeuristics

```
TextDirectionHeuristics()
```

## Properties

### ANYRTL_LTR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ANYRTL_LTR: TextDirectionHeuristic!
```

If the text contains any strong right to left non-format character, determines that the direction is right to left, falling back to left to right if it finds none. 

### FIRSTSTRONG_LTR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIRSTSTRONG_LTR: TextDirectionHeuristic!
```

Determines the direction based on the first strong directional character, including bidi format chars, falling back to left to right if it finds none. This is the default behavior of the Unicode Bidirectional Algorithm. 

### FIRSTSTRONG_RTL

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIRSTSTRONG_RTL: TextDirectionHeuristic!
```

Determines the direction based on the first strong directional character, including bidi format chars, falling back to right to left if it finds none. This is similar to the default behavior of the Unicode Bidirectional Algorithm, just with different fallback behavior. 

### LOCALE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCALE: TextDirectionHeuristic!
```

Force the paragraph direction to the Locale direction. Falls back to left to right. 

### LTR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LTR: TextDirectionHeuristic!
```

Always decides that the direction is left to right. 

### RTL

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTL: TextDirectionHeuristic!
```

Always decides that the direction is right to left.
