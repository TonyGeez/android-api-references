# RouteInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RouteInfo

Kotlin| [Java](../android/net/RouteInfo.md) 
| --- | --- |

```
class RouteInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.RouteInfo](../android/net/RouteInfo.md) |

Represents a network route.

This is used both to describe static network configuration and live network configuration information. A route contains three pieces of information:

- a destination [IpPrefix](../android/net/IpPrefix.md) specifying the network destinations covered by this route. If this is`null`it indicates a default route of the address family (IPv4 or IPv6) implied by the gateway IP address.
- a gateway [InetAddress](../java/net/InetAddress.md) indicating the next hop to use. If this is`null`it indicates a directly-connected route.
- an interface (which may be unspecified).

Either the destination or the gateway may be`null`, but not both. If the destination and gateway are both specified, they must be of the same address family (IPv4 or IPv6).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RTN_THROW](../android/net/RouteInfo.md) Throw route. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RTN_UNICAST](../android/net/RouteInfo.md) Unicast route. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RTN_UNREACHABLE](../android/net/RouteInfo.md) Unreachable route. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/RouteInfo.md))`()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/RouteInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this RouteInfo object against the specified object and indicates if they are equal. |
| [IpPrefix](../android/net/IpPrefix.md) | [getDestination](../android/net/RouteInfo.md))`()` Retrieves the destination address and prefix length in the form of an [IpPrefix](../android/net/IpPrefix.md). |
| --- | --- |
| [InetAddress](../java/net/InetAddress.md)? | [getGateway](../android/net/RouteInfo.md))`()` Retrieves the gateway or next hop [InetAddress](../java/net/InetAddress.md) for this route. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInterface](../android/net/RouteInfo.md))`()` Retrieves the interface used for this route if specified, else`null`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/net/RouteInfo.md))`()` Retrieves the type of this route. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasGateway](../android/net/RouteInfo.md))`()` Indicates if this route has a next hop (`true`) or is directly-connected (`false`). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/RouteInfo.md))`()` Returns a hashcode for this`RouteInfo`object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDefaultRoute](../android/net/RouteInfo.md))`()` Indicates if this route is a default route (ie, has no destination specified). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](../android/net/RouteInfo.md))`(`destination:` ` [InetAddress](../java/net/InetAddress.md)!`)` Determines whether the destination and prefix of this route includes the specified address. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/RouteInfo.md))`()` Returns a human-readable description of this object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/RouteInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RouteInfo](../android/net/RouteInfo.md)!\> | [CREATOR](../android/net/RouteInfo.md) Implement the Parcelable interface. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

Retrieves the destination address and prefix length in the form of an [IpPrefix](../android/net/IpPrefix.md).

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [IpPrefix](../android/net/IpPrefix.md) | [IpPrefix](../android/net/IpPrefix.md) specifying the destination. This is never`null`. |

### getGateway

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGateway(): InetAddress?
```

Retrieves the gateway or next hop [InetAddress](../java/net/InetAddress.md) for this route.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InetAddress](../java/net/InetAddress.md)? | [InetAddress](../java/net/InetAddress.md) specifying the gateway or next hop. This may be`null`for a directly-connected route." |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The type of this route; one of the`RTN_xxx`constants defined in this class. Value is [android.net.RouteInfo#RTN_UNICAST](../android/net/RouteInfo.md), [android.net.RouteInfo#RTN_UNREACHABLE](../android/net/RouteInfo.md), or [android.net.RouteInfo#RTN_THROW](../android/net/RouteInfo.md) |

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
| `destination` | [InetAddress](../java/net/InetAddress.md)!:A [InetAddress](../java/net/InetAddress.md) to test to see if it would match this route. |

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RouteInfo!>
```

Implement the Parcelable interface.
