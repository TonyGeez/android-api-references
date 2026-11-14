# RangingManager.RangingCapabilitiesCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingCapabilitiesCallback

Kotlin| [Java](https://developer.android.com/reference/android/ranging/RangingManager.RangingCapabilitiesCallback "View this page in Java") 

```
interface RangingCapabilitiesCallback
```

| [android.ranging.RangingManager.RangingCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback#) |

Callback interface to receive the availabilities and capabilities of all the ranging technology supported by the device.

This interface is used to asynchronously provide information about the supported ranging capabilities of the device. The callback is invoked first time when registered and if any capabilities are updated until it is unregistered.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback#onRangingCapabilities(android.ranging.RangingCapabilities))`(`capabilities:` ` [RangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities)`)` Called when the ranging capabilities are available. |

## Public methods

### onRangingCapabilities

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRangingCapabilities(capabilities: RangingCapabilities): Unit
```

Called when the ranging capabilities are available.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capabilities` | [RangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities):the [RangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities) object containing detailed information about the supported features and limitations of the ranging technology. This value cannot be`null`. |
