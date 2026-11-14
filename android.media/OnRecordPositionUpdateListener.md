# AudioRecord.OnRecordPositionUpdateListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnRecordPositionUpdateListener

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioRecord.OnRecordPositionUpdateListener "View this page in Java") 
| --- | --- |

```
interface OnRecordPositionUpdateListener
```

| [android.media.AudioRecord.OnRecordPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRecordPositionUpdateListener#) |

Interface definition for a callback to be invoked when an AudioRecord has reached a notification marker set by [AudioRecord.setNotificationMarkerPosition(int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setNotificationMarkerPosition(kotlin.Int))or for periodic updates on the progress of the record head, as set by [AudioRecord.setPositionNotificationPeriod(int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#setPositionNotificationPeriod(kotlin.Int)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMarkerReached](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRecordPositionUpdateListener#onMarkerReached(android.media.AudioRecord))`(`recorder:` ` [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord)!`)` Called on the listener to notify it that the previously set marker has been reached by the recording head. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicNotification](https://developer.android.com/reference/kotlin/android/media/AudioRecord.OnRecordPositionUpdateListener#onPeriodicNotification(android.media.AudioRecord))`(`recorder:` ` [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord)!`)` Called on the listener to periodically notify it that the record head has reached a multiple of the notification period. |

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
