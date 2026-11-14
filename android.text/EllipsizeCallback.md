# TextUtils.EllipsizeCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EllipsizeCallback

Kotlin| [Java](../android/text/TextUtils.EllipsizeCallback.md) 
| --- | --- |

```
interface EllipsizeCallback
```

| [android.text.TextUtils.EllipsizeCallback](../android/text/TextUtils.EllipsizeCallback.md) |

| Known Direct Subclasses [BoringLayout](BoringLayout.md) |------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [BoringLayout](BoringLayout.md) | A BoringLayout is a very simple Layout implementation for text that fits on a single line and is all left-to-right characters. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ellipsized](../android/text/TextUtils.EllipsizeCallback.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to report that the specified region of text was ellipsized away by a call to #ellipsize. |

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
