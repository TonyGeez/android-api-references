# AudioRecord.OnRecordPositionUpdateListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnRecordPositionUpdateListener

Kotlin| [Java](../android/media/AudioRecord.OnRecordPositionUpdateListener.md) 
| --- | --- |

```
interface OnRecordPositionUpdateListener
```

| [android.media.AudioRecord.OnRecordPositionUpdateListener](../android/media/AudioRecord.OnRecordPositionUpdateListener.md) |

Interface definition for a callback to be invoked when an AudioRecord has reached a notification marker set by [AudioRecord.setNotificationMarkerPosition(int)](../android/media/AudioRecord.md))or for periodic updates on the progress of the record head, as set by [AudioRecord.setPositionNotificationPeriod(int)](../android/media/AudioRecord.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMarkerReached](../android/media/AudioRecord.OnRecordPositionUpdateListener.md))`(`recorder:` ` [AudioRecord](../android/media/AudioRecord.md)!`)` Called on the listener to notify it that the previously set marker has been reached by the recording head. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicNotification](../android/media/AudioRecord.OnRecordPositionUpdateListener.md))`(`recorder:` ` [AudioRecord](../android/media/AudioRecord.md)!`)` Called on the listener to periodically notify it that the record head has reached a multiple of the notification period. |

## Public methods

### onMarkerReached

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMarkerReached(recorder: AudioRecord!): Unit
```

Called on the listener to notify it that the previously set marker has been reached by the recording head. 

### onPeriodicNotification

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPeriodicNotification(recorder: AudioRecord!): Unit
```

Called on the listener to periodically notify it that the record head has reached a multiple of the notification period.
