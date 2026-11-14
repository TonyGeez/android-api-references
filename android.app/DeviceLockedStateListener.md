# KeyguardManager.DeviceLockedStateListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceLockedStateListener

Kotlin| [Java](../android/app/KeyguardManager.DeviceLockedStateListener.md) 
| --- | --- |

```
@FunctionalInterface interface DeviceLockedStateListener
```

| [android.app.KeyguardManager.DeviceLockedStateListener](../android/app/KeyguardManager.DeviceLockedStateListener.md) |

Listener for device locked state changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeviceLockedStateChanged](../android/app/KeyguardManager.DeviceLockedStateListener.md))`(`isDeviceLocked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback function that executes when the device locked state changes. |

## Public methods

### onDeviceLockedStateChanged

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDeviceLockedStateChanged(isDeviceLocked: Boolean): Unit
```

Callback function that executes when the device locked state changes.
