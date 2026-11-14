# AltitudeConverter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AltitudeConverter

Kotlin| [Java](../android/location/altitude/AltitudeConverter.md) 
| --- | --- |

```
class AltitudeConverter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.altitude.AltitudeConverter](../android/location/altitude/AltitudeConverter.md) |

Converts altitudes reported above the World Geodetic System 1984 (WGS84) reference ellipsoid into ones above Mean Sea Level.

Reference: 

```kotlin
Brian Julian and Michael Angermann.
  "Resource efficient and accurate altitude conversion to Mean Sea Level."
  2023 IEEE/ION Position, Location and Navigation Symposium (PLANS).
  
```

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AltitudeConverter](../android/location/altitude/AltitudeConverter.md))`()` Creates an instance that manages an independent cache to optimized conversions of locations in proximity to one another. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addMslAltitudeToLocation](../android/location/altitude/AltitudeConverter.md))`(`context:` ` [Context](../android/content/Context.md)`, `location:` ` [Location](../android/location/Location.md)`)` Adds a Mean Sea Level altitude to the`location`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryAddMslAltitudeToLocation](../android/location/altitude/AltitudeConverter.md))`(`location:` ` [Location](../android/location/Location.md)`)` Same as [addMslAltitudeToLocation(android.content.Context,android.location.Location)](../android/location/altitude/AltitudeConverter.md))except that this method can be called on the main thread as data will not be loaded from raw assets. |

## Public constructors

### AltitudeConverter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AltitudeConverter()
```

Creates an instance that manages an independent cache to optimized conversions of locations in proximity to one another.

## Public methods

### addMslAltitudeToLocation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addMslAltitudeToLocation(
    context: Context, 
    location: Location
): Unit
```

Adds a Mean Sea Level altitude to the`location`. In addition, adds a Mean Sea Level altitude accuracy if the`location`has a finite and non-negative vertical accuracy; otherwise, does not add a corresponding accuracy.

Must be called off the main thread as data may be loaded from raw assets. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):This value cannot be`null`. |
| `location` | [Location](../android/location/Location.md):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when loading data from raw assets. |
| `java.lang.IllegalArgumentException` | if the`location`has an invalid latitude, longitude, or altitude above WGS84. Specifically, the latitude must be between -90 and 90 (both inclusive), the longitude must be between -180 and 180 (both inclusive), and the altitude above WGS84 must be finite. |

### tryAddMslAltitudeToLocation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun tryAddMslAltitudeToLocation(location: Location): Boolean
```

Same as [addMslAltitudeToLocation(android.content.Context,android.location.Location)](../android/location/altitude/AltitudeConverter.md))except that this method can be called on the main thread as data will not be loaded from raw assets. Returns true if a Mean Sea Level altitude is added to the`location`; otherwise, returns false and leaves the`location`unchanged.

Prior calls to [addMslAltitudeToLocation(android.content.Context,android.location.Location)](../android/location/altitude/AltitudeConverter.md))off the main thread are necessary to load data from raw assets. Example code on the main thread is as follows: 

```kotlin
<code>if (!mAltitudeConverter.tryAddMslAltitudeToLocation(location)) {
        // Queue up only one call off the main thread.
        if (mIsAltitudeConverterIdle) {
            mIsAltitudeConverterIdle = false;
            executeOffMainThread(() -&gt; {
                try {
                    // Load raw assets for next call attempt on main thread.
                    mAltitudeConverter.addMslAltitudeToLocation(mContext, location);
                } catch (IOException e) {
                    Log.e(TAG, "Not loading raw assets: " + e);
                }
                mIsAltitudeConverterIdle = true;
            });
        }
    }
  </code>
```

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------|
| `location` | [Location](../android/location/Location.md):This value cannot be`null`. |
