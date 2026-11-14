# IpPrefix

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IpPrefix

Kotlin| [Java](../android/net/IpPrefix.md) 
| --- | --- |

```
class IpPrefix : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.IpPrefix](../android/net/IpPrefix.md) |

This class represents an IP prefix, i.e., a contiguous block of IP addresses aligned on a power of two boundary (also known as an "IP subnet"). A prefix is specified by two pieces of information:

- A starting IP address (IPv4 or IPv6). This is the first IP address of the prefix.
- A prefix length. This specifies the length of the prefix by specifing the number of bits in the IP address, starting from the most significant bit in network byte order, that are constant for all addresses in the prefix.

For example, the prefix`192.0.2.0/24`covers the 256 IPv4 addresses from`192.0.2.0`to`192.0.2.255`, inclusive, and the prefix`2001:db8:1:2`covers the 2\^64 IPv6 addresses from`2001:db8:1:2::`to`2001:db8:1:2:ffff:ffff:ffff:ffff`, inclusive. Objects of this class are immutable.

<br />

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IpPrefix](../android/net/IpPrefix.md))`(`address:` ` [InetAddress](../java/net/InetAddress.md)`, `prefixLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`IpPrefix`from an IPv4 or IPv6 address and a prefix length. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../android/net/IpPrefix.md))`(`address:` ` [InetAddress](../java/net/InetAddress.md)`)` Determines whether the prefix contains the specified address. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/IpPrefix.md))`()` Implement the Parcelable interface. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/IpPrefix.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`IpPrefix`object against the specified object in`obj`. |
| --- | --- |
| [InetAddress](../java/net/InetAddress.md) | [getAddress](../android/net/IpPrefix.md))`()` Returns a copy of the first IP address in the prefix. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrefixLength](../android/net/IpPrefix.md))`()` Returns the prefix length of this`IpPrefix`. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getRawAddress](../android/net/IpPrefix.md))`()` Returns a copy of the IP address bytes in network order (the highest order byte is the zeroth element). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/IpPrefix.md))`()` Gets the hashcode of the represented IP prefix. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/IpPrefix.md))`()` Returns a string representation of this`IpPrefix`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/IpPrefix.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [IpPrefix](../android/net/IpPrefix.md)!\> | [CREATOR](../android/net/IpPrefix.md) Implement the Parcelable interface. |

## Public constructors

### IpPrefix

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IpPrefix(
    address: InetAddress, 
    prefixLength: Int)
```

Constructs a new`IpPrefix`from an IPv4 or IPv6 address and a prefix length. Silently truncates the address to the prefix length, so for example`192.0.2.1/24`is silently converted to`192.0.2.0/24`.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `address` | [InetAddress](../java/net/InetAddress.md):the IP address. Must be non-null. |
| `prefixLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the prefix length. Must be \>= 0 and \<= (32 or 128) (IPv4 or IPv6). Value is between 0 and 128 inclusive |

## Public methods

### contains

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun contains(address: InetAddress): Boolean
```

Determines whether the prefix contains the specified address.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `address` | [InetAddress](../java/net/InetAddress.md):An [InetAddress](../java/net/InetAddress.md) to test. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the prefix covers the given address.`false`otherwise. |

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this`IpPrefix`object against the specified object in`obj`. Two objects are equal if they have the same startAddress and prefixLength.

| Parameters ||
|-------|----------------------------------------------------------------|
| `obj` | the object to be tested for equality. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if both objects are equal,`false`otherwise. |

### getAddress

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAddress(): InetAddress
```

Returns a copy of the first IP address in the prefix. Modifying the returned object does not change this object's contents.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [InetAddress](../java/net/InetAddress.md) | the address in the form of a byte array. This value cannot be`null`. |

### getPrefixLength

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrefixLength(): Int
```

Returns the prefix length of this`IpPrefix`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the prefix length. Value is between 0 and 128 inclusive |

### getRawAddress

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRawAddress(): ByteArray
```

Returns a copy of the IP address bytes in network order (the highest order byte is the zeroth element). Modifying the returned array does not change this object's contents.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the address in the form of a byte array. This value cannot be`null`. |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Gets the hashcode of the represented IP prefix.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the appropriate hashcode value. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of this`IpPrefix`.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string such as`"192.0.2.0/24"`or`"2001:db8:1:2::/64"`. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<IpPrefix!>
```

Implement the Parcelable interface.
