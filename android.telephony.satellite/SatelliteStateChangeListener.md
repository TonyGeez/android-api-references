# SatelliteStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SatelliteStateChangeListener

Kotlin| [Java](SatelliteStateChangeListener.md) 
| --- | --- |

```
interface SatelliteStateChangeListener
```

| [android.telephony.satellite.SatelliteStateChangeListener](SatelliteStateChangeListener.md) |

A listener interface to monitor satellite state change events.

Call [SatelliteManager.registerStateChangeListener(Executor, SatelliteStateChangeListener)](SatelliteManager.md))to monitor. Call [SatelliteManager.unregisterStateChangeListener(SatelliteStateChangeListener)](SatelliteManager.md))to cancel.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEnabledStateChanged](SatelliteStateChangeListener.md))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when satellite modem enabled state may have changed. |

## Public methods

### onEnabledStateChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEnabledStateChanged(isEnabled: Boolean): Unit
```

Called when satellite modem enabled state may have changed.

Note:there is no guarantee that this callback will only be invoked upon a change of state. In other word, in some cases, the callback may report with the same enabled states. It is the caller's responsibility to filter uninterested states.

Note:satellite enabled state is a device state that is NOT associated with subscription or SIM slot.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `isEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`means satellite modem is enabled. |
