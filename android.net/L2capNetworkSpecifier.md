Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

# L2capNetworkSpecifier

```
class L2capNetworkSpecifier : NetworkSpecifier, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.NetworkSpecifier](NetworkSpecifier.md) ||
| | ↳ | [android.net.L2capNetworkSpecifier](L2capNetworkSpecifier.md) |

A NetworkSpecifier used to identify an L2CAP network over BLE. An L2CAP network is not symmetrical, meaning there exists both a server (Bluetooth peripheral) and a client (Bluetooth central) node. This specifier contains the information required to request a client L2CAP network using android.net.ConnectivityManager#requestNetwork while specifying the remote MAC address, and Protocol/Service Multiplexer (PSM). It can also contain information allocated by the system when reserving a server network using reserveNetwork such as the Protocol/Service Multiplexer (PSM). In both cases, the header compression option must be specified. An L2CAP server network allocates a Protocol/Service Multiplexer (PSM) to be advertised to the client. A new server network must always be reserved using `ConnectivityManager#reserveNetwork`. The subsequent onReserved callback includes an `L2CapNetworkSpecifier`. The getPsm method will return the Protocol/Service Multiplexer (PSM) of the reserved network so that the server can advertise it to the client and the client can connect. An L2CAP server network is backed by a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket.html#` which can, in theory, accept many connections. However, before SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` Bluetooth APIs do not expose the channel ID, so these connections are indistinguishable. In practice, this means that the network matching semantics in ConnectivityService will tear down all but the first connection. When the connection between client and server completes, a Network whose capabilities satisfy this `L2capNetworkSpecifier` will connect and the usual callbacks, such as NetworkCallback#onAvailable, will be called on the callback object passed to `ConnectivityManager#reserveNetwork` or `ConnectivityManager#requestNetwork`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier.Builder` A builder class for L2capNetworkSpecifier. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#HEADER_COMPRESSION_6LOWPAN:kotlin.Int` Use 6lowpan header compression as specified in rfc6282. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#HEADER_COMPRESSION_ANY:kotlin.Int` Accept any form of header compression. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#HEADER_COMPRESSION_NONE:kotlin.Int` Do not compress packets on this network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#PSM_ANY:kotlin.Int` Match any Protocol/Service Multiplexer (PSM). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#ROLE_ANY:kotlin.Int` Match any role. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#ROLE_CLIENT:kotlin.Int` Specifier describes a client network, i. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#ROLE_SERVER:kotlin.Int` Specifier describes a server network, i. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canBeSatisfiedBy <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHeaderCompression Returns the compression mechanism for this network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPsm Returns the Protocol/Service Multiplexer (PSM) for this network to connect to. |
| [MacAddress](MacAddress.md)? | getRemoteAddress Returns the remote MAC address for this network to connect to. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRole Returns the role to be used for this network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [NetworkSpecifier](NetworkSpecifier.md)? | redact <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [L2capNetworkSpecifier](L2capNetworkSpecifier.md)!\> | `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### HEADER_COMPRESSION_6LOWPAN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
static val HEADER_COMPRESSION_6LOWPAN: Int
```

Use 6lowpan header compression as specified in rfc6282.

 Value: 2

### HEADER_COMPRESSION_ANY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
static val HEADER_COMPRESSION_ANY: Int
```

Accept any form of header compression. This option is only meaningful in NetworkRequests. Specifiers for actual L2CAP networks never have this option set.

 Value: 0

### HEADER_COMPRESSION_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
static val HEADER_COMPRESSION_NONE: Int
```

Do not compress packets on this network.

 Value: 1

### PSM_ANY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
static val PSM_ANY: Int
```

Match any Protocol/Service Multiplexer (PSM). This PSM value is only meaningful in NetworkRequests. Specifiers for actual L2CAP networks never have this value set.

 Value: 0

### ROLE_ANY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
static val ROLE_ANY: Int
```

Match any role. This role is only meaningful in NetworkRequests. Specifiers for actual L2CAP networks never have this role set.

 Value: 0

### ROLE_CLIENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
static val ROLE_CLIENT: Int
```

Specifier describes a client network, i.e., the device is the Bluetooth central.

 Value: 1

### ROLE_SERVER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
static val ROLE_SERVER: Int
```

Specifier describes a server network, i.e., the device is the Bluetooth peripheral.

 Value: 2

## Public methods

### canBeSatisfiedBy

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
fun canBeSatisfiedBy(other: NetworkSpecifier!): Boolean
```

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

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

### getHeaderCompression

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
fun getHeaderCompression(): Int
```

Returns the compression mechanism for this network.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#HEADER_COMPRESSION_ANY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#HEADER_COMPRESSION_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#HEADER_COMPRESSION_6LOWPAN:kotlin.Int` |

### getPsm

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
fun getPsm(): Int
```

Returns the Protocol/Service Multiplexer (PSM) for this network to connect to.

### getRemoteAddress

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
fun getRemoteAddress(): MacAddress?
```

Returns the remote MAC address for this network to connect to. The remote address is only meaningful for networks that have ROLE_CLIENT. When receiving this L2capNetworkSpecifier from Connectivity APIs such as a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback`, the MAC address is redacted.

| Return ||
|---|---|
| MacAddress | This value may be `null`. |

### getRole

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
fun getRole(): Int
```

Returns the role to be used for this network.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#ROLE_ANY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#ROLE_CLIENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier#ROLE_SERVER:kotlin.Int` |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### redact

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
fun redact(): NetworkSpecifier?
```

| Return ||
|---|---|
| NetworkSpecifier | This value may be `null`. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<L2capNetworkSpecifier!>
```
