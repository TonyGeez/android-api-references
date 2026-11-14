# SEService.OnConnectedListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnConnectedListener

Kotlin| [Java](../android/se/omapi/SEService.OnConnectedListener.md) 
| --- | --- |

```
interface OnConnectedListener
```

| [android.se.omapi.SEService.OnConnectedListener](../android/se/omapi/SEService.OnConnectedListener.md) |

Interface to send call-backs to the application when the service is connected.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnected](../android/se/omapi/SEService.OnConnectedListener.md))`()` Called by the framework when the service is connected. |

## Public methods

### onConnected

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnected(): Unit
```

Called by the framework when the service is connected.
