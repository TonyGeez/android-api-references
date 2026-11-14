# GpsSatellite

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GpsSatellite

Kotlin| [Java](../android/location/GpsSatellite.md) 
| --- | --- |

```
class GpsSatellite
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.GpsSatellite](../android/location/GpsSatellite.md) |

| **This class was deprecated in API level 24.**
|
| use [GnssStatus](../android/location/GnssStatus.md) and [GnssStatus.Callback](../android/location/GnssStatus.Callback.md).

This class represents the current state of a GPS satellite. This class is used in conjunction with the [GpsStatus](../android/location/GpsStatus.md) class.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAzimuth](../android/location/GpsSatellite.md))`()` Returns the azimuth of the satellite in degrees. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getElevation](../android/location/GpsSatellite.md))`()` Returns the elevation of the satellite in degrees. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrn](../android/location/GpsSatellite.md))`()` Returns the PRN (pseudo-random number) for the satellite. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSnr](../android/location/GpsSatellite.md))`()` Returns the signal to noise ratio for the satellite. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlmanac](../android/location/GpsSatellite.md))`()` Returns true if the GPS engine has almanac data for the satellite. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasEphemeris](../android/location/GpsSatellite.md))`()` Returns true if the GPS engine has ephemeris data for the satellite. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [usedInFix](../android/location/GpsSatellite.md))`()` Returns true if the satellite was used by the GPS engine when calculating the most recent GPS fix. |

## Public methods

### getAzimuth

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAzimuth(): Float
```

**Deprecated:** *Deprecated in Java.*

Returns the azimuth of the satellite in degrees. The azimuth can vary between 0 and 360.

| Return ||
|--------------------------------------------------------------------------------|------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the azimuth in degrees |

### getElevation

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getElevation(): Float
```

**Deprecated:** *Deprecated in Java.*

Returns the elevation of the satellite in degrees. The elevation can vary between 0 and 90.

| Return ||
|--------------------------------------------------------------------------------|--------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the elevation in degrees |

### getPrn

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrn(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the PRN (pseudo-random number) for the satellite.

| Return ||
|----------------------------------------------------------------------------|------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | PRN number |

### getSnr

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSnr(): Float
```

**Deprecated:** *Deprecated in Java.*

Returns the signal to noise ratio for the satellite.

| Return ||
|--------------------------------------------------------------------------------|---------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the signal to noise ratio |

### hasAlmanac

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasAlmanac(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the GPS engine has almanac data for the satellite.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the satellite has almanac data |

### hasEphemeris

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasEphemeris(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the GPS engine has ephemeris data for the satellite.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the satellite has ephemeris data |

### usedInFix

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun usedInFix(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the satellite was used by the GPS engine when calculating the most recent GPS fix.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the satellite was used to compute the most recent fix. |
