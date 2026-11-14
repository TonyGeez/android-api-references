# SliceMetrics

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SliceMetrics

Kotlin | [Java](SliceMetrics.md) 
| --- | --- |

```
open class SliceMetrics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.slice.SliceMetrics](SliceMetrics.md) |

| **This class was deprecated in API level 35.**
|
| Slice framework has been deprecated, it will not receive any updates from android.os.Build.VANILLA_ICE_CREAM and forward. If you are looking for a framework that sends displayable data from one app to another, consider using [android.app.appsearch.AppSearchManager](../android.app.appsearch/AppSearchManager.md).

Metrics interface for slices. This is called by SliceView, so Slice developers should not need to reference this class.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SliceMetrics](SliceMetrics.md))`(`context:` ` [Context](../android.content/Context.md)`, `uri:` ` [Uri](../android.net/Uri.md)`)` An object to be used throughout the life of a slice to register events. |

| Public methods ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logHidden](SliceMetrics.md))`()` To be called whenever the slice becomes invisible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logTouch](SliceMetrics.md))`(`actionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subSlice:` ` [Uri](../android.net/Uri.md)`)` To be called whenever the user invokes a discrete action via a slice. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [logVisible](SliceMetrics.md))`()` To be called whenever the slice becomes visible to the user. |
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
| `context` | [Context](../android.content/Context.md): This value cannot be `null`. |
| `uri` | [Uri](../android.net/Uri.md): This value cannot be `null`. |

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
| `subSlice` | [Uri](../android.net/Uri.md): The URI of the sub-slice that is the subject of the interaction. This value cannot be `null`. |

**See Also**

### logVisible

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun logVisible(): Unit
```

**Deprecated:** *Deprecated in Java.*

To be called whenever the slice becomes visible to the user.
