# Location

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Location

Kotlin| [Java](Location.md) 
| --- | --- |

```
open class Location : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.Location](Location.md) |

A data class representing a geographic location. A location consists of a latitude, longitude, timestamp, accuracy, and other information such as bearing, altitude and velocity.

All locations generated through [LocationManager](LocationManager.md) are guaranteed to have a valid latitude, longitude, timestamp (both Unix epoch time and elapsed realtime since boot), and accuracy. All other parameters are optional.

Note that Android provides the ability for applications to submit "mock" or faked locations through [LocationManager](LocationManager.md), and that these locations can then be received by applications using LocationManager to obtain location information. These locations can be identified via the [isMock()](Location.md))API. Applications that wish to determine if a given location represents the best estimate of the real position of the device as opposed to a fake location coming from another application or the user should use this API. Keep in mind that the user may have a good reason for mocking their location, and thus apps should generally reject mock locations only when it is essential to their use case that only real locations are accepted.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_DEGREES](Location.md) Constant used to specify formatting of a latitude or longitude in the form "\[+-\]DDD. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_MINUTES](Location.md) Constant used to specify formatting of a latitude or longitude in the form "\[+-\]DDD:MM. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SECONDS](Location.md) Constant used to specify formatting of a latitude or longitude in the form "DDD:MM:SS. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Location](Location.md))`(`location:` ` [Location](Location.md)`)` Constructs a new location copied from the given location. |
| [Location](Location.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a new location with a named provider. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [bearingTo](Location.md))`(`dest:` ` [Location](Location.md)`)` Returns the approximate initial bearing in degrees east of true north when traveling along the shortest path between this location and the given location. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [convert](Location.md))`(`coordinate:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `outputType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts a latitude/longitude coordinate to a String representation. |
| openstatic [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [convert](Location.md))`(`coordinate:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Converts a String in one of the formats described by [FORMAT_DEGREES](Location.md), [FORMAT_MINUTES](Location.md), or [FORMAT_SECONDS](Location.md) into a double. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](Location.md))`()` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [distanceBetween](Location.md))`(`startLatitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `startLongitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `endLatitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `endLongitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `results:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Computes the approximate distance in meters between two locations, and optionally the initial and final bearings of the shortest path between them. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [distanceTo](Location.md))`(`dest:` ` [Location](Location.md)`)` Returns the approximate distance in meters between this location and the given location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](Location.md))`(`pw:` ` [Printer](../android.util/Printer.md)`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Dumps location information to the given Printer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Location.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Location equality is provided primarily for test purposes. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAccuracy](Location.md))`()` Returns the estimated horizontal accuracy radius in meters of this location at the 68th percentile confidence level. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAltitude](Location.md))`()` The altitude of this location in meters above the WGS84 reference ellipsoid. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getBearing](Location.md))`()` Returns the bearing at the time of this location in degrees. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getBearingAccuracyDegrees](Location.md))`()` Returns the estimated bearing accuracy in degrees of this location at the 68th percentile confidence level. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getElapsedRealtimeAgeMillis](Location.md))`()` A convenience methods that returns the age of this location in milliseconds with respect to the current elapsed realtime. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getElapsedRealtimeAgeMillis](Location.md))`(`referenceRealtimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` A convenience method that returns the age of this location with respect to the given reference elapsed realtime. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getElapsedRealtimeMillis](Location.md))`()` Return the time of this fix in milliseconds of elapsed realtime since system boot. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getElapsedRealtimeNanos](Location.md))`()` Return the time of this fix in nanoseconds of elapsed realtime since system boot. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getElapsedRealtimeUncertaintyNanos](Location.md))`()` Get the uncertainty in nanoseconds of the precision of [getElapsedRealtimeNanos()](Location.md))at the 68th percentile confidence level. |
| open [Bundle](../android.os/Bundle.md)? | [getExtras](Location.md))`()` Returns an optional bundle of additional information associated with this location. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getLatitude](Location.md))`()` Get the latitude in degrees. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getLongitude](Location.md))`()` Get the longitude in degrees. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMslAltitudeAccuracyMeters](Location.md))`()` Returns the estimated Mean Sea Level altitude accuracy in meters of this location at the 68th percentile confidence level. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getMslAltitudeMeters](Location.md))`()` Returns the Mean Sea Level altitude of this location in meters. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getProvider](Location.md))`()` Returns the name of the provider associated with this location. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpeed](Location.md))`()` Returns the speed at the time of this location in meters per second. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpeedAccuracyMetersPerSecond](Location.md))`()` Returns the estimated speed accuracy in meters per second of this location at the 68th percentile confidence level. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTime](Location.md))`()` Returns the Unix epoch time of this location fix, in milliseconds since the start of the Unix epoch (00:00:00 January 1, 1970 UTC). |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVerticalAccuracyMeters](Location.md))`()` Returns the estimated altitude accuracy in meters of this location at the 68th percentile confidence level. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAccuracy](Location.md))`()` Returns true if this location has a horizontal accuracy, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAltitude](Location.md))`()` Returns true if this location has an altitude, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasBearing](Location.md))`()` True if this location has a bearing, false otherwise. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasBearingAccuracy](Location.md))`()` Returns true if this location has a bearing accuracy, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasElapsedRealtimeUncertaintyNanos](Location.md))`()` True if this location has an elapsed realtime uncertainty, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMslAltitude](Location.md))`()` Returns true if this location has a Mean Sea Level altitude, false otherwise. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMslAltitudeAccuracy](Location.md))`()` Returns true if this location has a Mean Sea Level altitude accuracy, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSpeed](Location.md))`()` True if this location has a speed, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSpeedAccuracy](Location.md))`()` Returns true if this location has a speed accuracy, false otherwise. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasVerticalAccuracy](Location.md))`()` Returns true if this location has a vertical accuracy, false otherwise. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Location.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isComplete](Location.md))`()` Return true if this location is considered complete. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFromMockProvider](Location.md))`()` Returns true if this is a mock location. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMock](Location.md))`()` Returns true if this location is marked as a mock location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAccuracy](Location.md))`()` Remove the horizontal accuracy from this location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAltitude](Location.md))`()` Removes the altitude from this location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeBearing](Location.md))`()` Remove the bearing from this location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeBearingAccuracy](Location.md))`()` Remove the bearing accuracy from this location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeElapsedRealtimeUncertaintyNanos](Location.md))`()` Removes the elapsed realtime uncertainty from this location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMslAltitude](Location.md))`()` Removes the Mean Sea Level altitude from this location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMslAltitudeAccuracy](Location.md))`()` Removes the Mean Sea Level altitude accuracy from this location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeSpeed](Location.md))`()` Remove the speed from this location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeSpeedAccuracy](Location.md))`()` Remove the speed accuracy from this location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeVerticalAccuracy](Location.md))`()` Remove the vertical accuracy from this location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](Location.md))`()` Sets the provider to null, removes all optional fields, and sets the values of all other fields to zero. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](Location.md))`(`location:` ` [Location](Location.md)`)` Turns this location into a copy of the given location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccuracy](Location.md))`(`horizontalAccuracyMeters:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the horizontal accuracy in meters of this location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAltitude](Location.md))`(`altitudeMeters:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Set the altitude of this location in meters above the WGS84 reference ellipsoid. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBearing](Location.md))`(`bearingDegrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the bearing at the time of this location, in degrees. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBearingAccuracyDegrees](Location.md))`(`bearingAccuracyDegrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the bearing accuracy in degrees of this location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElapsedRealtimeNanos](Location.md))`(`elapsedRealtimeNs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Set the time of this location in nanoseconds of elapsed realtime since system boot. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElapsedRealtimeUncertaintyNanos](Location.md))`(`elapsedRealtimeUncertaintyNs:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the uncertainty in nanoseconds of the precision of the elapsed realtime timestamp at a 68% confidence level. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](Location.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)?`)` Sets the extra information associated with this fix to the given Bundle. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLatitude](Location.md))`(`latitudeDegrees:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Set the latitude of this location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLongitude](Location.md))`(`longitudeDegrees:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Set the longitude of this location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMock](Location.md))`(`mock:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this location is marked as a mock location. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMslAltitudeAccuracyMeters](Location.md))`(`mslAltitudeAccuracyMeters:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the Mean Sea Level altitude accuracy of this location in meters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMslAltitudeMeters](Location.md))`(`mslAltitudeMeters:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the Mean Sea Level altitude of this location in meters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProvider](Location.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the name of the provider associated with this location |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeed](Location.md))`(`speedMetersPerSecond:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the speed at the time of this location, in meters per second. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeedAccuracyMetersPerSecond](Location.md))`(`speedAccuracyMeterPerSecond:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the speed accuracy of this location in meters per second. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](Location.md))`(`timeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the Unix epoch time of this location fix, in milliseconds since the start of the Unix epoch (00:00:00 January 1 1970 UTC). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVerticalAccuracyMeters](Location.md))`(`altitudeAccuracyMeters:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the altitude accuracy of this location in meters. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Location.md))`()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](Location.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Location](Location.md)!\> | [CREATOR](Location.md) <br /> |

## Constants

### FORMAT_DEGREES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_DEGREES: Int
```

