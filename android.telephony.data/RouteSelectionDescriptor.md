# RouteSelectionDescriptor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RouteSelectionDescriptor

Kotlin| [Java](https://developer.android.com/reference/android/telephony/data/RouteSelectionDescriptor "View this page in Java") 

```
class RouteSelectionDescriptor : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.data.RouteSelectionDescriptor](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#) |

Represents a single route selection descriptor as defined in 3GPP TS 24.526.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_SSC_MODE_1](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#ROUTE_SSC_MODE_1:kotlin.Int) The route selection descriptor is using SSC mode 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_SSC_MODE_2](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#ROUTE_SSC_MODE_2:kotlin.Int) The route selection descriptor is using SSC mode 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_SSC_MODE_3](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#ROUTE_SSC_MODE_3:kotlin.Int) The route selection descriptor is using SSC mode 3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_TYPE_IPV4](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#SESSION_TYPE_IPV4:kotlin.Int) The route selection descriptor is for the session with IPV4 type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_TYPE_IPV4V6](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#SESSION_TYPE_IPV4V6:kotlin.Int) The route selection descriptor is for the session with both IP and IPV6 types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_TYPE_IPV6](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#SESSION_TYPE_IPV6:kotlin.Int) The route selection descriptor is for the session with IPV6 type. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDataNetworkName](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#getDataNetworkName())`()` DNN stands for Data Network Name and represents an APN as defined in 3GPP TS 23. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrecedence](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#getPrecedence())`()` Precedence value in the range of 0 to 255. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSessionType](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#getSessionType())`()` This is used for checking which session type defined in 3GPP TS 23. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [NetworkSliceInfo](https://developer.android.com/reference/kotlin/android/telephony/data/NetworkSliceInfo)!\> | [getSliceInfo](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#getSliceInfo())`()` This is the list of all the slices available in the route selection descriptor as indicated by the network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSscMode](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#getSscMode())`()` SSC mode stands for Session and Service Continuity mode (which specifies the IP continuity mode) as defined in 3GPP TS 23. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RouteSelectionDescriptor](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ROUTE_SSC_MODE_1

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUTE_SSC_MODE_1: Int
```

The route selection descriptor is using SSC mode 1. The session will provide continual support when UE's location is updated. 

 Value: 1

### ROUTE_SSC_MODE_2

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUTE_SSC_MODE_2: Int
```

The route selection descriptor is using SSC mode 2. The new session for the same network will be established after releasing the old session when UE's location is updated. 

 Value: 2

### ROUTE_SSC_MODE_3

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUTE_SSC_MODE_3: Int
```

The route selection descriptor is using SSC mode 3. The new session for the same network is allowed to be established before releasing the old session when UE's location is updated. 

 Value: 3

### SESSION_TYPE_IPV4

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_TYPE_IPV4: Int
```

The route selection descriptor is for the session with IPV4 type. 

 Value: 0

### SESSION_TYPE_IPV4V6

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_TYPE_IPV4V6: Int
```

The route selection descriptor is for the session with both IP and IPV6 types. 

 Value: 2

### SESSION_TYPE_IPV6

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_TYPE_IPV6: Int
```

The route selection descriptor is for the session with IPV6 type. 

 Value: 1

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

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

### getDataNetworkName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataNetworkName(): MutableList<String!>
```

DNN stands for Data Network Name and represents an APN as defined in 3GPP TS 23.003. There can be 0 or more DNNs specified in a route selection descriptor.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | the list of DNN for this route selection descriptor. This value cannot be`null`. |

### getPrecedence

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrecedence(): Int
```

Precedence value in the range of 0 to 255. Higher value has lower precedence.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the precedence value for this route selection descriptor. Value is between android.telephony.data.RouteSelectionDescriptor#MIN_ROUTE_PRECEDENCE and android.telephony.data.RouteSelectionDescriptor#MAX_ROUTE_PRECEDENCE inclusive |

### getSessionType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionType(): Int
```

This is used for checking which session type defined in 3GPP TS 23.501 is allowed for the route in a route selection descriptor.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the session type for this route selection descriptor. Value is [android.telephony.data.RouteSelectionDescriptor#SESSION_TYPE_IPV4](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#SESSION_TYPE_IPV4:kotlin.Int), [android.telephony.data.RouteSelectionDescriptor#SESSION_TYPE_IPV6](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#SESSION_TYPE_IPV6:kotlin.Int), or [android.telephony.data.RouteSelectionDescriptor#SESSION_TYPE_IPV4V6](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#SESSION_TYPE_IPV4V6:kotlin.Int) |

### getSliceInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSliceInfo(): MutableList<NetworkSliceInfo!>
```

This is the list of all the slices available in the route selection descriptor as indicated by the network. These are the slices that can be used by the device if this route selection descriptor is used based the traffic (see 3GPP TS 23.501 for details).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [NetworkSliceInfo](https://developer.android.com/reference/kotlin/android/telephony/data/NetworkSliceInfo)!> | the list of all the slices available in the route selection descriptor. This value cannot be`null`. |

### getSscMode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSscMode(): Int
```

SSC mode stands for Session and Service Continuity mode (which specifies the IP continuity mode) as defined in 3GPP TS 23.501.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the SSC mode for this route selection descriptor. Value is [android.telephony.data.RouteSelectionDescriptor#ROUTE_SSC_MODE_1](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#ROUTE_SSC_MODE_1:kotlin.Int), [android.telephony.data.RouteSelectionDescriptor#ROUTE_SSC_MODE_2](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#ROUTE_SSC_MODE_2:kotlin.Int), or [android.telephony.data.RouteSelectionDescriptor#ROUTE_SSC_MODE_3](https://developer.android.com/reference/kotlin/android/telephony/data/RouteSelectionDescriptor#ROUTE_SSC_MODE_3:kotlin.Int) |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RouteSelectionDescriptor!>
```
