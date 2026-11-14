# AudioTrack.OnRoutingChangedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnRoutingChangedListener

Kotlin| [Java](../android/media/AudioTrack.OnRoutingChangedListener.md) 
| --- | --- |

```
interface OnRoutingChangedListener : AudioRouting.OnRoutingChangedListener
```

| [android.media.AudioTrack.OnRoutingChangedListener](../android/media/AudioTrack.OnRoutingChangedListener.md) |

| **This interface was deprecated in API level 24.**
|
| users should switch to the general purpose [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) class instead.

Defines the interface by which applications can receive notifications of routing changes for the associated [AudioTrack](AudioTrack.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRoutingChanged](../android/media/AudioTrack.OnRoutingChangedListener.md))`(`router:` ` [AudioRouting](AudioRouting.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRoutingChanged](../android/media/AudioTrack.OnRoutingChangedListener.md))`(`audioTrack:` ` [AudioTrack](AudioTrack.md)!`)` Called when the routing of an AudioTrack changes from either and explicit or policy rerouting. |

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

Called when the routing of an AudioTrack changes from either and explicit or policy rerouting. Use [getRoutedDevice()](AudioTrack.md))to retrieve the newly routed-to device.
