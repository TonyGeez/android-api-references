# TetheringManager.TetheringEventCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TetheringEventCallback

Kotlin | [Java](https://developer.android.com/reference/android/net/TetheringManager.TetheringEventCallback "View this page in Java") 

```
interface TetheringEventCallback
```

| [android.net.TetheringManager.TetheringEventCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringEventCallback#) |

Callback for use with registerTetheringEventCallback to find out tethering upstream status.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTetheredInterfacesChanged](https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringEventCallback#onTetheredInterfacesChanged(kotlin.collections.MutableSet))`(`interfaces:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [TetheringInterface](https://developer.android.com/reference/kotlin/android/net/TetheringInterface)!>`)` Called when there was a change in the list of tethered interfaces. |

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
| `interfaces` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TetheringInterface](https://developer.android.com/reference/kotlin/android/net/TetheringInterface)!\>: The set of 0 or more TetheringInterface of currently tethered interface. This value cannot be `null`. |