Constant used to specify formatting of a latitude or longitude in the form "\[+-\]DDD.DDDDD where D indicates degrees. 

 Value: 0

### FORMAT_MINUTES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_MINUTES: Int
```

Constant used to specify formatting of a latitude or longitude in the form "\[+-\]DDD:MM.MMMMM" where D indicates degrees and M indicates minutes of arc (1 minute = 1/60th of a degree). 

 Value: 1

### FORMAT_SECONDS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SECONDS: Int
```

Constant used to specify formatting of a latitude or longitude in the form "DDD:MM:SS.SSSSS" where D indicates degrees, M indicates minutes of arc, and S indicates seconds of arc (1 minute = 1/60th of a degree, 1 second = 1/3600th of a degree). 

 Value: 2

## Public constructors

### Location

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Location(location: Location)
```

Constructs a new location copied from the given location.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------|
| `location` | [Location](Location.md):This value cannot be`null`. |

### Location

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Location(provider: String?)
```

Constructs a new location with a named provider. By default all values are zero, and no optional values are present.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the location provider name associated with this location This value may be`null`. |

## Public methods

### bearingTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bearingTo(dest: Location): Float
```

Returns the approximate initial bearing in degrees east of true north when traveling along the shortest path between this location and the given location. The shortest path is defined using the WGS84 ellipsoid. Locations that are (nearly) antipodal may produce meaningless results.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Location](Location.md):the destination location This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the initial bearing in degrees |

### convert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convert(
    coordinate: Double, 
    outputType: Int
): String
```

