# SliceMetrics

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SliceMetrics

Kotlin | [Java](https://developer.android.com/reference/android/app/slice/SliceMetrics "View this page in Java") 
| --- | --- |

```
open class SliceMetrics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.slice.SliceMetrics](https://developer.android.com/reference/kotlin/android/app/slice/SliceMetrics#) |

| **This class was deprecated in API level 35.**
|
| Slice framework has been deprecated, it will not receive any updates from android.os.Build.VANILLA_ICE_CREAM and forward. If you are looking for a framework that sends displayable data from one app to another, consider using [android.app.appsearch.AppSearchManager](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#).

Metrics interface for slices. This is called by SliceView, so Slice developers should not need to reference this class.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SliceMetrics](https://developer.android.com/reference/kotlin/android/app/slice/SliceMetrics#SliceMetrics(android.content.Context,%20android.net.Uri))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` An object to be used throughout the life of a slice to register events. |

| Public methods ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logHidden](https://developer.android.com/reference/kotlin/android/app/slice/SliceMetrics#logHidden())`()` To be called whenever the slice becomes invisible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logTouch](https://developer.android.com/reference/kotlin/android/app/slice/SliceMetrics#logTouch(kotlin.Int,%20android.net.Uri))`(`actionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subSlice:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` To be called whenever the user invokes a discrete action via a slice. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logVisible](https://developer.android.com/reference/kotlin/android/app/slice/SliceMetrics#logVisible())`()` To be called whenever the slice becomes visible to the user. |
| --- | --- |

## Public constructors

### SliceMetrics

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SliceMetrics(
    context: Context, 
    uri: Uri)
```

An object to be used throughout the life of a slice to register events.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |

## Public methods

### logHidden

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logHidden(): Unit
```

**Deprecated:** *Deprecated in Java.*

To be called whenever the slice becomes invisible to the user. 

### logTouch

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logTouch(
    actionType: Int, 
    subSlice: Uri
): Unit
```

**Deprecated:** *Deprecated in Java.*

To be called whenever the user invokes a discrete action via a slice.

Use this for discrete events like a tap or the end of a drag, not for a continuous streams of events, such as the motion during a gesture.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `actionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of the event. |
| `subSlice` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The URI of the sub-slice that is the subject of the interaction. This value cannot be `null`. |

**See Also**

### logVisible

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logVisible(): Unit
```

**Deprecated:** *Deprecated in Java.*

To be called whenever the slice becomes visible to the user.
