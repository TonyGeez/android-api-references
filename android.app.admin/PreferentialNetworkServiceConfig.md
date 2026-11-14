Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferentialNetworkServiceConfig

```
class PreferentialNetworkServiceConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.admin.PreferentialNetworkServiceConfig](https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#) |

Network configuration to be set for the user profile.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig.Builder` Builder used to create `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#` objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_1:kotlin.Int` Preferential network identifier 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_2:kotlin.Int` Preferential network identifier 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_3:kotlin.Int` Preferential network identifier 3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_4:kotlin.Int` Preferential network identifier 4. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_5:kotlin.Int` Preferential network identifier 5. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#getExcludedUids()()` Get the array of uids that are excluded for the profile preference. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#getIncludedUids()()` Get the array of uids that are applicable for the profile preference. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#getNetworkId()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#isEnabled()()` Is the preferential network enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#isFallbackToDefaultConnectionAllowed()()` Whether fallback to the device-wide default network is allowed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#shouldBlockNonMatchingNetworks()()` Whether to block UIDs from using other networks than the preferential service. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PreferentialNetworkServiceConfig](https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#)!\> | `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### PREFERENTIAL_NETWORK_ID_1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREFERENTIAL_NETWORK_ID_1: Int
```

Preferential network identifier 1.

 Value: 1

### PREFERENTIAL_NETWORK_ID_2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREFERENTIAL_NETWORK_ID_2: Int
```

Preferential network identifier 2.

 Value: 2

### PREFERENTIAL_NETWORK_ID_3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREFERENTIAL_NETWORK_ID_3: Int
```

Preferential network identifier 3.

 Value: 3

### PREFERENTIAL_NETWORK_ID_4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREFERENTIAL_NETWORK_ID_4: Int
```

Preferential network identifier 4.

 Value: 4

### PREFERENTIAL_NETWORK_ID_5

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREFERENTIAL_NETWORK_ID_5: Int
```

Preferential network identifier 5.

 Value: 5

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getExcludedUids

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExcludedUids(): IntArray
```

Get the array of uids that are excluded for the profile preference.

Included UIDs and Excluded UIDs can't both be non-empty. if both are empty, it means this request applies to all uids in the user profile. if included is not empty, then only included UIDs are applied. if excluded is not empty, then it is all uids in the user profile except these UIDs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | Array of uids that are excluded for the profile preference. Empty array would mean that this request applies to all uids in the profile. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#getIncludedUids()`

### getIncludedUids

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIncludedUids(): IntArray
```

Get the array of uids that are applicable for the profile preference.

Included UIDs and Excluded UIDs can't both be non-empty. if both are empty, it means this request applies to all uids in the user profile. if included is not empty, then only included UIDs are applied. if excluded is not empty, then it is all uids in the user profile except these UIDs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | Array of uids applicable for the profile preference. Empty array would mean that this request applies to all uids in the profile. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#getExcludedUids()`

### getNetworkId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNetworkId(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | preference enterprise identifier. preference identifier is applicable only if preference network service is enabled. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#PREFERENTIAL_NETWORK_ID_5:kotlin.Int` |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEnabled(): Boolean
```

Is the preferential network enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if enabled else false |

### isFallbackToDefaultConnectionAllowed

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFallbackToDefaultConnectionAllowed(): Boolean
```

Whether fallback to the device-wide default network is allowed.

This boolean configures whether the default connection (e.g. general cell network or wifi) should be used if no preferential network service connection is available. If true, the default connection will be used when no preferential service is available. If false, the UIDs subject to this configuration will have no default network. Note that while this boolean determines whether the UIDs subject to this configuration have a default network in the absence of a preferential service, apps can still explicitly decide to use another network than their default network by requesting them from the system. This boolean does not determine whether the UIDs are blocked from using such other networks. See `https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig#shouldBlockNonMatchingNetworks()` for that configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if fallback is allowed, else false. |

### shouldBlockNonMatchingNetworks

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun shouldBlockNonMatchingNetworks(): Boolean
```

Whether to block UIDs from using other networks than the preferential service.

Apps can inspect the list of available networks on the device and choose to use multiple of them concurrently for performance, privacy or other reasons. This boolean configures whether the concerned UIDs should be blocked from using networks that do not match the configured preferential network service even if these networks are otherwise open to all apps.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if UIDs should be blocked from using the other networks, else false. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PreferentialNetworkServiceConfig!>
```
