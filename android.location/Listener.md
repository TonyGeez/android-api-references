# GnssAntennaInfo.Listener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Listener

Kotlin| [Java](https://developer.android.com/reference/android/location/GnssAntennaInfo.Listener "View this page in Java") 

```
interface Listener
```

| [android.location.GnssAntennaInfo.Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener#) |

Used for receiving GNSS antenna info from the GNSS engine.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGnssAntennaInfoReceived](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener#onGnssAntennaInfoReceived(kotlin.collections.MutableList))`(`gnssAntennaInfos:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [GnssAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo)!>`)` Invoked on a change to GNSS antenna info. |

## Public methods

### onGnssAntennaInfoReceived

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGnssAntennaInfoReceived(gnssAntennaInfos: MutableList<GnssAntennaInfo!>): Unit
```

Invoked on a change to GNSS antenna info.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gnssAntennaInfos` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GnssAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo)!\>:This value cannot be`null`. |
