# Geocoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Geocoder

Kotlin| [Java](https://developer.android.com/reference/android/location/Geocoder "View this page in Java") 

```
class Geocoder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.location.Geocoder](https://developer.android.com/reference/kotlin/android/location/Geocoder#) |

A class for handling geocoding and reverse geocoding. Geocoding is the process of transforming a street address or other description of a location into a (latitude, longitude) coordinate. Reverse geocoding is the process of transforming a (latitude, longitude) coordinate into a (partial) address. The amount of detail in a reverse geocoded location description may vary, for example one might contain the full street address of the closest building, while another might contain only a city name and postal code.

Use the isPresent() method to determine whether a Geocoder implementation exists on the current device. If no implementation is present, any attempt to geocode will result in an error.

Geocoder implementations are only required to make a best effort to return results in the chosen locale. Note that geocoder implementations may return results in other locales if they have no information available for the chosen locale.

**Warning:**Geocoding services may provide no guarantees on availability or accuracy. Results are a best guess, and are not guaranteed to be meaningful or correct. Do not use this API for any safety-critical or regulatory compliance purpose.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [GeocodeListener](https://developer.android.com/reference/kotlin/android/location/Geocoder.GeocodeListener) A listener for asynchronous geocoding results. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Geocoder](https://developer.android.com/reference/kotlin/android/location/Geocoder#Geocoder(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Constructs a Geocoder localized for [Locale.getDefault()](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()). |
| [Geocoder](https://developer.android.com/reference/kotlin/android/location/Geocoder#Geocoder(android.content.Context,%20java.util.Locale))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` Constructs a Geocoder localized for the given locale. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Address](https://developer.android.com/reference/kotlin/android/location/Address)!\>? | [getFromLocation](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocation(kotlin.Double,%20kotlin.Double,%20kotlin.Int))`(`latitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `longitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `maxResults:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an array of Addresses that attempt to describe the area immediately surrounding the given latitude and longitude. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getFromLocation](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocation(kotlin.Double,%20kotlin.Double,%20kotlin.Int,%20android.location.Geocoder.GeocodeListener))`(`latitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `longitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `maxResults:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [Geocoder.GeocodeListener](https://developer.android.com/reference/kotlin/android/location/Geocoder.GeocodeListener)`)` Provides an array of Addresses that attempt to describe the area immediately surrounding the given latitude and longitude. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Address](https://developer.android.com/reference/kotlin/android/location/Address)!\>? | [getFromLocationName](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocationName(kotlin.String,%20kotlin.Int))`(`locationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `maxResults:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an array of Addresses that attempt to describe the named location, which may be a place name such as "Dalvik, Iceland", an address such as "1600 Amphitheatre Parkway, Mountain View, CA", an airport code such as "SFO", and so forth. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getFromLocationName](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocationName(kotlin.String,%20kotlin.Int,%20android.location.Geocoder.GeocodeListener))`(`locationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `maxResults:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [Geocoder.GeocodeListener](https://developer.android.com/reference/kotlin/android/location/Geocoder.GeocodeListener)`)` Provides an array of Addresses that attempt to describe the named location, which may be a place name such as "Dalvik, Iceland", an address such as "1600 Amphitheatre Parkway, Mountain View, CA", an airport code such as "SFO", and so forth. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Address](https://developer.android.com/reference/kotlin/android/location/Address)!\>? | [getFromLocationName](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocationName(kotlin.String,%20kotlin.Int,%20kotlin.Double,%20kotlin.Double,%20kotlin.Double,%20kotlin.Double))`(`locationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `maxResults:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lowerLeftLatitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `lowerLeftLongitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `upperRightLatitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `upperRightLongitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns an array of Addresses that attempt to describe the named location, which may be a place name such as "Dalvik, Iceland", an address such as "1600 Amphitheatre Parkway, Mountain View, CA", an airport code such as "SFO", and so forth. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getFromLocationName](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocationName(kotlin.String,%20kotlin.Int,%20kotlin.Double,%20kotlin.Double,%20kotlin.Double,%20kotlin.Double,%20android.location.Geocoder.GeocodeListener))`(`locationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `maxResults:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lowerLeftLatitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `lowerLeftLongitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `upperRightLatitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `upperRightLongitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `listener:` ` [Geocoder.GeocodeListener](https://developer.android.com/reference/kotlin/android/location/Geocoder.GeocodeListener)`)` Returns an array of Addresses that attempt to describe the named location, which may be a place name such as "Dalvik, Iceland", an address such as "1600 Amphitheatre Parkway, Mountain View, CA", an airport code such as "SFO", and so forth. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPresent](https://developer.android.com/reference/kotlin/android/location/Geocoder#isPresent())`()` Returns true if there is a geocoder implementation present on the device that may return results. |

## Public constructors

### Geocoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Geocoder(context: Context)
```

Constructs a Geocoder localized for [Locale.getDefault()](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):This value cannot be`null`. |

### Geocoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Geocoder(
    context: Context, 
    locale: Locale)
```

Constructs a Geocoder localized for the given locale. Note that geocoder implementations will only make a best effort to return results in the given locale, and there is no guarantee that returned results will be in the specific locale.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):This value cannot be`null`. |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#):This value cannot be`null`. |

