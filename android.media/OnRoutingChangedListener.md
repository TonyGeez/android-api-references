# AudioTrack.OnRoutingChangedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnRoutingChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioTrack.OnRoutingChangedListener "View this page in Java") 

```
interface OnRoutingChangedListener : AudioRouting.OnRoutingChangedListener
```

| [android.media.AudioTrack.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener#) |

| **This interface was deprecated in API level 24.**
|
| users should switch to the general purpose [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) class instead.

Defines the interface by which applications can receive notifications of routing changes for the associated [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRoutingChanged](https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener#onRoutingChanged(android.media.AudioRouting))`(`router:` ` [AudioRouting](https://developer.android.com/reference/kotlin/android/media/AudioRouting)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRoutingChanged](https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnRoutingChangedListener#onRoutingChanged(android.media.AudioTrack))`(`audioTrack:` ` [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack)!`)` Called when the routing of an AudioTrack changes from either and explicit or policy rerouting. |

## Public methods

### onRoutingChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRoutingChanged(router: AudioRouting!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### onRoutingChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRoutingChanged(audioTrack: AudioTrack!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the routing of an AudioTrack changes from either and explicit or policy rerouting. Use [getRoutedDevice()](https://developer.android.com/reference/kotlin/android/media/AudioTrack#getRoutedDevice())to retrieve the newly routed-to device.
