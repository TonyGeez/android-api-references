# SpanWatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpanWatcher

Kotlin| [Java](https://developer.android.com/reference/android/text/SpanWatcher "View this page in Java") 
| --- | --- |

```
interface SpanWatcher : NoCopySpan
```

| [android.text.SpanWatcher](https://developer.android.com/reference/kotlin/android/text/SpanWatcher#) |

| Known Direct Subclasses [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener), [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener) | This is the standard key listener for alphabetic input on 12-key keyboards. | | [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener) | This is the key listener for typing normal text. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

When an object of this type is attached to a Spannable, its methods will be called to notify it that other markup objects have been added, changed, or removed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpanAdded](https://developer.android.com/reference/kotlin/android/text/SpanWatcher#onSpanAdded(android.text.Spannable,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to notify you that the specified object has been attached to the specified range of the text. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpanChanged](https://developer.android.com/reference/kotlin/android/text/SpanWatcher#onSpanChanged(android.text.Spannable,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `ostart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nstart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to notify you that the specified object has been relocated from the range`ostart...oend`to the new range`nstart...nend`of the text. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpanRemoved](https://developer.android.com/reference/kotlin/android/text/SpanWatcher#onSpanRemoved(android.text.Spannable,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to notify you that the specified object has been detached from the specified range of the text. |
| --- | --- |

## Public methods

### onSpanAdded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSpanAdded(
    text: Spannable!, 
    what: Any!, 
    start: Int, 
    end: Int
): Unit
```

This method is called to notify you that the specified object has been attached to the specified range of the text. 

### onSpanChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSpanChanged(
    text: Spannable!, 
    what: Any!, 
    ostart: Int, 
    oend: Int, 
    nstart: Int, 
    nend: Int
): Unit
```

This method is called to notify you that the specified object has been relocated from the range`ostart...oend`to the new range`nstart...nend`of the text. 

### onSpanRemoved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSpanRemoved(
    text: Spannable!, 
    what: Any!, 
    start: Int, 
    end: Int
): Unit
```

This method is called to notify you that the specified object has been detached from the specified range of the text.
