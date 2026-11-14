# SEService.OnConnectedListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnConnectedListener

Kotlin| [Java](https://developer.android.com/reference/android/se/omapi/SEService.OnConnectedListener "View this page in Java") 
| --- | --- |

```
interface OnConnectedListener
```

| [android.se.omapi.SEService.OnConnectedListener](https://developer.android.com/reference/kotlin/android/se/omapi/SEService.OnConnectedListener#) |

Interface to send call-backs to the application when the service is connected.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnected](https://developer.android.com/reference/kotlin/android/se/omapi/SEService.OnConnectedListener#onConnected())`()` Called by the framework when the service is connected. |

## Public methods

### onConnected

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnected(): Unit
```

Called by the framework when the service is connected.
