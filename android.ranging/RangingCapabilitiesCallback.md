# RangingManager.RangingCapabilitiesCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingCapabilitiesCallback

Kotlin| [Java](../android/ranging/RangingManager.RangingCapabilitiesCallback.md) 
| --- | --- |

```
interface RangingCapabilitiesCallback
```

| [android.ranging.RangingManager.RangingCapabilitiesCallback](../android/ranging/RangingManager.RangingCapabilitiesCallback.md) |

Callback interface to receive the availabilities and capabilities of all the ranging technology supported by the device.

This interface is used to asynchronously provide information about the supported ranging capabilities of the device. The callback is invoked first time when registered and if any capabilities are updated until it is unregistered.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRangingCapabilities](../android/ranging/RangingManager.RangingCapabilitiesCallback.md))`(`capabilities:` ` [RangingCapabilities](RangingCapabilities.md)`)` Called when the ranging capabilities are available. |

## Public methods

### onRangingCapabilities

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRangingCapabilities(capabilities: RangingCapabilities): Unit
```

Called when the ranging capabilities are available.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capabilities` | [RangingCapabilities](RangingCapabilities.md):the [RangingCapabilities](RangingCapabilities.md) object containing detailed information about the supported features and limitations of the ranging technology. This value cannot be`null`. |
