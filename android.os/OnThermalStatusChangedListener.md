Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnThermalStatusChangedListener

```
interface OnThermalStatusChangedListener
```

| [android.os.PowerManager.OnThermalStatusChangedListener](https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalStatusChangedListener#) |

Listener passed to android.os.PowerManager#addThermalStatusListener and `https://developer.android.com/reference/kotlin/android/os/PowerManager#removeThermalStatusListener(android.os.PowerManager.OnThermalStatusChangedListener)` to notify caller of thermal status has changed.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalStatusChangedListener#onThermalStatusChanged(kotlin.Int)(status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when overall thermal throttling status changed. |

## Public methods

### onThermalStatusChanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onThermalStatusChanged(status: Int): Unit
```

Called when overall thermal throttling status changed.

| Parameters ||
|---|---|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the status |
