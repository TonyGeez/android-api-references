# AttachCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttachCallback

Kotlin| [Java](AttachCallback.md) 
| --- | --- |

```
open class AttachCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.AttachCallback](AttachCallback.md) |

Base class for Aware attach callbacks. Should be extended by applications and set when calling [WifiAwareManager.attach(AttachCallback, android.os.Handler)](WifiAwareManager.md)). These are callbacks applying to the Aware connection as a whole - not to specific publish or subscribe sessions - for that see [DiscoverySessionCallback](DiscoverySessionCallback.md).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------|---|
| [AttachCallback](AttachCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachFailed](AttachCallback.md))`()` Called when Aware attach operation [WifiAwareManager.attach(AttachCallback, android.os.Handler)](WifiAwareManager.md))failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttached](AttachCallback.md))`(`session:` ` [WifiAwareSession](WifiAwareSession.md)!`)` Called when Aware attach operation [WifiAwareManager.attach(AttachCallback, android.os.Handler)](WifiAwareManager.md))is completed and that we can now start discovery sessions or connections. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAwareSessionTerminated](AttachCallback.md))`()` Called when Aware attach session get from [onAttached(android.net.wifi.aware.WifiAwareSession)](AttachCallback.md))is terminated. |
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

Called when Aware attach operation [WifiAwareManager.attach(AttachCallback, android.os.Handler)](WifiAwareManager.md))failed. 

### onAttached

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttached(session: WifiAwareSession!): Unit
```

Called when Aware attach operation [WifiAwareManager.attach(AttachCallback, android.os.Handler)](WifiAwareManager.md))is completed and that we can now start discovery sessions or connections.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [WifiAwareSession](WifiAwareSession.md)!:The Aware object on which we can execute further Aware operations - e.g. discovery, connections. |

### onAwareSessionTerminated

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAwareSessionTerminated(): Unit
```

Called when Aware attach session get from [onAttached(android.net.wifi.aware.WifiAwareSession)](AttachCallback.md))is terminated. Use [WifiAwareManager.attach(AttachCallback, Handler)](WifiAwareManager.md))or [WifiAwareManager.attach(AttachCallback, IdentityChangedListener, Handler)](WifiAwareManager.md))to get a new active session.