Converts a latitude/longitude coordinate to a String representation. The outputType must be one of [FORMAT_DEGREES](Location.md), [FORMAT_MINUTES](Location.md), or [FORMAT_SECONDS](Location.md). The coordinate must be a number between -180.0 and 180.0, inclusive. This conversion is performed in a method that is dependent on the default locale, and so is not guaranteed to round-trip with [convert(java.lang.String)](Location.md)).

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outputType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.location.Location#FORMAT_DEGREES](Location.md), [android.location.Location#FORMAT_MINUTES](Location.md), or [android.location.Location#FORMAT_SECONDS](Location.md) |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if outputType is not a recognized value. |

### convert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convert(coordinate: String): Double
```

Converts a String in one of the formats described by [FORMAT_DEGREES](Location.md), [FORMAT_MINUTES](Location.md), or [FORMAT_SECONDS](Location.md) into a double. This conversion is performed in a locale agnostic method, and so is not guaranteed to round-trip with [convert(double,int)](Location.md)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------|
| `coordinate` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.NullPointerException` | if coordinate is null |
| `java.lang.IllegalArgumentException` | if the coordinate is not in one of the valid formats. |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### distanceBetween

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun distanceBetween(
    startLatitude: Double, 
    startLongitude: Double, 
    endLatitude: Double, 
    endLongitude: Double, 
    results: FloatArray!
): Unit
```

Computes the approximate distance in meters between two locations, and optionally the initial and final bearings of the shortest path between them. Distance and bearing are defined using the WGS84 ellipsoid.

The computed distance is stored in results\[0\]. If results has length 2 or greater, the initial bearing is stored in results\[1\]. If results has length 3 or greater, the final bearing is stored in results\[2\].

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startLatitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the starting latitude Value is between -90.0f and 90.0f inclusive |
| `startLongitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the starting longitude Value is between -180.0f and 180.0f inclusive |
| `endLatitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the ending latitude Value is between -90.0f and 90.0f inclusive |
| --- | --- |
| `endLongitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the ending longitude Value is between -180.0f and 180.0f inclusive |
| `results` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:an array of floats to hold the results |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | if results is null or has length \< 1 |

### distanceTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun distanceTo(dest: Location): Float
```

Returns the approximate distance in meters between this location and the given location. Distance is defined using the WGS84 ellipsoid.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Location](Location.md):the destination location This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the approximate distance in meters Value is 0.0f or greater |

### dump

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dump(
    pw: Printer, 
    prefix: String?
): Unit
```

**Deprecated:** *Prefer to use [toString()](Location.md))along with whatever custom formatting is required instead of this method. It is not this class's job to manage print representations.*

Dumps location information to the given Printer.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `pw` | [Printer](../android.util/Printer.md):This value cannot be`null`. |
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Location equality is provided primarily for test purposes. Comparing locations for equality in production may indicate incorrect assumptions, and should be avoided whenever possible.

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAccuracy(): Float
```

Returns the estimated horizontal accuracy radius in meters of this location at the 68th percentile confidence level. This means that there is a 68% chance that the true location of the device is within a distance of this uncertainty of the reported location. Another way of putting this is that if a circle with a radius equal to this accuracy is drawn around the reported location, there is a 68% chance that the true location falls within this circle. This accuracy value is only valid for horizontal positioning, and not vertical positioning.

This is only valid if [hasAccuracy()](Location.md))is true. All locations generated by the [LocationManager](LocationManager.md) include horizontal accuracy.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | horizontal accuracy of this location Value is 0.0f or greater |

### getAltitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAltitude(): Double
```

The altitude of this location in meters above the WGS84 reference ellipsoid.

This is only valid if [hasAltitude()](Location.md))is true.

| Return ||
|----------------------------------------------------------------------------------|---------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | altitude of this location |

### getBearing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBearing(): Float
```

Returns the bearing at the time of this location in degrees. Bearing is the horizontal direction of travel of this device and is unrelated to the device orientation. The bearing is guaranteed to be in the range \[0, 360).

This is only valid if [hasBearing()](Location.md))is true.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | bearing at the time of this location Value is between 0.0f and 360.0f inclusive |

### getBearingAccuracyDegrees

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBearingAccuracyDegrees(): Float
```

Returns the estimated bearing accuracy in degrees of this location at the 68th percentile confidence level. This means that there is 68% chance that the true bearing at the time of this location falls within [getBearing()](Location.md))()} +/- this uncertainty.

This is only valid if [hasBearingAccuracy()](Location.md))()} is true.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | bearing accuracy in degrees of this location Value is 0.0f or greater |

### getElapsedRealtimeAgeMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getElapsedRealtimeAgeMillis(): Long
```

A convenience methods that returns the age of this location in milliseconds with respect to the current elapsed realtime.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | age of this location in milliseconds Value is 0 or greater |

### getElapsedRealtimeAgeMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getElapsedRealtimeAgeMillis(referenceRealtimeMs: Long): Long
```

A convenience method that returns the age of this location with respect to the given reference elapsed realtime.

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `referenceRealtimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):reference realtime in milliseconds Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | age of this location in milliseconds |

### getElapsedRealtimeMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getElapsedRealtimeMillis(): Long
```

Return the time of this fix in milliseconds of elapsed realtime since system boot.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | elapsed realtime of this location in milliseconds Value is 0 or greater |

**See Also**

- <https://developer.android.com/reference/kotlin/android/location/Location#getElapsedRealtimeNanos()> 

### getElapsedRealtimeNanos

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getElapsedRealtimeNanos(): Long
```

Return the time of this fix in nanoseconds of elapsed realtime since system boot.

This value can be compared with [android.os.SystemClock#elapsedRealtimeNanos](../android.os/SystemClock.md))to reliably order or compare locations. This is reliable because elapsed realtime is guaranteed to be monotonic and continues to increment even when the system is in deep sleep (unlike [getTime](Location.md))). However, since elapsed realtime is with reference to system boot, it does not make sense to use this value to order or compare locations across boot cycles or devices.

All locations generated by the [LocationManager](LocationManager.md) are guaranteed to have a valid elapsed realtime set.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | elapsed realtime of this location in nanoseconds Value is 0 or greater |

### getElapsedRealtimeUncertaintyNanos

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getElapsedRealtimeUncertaintyNanos(): Double
```

