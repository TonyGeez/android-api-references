Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pUsdBasedServiceConfig

Kotlin | [Java](https://developer.android.com/reference/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig "View this page in Java")
| --- | --- |

```
class WifiP2pUsdBasedServiceConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#) |

A class for creating a USD based service discovery configuration for use with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo`. 
or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest`. 
For the details of the configuration, refer Wi-Fi Alliance Wi-Fi Direct R2 specification - Appendix H - Unsynchronized Service Discovery (as defined in Wi-Fi Aware) and section 4.2.13 USD frame format.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig.Builder` Builder used to build `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#` objects for USD based service discovery and advertisement. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#SERVICE_PROTOCOL_TYPE_BONJOUR:kotlin.Int` Bonjour service protocol type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#SERVICE_PROTOCOL_TYPE_GENERIC:kotlin.Int` Generic service protocol type |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#WifiP2pUsdBasedServiceConfig()()` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#describeContents()()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#getMaxAllowedServiceSpecificInfoLength()()` Maximum allowed length of service specific information that can be set in the USD service configuration. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#getServiceName()()` Get the service name of this USD service configuration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#getServiceProtocolType()()` Get the service protocol type of this USD service configuration. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#getServiceSpecificInfo()()` Get the service specific info of this USD service configuration. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#toString()()` Generates a string of all the defined elements. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Implement the Parcelable interface |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiP2pUsdBasedServiceConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig#CREATOR:android.os.Parcelable.Creator` Implement the Parcelable interface |

## Constants

### SERVICE_PROTOCOL_TYPE_BONJOUR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_PROTOCOL_TYPE_BONJOUR: Int
```

Bonjour service protocol type

 Value: 1

### SERVICE_PROTOCOL_TYPE_GENERIC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_PROTOCOL_TYPE_GENERIC: Int
```

Generic service protocol type

 Value: 2

## Public constructors

### WifiP2pUsdBasedServiceConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WifiP2pUsdBasedServiceConfig()
```

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getMaxAllowedServiceSpecificInfoLength

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMaxAllowedServiceSpecificInfoLength(): Int
```

Maximum allowed length of service specific information that can be set in the USD service configuration. See also `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig.Builder#setServiceSpecificInfo(kotlin.ByteArray)`.

### getServiceName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceName(): String
```

Get the service name of this USD service configuration. See also `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig.Builder`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | UTF-8 string defining the service. This value cannot be `null`. |

### getServiceProtocolType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceProtocolType(): Int
```

Get the service protocol type of this USD service configuration. See also `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig.Builder#setServiceProtocolType(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A non-negative service layer protocol type. Value is between 0 and 255 inclusive |

### getServiceSpecificInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceSpecificInfo(): ByteArray?
```

Get the service specific info of this USD service configuration. See also `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig.Builder#setServiceSpecificInfo(kotlin.ByteArray)` .

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | A byte-array of service specification information, or null if unset. |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Generates a string of all the defined elements.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a compiled string representing all elements |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<WifiP2pUsdBasedServiceConfig!>
```

Implement the Parcelable interface
