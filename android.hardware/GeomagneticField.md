# GeomagneticField

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GeomagneticField

Kotlin| [Java](https://developer.android.com/reference/android/hardware/GeomagneticField "View this page in Java") 

```
open class GeomagneticField
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.GeomagneticField](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#) |

Estimates magnetic field at a given point on Earth, and in particular, to compute the magnetic declination from true north.

This uses the World Magnetic Model produced by the United States National Geospatial-Intelligence Agency. More details about the model can be found at<http://www.ngdc.noaa.gov/geomag/WMM/DoDWMM.shtml>. This class currently uses WMM-2020 which is valid until 2025, but should produce acceptable results for several years after that. Future versions of Android may use a newer version of the model.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GeomagneticField](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#GeomagneticField(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Long))`(`gdLatitudeDeg:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `gdLongitudeDeg:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `altitudeMeters:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `timeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Estimate the magnetic field at a given point and time. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDeclination](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#getDeclination())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFieldStrength](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#getFieldStrength())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHorizontalStrength](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#getHorizontalStrength())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInclination](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#getInclination())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getX](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#getX())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getY](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#getY())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getZ](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField#getZ())`()` <br /> |

## Public constructors

### GeomagneticField

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GeomagneticField(
    gdLatitudeDeg: Float, 
    gdLongitudeDeg: Float, 
    altitudeMeters: Float, 
    timeMillis: Long)
```

Estimate the magnetic field at a given point and time.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gdLatitudeDeg` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Latitude in WGS84 geodetic coordinates -- positive is east. |
| `gdLongitudeDeg` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Longitude in WGS84 geodetic coordinates -- positive is north. |
| `altitudeMeters` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Altitude in WGS84 geodetic coordinates, in meters. |
| `timeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Time at which to evaluate the declination, in milliseconds since January 1, 1970. (approximate is fine -- the declination changes very slowly). |

## Public methods

### getDeclination

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeclination(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The declination of the horizontal component of the magnetic field from true north, in degrees (i.e. positive means the magnetic field is rotated east that much from true north). |

### getFieldStrength

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFieldStrength(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Total field strength in nanoteslas. |

### getHorizontalStrength

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHorizontalStrength(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Horizontal component of the field strength in nanoteslas. |

### getInclination

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInclination(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The inclination of the magnetic field in degrees -- positive means the magnetic field is rotated downwards. |

### getX

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getX(): Float
```

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The X (northward) component of the magnetic field in nanoteslas. |

### getY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getY(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The Y (eastward) component of the magnetic field in nanoteslas. |

### getZ

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getZ(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The Z (downward) component of the magnetic field in nanoteslas. |
