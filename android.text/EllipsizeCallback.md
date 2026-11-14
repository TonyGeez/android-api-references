# TextUtils.EllipsizeCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EllipsizeCallback

Kotlin| [Java](https://developer.android.com/reference/android/text/TextUtils.EllipsizeCallback "View this page in Java") 

```
interface EllipsizeCallback
```

| [android.text.TextUtils.EllipsizeCallback](https://developer.android.com/reference/kotlin/android/text/TextUtils.EllipsizeCallback#) |

| Known Direct Subclasses [BoringLayout](https://developer.android.com/reference/kotlin/android/text/BoringLayout) |------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [BoringLayout](https://developer.android.com/reference/kotlin/android/text/BoringLayout) | A BoringLayout is a very simple Layout implementation for text that fits on a single line and is all left-to-right characters. | |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ellipsized](https://developer.android.com/reference/kotlin/android/text/TextUtils.EllipsizeCallback#ellipsized(kotlin.Int,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to report that the specified region of text was ellipsized away by a call to #ellipsize. |

## Public methods

### ellipsized

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ellipsized(
    start: Int, 
    end: Int
): Unit
```

This method is called to report that the specified region of text was ellipsized away by a call to #ellipsize.
