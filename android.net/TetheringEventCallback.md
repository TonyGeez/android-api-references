# TetheringManager.TetheringEventCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TetheringEventCallback

Kotlin | [Java](../android/net/TetheringManager.TetheringEventCallback.md) 
| --- | --- |

```
interface TetheringEventCallback
```

| [android.net.TetheringManager.TetheringEventCallback](../android/net/TetheringManager.TetheringEventCallback.md) |

Callback for use with registerTetheringEventCallback to find out tethering upstream status.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTetheredInterfacesChanged](../android/net/TetheringManager.TetheringEventCallback.md))`(`interfaces:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [TetheringInterface](../android/net/TetheringInterface.md)!>`)` Called when there was a change in the list of tethered interfaces. |

## Public methods

### onTetheredInterfacesChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTetheredInterfacesChanged(interfaces: MutableSet<TetheringInterface!>): Unit
```

Called when there was a change in the list of tethered interfaces.

This will be called immediately after the callback is registered, and may be called multiple times later upon changes.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `interfaces` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TetheringInterface](../android/net/TetheringInterface.md)!\>: The set of 0 or more TetheringInterface of currently tethered interface. This value cannot be `null`. |
