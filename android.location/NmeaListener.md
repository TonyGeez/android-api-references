# GpsStatus.NmeaListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NmeaListener

Kotlin| [Java](../android/location/GpsStatus.NmeaListener.md) 
| --- | --- |

```
interface NmeaListener
```

| [android.location.GpsStatus.NmeaListener](../android/location/GpsStatus.NmeaListener.md) |

| **This interface was deprecated in API level 24.**
|
| use [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md) instead.

Used for receiving NMEA sentences from the GPS. NMEA 0183 is a standard for communicating with marine electronic devices and is a common method for receiving data from a GPS, typically over a serial port. See [NMEA 0183](http://en.wikipedia.org/wiki/NMEA_0183) for more details. You can implement this interface and call android.location.LocationManager#addNmeaListener to receive NMEA data from the GPS engine.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNmeaReceived](../android/location/GpsStatus.NmeaListener.md))`(`timestamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `nmea:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public methods

### onNmeaReceived

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNmeaReceived(
    timestamp: Long, 
    nmea: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*