## Public methods

### getFromLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFromLocation(
    latitude: Double, 
    longitude: Double, 
    maxResults: Int
): MutableList<Address!>?
```

**Deprecated:** *Use [getFromLocation(double,double,int,android.location.Geocoder.GeocodeListener)](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocation(kotlin.Double,%20kotlin.Double,%20kotlin.Int,%20android.location.Geocoder.GeocodeListener))instead to avoid blocking a thread waiting for results.*

Returns an array of Addresses that attempt to describe the area immediately surrounding the given latitude and longitude. The returned addresses should be localized for the locale provided to this class's constructor.

**Warning:** Geocoding services may provide no guarantees on availability or accuracy. Results are a best guess, and are not guaranteed to be meaningful or correct. Do**NOT**use this API for any safety-critical or regulatory compliance purposes.

**Warning:**This API may hit the network, and may block for excessive amounts of time. It's strongly encouraged to use the asynchronous version of this API. If that is not possible, this should be run on a background thread to avoid blocking other operations.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `latitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the latitude a point for the search Value is between -90.0f and 90.0f inclusive |
| `longitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the longitude a point for the search Value is between -180.0f and 180.0f inclusive |
| `maxResults` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):max number of addresses to return. Smaller numbers (1 to 5) are recommended Value is 1 or greater |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Address](https://developer.android.com/reference/kotlin/android/location/Address)!>? | a list of Address objects. Returns null or empty list if no matches were found or there is no backend service available. |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if latitude or longitude is invalid |
| `java.io.IOException` | if there is a failure |

### getFromLocation

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFromLocation(
    latitude: Double, 
    longitude: Double, 
    maxResults: Int, 
    listener: Geocoder.GeocodeListener
): Unit
```

Provides an array of Addresses that attempt to describe the area immediately surrounding the given latitude and longitude. The returned addresses should be localized for the locale provided to this class's constructor.

**Warning:** Geocoding services may provide no guarantees on availability or accuracy. Results are a best guess, and are not guaranteed to be meaningful or correct. Do**NOT**use this API for any safety-critical or regulatory compliance purposes.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `latitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the latitude a point for the search Value is between -90.0f and 90.0f inclusive |
| `longitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the longitude a point for the search Value is between -180.0f and 180.0f inclusive |
| `maxResults` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):max number of addresses to return. Smaller numbers (1 to 5) are recommended Value is 1 or greater |
| `listener` | [Geocoder.GeocodeListener](https://developer.android.com/reference/kotlin/android/location/Geocoder.GeocodeListener):a listener for receiving results This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if latitude or longitude is invalid |

### getFromLocationName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFromLocationName(
    locationName: String, 
    maxResults: Int
): MutableList<Address!>?
```

**Deprecated:** *Use [getFromLocationName(java.lang.String,int,android.location.Geocoder.GeocodeListener)](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocationName(kotlin.String,%20kotlin.Int,%20android.location.Geocoder.GeocodeListener))instead to avoid blocking a thread waiting for results.*

Returns an array of Addresses that attempt to describe the named location, which may be a place name such as "Dalvik, Iceland", an address such as "1600 Amphitheatre Parkway, Mountain View, CA", an airport code such as "SFO", and so forth. The returned addresses should be localized for the locale provided to this class's constructor.

**Warning:** Geocoding services may provide no guarantees on availability or accuracy. Results are a best guess, and are not guaranteed to be meaningful or correct. Do**NOT**use this API for any safety-critical or regulatory compliance purposes.

**Warning:**This API may hit the network, and may block for excessive amounts of time. It's strongly encouraged to use the asynchronous version of this API. If that is not possible, this should be run on a background thread to avoid blocking other operations.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a user-supplied description of a location This value cannot be`null`. |
| `maxResults` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):max number of results to return. Smaller numbers (1 to 5) are recommended Value is 1 or greater |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Address](https://developer.android.com/reference/kotlin/android/location/Address)!>? | a list of Address objects. Returns null or empty list if no matches were found or there is no backend service available. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if locationName is null |
| `java.io.IOException` | if there is a failure |

### getFromLocationName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFromLocationName(
    locationName: String, 
    maxResults: Int, 
    listener: Geocoder.GeocodeListener
): Unit
```

Provides an array of Addresses that attempt to describe the named location, which may be a place name such as "Dalvik, Iceland", an address such as "1600 Amphitheatre Parkway, Mountain View, CA", an airport code such as "SFO", and so forth. The returned addresses should be localized for the locale provided to this class's constructor.

