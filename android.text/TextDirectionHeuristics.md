# TextDirectionHeuristics

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextDirectionHeuristics

Kotlin| [Java](https://developer.android.com/reference/android/text/TextDirectionHeuristics "View this page in Java") 
| --- | --- |

```
open class TextDirectionHeuristics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.TextDirectionHeuristics](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#) |

Some objects that implement [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic). Use these with the android.text.BidiFormatter#unicodeWrap methods in [BidiFormatter](https://developer.android.com/reference/kotlin/android/text/BidiFormatter). Also notice that these direction heuristics correspond to the same types of constants provided in the [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) class for [setTextDirection()](https://developer.android.com/reference/kotlin/android/view/View.html#setTextDirection(kotlin.Int)), such as [android.view.View#TEXT_DIRECTION_RTL](https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_RTL:kotlin.Int).

To support versions lower than [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), you can use the support library's androidx.core.text.TextDirectionHeuristicsCompat class.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextDirectionHeuristics](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#TextDirectionHeuristics())`()` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)! | [ANYRTL_LTR](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#ANYRTL_LTR:android.text.TextDirectionHeuristic) If the text contains any strong right to left non-format character, determines that the direction is right to left, falling back to left to right if it finds none. |
| static [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)! | [FIRSTSTRONG_LTR](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#FIRSTSTRONG_LTR:android.text.TextDirectionHeuristic) Determines the direction based on the first strong directional character, including bidi format chars, falling back to left to right if it finds none. |
| static [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)! | [FIRSTSTRONG_RTL](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#FIRSTSTRONG_RTL:android.text.TextDirectionHeuristic) Determines the direction based on the first strong directional character, including bidi format chars, falling back to right to left if it finds none. |
| --- | --- |
| static [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)! | [LOCALE](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#LOCALE:android.text.TextDirectionHeuristic) Force the paragraph direction to the Locale direction. |
| static [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)! | [LTR](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#LTR:android.text.TextDirectionHeuristic) Always decides that the direction is left to right. |
| static [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)! | [RTL](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#RTL:android.text.TextDirectionHeuristic) Always decides that the direction is right to left. |
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
