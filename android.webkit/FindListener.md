# WebView.FindListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FindListener

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebView.FindListener "View this page in Java") 
| --- | --- |

```
interface FindListener
```

| [android.webkit.WebView.FindListener](https://developer.android.com/reference/kotlin/android/webkit/WebView.FindListener#) |

Interface to listen for find results.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFindResultReceived](https://developer.android.com/reference/kotlin/android/webkit/WebView.FindListener#onFindResultReceived(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`activeMatchOrdinal:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `numberOfMatches:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isDoneCounting:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notifies the listener about progress made by a find operation. |

## Public methods

### onFindResultReceived

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFindResultReceived(
    activeMatchOrdinal: Int, 
    numberOfMatches: Int, 
    isDoneCounting: Boolean
): Unit
```

Notifies the listener about progress made by a find operation.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activeMatchOrdinal` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based ordinal of the currently selected match |
| `numberOfMatches` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):how many matches have been found |
| `isDoneCounting` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the find operation has actually completed. The listener may be notified multiple times while the operation is underway, and the numberOfMatches value should not be considered final unless isDoneCounting is`true`. |
| --- | --- |
