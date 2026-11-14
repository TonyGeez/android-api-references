# RouteInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RouteInfo

Kotlin| [Java](https://developer.android.com/reference/android/net/RouteInfo "View this page in Java") 

```
class RouteInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo#) |

Represents a network route.

This is used both to describe static network configuration and live network configuration information. A route contains three pieces of information:

- a destination [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix) specifying the network destinations covered by this route. If this is`null`it indicates a default route of the address family (IPv4 or IPv6) implied by the gateway IP address.
- a gateway [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) indicating the next hop to use. If this is`null`it indicates a directly-connected route.
- an interface (which may be unspecified).

Either the destination or the gateway may be`null`, but not both. If the destination and gateway are both specified, they must be of the same address family (IPv4 or IPv6).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RTN_THROW](https://developer.android.com/reference/kotlin/android/net/RouteInfo#RTN_THROW:kotlin.Int) Throw route. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RTN_UNICAST](https://developer.android.com/reference/kotlin/android/net/RouteInfo#RTN_UNICAST:kotlin.Int) Unicast route. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RTN_UNREACHABLE](https://developer.android.com/reference/kotlin/android/net/RouteInfo#RTN_UNREACHABLE:kotlin.Int) Unreachable route. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/RouteInfo#describeContents())`()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/RouteInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this RouteInfo object against the specified object and indicates if they are equal. |
| [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix) | [getDestination](https://developer.android.com/reference/kotlin/android/net/RouteInfo#getDestination())`()` Retrieves the destination address and prefix length in the form of an [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix). |
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)? | [getGateway](https://developer.android.com/reference/kotlin/android/net/RouteInfo#getGateway())`()` Retrieves the gateway or next hop [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) for this route. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInterface](https://developer.android.com/reference/kotlin/android/net/RouteInfo#getInterface())`()` Retrieves the interface used for this route if specified, else`null`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/net/RouteInfo#getType())`()` Retrieves the type of this route. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasGateway](https://developer.android.com/reference/kotlin/android/net/RouteInfo#hasGateway())`()` Indicates if this route has a next hop (`true`) or is directly-connected (`false`). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/RouteInfo#hashCode())`()` Returns a hashcode for this`RouteInfo`object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDefaultRoute](https://developer.android.com/reference/kotlin/android/net/RouteInfo#isDefaultRoute())`()` Indicates if this route is a default route (ie, has no destination specified). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](https://developer.android.com/reference/kotlin/android/net/RouteInfo#matches(java.net.InetAddress))`(`destination:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` Determines whether the destination and prefix of this route includes the specified address. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/RouteInfo#toString())`()` Returns a human-readable description of this object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/RouteInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/RouteInfo#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface. |

## Constants

### RTN_THROW

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTN_THROW: Int
```

Throw route. Indicates that routing information about this destination is not in this table. Routing lookup should continue in another table. 

 Value: 9

### RTN_UNICAST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTN_UNICAST: Int
```

Unicast route. Indicates that destination is reachable directly or via gateway. 

 Value: 1

### RTN_UNREACHABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTN_UNREACHABLE: Int
```

Unreachable route. Indicates that destination is unreachable. 

 Value: 7

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this RouteInfo object against the specified object and indicates if they are equal.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are equal,`false`otherwise. |

### getDestination

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDestination(): IpPrefix
```

Retrieves the destination address and prefix length in the form of an [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix).

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix) | [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix) specifying the destination. This is never`null`. |

### getGateway

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGateway(): InetAddress?
```

Retrieves the gateway or next hop [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) for this route.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)? | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) specifying the gateway or next hop. This may be`null`for a directly-connected route." |

### getInterface

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInterface(): String?
```

Retrieves the interface used for this route if specified, else`null`.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The name of the interface used for this route. |

### getType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Retrieves the type of this route.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The type of this route; one of the`RTN_xxx`constants defined in this class. Value is [android.net.RouteInfo#RTN_UNICAST](https://developer.android.com/reference/kotlin/android/net/RouteInfo#RTN_UNICAST:kotlin.Int), [android.net.RouteInfo#RTN_UNREACHABLE](https://developer.android.com/reference/kotlin/android/net/RouteInfo#RTN_UNREACHABLE:kotlin.Int), or [android.net.RouteInfo#RTN_THROW](https://developer.android.com/reference/kotlin/android/net/RouteInfo#RTN_THROW:kotlin.Int) |

### hasGateway

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasGateway(): Boolean
```

Indicates if this route has a next hop (`true`) or is directly-connected (`false`).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if a gateway is specified |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hashcode for this`RouteInfo`object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isDefaultRoute

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDefaultRoute(): Boolean
```

Indicates if this route is a default route (ie, has no destination specified).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the destination has a prefix length of 0. |

### matches

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun matches(destination: InetAddress!): Boolean
```

Determines whether the destination and prefix of this route includes the specified address.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:A [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) to test to see if it would match this route. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the destination and prefix length cover the given address. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a human-readable description of this object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RouteInfo!>
```

Implement the Parcelable interface.
