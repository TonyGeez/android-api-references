# UUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UUID

```
class UUID : Comparable<UUID!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.UUID](../java/util/UUID.md) |

A class that represents an immutable universally unique identifier (UUID). A UUID represents a 128-bit value.

There exist different variants of these global identifiers. The methods of this class are for manipulating the Leach-Salz variant, although the constructors allow the creation of any variant of UUID (described below).

The layout of a variant 2 (Leach-Salz) UUID is as follows: The most significant long consists of the following unsigned fields: 

```kotlin
0xFFFFFFFF00000000 time_low
  0x00000000FFFF0000 time_mid
  0x000000000000F000 version
  0x0000000000000FFF time_hi
  
```
The least significant long consists of the following unsigned fields: 

```kotlin
0xC000000000000000 variant
  0x3FFF000000000000 clock_seq
  0x0000FFFFFFFFFFFF node
  
```

The variant field contains a value which identifies the layout of the `UUID`. The bit layout described above is valid only for a `UUID` with a variant value of 2, which indicates the Leach-Salz variant.

The version field holds a value that describes the type of this `UUID`. There are four different basic types of UUIDs: time-based, DCE security, name-based, and randomly generated UUIDs. These types have a version value of 1, 2, 3 and 4, respectively.

For more information including algorithms used to create `UUID`s, see [*RFC 4122: A Universally Unique IDentifier (UUID) URN Namespace*](http://www.ietf.org/rfc/rfc4122.txt), section 4.2 "Algorithms for Creating a Time-Based UUID".

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UUID](../java/util/UUID.md))`(`mostSigBits:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `leastSigBits:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a new `UUID` using the specified data. |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [clockSequence](../java/util/UUID.md))`()` The clock sequence value associated with this UUID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../java/util/UUID.md))`(`other:` ` [UUID](../java/util/UUID.md)!`)` Compares this UUID with the specified UUID. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/util/UUID.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object to the specified object. |
| --- | --- |
| static [UUID](../java/util/UUID.md)! | [fromString](../java/util/UUID.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a `UUID` from the string standard representation as described in the [toString](../java/util/UUID.md)) method. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLeastSignificantBits](../java/util/UUID.md))`()` Returns the least significant 64 bits of this UUID's 128 bit value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMostSignificantBits](../java/util/UUID.md))`()` Returns the most significant 64 bits of this UUID's 128 bit value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/util/UUID.md))`()` Returns a hash code for this `UUID`. |
| static [UUID](../java/util/UUID.md)! | [nameUUIDFromBytes](../java/util/UUID.md))`(`name:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Static factory to retrieve a type 3 (name based) `UUID` based on the specified byte array. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [node](../java/util/UUID.md))`()` The node value associated with this UUID. |
| --- | --- |
| static [UUID](../java/util/UUID.md)! | [randomUUID](../java/util/UUID.md))`()` Static factory to retrieve a type 4 (pseudo randomly generated) UUID. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [timestamp](../java/util/UUID.md))`()` The timestamp value associated with this UUID. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/UUID.md))`()` Returns a `String` object representing this `UUID`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [variant](../java/util/UUID.md))`()` The variant number associated with this `UUID`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [version](../java/util/UUID.md))`()` The version number associated with this `UUID`. |

## Public constructors

### UUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UUID(
    mostSigBits: Long, 
    leastSigBits: Long)
```

Constructs a new `UUID` using the specified data. `mostSigBits` is used for the most significant 64 bits of the `UUID` and `leastSigBits` becomes the least significant 64 bits of the `UUID`.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------|
| `mostSigBits` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The most significant bits of the `UUID` |
| `leastSigBits` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The least significant bits of the `UUID` |

## Public methods

### clockSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clockSequence(): Int
```

The clock sequence value associated with this UUID.

The 14 bit clock sequence value is constructed from the clock sequence field of this UUID. The clock sequence field is used to guarantee temporal uniqueness in a time-based UUID.

The `clockSequence` value is only meaningful in a time-based UUID, which has version type 1. If this UUID is not a time-based UUID then this method throws UnsupportedOperationException.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The clock sequence of this `UUID` |

| Exceptions ||
|-------------------------------------------|--------------------------------------|
| `java.lang.UnsupportedOperationException` | If this UUID is not a version 1 UUID |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: UUID!): Int
```

Compares this UUID with the specified UUID.

The first of two UUIDs is greater than the second if the most significant field in which the UUIDs differ is greater for the first UUID.

| Parameters ||
|-------|-----------------------------------------------|
| `o` | the object to be compared. |
| `val` | `UUID` to which this `UUID` is to be compared |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | -1, 0 or 1 as this `UUID` is less than, equal to, or greater than `val` |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object to the specified object. The result is `true` if and only if the argument is not `null`, is a `UUID` object, has the same variant, and contains the same value, bit for bit, as this `UUID`.

| Parameters ||
|-------|---------------------------|
| `obj` | The object to be compared |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the objects are the same; `false` otherwise |

### fromString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromString(name: String!): UUID!
```