**Warning:** Geocoding services may provide no guarantees on availability or accuracy. Results are a best guess, and are not guaranteed to be meaningful or correct. Do**NOT**use this API for any safety-critical or regulatory compliance purposes.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a user-supplied description of a location This value cannot be`null`. |
| `maxResults` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):max number of results to return. Smaller numbers (1 to 5) are recommended Value is 1 or greater |
| `listener` | [Geocoder.GeocodeListener](https://developer.android.com/reference/kotlin/android/location/Geocoder.GeocodeListener):a listener for receiving results This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if locationName is null |

### getFromLocationName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFromLocationName(
    locationName: String, 
    maxResults: Int, 
    lowerLeftLatitude: Double, 
    lowerLeftLongitude: Double, 
    upperRightLatitude: Double, 
    upperRightLongitude: Double
): MutableList<Address!>?
```

**Deprecated:** *Use [getFromLocationName(java.lang.String,int,double,double,double,double,android.location.Geocoder.GeocodeListener)](https://developer.android.com/reference/kotlin/android/location/Geocoder#getFromLocationName(kotlin.String,%20kotlin.Int,%20kotlin.Double,%20kotlin.Double,%20kotlin.Double,%20kotlin.Double,%20android.location.Geocoder.GeocodeListener))instead to avoid blocking a thread waiting for results.*

Returns an array of Addresses that attempt to describe the named location, which may be a place name such as "Dalvik, Iceland", an address such as "1600 Amphitheatre Parkway, Mountain View, CA", an airport code such as "SFO", and so forth. The returned addresses should be localized for the locale provided to this class's constructor.

You may specify a bounding box for the search results by including the latitude and longitude of the lower left point and upper right point of the box.

**Warning:** Geocoding services may provide no guarantees on availability or accuracy. Results are a best guess, and are not guaranteed to be meaningful or correct. Do**NOT**use this API for any safety-critical or regulatory compliance purposes.

**Warning:**This API may hit the network, and may block for excessive amounts of time. It's strongly encouraged to use the asynchronous version of this API. If that is not possible, this should be run on a background thread to avoid blocking other operations.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a user-supplied description of a location This value cannot be`null`. |
| `maxResults` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):max number of addresses to return. Smaller numbers (1 to 5) are recommended Value is 1 or greater |
| `lowerLeftLatitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the latitude of the lower left corner of the bounding box Value is between -90.0f and 90.0f inclusive |
| `lowerLeftLongitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the longitude of the lower left corner of the bounding box Value is between -180.0f and 180.0f inclusive |
| `upperRightLatitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the latitude of the upper right corner of the bounding box Value is between -90.0f and 90.0f inclusive |
| `upperRightLongitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the longitude of the upper right corner of the bounding box Value is between -180.0f and 180.0f inclusive |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Address](https://developer.android.com/reference/kotlin/android/location/Address)!>? | a list of Address objects. Returns null or empty list if no matches were found or there is no backend service available. |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if any latitude or longitude is invalid |
| `java.io.IOException` | if there is a failure |

### getFromLocationName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFromLocationName(
    locationName: String, 
    maxResults: Int, 
    lowerLeftLatitude: Double, 
    lowerLeftLongitude: Double, 
    upperRightLatitude: Double, 
    upperRightLongitude: Double, 
    listener: Geocoder.GeocodeListener
): Unit
```

Returns an array of Addresses that attempt to describe the named location, which may be a place name such as "Dalvik, Iceland", an address such as "1600 Amphitheatre Parkway, Mountain View, CA", an airport code such as "SFO", and so forth. The returned addresses should be localized for the locale provided to this class's constructor.

You may specify a bounding box for the search results by including the latitude and longitude of the lower left point and upper right point of the box.

**Warning:** Geocoding services may provide no guarantees on availability or accuracy. Results are a best guess, and are not guaranteed to be meaningful or correct. Do**NOT**use this API for any safety-critical or regulatory compliance purposes.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a user-supplied description of a location This value cannot be`null`. |
| `maxResults` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):max number of addresses to return. Smaller numbers (1 to 5) are recommended Value is 1 or greater |
| `lowerLeftLatitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the latitude of the lower left corner of the bounding box Value is between -90.0f and 90.0f inclusive |
| `lowerLeftLongitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the longitude of the lower left corner of the bounding box Value is between -180.0f and 180.0f inclusive |
| `upperRightLatitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the latitude of the upper right corner of the bounding box Value is between -90.0f and 90.0f inclusive |
| `upperRightLongitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the longitude of the upper right corner of the bounding box Value is between -180.0f and 180.0f inclusive |
| `listener` | [Geocoder.GeocodeListener](https://developer.android.com/reference/kotlin/android/location/Geocoder.GeocodeListener):a listener for receiving results This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if any latitude or longitude is invalid |

### isPresent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isPresent(): Boolean
```

Returns true if there is a geocoder implementation present on the device that may return results. If true, there is still no guarantee that any individual geocoding attempt will succeed.
