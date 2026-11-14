# GnssAntennaInfo.Listener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Listener

Kotlin| [Java](../android/location/GnssAntennaInfo.Listener.md) 
| --- | --- |

```
interface Listener
```

| [android.location.GnssAntennaInfo.Listener](../android/location/GnssAntennaInfo.Listener.md) |

Used for receiving GNSS antenna info from the GNSS engine.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGnssAntennaInfoReceived](../android/location/GnssAntennaInfo.Listener.md))`(`gnssAntennaInfos:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [GnssAntennaInfo](GnssAntennaInfo.md)!>`)` Invoked on a change to GNSS antenna info. |

## Public methods

### onGnssAntennaInfoReceived

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGnssAntennaInfoReceived(gnssAntennaInfos: MutableList<GnssAntennaInfo!>): Unit
```

Invoked on a change to GNSS antenna info.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gnssAntennaInfos` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GnssAntennaInfo](GnssAntennaInfo.md)!\>:This value cannot be`null`. |
