# WifiP2pManager.ActionListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActionListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.ActionListener.md) 
| --- | --- |

```
interface ActionListener
```

| [android.net.wifi.p2p.WifiP2pManager.ActionListener](../android/net/wifi/p2p/WifiP2pManager.ActionListener.md) |

Interface for callback invocation on an application action

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](../android/net/wifi/p2p/WifiP2pManager.ActionListener.md))`(`reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The operation failed |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](../android/net/wifi/p2p/WifiP2pManager.ActionListener.md))`()` The operation succeeded |

## Public methods

### onFailure

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFailure(reason: Int): Unit
```

The operation failed

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The reason for failure could be one of [P2P_UNSUPPORTED](WifiP2pManager.md), [ERROR](WifiP2pManager.md) or [BUSY](WifiP2pManager.md) |

### onSuccess

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(): Unit
```

The operation succeeded
