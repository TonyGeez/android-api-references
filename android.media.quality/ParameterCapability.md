# ParameterCapability

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParameterCapability

Kotlin| [Java](https://developer.android.com/reference/android/media/quality/ParameterCapability "View this page in Java") 
| --- | --- |

```
class ParameterCapability : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.quality.ParameterCapability](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#) |

Capability info of media quality parameters

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAPABILITY_DEFAULT](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#CAPABILITY_DEFAULT:kotlin.String) The key for the default value of this parameter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAPABILITY_ENUM](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#CAPABILITY_ENUM:kotlin.String) The key for the enumeration of this parameter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAPABILITY_MAX](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#CAPABILITY_MAX:kotlin.String) The key for the max possible value of this parameter. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAPABILITY_MIN](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#CAPABILITY_MIN:kotlin.String) The key for the min possible value of this parameter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DOUBLE](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_DOUBLE:kotlin.Int) Double parameter type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_INT:kotlin.Int) Integer parameter type |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LONG](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_LONG:kotlin.Int) Long integer parameter type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NONE](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_NONE:kotlin.Int) None parameter type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STRING](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_STRING:kotlin.Int) String parameter type |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#describeContents())`()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getCapabilities](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#getCapabilities())`()` Gets capability information. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getParameterName](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#getParameterName())`()` Gets parameter name. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameterType](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#getParameterType())`()` Gets parameter type. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#isSupported())`()` Returns whether this parameter is supported or not. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ParameterCapability](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CAPABILITY_DEFAULT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_DEFAULT: String
```

The key for the default value of this parameter. 

 Value: "default"

### CAPABILITY_ENUM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_ENUM: String
```

The key for the enumeration of this parameter. 

 Value: "enum"

### CAPABILITY_MAX

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_MAX: String
```

The key for the max possible value of this parameter. 

 Value: "max"

### CAPABILITY_MIN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_MIN: String
```

The key for the min possible value of this parameter. 

 Value: "min"

### TYPE_DOUBLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DOUBLE: Int
```

Double parameter type 

 Value: 3

### TYPE_INT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INT: Int
```

Integer parameter type 

 Value: 1

### TYPE_LONG

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LONG: Int
```

Long integer parameter type 

 Value: 2

### TYPE_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NONE: Int
```

None parameter type. It's used when a parameter is not supported. 

 Value: 0

### TYPE_STRING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_STRING: Int
```

String parameter type 

 Value: 4

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCapabilities

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapabilities(): Bundle
```

Gets capability information.

e.g. use the key [CAPABILITY_MAX](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#CAPABILITY_MAX:kotlin.String) to get the max value. 

### getParameterName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameterName(): String
```

Gets parameter name. 

### getParameterType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameterType(): Int
```

Gets parameter type.

It's [TYPE_NONE](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_NONE:kotlin.Int) if [isSupported()](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#isSupported())is`false`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.media.quality.ParameterCapability#TYPE_NONE](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_NONE:kotlin.Int), [android.media.quality.ParameterCapability#TYPE_INT](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_INT:kotlin.Int), [android.media.quality.ParameterCapability#TYPE_LONG](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_LONG:kotlin.Int), [android.media.quality.ParameterCapability#TYPE_DOUBLE](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_DOUBLE:kotlin.Int), and [android.media.quality.ParameterCapability#TYPE_STRING](https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability#TYPE_STRING:kotlin.Int) |

### isSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(): Boolean
```

Returns whether this parameter is supported or not. 

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ParameterCapability!>
```
