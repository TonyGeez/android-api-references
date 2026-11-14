# RemoteControlClient.OnMetadataUpdateListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnMetadataUpdateListener

Kotlin| [Java](https://developer.android.com/reference/android/media/RemoteControlClient.OnMetadataUpdateListener "View this page in Java") 
| --- | --- |

```
interface OnMetadataUpdateListener
```

| [android.media.RemoteControlClient.OnMetadataUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnMetadataUpdateListener#) |

| **This interface was deprecated in API level 29.**
|
| Deprecated in Java.

Interface definition for a callback to be invoked when one of the metadata values has been updated. Implement this interface to receive metadata updates after registering your listener through [RemoteControlClient.setMetadataUpdateListener(OnMetadataUpdateListener)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setMetadataUpdateListener(android.media.RemoteControlClient.OnMetadataUpdateListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMetadataUpdate](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnMetadataUpdateListener#onMetadataUpdate(kotlin.Int,%20kotlin.Any))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Called on the implementer to notify that the metadata field for the given key has been updated to the new value. |

## Public methods

### onMetadataUpdate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMetadataUpdate(
    key: Int, 
    newValue: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called on the implementer to notify that the metadata field for the given key has been updated to the new value.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identifier of the updated metadata field. |
| `newValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the Object storing the new value for the key. |
