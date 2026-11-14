# WifiP2pManager.ActionListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActionListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.ActionListener "View this page in Java") 
| --- | --- |

```
interface ActionListener
```

| [android.net.wifi.p2p.WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#) |

Interface for callback invocation on an application action

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int))`(`reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The operation failed |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess())`()` The operation succeeded |

## Public methods

### onFailure

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFailure(reason: Int): Unit
```

The operation failed

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The reason for failure could be one of [P2P_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#P2P_UNSUPPORTED:kotlin.Int), [ERROR](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ERROR:kotlin.Int) or [BUSY](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#BUSY:kotlin.Int) |

### onSuccess

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(): Unit
```

The operation succeeded
