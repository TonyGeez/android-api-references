Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocationRequest

Kotlin | [Java](../android/location/LocationRequest.md)
| --- | --- |

```
class LocationRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.LocationRequest](../android/location/LocationRequest.md) |

An encapsulation of various parameters for requesting location via `https://developer.android.com/reference/kotlin/android/location/LocationManager`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/location/LocationRequest.Builder` A builder class for `https://developer.android.com/reference/kotlin/android/location/LocationRequest#`. |

| Constants ||
|---|---|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#PASSIVE_INTERVAL:kotlin.Long` Represents a passive only request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#QUALITY_BALANCED_POWER_ACCURACY:kotlin.Int` A quality constant indicating a location provider may choose to satisfy this request by equally balancing power and accuracy constraints. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#QUALITY_HIGH_ACCURACY:kotlin.Int` A quality constant indicating a location provider may choose to satisfy this request by providing very accurate locations at the expense of potentially increased power usage. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#QUALITY_LOW_POWER:kotlin.Int` A quality constant indicating a location provider may choose to satisfy this request by providing less accurate locations in order to save power. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getDurationMillis()()` Returns the duration for which location will be provided before the request is automatically removed. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getIntervalMillis()()` Returns the desired interval of location updates, or `https://developer.android.com/reference/kotlin/android/location/LocationRequest#PASSIVE_INTERVAL:kotlin.Long` if this is a passive, no power request. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getMaxUpdateDelayMillis()()` Returns the maximum time any location update may be delayed, and thus grouped with following updates to enable location batching. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getMaxUpdates()()` Returns the maximum number of location updates for this request before the request is automatically removed. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getMinUpdateDistanceMeters()()` Returns the minimum distance between location updates. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getMinUpdateIntervalMillis()()` Returns the minimum update interval. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getQuality()()` Returns the quality hint for this location request. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [LocationRequest](../android/location/LocationRequest.md)!\> | `https://developer.android.com/reference/kotlin/android/location/LocationRequest#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### PASSIVE_INTERVAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PASSIVE_INTERVAL: Long
```

Represents a passive only request. Such a request will not trigger any active locations or power usage itself, but may receive locations generated in response to other requests.

 Value: 9223372036854775807L

**See Also**

- `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getIntervalMillis()`

### QUALITY_BALANCED_POWER_ACCURACY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUALITY_BALANCED_POWER_ACCURACY: Int
```

A quality constant indicating a location provider may choose to satisfy this request by equally balancing power and accuracy constraints. Each location provider may interpret this field differently, but location providers will generally use their default behavior when this flag is present.

 Value: 102

### QUALITY_HIGH_ACCURACY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUALITY_HIGH_ACCURACY: Int
```

A quality constant indicating a location provider may choose to satisfy this request by providing very accurate locations at the expense of potentially increased power usage. Each location provider may interpret this field differently, but as an example, the network provider may choose to return only wifi based locations rather than cell based locations in order to have greater accuracy when this flag is present.

 Value: 100

### QUALITY_LOW_POWER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUALITY_LOW_POWER: Int
```

A quality constant indicating a location provider may choose to satisfy this request by providing less accurate locations in order to save power. Each location provider may interpret this field differently, but as an example, the network provider may choose to return cell based locations rather than wifi based locations in order to save power when this flag is present.

 Value: 104

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getDurationMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDurationMillis(): Long
```

Returns the duration for which location will be provided before the request is automatically removed. A duration of `Long.MAX_VALUE` represents an unlimited duration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the duration for which location will be provided. Value is 1 or greater |

### getIntervalMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIntervalMillis(): Long
```

Returns the desired interval of location updates, or `https://developer.android.com/reference/kotlin/android/location/LocationRequest#PASSIVE_INTERVAL:kotlin.Long` if this is a passive, no power request. A passive request will not actively generate location updates (and thus will not be power blamed for location), but may receive location updates generated as a result of other location requests. A passive request must always have an explicit minimum update interval set.

Locations may be available at a faster interval than specified here, see `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getMinUpdateIntervalMillis()` for the behavior in that case.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the desired interval of location updates. Value is 0 or greater |

### getMaxUpdateDelayMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxUpdateDelayMillis(): Long
```

Returns the maximum time any location update may be delayed, and thus grouped with following updates to enable location batching. If the maximum update delay is equal to or greater than twice the interval, then location providers may provide batched results. The maximum batch size is the maximum update delay divided by the interval. Not all devices or location providers support batching, and use of this parameter does not guarantee that the client will see batched results, or that batched results will always be of the maximum size. When available, batching can provide substantial power savings to the device, and clients are encouraged to take advantage where appropriate for the use case.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the maximum time by which a location update may be delayed. Value is 0 or greater |

**See Also**

- `https://developer.android.com/reference/kotlin/android/location/LocationListener#onLocationChanged(kotlin.collections.MutableList)`

### getMaxUpdates

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxUpdates(): Int
```

Returns the maximum number of location updates for this request before the request is automatically removed. A max updates value of `Integer.MAX_VALUE` represents an unlimited number of updates.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 1 and `https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int` inclusive |

### getMinUpdateDistanceMeters

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinUpdateDistanceMeters(): Float
```

Returns the minimum distance between location updates. If a potential location update is closer to the last location update than the minimum update distance, then the potential location update will not occur. A value of 0 meters implies that no location update will ever be rejected due to failing this constraint.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the minimum distance between location updates. Value is between 0.0f and `https://developer.android.com/reference/kotlin/java/lang/Float.html#MAX_VALUE:kotlin.Float` inclusive |

### getMinUpdateIntervalMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinUpdateIntervalMillis(): Long
```

Returns the minimum update interval. If location updates are available faster than the request interval then locations will only be updated if the minimum update interval has expired since the last location update.

**Note:** Some allowance for jitter is already built into the minimum update interval, so you need not worry about updates blocked simply because they arrived a fraction of a second earlier than expected.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the minimum update interval. Value is 0 or greater |

### getQuality

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQuality(): Int
```

Returns the quality hint for this location request. The quality hint informs the provider how it should attempt to manage any accuracy vs power tradeoffs while attempting to satisfy this location request.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the desired quality tradeoffs between accuracy and power. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/location/LocationRequest#QUALITY_LOW_POWER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/LocationRequest#QUALITY_BALANCED_POWER_ACCURACY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/LocationRequest#QUALITY_HIGH_ACCURACY:kotlin.Int` |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `parcel` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<LocationRequest!>
```
