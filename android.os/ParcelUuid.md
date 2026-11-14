# ParcelUuid

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParcelUuid

Kotlin| [Java](ParcelUuid.md) 
| --- | --- |

```
class ParcelUuid : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.ParcelUuid](ParcelUuid.md) |

This class is a Parcelable wrapper around [UUID](../java.util/UUID.md) which is an immutable representation of a 128-bit universally unique identifier.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](Parcelable.md) <br /> Descriptor bit used with [describeContents()](Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md) <br /> Flag for use with [writeToParcel](Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParcelUuid](ParcelUuid.md))`(`uuid:` ` [UUID](../java.util/UUID.md)!`)` Constructor creates a ParcelUuid instance from the given [UUID](../java.util/UUID.md). |

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](ParcelUuid.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ParcelUuid.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this ParcelUuid to another object for equality. |
| static [ParcelUuid](ParcelUuid.md)! | [fromString](ParcelUuid.md))`(`uuid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new ParcelUuid from a string representation of [UUID](../java.util/UUID.md). |
| --- | --- |
| [UUID](../java.util/UUID.md)! | [getUuid](ParcelUuid.md))`()` Get the [UUID](../java.util/UUID.md) represented by the ParcelUuid. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](ParcelUuid.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ParcelUuid.md))`()` Returns a string representation of the ParcelUuid For example: 0000110B-0000-1000-8000-00805F9B34FB will be the return value. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](ParcelUuid.md))`(`dest:` ` [Parcel](Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ParcelUuid](ParcelUuid.md)!\> | [CREATOR](ParcelUuid.md) <br /> |

## Public constructors

### ParcelUuid

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParcelUuid(uuid: UUID!)
```

Constructor creates a ParcelUuid instance from the given [UUID](../java.util/UUID.md).

| Parameters ||
|--------|-----------------------------------------------------------------------------------|
| `uuid` | [UUID](../java.util/UUID.md)!:UUID |

## Public methods

### describeContents

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](Parcelable.md) |

### equals

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this ParcelUuid to another object for equality. If`object`is not`null`, is a ParcelUuid instance, and all bits are equal, then`true`is returned.

| Parameters ||
|----------|----------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `object` | the`Object`to compare to. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this ParcelUuid is equal to`object`or`false`if not. |

### fromString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromString(uuid: String!): ParcelUuid!
```

Creates a new ParcelUuid from a string representation of [UUID](../java.util/UUID.md).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `uuid` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the UUID string to parse. |

| Return ||
|--------------------------------------------------------------------------------------|------------------------|
| [ParcelUuid](ParcelUuid.md)! | a ParcelUuid instance. |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if`uuid`is`null`. |
| `java.lang.IllegalArgumentException` | if`uuid`is not formatted correctly. |

### getUuid

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUuid(): UUID!
```

Get the [UUID](../java.util/UUID.md) represented by the ParcelUuid.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------|
| [UUID](../java.util/UUID.md)! | UUID contained in the ParcelUuid. |

### hashCode

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the ParcelUuid For example: 0000110B-0000-1000-8000-00805F9B34FB will be the return value.

| Return ||
|----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a String instance. |

### writeToParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ParcelUuid!>
```
