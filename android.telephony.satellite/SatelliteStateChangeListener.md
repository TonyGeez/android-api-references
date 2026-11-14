# SatelliteStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SatelliteStateChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/satellite/SatelliteStateChangeListener "View this page in Java") 
| --- | --- |

```
interface SatelliteStateChangeListener
```

| [android.telephony.satellite.SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener#) |

A listener interface to monitor satellite state change events.

Call [SatelliteManager.registerStateChangeListener(Executor, SatelliteStateChangeListener)](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager#registerStateChangeListener(java.util.concurrent.Executor,%20android.telephony.satellite.SatelliteStateChangeListener))to monitor. Call [SatelliteManager.unregisterStateChangeListener(SatelliteStateChangeListener)](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager#unregisterStateChangeListener(android.telephony.satellite.SatelliteStateChangeListener))to cancel.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEnabledStateChanged](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener#onEnabledStateChanged(kotlin.Boolean))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when satellite modem enabled state may have changed. |

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