Get the uncertainty in nanoseconds of the precision of [getElapsedRealtimeNanos()](Location.md))at the 68th percentile confidence level. This means that there is 68% chance that the true elapsed realtime of this location is within [getElapsedRealtimeNanos()](Location.md))+/- this uncertainty.

This is only valid if [hasElapsedRealtimeUncertaintyNanos()](Location.md))is true.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | uncertainty in nanoseconds of the elapsed realtime of this location Value is 0.0f or greater |

### getExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): Bundle?
```

Returns an optional bundle of additional information associated with this location. The keys and values within the bundle are determined by the location provider.

Common key/value pairs are listed below. There is no guarantee that these key/value pairs will be present for any location.

- satellites - the number of satellites used to derive a GNSS fix. This key was deprecated in API 34 because the information can be obtained through more accurate means, such as by referencing [GnssStatus.usedInFix](GnssStatus.md)).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](../android.os/Bundle.md)? | This value may be`null`. |

### getLatitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLatitude(): Double
```

Get the latitude in degrees. All locations generated by the [LocationManager](LocationManager.md) will have a valid latitude.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | latitude of this location Value is between -90.0f and 90.0f inclusive |

### getLongitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLongitude(): Double
```

Get the longitude in degrees. All locations generated by the [LocationManager](LocationManager.md) will have a valid longitude.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | longitude of this location Value is between -180.0f and 180.0f inclusive |

### getMslAltitudeAccuracyMeters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMslAltitudeAccuracyMeters(): Float
```

Returns the estimated Mean Sea Level altitude accuracy in meters of this location at the 68th percentile confidence level. This means that there is 68% chance that the true Mean Sea Level altitude of this location falls within [getMslAltitudeMeters()](Location.md))+/- this uncertainty.

This is only valid if [hasMslAltitudeAccuracy()](Location.md))is true.

| Return ||
|--------------------------------------------------------------------------------|--------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is 0.0f or greater |

### getMslAltitudeMeters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMslAltitudeMeters(): Double
```

Returns the Mean Sea Level altitude of this location in meters.

This is only valid if [hasMslAltitude()](Location.md))is true. 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvider(): String?
```

Returns the name of the provider associated with this location.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the name of the provider This value may be`null`. |

### getSpeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpeed(): Float
```

Returns the speed at the time of this location in meters per second. Note that the speed returned here may be more accurate than would be obtained simply by calculating`distance / time`for sequential positions, such as if the Doppler measurements from GNSS satellites are taken into account.

This is only valid if [hasSpeed()](Location.md))is true.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | speed at the time of this location Value is 0.0f or greater |

### getSpeedAccuracyMetersPerSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpeedAccuracyMetersPerSecond(): Float
```

Returns the estimated speed accuracy in meters per second of this location at the 68th percentile confidence level. This means that there is 68% chance that the true speed at the time of this location falls within [getSpeed()](Location.md))()} +/- this uncertainty.

This is only valid if [hasSpeedAccuracy()](Location.md))is true.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | vertical accuracy of this location Value is 0.0f or greater |

### getTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTime(): Long
```

Returns the Unix epoch time of this location fix, in milliseconds since the start of the Unix epoch (00:00:00 January 1, 1970 UTC).

There is no guarantee that different locations have times set from the same clock. Locations derived from the [LocationManager.GPS_PROVIDER](LocationManager.md) are guaranteed to have their time originate from the clock in use by the satellite constellation that provided the fix. Locations derived from other providers may use any clock to set their time, though it is most common to use the device's Unix epoch time system clock (which may be incorrect).

Note that the device's Unix epoch time system clock is not monotonic; it can jump forwards or backwards unpredictably and may be changed at any time by the user, so this time should not be used to order or compare locations. Prefer [getElapsedRealtimeNanos](Location.md))for that purpose, as the elapsed realtime clock is guaranteed to be monotonic.

On the other hand, this method may be useful for presenting a human-readable time to the user, or as a heuristic for comparing location fixes across reboot or across devices.

All locations generated by the [LocationManager](LocationManager.md) are guaranteed to have this time set, however remember that the device's system clock may have changed since the location was generated.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the Unix epoch time of this location Value is 0 or greater |

### getVerticalAccuracyMeters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVerticalAccuracyMeters(): Float
```