Creates a `UUID` from the string standard representation as described in the [toString](../java/util/UUID.md)) method.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string that specifies a `UUID` |

| Return ||
|-------------------------------------------------------------------------|-----------------------------------|
| [UUID](../java/util/UUID.md)! | A `UUID` with the specified value |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If name does not conform to the string representation as described in [toString](../java/util/UUID.md)) |

### getLeastSignificantBits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLeastSignificantBits(): Long
```

Returns the least significant 64 bits of this UUID's 128 bit value.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The least significant 64 bits of this UUID's 128 bit value |

### getMostSignificantBits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMostSignificantBits(): Long
```

Returns the most significant 64 bits of this UUID's 128 bit value.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The most significant 64 bits of this UUID's 128 bit value |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code for this `UUID`.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A hash code value for this `UUID` |

### nameUUIDFromBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun nameUUIDFromBytes(name: ByteArray!): UUID!
```

Static factory to retrieve a type 3 (name based) `UUID` based on the specified byte array.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: A byte array to be used to construct a `UUID` |

| Return ||
|-------------------------------------------------------------------------|---------------------------------------------|
| [UUID](../java/util/UUID.md)! | A `UUID` generated from the specified array |

### node

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun node(): Long
```

The node value associated with this UUID.

The 48 bit node value is constructed from the node field of this UUID. This field is intended to hold the IEEE 802 address of the machine that generated this UUID to guarantee spatial uniqueness.

The node value is only meaningful in a time-based UUID, which has version type 1. If this UUID is not a time-based UUID then this method throws UnsupportedOperationException.

| Return ||
|------------------------------------------------------------------------------|-------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The node value of this `UUID` |

| Exceptions ||
|-------------------------------------------|--------------------------------------|
| `java.lang.UnsupportedOperationException` | If this UUID is not a version 1 UUID |

### randomUUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun randomUUID(): UUID!
```

Static factory to retrieve a type 4 (pseudo randomly generated) UUID. The `UUID` is generated using a cryptographically strong pseudo random number generator.

| Return ||
|-------------------------------------------------------------------------|-----------------------------|
| [UUID](../java/util/UUID.md)! | A randomly generated `UUID` |

### timestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun timestamp(): Long
```

The timestamp value associated with this UUID.

The 60 bit timestamp value is constructed from the time_low, time_mid, and time_hi fields of this `UUID`. The resulting timestamp is measured in 100-nanosecond units since midnight, October 15, 1582 UTC.

The timestamp value is only meaningful in a time-based UUID, which has version type 1. If this `UUID` is not a time-based UUID then this method throws UnsupportedOperationException.

| Return ||
|------------------------------------------------------------------------------|-------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The timestamp of this `UUID`. |

| Exceptions ||
|-------------------------------------------|--------------------------------------|
| `java.lang.UnsupportedOperationException` | If this UUID is not a version 1 UUID |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a `String` object representing this `UUID`.

The UUID string representation is as described by this BNF: 

```kotlin
<code>UUID                   = &lt;time_low&gt; "-" &lt;time_mid&gt; "-"
                           &lt;time_high_and_version&gt; "-"
                           &lt;variant_and_sequence&gt; "-"
                           &lt;node&gt;
  time_low               = 4*&lt;hexOctet&gt;
  time_mid               = 2*&lt;hexOctet&gt;
  time_high_and_version  = 2*&lt;hexOctet&gt;
  variant_and_sequence   = 2*&lt;hexOctet&gt;
  node                   = 6*&lt;hexOctet&gt;
  hexOctet               = &lt;hexDigit&gt;&lt;hexDigit&gt;
  hexDigit               =
        "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
        | "a" | "b" | "c" | "d" | "e" | "f"
        | "A" | "B" | "C" | "D" | "E" | "F"
  </code>
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A string representation of this `UUID` |

### variant

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun variant(): Int
```

The variant number associated with this `UUID`. The variant number describes the layout of the `UUID`. The variant number has the following meaning:

- 0 Reserved for NCS backward compatibility
- 2 [IETF RFC 4122](http://www.ietf.org/rfc/rfc4122.txt) (Leach-Salz), used by this class
- 6 Reserved, Microsoft Corporation backward compatibility
- 7 Reserved for future definition

<br />

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The variant number of this `UUID` |

### version

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun version(): Int
```

The version number associated with this `UUID`. The version number describes how this `UUID` was generated. The version number has the following meaning:

- 1 Time-based UUID
- 2 DCE security UUID
- 3 Name-based UUID
- 4 Randomly generated UUID

<br />

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The version number of this `UUID` |
