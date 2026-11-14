# NdefMessage

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NdefMessage

Kotlin| [Java](https://developer.android.com/reference/android/nfc/NdefMessage "View this page in Java") 
| --- | --- |

```
class NdefMessage : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#) |

Represents an immutable NDEF Message.

NDEF (NFC Data Exchange Format) is a light-weight binary format, used to encapsulate typed data. It is specified by the NFC Forum, for transmission and storage with NFC, however it is transport agnostic.

NDEF defines messages and records. An NDEF Record contains typed data, such as MIME-type media, a URI, or a custom application payload. An NDEF Message is a container for one or more NDEF Records.

When an Android device receives an NDEF Message (for example by reading an NFC tag) it processes it through a dispatch mechanism to determine an activity to launch. The type of the*first*record in the message has special importance for message dispatch, so design this record carefully.

Use[NdefMessage(byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.ByteArray))to construct an NDEF Message from binary data, or[NdefMessage(android.nfc.NdefRecord[])](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.Array))to construct from one or more [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord) s.

[NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#) and [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord) implementations are always available, even on Android devices that do not have NFC hardware.

[NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord) s are intended to be immutable (and thread-safe), however they may contain mutable fields. So take care not to modify mutable fields passed into constructors, or modify mutable fields obtained by getter methods, unless such modification is explicitly marked as safe.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(android.nfc.NdefRecord,%20android.nfc.NdefRecord))`(`record:` ` [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord)!`, `vararg` `records:` ` [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord)!`)` Construct an NDEF Message from one or more NDEF Records. |
| [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.Array))`(`records:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord)!>!`)` Construct an NDEF Message from one or more NDEF Records. |
| [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.ByteArray))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Construct an NDEF Message by parsing raw bytes. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the specified NDEF Message contains identical NDEF Records. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getByteArrayLength](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#getByteArrayLength())`()` Return the length of this NDEF Message if it is written to a byte array with [toByteArray](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray()). |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord)!\>! | [getRecords](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#getRecords())`()` Get the NDEF Records inside this NDEF Message. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#hashCode())`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [toByteArray](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray())`()` Return this NDEF Message as raw bytes. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| `record` | [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord)!:first record (mandatory) |
| `records` | [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord)!:additional records (optional) |

### NdefMessage

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NdefMessage(records: Array<NdefRecord!>!)
```

Construct an NDEF Message from one or more NDEF Records.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `records` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord)!\>!:one or more records |

### NdefMessage

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NdefMessage(data: ByteArray!)
```

Construct an NDEF Message by parsing raw bytes.

Strict validation of the NDEF binary structure is performed: there must be at least one record, every record flag must be correct, and the total length of the message must match the length of the input data.

This parser can handle chunked records, and converts them into logical [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord) s within the message.

Once the input data has been parsed to one or more logical records, basic validation of the tnf, type, id, and payload fields of each record is performed, as per the documentation on on[NdefRecord.NdefRecord(short, byte[], byte[], byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#NdefRecord(kotlin.Short,%20kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.ByteArray))

If either strict validation of the binary format fails, or basic validation during record construction fails, a [FormatException](https://developer.android.com/reference/kotlin/android/nfc/FormatException) is thrown

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Return the length of this NDEF Message if it is written to a byte array with [toByteArray](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray()).

An NDEF Message can be formatted to bytes in different ways depending on chunking, SR, and ID flags, so the length returned by this method may not be equal to the length of the original byte array used to construct this NDEF Message. However it will always be equal to the length of the byte array produced by [toByteArray](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray()).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length of this NDEF Message when written to bytes with [toByteArray](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray()) |

**See Also**

- [#toByteArray](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray()) 

### getRecords

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecords(): Array<NdefRecord!>!
```

Get the NDEF Records inside this NDEF Message.

An [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#) always has one or more NDEF Records: so the following code to retrieve the first record is always safe (no need to check for null or array length \>= 1): 

```kotlin
NdefRecord firstRecord = ndefMessage.getRecords()[0];
  
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord)!>! | array of one or more NDEF records. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NdefMessage!>
```
