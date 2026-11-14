Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PublishConfig

```
class PublishConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.PublishConfig](PublishConfig.md) |

Defines the configuration of an Aware publish session. Built using `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder`. A publish session is created using `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler)` or updated using `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession#updatePublish(android.net.wifi.aware.PublishConfig)`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder` Builder used to build `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#` objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#PUBLISH_TYPE_SOLICITED:kotlin.Int` Defines a solicited publish session - a publish session which is silent, waiting for a matching active subscribe session - and responding to it in unicast. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#PUBLISH_TYPE_UNSOLICITED:kotlin.Int` Defines an unsolicited publish session - a publish session where the publisher is advertising itself by broadcasting on-the-air. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#getInstantCommunicationBand()()` Get the Wi-Fi band for instant communication mode for this publish session |
| --- | --- |
| [AwarePairingConfig](AwarePairingConfig.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#getPairingConfig()()` Get the Aware Pairing config for this publish session |
| [WifiAwareDataPathSecurityConfig](WifiAwareDataPathSecurityConfig.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#getSecurityConfig()()` Get the data-path security config for this publish session |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#isFrameworkOffloadedPairingEnabled()()` Get whether framework offloaded pairing is enabled for this publish config. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#isInstantCommunicationModeEnabled()()` Check if instant communication mode is enabled for this publish session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PublishConfig](PublishConfig.md)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### PUBLISH_TYPE_SOLICITED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PUBLISH_TYPE_SOLICITED: Int
```

Defines a solicited publish session - a publish session which is silent, waiting for a matching active subscribe session - and responding to it in unicast. A solicited publish session is paired with an active subscribe session `https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig#SUBSCRIBE_TYPE_ACTIVE:kotlin.Int`. Configuration is done using `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setPublishType(kotlin.Int)`.

 Value: 1

### PUBLISH_TYPE_UNSOLICITED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PUBLISH_TYPE_UNSOLICITED: Int
```

Defines an unsolicited publish session - a publish session where the publisher is advertising itself by broadcasting on-the-air. An unsolicited publish session is paired with a passive subscribe session `https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig#SUBSCRIBE_TYPE_PASSIVE:kotlin.Int`. Configuration is done using `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setPublishType(kotlin.Int)`.

 Value: 0

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getInstantCommunicationBand

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInstantCommunicationBand(): Int
```

Get the Wi-Fi band for instant communication mode for this publish session

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The Wi-Fi band. If instant communication mode is not enabled will return `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_BAND_24_GHZ:kotlin.Int` as default. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_BAND_24_GHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_BAND_5_GHZ:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setInstantCommunicationModeEnabled(kotlin.Boolean,%20kotlin.Int)`

### getPairingConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPairingConfig(): AwarePairingConfig?
```

Get the Aware Pairing config for this publish session

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig?` | A `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig` specified in this config. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setPairingConfig(android.net.wifi.aware.AwarePairingConfig)`

### getSecurityConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSecurityConfig(): WifiAwareDataPathSecurityConfig?
```

Get the data-path security config for this publish session

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareDataPathSecurityConfig?` | A `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareDataPathSecurityConfig` specified in this config. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setDataPathSecurityConfig(android.net.wifi.aware.WifiAwareDataPathSecurityConfig)`

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isFrameworkOffloadedPairingEnabled

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFrameworkOffloadedPairingEnabled(): Boolean
```

Get whether framework offloaded pairing is enabled for this publish config.

If this is enabled, the wifi framework will attempt to perform Wi-Fi Aware pairing automatically before starting the NAN datapath. When pairing happens for the first time, user authorization may be required (such as entering a pincode or password on the system UI).

As a result, apps are highly recommended to increase their connection timeout to at least 30 seconds when starting a datapath with this field enabled. Additionally, if the app is using framework offloaded pairing, the framework will override the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig` with a framework managed configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if framework offloaded pairing is enabled, false otherwise. |

### isInstantCommunicationModeEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInstantCommunicationModeEnabled(): Boolean
```

Check if instant communication mode is enabled for this publish session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true for enabled, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setInstantCommunicationModeEnabled(kotlin.Boolean,%20kotlin.Int)`

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PublishConfig!>
```
