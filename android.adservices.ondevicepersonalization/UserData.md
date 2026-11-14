Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserData

```
class UserData : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.UserData](UserData.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

User data provided by the platform to an IsolatedService.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [AppInfo](AppInfo.md)!\> | getAppInfos A map from package name to app information for installed and uninstalled apps. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAvailableStorageBytes The available space on device in bytes. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBatteryPercentage Battery percentage. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getCarrier The Service Provider Name (SPN) returned by getSimOperatorName |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDataNetworkType Data network type. |
| [NetworkCapabilities](../android.net/NetworkCapabilities.md)? | getNetworkCapabilities A filtered subset of the Network capabilities of the device that contains upstream and downstream speeds, and whether the network is metered. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOrientation The device orientation. |
| --- | --- |
| [Duration](../java.time/Duration.md) | getTimezoneUtcOffset The device timezone +/- offset from UTC. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [UserData](UserData.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/UserData#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

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
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAppInfos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAppInfos(): MutableMap<String!, AppInfo!>
```

**Deprecated:** *Deprecated in Java.*

A map from package name to app information for installed and uninstalled apps.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/AppInfo!>` | This value cannot be `null`. |

### getAvailableStorageBytes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableStorageBytes(): Long
```

**Deprecated:** *Deprecated in Java.*

The available space on device in bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is 0 or greater |

### getBatteryPercentage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBatteryPercentage(): Int
```

**Deprecated:** *Deprecated in Java.*

Battery percentage.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 0 and 100 inclusive |

### getCarrier

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCarrier(): String
```

**Deprecated:** *Deprecated in Java.*

The Service Provider Name (SPN) returned by getSimOperatorName

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getDataNetworkType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataNetworkType(): Int
```

**Deprecated:** *Deprecated in Java.*

Data network type. This is the value of getDataNetworkType.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_GPRS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_UMTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_CDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_EVDO_0:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_EVDO_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_1xRTT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_HSDPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_HSUPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_HSPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_EVDO_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_LTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_EHRPD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_HSPAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_GSM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_TD_SCDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_IWLAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_NR:kotlin.Int` |

### getNetworkCapabilities

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNetworkCapabilities(): NetworkCapabilities?
```

**Deprecated:** *Deprecated in Java.*

A filtered subset of the Network capabilities of the device that contains upstream and downstream speeds, and whether the network is metered. This is an instance of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#` that contains the capability `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_NOT_METERED:kotlin.Int` if the network is not metered, and getLinkDownstreamBandwidthKbps and getLinkUpstreamBandwidthKbps return the downstream and upstream connection speeds. All other methods of this `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#` object return empty or default values.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#?` | This value may be `null`. |

### getOrientation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOrientation(): Int
```

**Deprecated:** *Deprecated in Java.*

The device orientation. The value can be one of the constants ORIENTATION_UNDEFINED, ORIENTATION_PORTRAIT or ORIENTATION_LANDSCAPE defined in `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#ORIENTATION_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#ORIENTATION_PORTRAIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#ORIENTATION_LANDSCAPE:kotlin.Int` |

### getTimezoneUtcOffset

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimezoneUtcOffset(): Duration
```

**Deprecated:** *Deprecated in Java.*

The device timezone +/- offset from UTC.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#` | This value cannot be `null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<UserData!>
```

**Deprecated:** *Deprecated in Java.*
