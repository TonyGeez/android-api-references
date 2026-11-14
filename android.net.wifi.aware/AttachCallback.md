# AttachCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttachCallback

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/aware/AttachCallback "View this page in Java") 
| --- | --- |

```
open class AttachCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback#) |

Base class for Aware attach callbacks. Should be extended by applications and set when calling [WifiAwareManager.attach(AttachCallback, android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler)). These are callbacks applying to the Aware connection as a whole - not to specific publish or subscribe sessions - for that see [DiscoverySessionCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------|---|
| [AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback#AttachCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachFailed](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback#onAttachFailed())`()` Called when Aware attach operation [WifiAwareManager.attach(AttachCallback, android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttached](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback#onAttached(android.net.wifi.aware.WifiAwareSession))`(`session:` ` [WifiAwareSession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession)!`)` Called when Aware attach operation [WifiAwareManager.attach(AttachCallback, android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))is completed and that we can now start discovery sessions or connections. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAwareSessionTerminated](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback#onAwareSessionTerminated())`()` Called when Aware attach session get from [onAttached(android.net.wifi.aware.WifiAwareSession)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback#onAttached(android.net.wifi.aware.WifiAwareSession))is terminated. |
| --- | --- |

## Public constructors

### AttachCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttachCallback()
```

## Public methods

### onAttachFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttachFailed(): Unit
```

Called when Aware attach operation [WifiAwareManager.attach(AttachCallback, android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))failed. 

### onAttached

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttached(session: WifiAwareSession!): Unit
```

Called when Aware attach operation [WifiAwareManager.attach(AttachCallback, android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))is completed and that we can now start discovery sessions or connections.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [WifiAwareSession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession)!:The Aware object on which we can execute further Aware operations - e.g. discovery, connections. |

### onAwareSessionTerminated

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAwareSessionTerminated(): Unit
```

Called when Aware attach session get from [onAttached(android.net.wifi.aware.WifiAwareSession)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback#onAttached(android.net.wifi.aware.WifiAwareSession))is terminated. Use [WifiAwareManager.attach(AttachCallback, Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))or [WifiAwareManager.attach(AttachCallback, IdentityChangedListener, Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.net.wifi.aware.IdentityChangedListener,%20android.os.Handler))to get a new active session.
