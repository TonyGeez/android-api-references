# GpsStatus

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GpsStatus

Kotlin| [Java](../android/location/GpsStatus.md) 
| --- | --- |

```
class GpsStatus
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.GpsStatus](../android/location/GpsStatus.md) |

| **This class was deprecated in API level 24.**
|
| Use [GnssStatus](../android/location/GnssStatus.md) instead.

This class represents the current state of the GPS engine and is used in conjunction with [GpsStatus.Listener](../android/location/GpsStatus.Listener.md).

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Listener](../android/location/GpsStatus.Listener.md) Used for receiving notifications when GPS status has changed. |
| abstract | [NmeaListener](../android/location/GpsStatus.NmeaListener.md) Used for receiving NMEA sentences from the GPS. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPS_EVENT_FIRST_FIX](../android/location/GpsStatus.md) Event sent when the GPS system has received its first fix since starting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPS_EVENT_SATELLITE_STATUS](../android/location/GpsStatus.md) Event sent periodically to report GPS satellite status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPS_EVENT_STARTED](../android/location/GpsStatus.md) Event sent when the GPS system has started. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPS_EVENT_STOPPED](../android/location/GpsStatus.md) Event sent when the GPS system has stopped. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [GpsStatus](../android/location/GpsStatus.md) | [create](../android/location/GpsStatus.md))`(`gnssStatus:` ` [GnssStatus](../android/location/GnssStatus.md)`, `timeToFirstFix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Builds a GpsStatus from the given GnssStatus. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSatellites](../android/location/GpsStatus.md))`()` Returns the maximum number of satellites that can be in the satellite list that can be returned by [getSatellites()](../android/location/GpsStatus.md)). |
| [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\< [GpsSatellite](../android/location/GpsSatellite.md)!\>! | [getSatellites](../android/location/GpsStatus.md))`()` Returns an array of [GpsSatellite](../android/location/GpsSatellite.md) objects, which represent the current state of the GPS engine. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeToFirstFix](../android/location/GpsStatus.md))`()` Returns the time required to receive the first fix since the most recent restart of the GPS engine. |

## Constants

### GPS_EVENT_FIRST_FIX

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPS_EVENT_FIRST_FIX: Int
```

**Deprecated:** *Deprecated in Java.*

Event sent when the GPS system has received its first fix since starting. Call [getTimeToFirstFix()](../android/location/GpsStatus.md))to find the time from start to first fix. 

 Value: 3

### GPS_EVENT_SATELLITE_STATUS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPS_EVENT_SATELLITE_STATUS: Int
```

**Deprecated:** *Deprecated in Java.*

Event sent periodically to report GPS satellite status. Call [getSatellites()](../android/location/GpsStatus.md))to retrieve the status for each satellite. 

 Value: 4

### GPS_EVENT_STARTED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPS_EVENT_STARTED: Int
```

**Deprecated:** *Deprecated in Java.*

Event sent when the GPS system has started. 

 Value: 1

### GPS_EVENT_STOPPED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPS_EVENT_STOPPED: Int
```

**Deprecated:** *Deprecated in Java.*

Event sent when the GPS system has stopped. 

 Value: 2

## Public methods

### create

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    gnssStatus: GnssStatus, 
    timeToFirstFix: Int
): GpsStatus
```

**Deprecated:** *Deprecated in Java.*

Builds a GpsStatus from the given GnssStatus.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------|
| `gnssStatus` | [GnssStatus](../android/location/GnssStatus.md):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [GpsStatus](../android/location/GpsStatus.md) | This value cannot be`null`. |

### getMaxSatellites

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxSatellites(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the maximum number of satellites that can be in the satellite list that can be returned by [getSatellites()](../android/location/GpsStatus.md)).

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of satellites |

### getSatellites

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSatellites(): MutableIterable<GpsSatellite!>!
```

**Deprecated:** *Deprecated in Java.*

Returns an array of [GpsSatellite](../android/location/GpsSatellite.md) objects, which represent the current state of the GPS engine.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)< [GpsSatellite](../android/location/GpsSatellite.md)!>! | the list of satellites |

### getTimeToFirstFix

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeToFirstFix(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the time required to receive the first fix since the most recent restart of the GPS engine.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | time to first fix in milliseconds |
