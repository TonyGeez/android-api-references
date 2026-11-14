# LocationProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocationProvider

Kotlin| [Java](https://developer.android.com/reference/android/location/LocationProvider "View this page in Java") 

```
open class LocationProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.location.LocationProvider](https://developer.android.com/reference/kotlin/android/location/LocationProvider#) |

| **This class was deprecated in API level 31.**
|
| This class is incapable of representing unknown provider properties and may return incorrect results on the rare occasion when a provider's properties are unknown. Prefer using [LocationManager.getProviderProperties(String)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getProviderProperties(kotlin.String))to retrieve [ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties) instead.

Information about the properties of a location provider.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABLE](https://developer.android.com/reference/kotlin/android/location/LocationProvider#AVAILABLE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OUT_OF_SERVICE](https://developer.android.com/reference/kotlin/android/location/LocationProvider#OUT_OF_SERVICE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPORARILY_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/location/LocationProvider#TEMPORARILY_UNAVAILABLE:kotlin.Int) <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAccuracy](https://developer.android.com/reference/kotlin/android/location/LocationProvider#getAccuracy())`()` Returns the rough accuracy of this provider, one of the ProviderProperties. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/location/LocationProvider#getName())`()` Returns the name of this provider. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPowerRequirement](https://developer.android.com/reference/kotlin/android/location/LocationProvider#getPowerRequirement())`()` Returns the power requirement for this provider, one of the ProviderProperties. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMonetaryCost](https://developer.android.com/reference/kotlin/android/location/LocationProvider#hasMonetaryCost())`()` Returns true if the use of this provider may result in a monetary charge to the user, false if use is free. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [meetsCriteria](https://developer.android.com/reference/kotlin/android/location/LocationProvider#meetsCriteria(android.location.Criteria))`(`criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria)!`)` Returns true if this provider meets the given criteria, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresCell](https://developer.android.com/reference/kotlin/android/location/LocationProvider#requiresCell())`()` Returns true if the provider requires access to an appropriate cellular network (e.g., to make use of cell tower IDs), false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresNetwork](https://developer.android.com/reference/kotlin/android/location/LocationProvider#requiresNetwork())`()` Returns true if the provider requires access to a data network (e.g., the Internet), false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresSatellite](https://developer.android.com/reference/kotlin/android/location/LocationProvider#requiresSatellite())`()` Returns true if the provider requires access to a satellite-based positioning system (e.g., GPS), false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsAltitude](https://developer.android.com/reference/kotlin/android/location/LocationProvider#supportsAltitude())`()` Returns true if the provider is able to provide altitude information, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsBearing](https://developer.android.com/reference/kotlin/android/location/LocationProvider#supportsBearing())`()` Returns true if the provider is able to provide bearing information, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSpeed](https://developer.android.com/reference/kotlin/android/location/LocationProvider#supportsSpeed())`()` Returns true if the provider is able to provide speed information, false otherwise. |

## Constants

### AVAILABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABLE: Int
```

**Deprecated:** *Location provider statuses are no longer supported.* 

 Value: 2

### OUT_OF_SERVICE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OUT_OF_SERVICE: Int
```

**Deprecated:** *Location provider statuses are no longer supported.* 

 Value: 0

### TEMPORARILY_UNAVAILABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEMPORARILY_UNAVAILABLE: Int
```

**Deprecated:** *Location provider statuses are no longer supported.* 

 Value: 1

## Public methods

### getAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAccuracy(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the rough accuracy of this provider, one of the ProviderProperties.ACCURACY_\* constants. 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the name of this provider. 

### getPowerRequirement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPowerRequirement(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the power requirement for this provider, one of the ProviderProperties.POWER_USAGE_\* constants. 

### hasMonetaryCost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMonetaryCost(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the use of this provider may result in a monetary charge to the user, false if use is free. It is up to each provider to give accurate information. 

### meetsCriteria

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun meetsCriteria(criteria: Criteria!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if this provider meets the given criteria, false otherwise. 

### requiresCell

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requiresCell(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the provider requires access to an appropriate cellular network (e.g., to make use of cell tower IDs), false otherwise. 

### requiresNetwork

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requiresNetwork(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the provider requires access to a data network (e.g., the Internet), false otherwise. 

### requiresSatellite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requiresSatellite(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the provider requires access to a satellite-based positioning system (e.g., GPS), false otherwise. 

### supportsAltitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun supportsAltitude(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the provider is able to provide altitude information, false otherwise. A provider that reports altitude under most circumstances but may occassionally not report it should return true. 

### supportsBearing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun supportsBearing(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the provider is able to provide bearing information, false otherwise. A provider that reports bearing under most circumstances but may occassionally not report it should return true. 

### supportsSpeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun supportsSpeed(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the provider is able to provide speed information, false otherwise. A provider that reports speed under most circumstances but may occassionally not report it should return true.
