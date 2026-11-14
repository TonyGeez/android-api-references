# Criteria

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Criteria

Kotlin | [Java](../android/location/Criteria.md) 
| --- | --- |

```
open class Criteria : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.Criteria](../android/location/Criteria.md) |

| **This class was deprecated in API level 34.**
|
| Criteria based APIs are deprecated because they cannot fully capture the complexity of location providers, and encourage bad development practices. Prefer to explicit select the location provider of interest ([LocationManager.FUSED_PROVIDER](../android/location/LocationManager.md), [etc](../android/location/LocationManager.md)), rather than relying on Criteria.

A class indicating the application criteria for selecting a location provider. Providers may be ordered according to accuracy, power usage, ability to report altitude, speed, bearing, and monetary cost.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_COARSE](../android/location/Criteria.md) A constant indicating an approximate accuracy requirement |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_FINE](../android/location/Criteria.md) A constant indicating a finer location accuracy requirement |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_HIGH](../android/location/Criteria.md) a constant indicating a high accuracy requirement - may be used for horizontal, altitude, speed or bearing accuracy. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_LOW](../android/location/Criteria.md) A constant indicating a low location accuracy requirement - may be used for horizontal, altitude, speed or bearing accuracy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_MEDIUM](../android/location/Criteria.md) A constant indicating a medium accuracy requirement - currently used only for horizontal accuracy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_REQUIREMENT](../android/location/Criteria.md) A constant indicating that the application does not choose to place requirement on a particular feature. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_HIGH](../android/location/Criteria.md) A constant indicating a high power requirement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_LOW](../android/location/Criteria.md) A constant indicating a low power requirement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_MEDIUM](../android/location/Criteria.md) A constant indicating a medium power requirement. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Criteria](../android/location/Criteria.md))`()` Constructs a new Criteria object. |
| [Criteria](../android/location/Criteria.md))`(`criteria:` ` [Criteria](../android/location/Criteria.md)!`)` Constructs a new Criteria object that is a copy of the given criteria. |

| Public methods ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/location/Criteria.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAccuracy](../android/location/Criteria.md))`()` Returns a constant indicating desired accuracy of location. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBearingAccuracy](../android/location/Criteria.md))`()` Returns a constant indicating the desired bearing accuracy. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHorizontalAccuracy](../android/location/Criteria.md))`()` Returns a constant indicating the desired horizontal accuracy (latitude and longitude). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPowerRequirement](../android/location/Criteria.md))`()` Returns a constant indicating the desired maximum power requirement. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpeedAccuracy](../android/location/Criteria.md))`()` Returns a constant indicating the desired speed accuracy. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVerticalAccuracy](../android/location/Criteria.md))`()` Returns a constant indicating the desired vertical accuracy (altitude). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAltitudeRequired](../android/location/Criteria.md))`()` Returns whether the provider must provide altitude information. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBearingRequired](../android/location/Criteria.md))`()` Returns whether the provider must provide bearing information. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCostAllowed](../android/location/Criteria.md))`()` Returns whether the provider is allowed to incur monetary cost. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpeedRequired](../android/location/Criteria.md))`()` Returns whether the provider must provide speed information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccuracy](../android/location/Criteria.md))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired accuracy for latitude and longitude. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAltitudeRequired](../android/location/Criteria.md))`(`altitudeRequired:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the provider must provide altitude information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBearingAccuracy](../android/location/Criteria.md))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired bearing accuracy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBearingRequired](../android/location/Criteria.md))`(`bearingRequired:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the provider must provide bearing information. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCostAllowed](../android/location/Criteria.md))`(`costAllowed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the provider is allowed to incur monetary cost. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHorizontalAccuracy](../android/location/Criteria.md))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired horizontal accuracy (latitude and longitude). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPowerRequirement](../android/location/Criteria.md))`(`powerRequirement:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired maximum power requirement. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeedAccuracy](../android/location/Criteria.md))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired speed accuracy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeedRequired](../android/location/Criteria.md))`(`speedRequired:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the provider must provide speed information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVerticalAccuracy](../android/location/Criteria.md))`(`accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the desired vertical accuracy (altitude). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/location/Criteria.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/location/Criteria.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Criteria](../android/location/Criteria.md)!\> | [CREATOR](../android/location/Criteria.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAccuracy(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a constant indicating desired accuracy of location.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_FINE](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_COARSE](../android/location/Criteria.md) |

**See Also**

- [#setAccuracy(int)](../android/location/Criteria.md)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_LOW](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_HIGH](../android/location/Criteria.md) |

**See Also**

- [#setBearingAccuracy(int)](../android/location/Criteria.md)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_LOW](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_HIGH](../android/location/Criteria.md) |

**See Also**

- [#setHorizontalAccuracy(int)](../android/location/Criteria.md)) 

### getPowerRequirement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPowerRequirement(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a constant indicating the desired maximum power requirement.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#POWER_LOW](../android/location/Criteria.md), [android.location.Criteria#POWER_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#POWER_HIGH](../android/location/Criteria.md) |

**See Also**

- [#setPowerRequirement(int)](../android/location/Criteria.md)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_LOW](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_HIGH](../android/location/Criteria.md) |

**See Also**

- [#setSpeedAccuracy(int)](../android/location/Criteria.md)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_LOW](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_HIGH](../android/location/Criteria.md) |

**See Also**

- [#setVerticalAccuracy(int)](../android/location/Criteria.md)) 

### isAltitudeRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAltitudeRequired(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the provider must provide altitude information. 
**See Also**

- [#setAltitudeRequired(boolean)](../android/location/Criteria.md)) 

### isBearingRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBearingRequired(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the provider must provide bearing information. 
**See Also**

- [#setBearingRequired(boolean)](../android/location/Criteria.md)) 

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

- [#setSpeedRequired(boolean)](../android/location/Criteria.md)) 

### setAccuracy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAccuracy(accuracy: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired accuracy for latitude and longitude. Accuracy may be [ACCURACY_FINE](../android/location/Criteria.md) or [ACCURACY_COARSE](../android/location/Criteria.md). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_FINE](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_COARSE](../android/location/Criteria.md) |

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

Indicates the desired bearing accuracy. Accuracy may be [ACCURACY_LOW](../android/location/Criteria.md), [ACCURACY_MEDIUM](../android/location/Criteria.md), [ACCURACY_HIGH](../android/location/Criteria.md), or [NO_REQUIREMENT](../android/location/Criteria.md). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_LOW](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_HIGH](../android/location/Criteria.md) |

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

Indicates the desired horizontal accuracy (latitude and longitude). Accuracy may be [ACCURACY_LOW](../android/location/Criteria.md), [ACCURACY_MEDIUM](../android/location/Criteria.md), [ACCURACY_HIGH](../android/location/Criteria.md) or [NO_REQUIREMENT](../android/location/Criteria.md). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_LOW](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_HIGH](../android/location/Criteria.md) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if accuracy is not one of the supported constants |

### setPowerRequirement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPowerRequirement(powerRequirement: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired maximum power requirement. The power requirement parameter may be [NO_REQUIREMENT](../android/location/Criteria.md), [POWER_LOW](../android/location/Criteria.md), [POWER_MEDIUM](../android/location/Criteria.md), or [POWER_HIGH](../android/location/Criteria.md).

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powerRequirement` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#POWER_LOW](../android/location/Criteria.md), [android.location.Criteria#POWER_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#POWER_HIGH](../android/location/Criteria.md) |

### setSpeedAccuracy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpeedAccuracy(accuracy: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates the desired speed accuracy. Accuracy may be [ACCURACY_LOW](../android/location/Criteria.md), [ACCURACY_MEDIUM](../android/location/Criteria.md), [ACCURACY_HIGH](../android/location/Criteria.md), or [NO_REQUIREMENT](../android/location/Criteria.md). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_LOW](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_HIGH](../android/location/Criteria.md) |

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

Indicates the desired vertical accuracy (altitude). Accuracy may be [ACCURACY_LOW](../android/location/Criteria.md), [ACCURACY_MEDIUM](../android/location/Criteria.md), [ACCURACY_HIGH](../android/location/Criteria.md) or [NO_REQUIREMENT](../android/location/Criteria.md). More accurate location may consume more power and may take longer.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.location.Criteria#NO_REQUIREMENT](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_LOW](../android/location/Criteria.md), [android.location.Criteria#ACCURACY_MEDIUM](../android/location/Criteria.md), or [android.location.Criteria#ACCURACY_HIGH](../android/location/Criteria.md) |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Criteria!>
```

**Deprecated:** *Deprecated in Java.*
