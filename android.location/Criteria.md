# Criteria

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Criteria

Kotlin | [Java](https://developer.android.com/reference/android/location/Criteria "View this page in Java") 

```
open class Criteria : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.location.Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria#) |

| **This class was deprecated in API level 34.**
|
| Criteria based APIs are deprecated because they cannot fully capture the complexity of location providers, and encourage bad development practices. Prefer to explicit select the location provider of interest ([LocationManager.FUSED_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#FUSED_PROVIDER:kotlin.String), [etc](https://developer.android.com/reference/kotlin/android/location/LocationManager#GPS_PROVIDER:kotlin.String)), rather than relying on Criteria.

A class indicating the application criteria for selecting a location provider. Providers may be ordered according to accuracy, power usage, ability to report altitude, speed, bearing, and monetary cost.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_COARSE](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_COARSE:kotlin.Int) A constant indicating an approximate accuracy requirement |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_FINE](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_FINE:kotlin.Int) A constant indicating a finer location accuracy requirement |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) a constant indicating a high accuracy requirement - may be used for horizontal, altitude, speed or bearing accuracy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int) A constant indicating a low location accuracy requirement - may be used for horizontal, altitude, speed or bearing accuracy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int) A constant indicating a medium accuracy requirement - currently used only for horizontal accuracy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int) A constant indicating that the application does not choose to place requirement on a particular feature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_HIGH:kotlin.Int) A constant indicating a high power requirement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_LOW:kotlin.Int) A constant indicating a low power requirement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_MEDIUM:kotlin.Int) A constant indicating a medium power requirement. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria#Criteria())`()` Constructs a new Criteria object. |
| [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria#Criteria(android.location.Criteria))`(`criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria#)!`)` Constructs a new Criteria object that is a copy of the given criteria. |

| Public methods ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/location/Criteria#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#getAccuracy())`()` Returns a constant indicating desired accuracy of location. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBearingAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#getBearingAccuracy())`()` Returns a constant indicating the desired bearing accuracy. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHorizontalAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#getHorizontalAccuracy())`()` Returns a constant indicating the desired horizontal accuracy (latitude and longitude). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPowerRequirement](https://developer.android.com/reference/kotlin/android/location/Criteria#getPowerRequirement())`()` Returns a constant indicating the desired maximum power requirement. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpeedAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#getSpeedAccuracy())`()` Returns a constant indicating the desired speed accuracy. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVerticalAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#getVerticalAccuracy())`()` Returns a constant indicating the desired vertical accuracy (altitude). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAltitudeRequired](https://developer.android.com/reference/kotlin/android/location/Criteria#isAltitudeRequired())`()` Returns whether the provider must provide altitude information. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBearingRequired](https://developer.android.com/reference/kotlin/android/location/Criteria#isBearingRequired())`()` Returns whether the provider must provide bearing information. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCostAllowed](https://developer.android.com/reference/kotlin/android/location/Criteria#isCostAllowed())`()` Returns whether the provider is allowed to incur monetary cost. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpeedRequired](https://developer.android.com/reference/kotlin/android/location/Criteria#isSpeedRequired())`()` Returns whether the provider must provide speed information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#setAccuracy(kotlin.Int))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired accuracy for latitude and longitude. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAltitudeRequired](https://developer.android.com/reference/kotlin/android/location/Criteria#setAltitudeRequired(kotlin.Boolean))`(`altitudeRequired:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the provider must provide altitude information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBearingAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#setBearingAccuracy(kotlin.Int))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired bearing accuracy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBearingRequired](https://developer.android.com/reference/kotlin/android/location/Criteria#setBearingRequired(kotlin.Boolean))`(`bearingRequired:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the provider must provide bearing information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCostAllowed](https://developer.android.com/reference/kotlin/android/location/Criteria#setCostAllowed(kotlin.Boolean))`(`costAllowed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the provider is allowed to incur monetary cost. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHorizontalAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#setHorizontalAccuracy(kotlin.Int))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired horizontal accuracy (latitude and longitude). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPowerRequirement](https://developer.android.com/reference/kotlin/android/location/Criteria#setPowerRequirement(kotlin.Int))`(`powerRequirement:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired maximum power requirement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeedAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#setSpeedAccuracy(kotlin.Int))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired speed accuracy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeedRequired](https://developer.android.com/reference/kotlin/android/location/Criteria#setSpeedRequired(kotlin.Boolean))`(`speedRequired:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the provider must provide speed information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVerticalAccuracy](https://developer.android.com/reference/kotlin/android/location/Criteria#setVerticalAccuracy(kotlin.Int))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired vertical accuracy (altitude). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/location/Criteria#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/location/Criteria#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/location/Criteria#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ACCURACY_COARSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCURACY_COARSE: Int
```

**Deprecated:** *Deprecated in Java.*

A constant indicating an approximate accuracy requirement 

 Value: 2

### ACCURACY_FINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCURACY_FINE: Int
```

**Deprecated:** *Deprecated in Java.*

A constant indicating a finer location accuracy requirement 

 Value: 1

### ACCURACY_HIGH

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCURACY_HIGH: Int
```

**Deprecated:** *Deprecated in Java.*

a constant indicating a high accuracy requirement - may be used for horizontal, altitude, speed or bearing accuracy. For horizontal and vertical position this corresponds roughly to an accuracy of less than 100 meters. 

 Value: 3

### ACCURACY_LOW

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCURACY_LOW: Int
```

**Deprecated:** *Deprecated in Java.*

A constant indicating a low location accuracy requirement - may be used for horizontal, altitude, speed or bearing accuracy. For horizontal and vertical position this corresponds roughly to an accuracy of greater than 500 meters. 

 Value: 1

### ACCURACY_MEDIUM

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCURACY_MEDIUM: Int
```

**Deprecated:** *Deprecated in Java.*

A constant indicating a medium accuracy requirement - currently used only for horizontal accuracy. For horizontal position this corresponds roughly to to an accuracy of between 100 and 500 meters. 

 Value: 2

### NO_REQUIREMENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_REQUIREMENT: Int
```

**Deprecated:** *Deprecated in Java.*

A constant indicating that the application does not choose to place requirement on a particular feature. 

 Value: 0

### POWER_HIGH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POWER_HIGH: Int
```

**Deprecated:** *Deprecated in Java.*

A constant indicating a high power requirement. 

 Value: 3

### POWER_LOW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POWER_LOW: Int
```

**Deprecated:** *Deprecated in Java.*

A constant indicating a low power requirement. 

 Value: 1

### POWER_MEDIUM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POWER_MEDIUM: Int
```

**Deprecated:** *Deprecated in Java.*

A constant indicating a medium power requirement. 

 Value: 2

## Public constructors

### Criteria

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Criteria()
```

Constructs a new Criteria object. The new object will have no requirements on accuracy, power, or response time; will not require altitude, speed, or bearing; and will not allow monetary cost. 

### Criteria

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Criteria(criteria: Criteria!)
```

Constructs a new Criteria object that is a copy of the given criteria.

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAccuracy(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a constant indicating desired accuracy of location.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_FINE](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_FINE:kotlin.Int), or [android.location.Criteria#ACCURACY_COARSE](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_COARSE:kotlin.Int) |

**See Also**

- [#setAccuracy(int)](https://developer.android.com/reference/kotlin/android/location/Criteria#setAccuracy(kotlin.Int)) 

### getBearingAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBearingAccuracy(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a constant indicating the desired bearing accuracy.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [android.location.Criteria#ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), or [android.location.Criteria#ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) |

**See Also**

- [#setBearingAccuracy(int)](https://developer.android.com/reference/kotlin/android/location/Criteria#setBearingAccuracy(kotlin.Int)) 

### getHorizontalAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHorizontalAccuracy(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a constant indicating the desired horizontal accuracy (latitude and longitude).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [android.location.Criteria#ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), or [android.location.Criteria#ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) |

**See Also**

- [#setHorizontalAccuracy(int)](https://developer.android.com/reference/kotlin/android/location/Criteria#setHorizontalAccuracy(kotlin.Int)) 

### getPowerRequirement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPowerRequirement(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a constant indicating the desired maximum power requirement.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#POWER_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_LOW:kotlin.Int), [android.location.Criteria#POWER_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_MEDIUM:kotlin.Int), or [android.location.Criteria#POWER_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_HIGH:kotlin.Int) |

**See Also**

- [#setPowerRequirement(int)](https://developer.android.com/reference/kotlin/android/location/Criteria#setPowerRequirement(kotlin.Int)) 

### getSpeedAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpeedAccuracy(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a constant indicating the desired speed accuracy.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [android.location.Criteria#ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), or [android.location.Criteria#ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) |

**See Also**

- [#setSpeedAccuracy(int)](https://developer.android.com/reference/kotlin/android/location/Criteria#setSpeedAccuracy(kotlin.Int)) 

### getVerticalAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVerticalAccuracy(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a constant indicating the desired vertical accuracy (altitude).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [android.location.Criteria#ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), or [android.location.Criteria#ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) |

**See Also**

- [#setVerticalAccuracy(int)](https://developer.android.com/reference/kotlin/android/location/Criteria#setVerticalAccuracy(kotlin.Int)) 

### isAltitudeRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAltitudeRequired(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the provider must provide altitude information. 
**See Also**

- [#setAltitudeRequired(boolean)](https://developer.android.com/reference/kotlin/android/location/Criteria#setAltitudeRequired(kotlin.Boolean)) 

### isBearingRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBearingRequired(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the provider must provide bearing information. 
**See Also**

- [#setBearingRequired(boolean)](https://developer.android.com/reference/kotlin/android/location/Criteria#setBearingRequired(kotlin.Boolean)) 

### isCostAllowed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCostAllowed(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the provider is allowed to incur monetary cost. 

### isSpeedRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSpeedRequired(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the provider must provide speed information. 
**See Also**

- [#setSpeedRequired(boolean)](https://developer.android.com/reference/kotlin/android/location/Criteria#setSpeedRequired(kotlin.Boolean)) 

### setAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAccuracy(accuracy: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired accuracy for latitude and longitude. Accuracy may be [ACCURACY_FINE](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_FINE:kotlin.Int) or [ACCURACY_COARSE](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_COARSE:kotlin.Int). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_FINE](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_FINE:kotlin.Int), or [android.location.Criteria#ACCURACY_COARSE](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_COARSE:kotlin.Int) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if accuracy is not one of the supported constants |

### setAltitudeRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAltitudeRequired(altitudeRequired: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates whether the provider must provide altitude information. Not all fixes are guaranteed to contain such information. 

### setBearingAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBearingAccuracy(accuracy: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired bearing accuracy. Accuracy may be [ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), [ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int), or [NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [android.location.Criteria#ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), or [android.location.Criteria#ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if accuracy is not one of the supported constants |

### setBearingRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBearingRequired(bearingRequired: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates whether the provider must provide bearing information. Not all fixes are guaranteed to contain such information. 

### setCostAllowed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCostAllowed(costAllowed: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates whether the provider is allowed to incur monetary cost. 

### setHorizontalAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHorizontalAccuracy(accuracy: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired horizontal accuracy (latitude and longitude). Accuracy may be [ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), [ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) or [NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [android.location.Criteria#ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), or [android.location.Criteria#ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if accuracy is not one of the supported constants |

### setPowerRequirement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPowerRequirement(powerRequirement: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired maximum power requirement. The power requirement parameter may be [NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [POWER_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_LOW:kotlin.Int), [POWER_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_MEDIUM:kotlin.Int), or [POWER_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_HIGH:kotlin.Int).

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powerRequirement` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#POWER_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_LOW:kotlin.Int), [android.location.Criteria#POWER_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_MEDIUM:kotlin.Int), or [android.location.Criteria#POWER_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#POWER_HIGH:kotlin.Int) |

### setSpeedAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpeedAccuracy(accuracy: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired speed accuracy. Accuracy may be [ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), [ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int), or [NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [android.location.Criteria#ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), or [android.location.Criteria#ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if accuracy is not one of the supported constants |

### setSpeedRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpeedRequired(speedRequired: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates whether the provider must provide speed information. Not all fixes are guaranteed to contain such information. 

### setVerticalAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVerticalAccuracy(accuracy: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired vertical accuracy (altitude). Accuracy may be [ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), [ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) or [NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](https://developer.android.com/reference/kotlin/android/location/Criteria#NO_REQUIREMENT:kotlin.Int), [android.location.Criteria#ACCURACY_LOW](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_LOW:kotlin.Int), [android.location.Criteria#ACCURACY_MEDIUM](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_MEDIUM:kotlin.Int), or [android.location.Criteria#ACCURACY_HIGH](https://developer.android.com/reference/kotlin/android/location/Criteria#ACCURACY_HIGH:kotlin.Int) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if accuracy is not one of the supported constants |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Criteria!>
```

**Deprecated:** *Deprecated in Java.*
