# MacAddress

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MacAddress

Kotlin| [Java](https://developer.android.com/reference/android/net/MacAddress "View this page in Java") 
| --- | --- |

```
class MacAddress : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#) |

Representation of a MAC address. This class only supports 48 bits long addresses and does not support 64 bits long addresses. Instances of this class are immutable. This class provides implementations of hashCode() and equals() that make it suitable for use as keys in standard implementations of [java.util.Map](https://developer.android.com/reference/kotlin/java/util/Map.html#).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BROADCAST](https://developer.android.com/reference/kotlin/android/net/MacAddress#TYPE_BROADCAST:kotlin.Int) Indicates a MAC address is the broadcast address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MULTICAST](https://developer.android.com/reference/kotlin/android/net/MacAddress#TYPE_MULTICAST:kotlin.Int) Indicates a MAC address is a multicast address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNICAST](https://developer.android.com/reference/kotlin/android/net/MacAddress#TYPE_UNICAST:kotlin.Int) Indicates a MAC address is a unicast address. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/MacAddress#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/MacAddress#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#) | [fromBytes](https://developer.android.com/reference/kotlin/android/net/MacAddress#fromBytes(kotlin.ByteArray))`(`addr:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Creates a MacAddress from the given byte array representation. |
| --- | --- |
| static [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#) | [fromString](https://developer.android.com/reference/kotlin/android/net/MacAddress#fromString(kotlin.String))`(`addr:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a MacAddress from the given String representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAddressType](https://developer.android.com/reference/kotlin/android/net/MacAddress#getAddressType())`()` Returns the type of this address. |
| [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address.html#)? | [getLinkLocalIpv6FromEui48Mac](https://developer.android.com/reference/kotlin/android/net/MacAddress#getLinkLocalIpv6FromEui48Mac())`()` Create a link-local Inet6Address from the MAC address. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/MacAddress#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLocallyAssigned](https://developer.android.com/reference/kotlin/android/net/MacAddress#isLocallyAssigned())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](https://developer.android.com/reference/kotlin/android/net/MacAddress#matches(android.net.MacAddress,%20android.net.MacAddress))`(`baseAddress:` ` [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#)`, `mask:` ` [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#)`)` Checks if this MAC Address matches the provided range. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [toByteArray](https://developer.android.com/reference/kotlin/android/net/MacAddress#toByteArray())`()` Convert this MacAddress to a byte array. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toOuiString](https://developer.android.com/reference/kotlin/android/net/MacAddress#toOuiString())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/MacAddress#toString())`()` Returns a human-readable representation of this MacAddress. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/MacAddress#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#)! | [BROADCAST_ADDRESS](https://developer.android.com/reference/kotlin/android/net/MacAddress#BROADCAST_ADDRESS:android.net.MacAddress) The MacAddress representing the unique broadcast MAC address. |
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/MacAddress#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TYPE_BROADCAST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BROADCAST: Int
```

Indicates a MAC address is the broadcast address. 

 Value: 3

### TYPE_MULTICAST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MULTICAST: Int
```

Indicates a MAC address is a multicast address. 

 Value: 2

### TYPE_UNICAST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNICAST: Int
```

Indicates a MAC address is a unicast address. 

 Value: 1

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### fromBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromBytes(addr: ByteArray): MacAddress
```

Creates a MacAddress from the given byte array representation. A valid byte array representation for a MacAddress is a non-null array of length 6.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addr` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):a byte array representation of a MAC address. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#) | the MacAddress corresponding to the given byte array representation. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given byte array is not a valid representation. |

### fromString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromString(addr: String): MacAddress
```

Creates a MacAddress from the given String representation. A valid String representation for a MacAddress is a series of 6 values in the range \[0,ff\] printed in hexadecimal and joined by ':' characters.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addr` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a String representation of a MAC address. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#) | the MacAddress corresponding to the given String representation. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given String is not a valid representation. |

### getAddressType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAddressType(): Int
```

Returns the type of this address.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the int constant representing the MAC address type of this MacAddress. Value is android.net.MacAddress.TYPE_UNKNOWN, [android.net.MacAddress#TYPE_UNICAST](https://developer.android.com/reference/kotlin/android/net/MacAddress#TYPE_UNICAST:kotlin.Int), [android.net.MacAddress#TYPE_MULTICAST](https://developer.android.com/reference/kotlin/android/net/MacAddress#TYPE_MULTICAST:kotlin.Int), or [android.net.MacAddress#TYPE_BROADCAST](https://developer.android.com/reference/kotlin/android/net/MacAddress#TYPE_BROADCAST:kotlin.Int) |

### getLinkLocalIpv6FromEui48Mac

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLinkLocalIpv6FromEui48Mac(): Inet6Address?
```

Create a link-local Inet6Address from the MAC address. The EUI-48 MAC address is converted to an EUI-64 MAC address per RFC 4291. The resulting EUI-64 is used to construct a link-local IPv6 address per RFC 4862.

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address.html#)? | A link-local Inet6Address constructed from the MAC address. This value may be`null`. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isLocallyAssigned

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLocallyAssigned(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this MacAddress is a locally assigned address. |

### matches

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun matches(
    baseAddress: MacAddress, 
    mask: MacAddress
): Boolean
```

Checks if this MAC Address matches the provided range.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `baseAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#):MacAddress representing the base address to compare with. This value cannot be`null`. |
| `mask` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress#):MacAddress representing the mask to use during comparison. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this MAC Address matches the given range. |

### toByteArray

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByteArray(): ByteArray
```

Convert this MacAddress to a byte array. The returned array is in network order. For example, if this MacAddress is 01:02:03:04:05:06, the returned array is \[1, 2, 3, 4, 5, 6\].

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | a byte array representation of this MacAddress. This value cannot be`null`. |

### toOuiString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toOuiString(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a String representation of the OUI part of this MacAddress made of 3 hexadecimal numbers in \[0,ff\] joined by ':' characters. This value cannot be`null`. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a human-readable representation of this MacAddress. The exact format is implementation-dependent and should not be assumed to have any particular format.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### BROADCAST_ADDRESS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_ADDRESS: MacAddress!
```

The MacAddress representing the unique broadcast MAC address. 

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MacAddress!>
```