Returns the estimated altitude accuracy in meters of this location at the 68th percentile confidence level. This means that there is 68% chance that the true altitude of this location falls within [getAltitude()](Location.md))()} +/- this uncertainty.

This is only valid if [hasVerticalAccuracy()](Location.md))is true.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | vertical accuracy of this location Value is 0.0f or greater |

### hasAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasAccuracy(): Boolean
```

Returns true if this location has a horizontal accuracy, false otherwise. 

### hasAltitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasAltitude(): Boolean
```

Returns true if this location has an altitude, false otherwise. 

### hasBearing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasBearing(): Boolean
```

True if this location has a bearing, false otherwise. 

### hasBearingAccuracy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasBearingAccuracy(): Boolean
```

Returns true if this location has a bearing accuracy, false otherwise. 

### hasElapsedRealtimeUncertaintyNanos

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasElapsedRealtimeUncertaintyNanos(): Boolean
```

True if this location has an elapsed realtime uncertainty, false otherwise. 

### hasMslAltitude

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMslAltitude(): Boolean
```

Returns true if this location has a Mean Sea Level altitude, false otherwise. 

### hasMslAltitudeAccuracy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMslAltitudeAccuracy(): Boolean
```

Returns true if this location has a Mean Sea Level altitude accuracy, false otherwise. 

### hasSpeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasSpeed(): Boolean
```

True if this location has a speed, false otherwise. 

### hasSpeedAccuracy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasSpeedAccuracy(): Boolean
```

Returns true if this location has a speed accuracy, false otherwise. 

### hasVerticalAccuracy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasVerticalAccuracy(): Boolean
```

Returns true if this location has a vertical accuracy, false otherwise. 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isComplete

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isComplete(): Boolean
```

Return true if this location is considered complete. A location is considered complete if it has a non-null provider, accuracy, and non-zero time and elapsed realtime. The exact definition of completeness may change over time.

All locations supplied by the [LocationManager](LocationManager.md) are guaranteed to be complete. 

### isFromMockProvider

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFromMockProvider(): Boolean
```

**Deprecated:** *Prefer [isMock()](Location.md))instead.*

Returns true if this is a mock location. If this location comes from the Android framework, this indicates that the location was provided by a test location provider, and thus may not be related to the actual location of the device.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this location came from a mock provider, false otherwise |

### isMock

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMock(): Boolean
```

Returns true if this location is marked as a mock location. If this location comes from the Android framework, this indicates that the location was provided by a test location provider, and thus may not be related to the actual location of the device. 
**See Also**

### removeAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAccuracy(): Unit
```

Remove the horizontal accuracy from this location. 

### removeAltitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAltitude(): Unit
```

Removes the altitude from this location. 

### removeBearing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeBearing(): Unit
```

Remove the bearing from this location. 

### removeBearingAccuracy

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeBearingAccuracy(): Unit
```

Remove the bearing accuracy from this location. 

### removeElapsedRealtimeUncertaintyNanos

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeElapsedRealtimeUncertaintyNanos(): Unit
```

Removes the elapsed realtime uncertainty from this location. 

### removeMslAltitude

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeMslAltitude(): Unit
```

Removes the Mean Sea Level altitude from this location. 

### removeMslAltitudeAccuracy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeMslAltitudeAccuracy(): Unit
```

Removes the Mean Sea Level altitude accuracy from this location. 

### removeSpeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeSpeed(): Unit
```

Remove the speed from this location. 

### removeSpeedAccuracy

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeSpeedAccuracy(): Unit
```

Remove the speed accuracy from this location. 

### removeVerticalAccuracy

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeVerticalAccuracy(): Unit
```

Remove the vertical accuracy from this location. 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Sets the provider to null, removes all optional fields, and sets the values of all other fields to zero. 

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(location: Location): Unit
```

Turns this location into a copy of the given location.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------|
| `location` | [Location](Location.md):This value cannot be`null`. |

### setAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAccuracy(horizontalAccuracyMeters: Float): Unit
```

Set the horizontal accuracy in meters of this location.

| Parameters ||
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `horizontalAccuracyMeters` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):horizontal altitude in meters Value is 0.0f or greater |

### setAltitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAltitude(altitudeMeters: Double): Unit
```

Set the altitude of this location in meters above the WGS84 reference ellipsoid.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------|
| `altitudeMeters` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):altitude in meters |

### setBearing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBearing(bearingDegrees: Float): Unit
```

Set the bearing at the time of this location, in degrees. The given bearing will be converted into the range \[0, 360).

Note: passing in extremely high or low floating point values to this function may produce strange results due to the intricacies of floating point math.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------|
| `bearingDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):bearing in degrees |

### setBearingAccuracyDegrees

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBearingAccuracyDegrees(bearingAccuracyDegrees: Float): Unit
```

Set the bearing accuracy in degrees of this location.

| Parameters ||
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `bearingAccuracyDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):bearing accuracy in degrees Value is 0.0f or greater |

### setElapsedRealtimeNanos

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setElapsedRealtimeNanos(elapsedRealtimeNs: Long): Unit
```

Set the time of this location in nanoseconds of elapsed realtime since system boot.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `elapsedRealtimeNs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):elapsed realtime in nanoseconds Value is 0 or greater |

### setElapsedRealtimeUncertaintyNanos

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setElapsedRealtimeUncertaintyNanos(elapsedRealtimeUncertaintyNs: Double): Unit
```

Sets the uncertainty in nanoseconds of the precision of the elapsed realtime timestamp at a 68% confidence level.

| Parameters ||
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `elapsedRealtimeUncertaintyNs` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):uncertainty in nanoseconds of the elapsed realtime of this location Value is 0.0f or greater |

### setExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExtras(extras: Bundle?): Unit
```

Sets the extra information associated with this fix to the given Bundle.

Note this stores a copy of the given extras, so any changes to extras after calling this method won't be reflected in the location bundle.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |

### setLatitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLatitude(latitudeDegrees: Double): Unit
```

Set the latitude of this location.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `latitudeDegrees` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):latitude in degrees Value is between -90.0f and 90.0f inclusive |

### setLongitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLongitude(longitudeDegrees: Double): Unit
```

Set the longitude of this location.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `longitudeDegrees` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):longitude in degrees Value is between -180.0f and 180.0f inclusive |

### setMock

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMock(mock: Boolean): Unit
```

Sets whether this location is marked as a mock location. 

### setMslAltitudeAccuracyMeters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMslAltitudeAccuracyMeters(mslAltitudeAccuracyMeters: Float): Unit
```

Sets the Mean Sea Level altitude accuracy of this location in meters.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------|
| `mslAltitudeAccuracyMeters` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Value is 0.0f or greater |

### setMslAltitudeMeters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMslAltitudeMeters(mslAltitudeMeters: Double): Unit
```

Sets the Mean Sea Level altitude of this location in meters. 

### setProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProvider(provider: String?): Unit
```

Sets the name of the provider associated with this location

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the name of the provider This value may be`null`. |

### setSpeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpeed(speedMetersPerSecond: Float): Unit
```

Set the speed at the time of this location, in meters per second.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `speedMetersPerSecond` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):speed in meters per second Value is 0.0f or greater |

### setSpeedAccuracyMetersPerSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpeedAccuracyMetersPerSecond(speedAccuracyMeterPerSecond: Float): Unit
```

Set the speed accuracy of this location in meters per second.

| Parameters ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `speedAccuracyMeterPerSecond` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):speed accuracy in meters per second Value is 0.0f or greater |

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTime(timeMs: Long): Unit
```

Sets the Unix epoch time of this location fix, in milliseconds since the start of the Unix epoch (00:00:00 January 1 1970 UTC).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `timeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the Unix epoch time of this location Value is 0 or greater |

### setVerticalAccuracyMeters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVerticalAccuracyMeters(altitudeAccuracyMeters: Float): Unit
```

Set the altitude accuracy of this location in meters.

| Parameters ||
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `altitudeAccuracyMeters` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):altitude accuracy in meters Value is 0.0f or greater |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Location!>
```
