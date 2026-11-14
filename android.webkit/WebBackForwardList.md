# WebBackForwardList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebBackForwardList

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebBackForwardList "View this page in Java") 
| --- | --- |

```
abstract class WebBackForwardList : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebBackForwardList](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#) |

This class contains the back/forward list for a WebView. WebView.copyBackForwardList() will return a copy of this class used to inspect the entries in the list.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------|---|
| [WebBackForwardList](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#WebBackForwardList())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentIndex](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#getCurrentIndex())`()` Get the index of the current history item. |
| abstract [WebHistoryItem](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem)? | [getCurrentItem](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#getCurrentItem())`()` Return the current history item. |
| abstract [WebHistoryItem](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem)! | [getItemAtIndex](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#getItemAtIndex(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the history item at the given index. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#getSize())`()` Get the total size of the back/forward list. |

| Protected methods ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [WebBackForwardList](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#) | [clone](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#clone())`()` Clone the entire object to be used in the UI thread by clients of WebView. |

## Public constructors

### WebBackForwardList

```
WebBackForwardList()
```

## Public methods

### getCurrentIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCurrentIndex(): Int
```

Get the index of the current history item. This index can be used to directly index into the array list.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current index from 0...n or -1 if the list is empty. |

### getCurrentItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCurrentItem(): WebHistoryItem?
```

Return the current history item. This method returns`null`if the list is empty.

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------|
| [WebHistoryItem](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem)? | The current history item. |

### getItemAtIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getItemAtIndex(index: Int): WebHistoryItem!
```

Get the history item at the given index. The index range is from 0...n where 0 is the first item and n is the last item.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index to retrieve. |

### getSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSize(): Int
```

Get the total size of the back/forward list.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The size of the list. |

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun clone(): WebBackForwardList
```

Clone the entire object to be used in the UI thread by clients of WebView. This creates a copy that should never be modified by any of the webkit package classes. On Android 4.4 and later there is no need to use this, as the object is already a read-only copy of the internal state.

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------|
| [WebBackForwardList](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList#) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
