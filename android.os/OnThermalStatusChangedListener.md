Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnThermalStatusChangedListener

```
interface OnThermalStatusChangedListener
```

| [android.os.PowerManager.OnThermalStatusChangedListener](../android/os/PowerManager.OnThermalStatusChangedListener.md) |

Listener passed to android.os.PowerManager#addThermalStatusListener and removeThermalStatusListener to notify caller of thermal status has changed.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onThermalStatusChanged Called when overall thermal throttling status changed. |

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
