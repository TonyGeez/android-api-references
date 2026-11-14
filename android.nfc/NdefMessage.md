# NdefMessage

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NdefMessage

Kotlin| [Java](../android/nfc/NdefMessage.md) 
| --- | --- |

```
class NdefMessage : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.NdefMessage](../android/nfc/NdefMessage.md) |

Represents an immutable NDEF Message.

NDEF (NFC Data Exchange Format) is a light-weight binary format, used to encapsulate typed data. It is specified by the NFC Forum, for transmission and storage with NFC, however it is transport agnostic.

NDEF defines messages and records. An NDEF Record contains typed data, such as MIME-type media, a URI, or a custom application payload. An NDEF Message is a container for one or more NDEF Records.

When an Android device receives an NDEF Message (for example by reading an NFC tag) it processes it through a dispatch mechanism to determine an activity to launch. The type of the*first*record in the message has special importance for message dispatch, so design this record carefully.

Use[NdefMessage(byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.ByteArray))to construct an NDEF Message from binary data, or[NdefMessage(android.nfc.NdefRecord[])](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.Array))to construct from one or more [NdefRecord](../android/nfc/NdefRecord.md) s.

[NdefMessage](../android/nfc/NdefMessage.md) and [NdefRecord](../android/nfc/NdefRecord.md) implementations are always available, even on Android devices that do not have NFC hardware.

[NdefRecord](../android/nfc/NdefRecord.md) s are intended to be immutable (and thread-safe), however they may contain mutable fields. So take care not to modify mutable fields passed into constructors, or modify mutable fields obtained by getter methods, unless such modification is explicitly marked as safe.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NdefMessage](../android/nfc/NdefMessage.md))`(`record:` ` [NdefRecord](../android/nfc/NdefRecord.md)!`, `vararg` `records:` ` [NdefRecord](../android/nfc/NdefRecord.md)!`)` Construct an NDEF Message from one or more NDEF Records. |
| [NdefMessage](../android/nfc/NdefMessage.md))`(`records:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [NdefRecord](../android/nfc/NdefRecord.md)!>!`)` Construct an NDEF Message from one or more NDEF Records. |
| [NdefMessage](../android/nfc/NdefMessage.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Construct an NDEF Message by parsing raw bytes. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/nfc/NdefMessage.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/nfc/NdefMessage.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the specified NDEF Message contains identical NDEF Records. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getByteArrayLength](../android/nfc/NdefMessage.md))`()` Return the length of this NDEF Message if it is written to a byte array with [toByteArray](../android/nfc/NdefMessage.md)). |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [NdefRecord](../android/nfc/NdefRecord.md)!\>! | [getRecords](../android/nfc/NdefMessage.md))`()` Get the NDEF Records inside this NDEF Message. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/nfc/NdefMessage.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [toByteArray](../android/nfc/NdefMessage.md))`()` Return this NDEF Message as raw bytes. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/nfc/NdefMessage.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/nfc/NdefMessage.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [NdefMessage](../android/nfc/NdefMessage.md)!\> | [CREATOR](../android/nfc/NdefMessage.md) <br /> |

## Public constructors

### NdefMessage

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NdefMessage(
    record: NdefRecord!, 
    vararg records: NdefRecord!)
```

Construct an NDEF Message from one or more NDEF Records.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `record` | [NdefRecord](../android/nfc/NdefRecord.md)!:first record (mandatory) |
| `records` | [NdefRecord](../android/nfc/NdefRecord.md)!:additional records (optional) |

### NdefMessage

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NdefMessage(records: Array<NdefRecord!>!)
```

Construct an NDEF Message from one or more NDEF Records.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `records` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [NdefRecord](../android/nfc/NdefRecord.md)!\>!:one or more records |

### NdefMessage

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NdefMessage(data: ByteArray!)
```

Construct an NDEF Message by parsing raw bytes.

Strict validation of the NDEF binary structure is performed: there must be at least one record, every record flag must be correct, and the total length of the message must match the length of the input data.

This parser can handle chunked records, and converts them into logical [NdefRecord](../android/nfc/NdefRecord.md) s within the message.

Once the input data has been parsed to one or more logical records, basic validation of the tnf, type, id, and payload fields of each record is performed, as per the documentation on on[NdefRecord.NdefRecord(short, byte[], byte[], byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#NdefRecord(kotlin.Short,%20kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.ByteArray))

If either strict validation of the binary format fails, or basic validation during record construction fails, a [FormatException](../android/nfc/FormatException.md) is thrown

Deep inspection of the type, id and payload fields of each record is not performed, so it is possible to parse input that has a valid binary format and confirms to the basic validation requirements of[NdefRecord.NdefRecord(short, byte[], byte[], byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#NdefRecord(kotlin.Short,%20kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.ByteArray)), but fails more strict requirements as specified by the NFC Forum.

It is safe to re-use the data byte array after construction: this constructor will make an internal copy of all necessary fields.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:raw bytes to parse |

| Exceptions ||
|-------------------------------|------------------------------|
| `android.nfc.FormatException` | if the data cannot be parsed |

## Public methods

### describeContents

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Returns true if the specified NDEF Message contains identical NDEF Records.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getByteArrayLength

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getByteArrayLength(): Int
```

Return the length of this NDEF Message if it is written to a byte array with [toByteArray](../android/nfc/NdefMessage.md)).

An NDEF Message can be formatted to bytes in different ways depending on chunking, SR, and ID flags, so the length returned by this method may not be equal to the length of the original byte array used to construct this NDEF Message. However it will always be equal to the length of the byte array produced by [toByteArray](../android/nfc/NdefMessage.md)).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length of this NDEF Message when written to bytes with [toByteArray](../android/nfc/NdefMessage.md)) |

**See Also**

- [#toByteArray](../android/nfc/NdefMessage.md)) 

### getRecords

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecords(): Array<NdefRecord!>!
```

Get the NDEF Records inside this NDEF Message.

An [NdefMessage](../android/nfc/NdefMessage.md) always has one or more NDEF Records: so the following code to retrieve the first record is always safe (no need to check for null or array length \>= 1): 

```kotlin
NdefRecord firstRecord = ndefMessage.getRecords()[0];
  
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [NdefRecord](../android/nfc/NdefRecord.md)!>! | array of one or more NDEF records. |

### hashCode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toByteArray

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByteArray(): ByteArray!
```

Return this NDEF Message as raw bytes.

The NDEF Message is formatted as per the NDEF 1.0 specification, and the byte array is suitable for network transmission or storage in an NFC Forum NDEF compatible tag.

This method will not chunk any records, and will always use the short record (SR) format and omit the identifier field when possible.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | NDEF Message in binary format |

**See Also**

- <https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#getByteArrayLength()> 

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NdefMessage!>
```
