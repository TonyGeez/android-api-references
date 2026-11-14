# VirtualDisplayConfig.BrightnessListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BrightnessListener

Kotlin| [Java](../android/hardware/display/VirtualDisplayConfig.BrightnessListener.md) 
| --- | --- |

```
interface BrightnessListener
```

| [android.hardware.display.VirtualDisplayConfig.BrightnessListener](../android/hardware/display/VirtualDisplayConfig.BrightnessListener.md) |

Listener for display brightness changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBrightnessChanged](../android/hardware/display/VirtualDisplayConfig.BrightnessListener.md))`(`brightness:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Called when the display's brightness has changed. |

## Public methods

### onBrightnessChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBrightnessChanged(brightness: Float): Unit
```

Called when the display's brightness has changed.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `brightness` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the new brightness of the display. Value of`0.0`indicates the minimum supported brightness and value of`1.0`indicates the maximum supported brightness. Value is between 0.0f and 1.0f inclusive |
