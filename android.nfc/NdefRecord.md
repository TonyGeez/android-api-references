# NdefRecord

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NdefRecord

Kotlin| [Java](https://developer.android.com/reference/android/nfc/NdefRecord "View this page in Java") 
| --- | --- |

```
class NdefRecord : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#) |

Represents an immutable NDEF Record.

NDEF (NFC Data Exchange Format) is a light-weight binary format, used to encapsulate typed data. It is specified by the NFC Forum, for transmission and storage with NFC, however it is transport agnostic.

NDEF defines messages and records. An NDEF Record contains typed data, such as MIME-type media, a URI, or a custom application payload. An NDEF Message is a container for one or more NDEF Records.

This class represents logical (complete) NDEF Records, and can not be used to represent chunked (partial) NDEF Records. However[NdefMessage.NdefMessage(byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.ByteArray))can be used to parse a message containing chunked records, and will return a message with unchunked (complete) records.

A logical NDEF Record always contains a 3-bit TNF (Type Name Field) that provides high level typing for the rest of the record. The remaining fields are variable length and not always present:

- *type*: detailed typing for the payload
- *id*: identifier meta-data, not commonly used
- *payload*: the actual payload

Helpers such as android.nfc.NdefRecord#createUri, [NdefRecord.createMime](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createMime(kotlin.String,%20kotlin.ByteArray))and [NdefRecord.createExternal](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createExternal(kotlin.String,%20kotlin.String,%20kotlin.ByteArray))are included to create well-formatted NDEF Records with correctly set tnf, type, id and payload fields, please use these helpers whenever possible.

Use the constructor[NdefRecord(short,byte[],byte[],byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#NdefRecord(kotlin.Short,%20kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.ByteArray))if you know what you are doing and what to set the fields individually. Only basic validation is performed with this constructor, so it is possible to create records that do not confirm to the strict NFC Forum specifications.

The binary representation of an NDEF Record includes additional flags to indicate location with an NDEF message, provide support for chunking of NDEF records, and to pack optional fields. This class does not expose those details. To write an NDEF Record as binary you must first put it into an [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage), then call [NdefMessage.toByteArray()](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray()).

[NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage) and [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#) implementations are always available, even on Android devices that do not have NFC hardware.

[NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#) s are intended to be immutable (and thread-safe), however they may contain mutable fields. So take care not to modify mutable fields passed into constructors, or modify mutable fields obtained by getter methods, unless such modification is explicitly marked as safe.

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TNF_ABSOLUTE_URI](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_ABSOLUTE_URI:kotlin.Short) Indicates the type field contains an absolute-URI BNF construct defined by RFC 3986. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TNF_EMPTY](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_EMPTY:kotlin.Short) Indicates the record is empty. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TNF_EXTERNAL_TYPE](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_EXTERNAL_TYPE:kotlin.Short) Indicates the type field contains an external type name. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TNF_MIME_MEDIA](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_MIME_MEDIA:kotlin.Short) Indicates the type field contains a media-type BNF construct, defined by RFC 2046. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TNF_UNCHANGED](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_UNCHANGED:kotlin.Short) Indicates the payload is an intermediate or final chunk of a chunked NDEF Record. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TNF_UNKNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_UNKNOWN:kotlin.Short) Indicates the payload type is unknown. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) Indicates the type field contains a well-known RTD type name. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#NdefRecord(kotlin.ByteArray))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Construct an NDEF Record from raw bytes. |
| [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#NdefRecord(kotlin.Short,%20kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.ByteArray))`(`tnf:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `type:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `id:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `payload:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Construct an NDEF Record from its component fields. |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | [createApplicationRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createApplicationRecord(kotlin.String))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new Android Application Record (AAR). |
| static [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | [createExternal](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createExternal(kotlin.String,%20kotlin.String,%20kotlin.ByteArray))`(`domain:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Create a new NDEF Record containing external (application-specific) data. |
| static [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | [createMime](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createMime(kotlin.String,%20kotlin.ByteArray))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Create a new NDEF Record containing MIME data. |
| --- | --- |
| static [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | [createTextRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createTextRecord(kotlin.String,%20kotlin.String))`(`languageCode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new NDEF record containing UTF-8 text data. |
| static [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | [createUri](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createUri(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Create a new NDEF Record containing a URI. |
| static [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | [createUri](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createUri(kotlin.String))`(`uriString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new NDEF Record containing a URI. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the specified NDEF Record contains identical tnf, type, id and payload fields. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getId](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#getId())`()` Returns the variable length ID. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getPayload](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#getPayload())`()` Returns the variable length payload. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getTnf](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#getTnf())`()` Returns the 3-bit TNF. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getType](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#getType())`()` Returns the variable length Type field. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#hashCode())`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [toByteArray](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#toByteArray())`()` Return this NDEF Record as a byte array. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toMimeType](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#toMimeType())`()` Map this record to a MIME type, or return null if it cannot be mapped. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#toString())`()` <br /> |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [toUri](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#toUri())`()` Map this record to a URI, or return null if it cannot be mapped. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#CREATOR:android.os.Parcelable.Creator) <br /> |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [RTD_ALTERNATIVE_CARRIER](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_ALTERNATIVE_CARRIER:kotlin.ByteArray) RTD Alternative Carrier type. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [RTD_HANDOVER_CARRIER](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_HANDOVER_CARRIER:kotlin.ByteArray) RTD Handover Carrier type. |
| --- | --- |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [RTD_HANDOVER_REQUEST](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_HANDOVER_REQUEST:kotlin.ByteArray) RTD Handover Request type. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [RTD_HANDOVER_SELECT](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_HANDOVER_SELECT:kotlin.ByteArray) RTD Handover Select type. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [RTD_SMART_POSTER](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_SMART_POSTER:kotlin.ByteArray) RTD Smart Poster type. |
| --- | --- |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [RTD_TEXT](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_TEXT:kotlin.ByteArray) RTD Text type. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [RTD_URI](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_URI:kotlin.ByteArray) RTD URI type. |

## Constants

### TNF_ABSOLUTE_URI

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TNF_ABSOLUTE_URI: Short
```

Indicates the type field contains an absolute-URI BNF construct defined by RFC 3986.

When creating new records prefer #createUri, since it offers more compact URI encoding (#RTD_URI allows compression of common URI prefixes). 

 Value: 3

**See Also**

### TNF_EMPTY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TNF_EMPTY: Short
```

Indicates the record is empty.

Type, id and payload fields are empty in a TNF_EMPTY record. 

 Value: 0

### TNF_EXTERNAL_TYPE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TNF_EXTERNAL_TYPE: Short
```

Indicates the type field contains an external type name.

Used to encode custom payloads. When creating new records use the helper [createExternal](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createExternal(kotlin.String,%20kotlin.String,%20kotlin.ByteArray)).

The external-type RTD format is specified in NFCForum-TS-RTD_1.0.

<br />

Note this TNF should not be used with RTD_TEXT or RTD_URI constants. Those are well known RTD constants, not external RTD constants. 

 Value: 4

**See Also**

- [#createExternal](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createExternal(kotlin.String,%20kotlin.String,%20kotlin.ByteArray)) 

### TNF_MIME_MEDIA

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TNF_MIME_MEDIA: Short
```

Indicates the type field contains a media-type BNF construct, defined by RFC 2046.

Use this with MIME type names such as "image/jpeg", or using the helper [createMime](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createMime(kotlin.String,%20kotlin.ByteArray)). 

 Value: 2

**See Also**

- [#createMime](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createMime(kotlin.String,%20kotlin.ByteArray)) 

### TNF_UNCHANGED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TNF_UNCHANGED: Short
```

Indicates the payload is an intermediate or final chunk of a chunked NDEF Record.

TNF_UNCHANGED can not be used with this class since all [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#) s are already unchunked, however they may appear in the binary format. 

 Value: 6

### TNF_UNKNOWN

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TNF_UNKNOWN: Short
```

Indicates the payload type is unknown.

NFC Forum explains this should be treated similarly to the "application/octet-stream" MIME type. The payload type is not explicitly encoded within the record.

The type field is empty in an TNF_UNKNOWN record. 

 Value: 5

### TNF_WELL_KNOWN

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TNF_WELL_KNOWN: Short
```

Indicates the type field contains a well-known RTD type name.

Use this tnf with RTD types such as [RTD_TEXT](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_TEXT:kotlin.ByteArray), [RTD_URI](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_URI:kotlin.ByteArray).

The RTD type name format is specified in NFCForum-TS-RTD_1.0. 

 Value: 1

**See Also**

- [#RTD_URI](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_URI:kotlin.ByteArray)
- [#RTD_TEXT](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_TEXT:kotlin.ByteArray)
- [#RTD_SMART_POSTER](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_SMART_POSTER:kotlin.ByteArray)

## Public constructors

### NdefRecord

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NdefRecord(data: ByteArray!)
```

**Deprecated:** *use[NdefMessage.NdefMessage(byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.ByteArray))instead.*

Construct an NDEF Record from raw bytes.

This method is deprecated, use[NdefMessage.NdefMessage(byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.ByteArray))instead. This is because it does not make sense to parse a record: the NDEF binary format is only defined for a message, and the record flags MB and ME do not make sense outside of the context of an entire message.

This implementation will attempt to parse a single record by ignoring the MB and ME flags, and otherwise following the rules of[NdefMessage.NdefMessage(byte[])](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#NdefMessage(kotlin.ByteArray)).

<br />

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:raw bytes to parse |

| Exceptions ||
|-------------------------------|--------------------------------------------------|
| `android.nfc.FormatException` | if the data cannot be parsed into a valid record |

### NdefRecord

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NdefRecord(
    tnf: Short, 
    type: ByteArray!, 
    id: ByteArray!, 
    payload: ByteArray!)
```

Construct an NDEF Record from its component fields.

Recommend to use helpers such as {#createUri} or { [createExternal](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#createExternal(kotlin.String,%20kotlin.String,%20kotlin.ByteArray))where possible, since they perform stricter validation that the record is correctly formatted as per NDEF specifications. However if you know what you are doing then this constructor offers the most flexibility.

An [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#) represents a logical (complete) record, and cannot represent NDEF Record chunks.

Basic validation of the tnf, type, id and payload is performed as per the following rules:

- The tnf paramter must be a 3-bit value.
- Records with a tnf of [TNF_EMPTY](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_EMPTY:kotlin.Short) cannot have a type, id or payload.
- Records with a tnf of [TNF_UNKNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_UNKNOWN:kotlin.Short) or 0x07 cannot have a type.
- Records with a tnf of [TNF_UNCHANGED](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_UNCHANGED:kotlin.Short) are not allowed since this class only represents complete (unchunked) records.

This minimal validation is specified by NFCForum-TS-NDEF_1.0 section 3.2.6 (Type Name Format).

If any of the above validation steps fail then [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) is thrown.

Deep inspection of the type, id and payload fields is not performed, so it is possible to create NDEF Records that conform to section 3.2.6 but fail other more strict NDEF specification requirements. For example, the payload may be invalid given the tnf and type.

To omit a type, id or payload field, set the parameter to an empty byte array or null.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tnf` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):a 3-bit TNF constant |
| `type` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array, containing zero to 255 bytes, or null |
| `id` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array, containing zero to 255 bytes, or null |
| --- | --- |
| `payload` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array, containing zero to (2 \*\* 32 - 1) bytes, or null |

| Exceptions ||
|----------------------------|-------------------------------------|
| `IllegalArugmentException` | if a valid record cannot be created |

## Public methods

### createApplicationRecord

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createApplicationRecord(packageName: String!): NdefRecord!
```

Create a new Android Application Record (AAR).

This record indicates to other Android devices the package that should be used to handle the entire NDEF message. You can embed this record anywhere into your message to ensure that the intended package receives the message.

When an Android device dispatches an [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage) containing one or more Android application records, the applications contained in those records will be the preferred target for the [NfcAdapter.ACTION_NDEF_DISCOVERED](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String) intent, in the order in which they appear in the message. This dispatch behavior was first added to Android in Ice Cream Sandwich.

If none of the applications have a are installed on the device, a Market link will be opened to the first application.

Note that Android application records do not overrule applications that have called [NfcAdapter.enableForegroundDispatch](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableForegroundDispatch(android.app.Activity,%20android.app.PendingIntent,%20kotlin.Array,%20kotlin.Array)).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Android package name |

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------|
| [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | Android application NDEF record |

### createExternal

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createExternal(
    domain: String!, 
    type: String!, 
    data: ByteArray!
): NdefRecord!
```

Create a new NDEF Record containing external (application-specific) data.

Use this method to encode application specific data into an NDEF Record. The data is typed by a domain name (usually your Android package name) and a domain-specific type. This data is packaged into a "NFC Forum External Type" NDEF Record.

NFC Forum requires that the domain and type used in an external record are treated as case insensitive, however Android intent filtering is always case sensitive. So this method will force the domain and type to lower-case before creating the NDEF Record.

The unchecked exception [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) will be thrown if the domain and type have serious problems, for example if either field is empty, so always catch this exception if you are passing user-generated data into this method.

There are no such restrictions on the payload data.

For efficiency, This method might not make an internal copy of the data byte array, so take care not to modify the data byte array while still using the returned NdefRecord. Reference specification: NFCForum-TS-RTD_1.0

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `domain` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:domain-name of issuing organization |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:domain-specific type of data |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:payload as bytes |
| --- | --- |

| Exceptions ||
|----------------------------|-----------------------------------------------|
| `IllegalArugmentException` | if either domain or type are empty or invalid |

### createMime

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createMime(
    mimeType: String!, 
    mimeData: ByteArray!
): NdefRecord!
```

Create a new NDEF Record containing MIME data.

Use this method to encode MIME-typed data into an NDEF Record, such as "text/plain", or "image/jpeg".

The mimeType parameter will be normalized with [Intent.normalizeMimeType](https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String))to follow Android best practices for intent filtering, for example to force lower-case. However the unchecked exception [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) may be thrown if the mimeType parameter has serious problems, for example if it is empty, so always catch this exception if you are passing user-generated data into this method.

For efficiency, This method might not make an internal copy of the mimeData byte array, so take care not to modify the mimeData byte array while still using the returned NdefRecord.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a valid MIME type |
| `mimeData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:MIME data as bytes |

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------|
| [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | an NDEF Record containing the MIME-typed data |

| Exceptions ||
|----------------------------|-------------------------------------|
| `IllegalArugmentException` | if the mimeType is empty or invalid |

### createTextRecord

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createTextRecord(
    languageCode: String!, 
    text: String!
): NdefRecord!
```

Create a new NDEF record containing UTF-8 text data.

The caller can either specify the language code for the provided text, or otherwise the language code corresponding to the current default locale will be used. Reference specification: NFCForum-TS-RTD_Text_1.0

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `languageCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The languageCode for the record. If locale is empty or null, the language code of the current default locale will be used. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The text to be encoded in the record. Will be represented in UTF-8 format. |

| Exceptions ||
|--------------------------------------|-----------------|
| `java.lang.IllegalArgumentException` | if text is null |

### createUri

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createUri(uri: Uri!): NdefRecord!
```

Create a new NDEF Record containing a URI.

Use this method to encode a URI (or URL) into an NDEF Record.

Uses the well known URI type representation: [TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) and [RTD_URI](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_URI:kotlin.ByteArray). This is the most efficient encoding of a URI into NDEF.

The uri parameter will be normalized with [Uri.normalizeScheme](https://developer.android.com/reference/kotlin/android/net/Uri.html#normalizeScheme())to set the scheme to lower case to follow Android best practices for intent filtering. However the unchecked exception [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) may be thrown if the uri parameter has serious problems, for example if it is empty, so always catch this exception if you are passing user-generated data into this method.

Reference specification: NFCForum-TS-RTD_URI_1.0

| Parameters ||
|-------|---------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:URI to encode. |

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------|
| [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | an NDEF Record containing the URI |

| Exceptions ||
|----------------------------|--------------------------------|
| `IllegalArugmentException` | if the uri is empty or invalid |

### createUri

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createUri(uriString: String!): NdefRecord!
```

Create a new NDEF Record containing a URI.

Use this method to encode a URI (or URL) into an NDEF Record.

Uses the well known URI type representation: [TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) and [RTD_URI](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_URI:kotlin.ByteArray). This is the most efficient encoding of a URI into NDEF.

The uriString parameter will be normalized with [Uri.normalizeScheme](https://developer.android.com/reference/kotlin/android/net/Uri.html#normalizeScheme())to set the scheme to lower case to follow Android best practices for intent filtering. However the unchecked exception [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) may be thrown if the uriString parameter has serious problems, for example if it is empty, so always catch this exception if you are passing user-generated data into this method.

Reference specification: NFCForum-TS-RTD_URI_1.0

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------|
| `uriString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string URI to encode. |

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------|
| [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#)! | an NDEF Record containing the URI |

| Exceptions ||
|----------------------------|--------------------------------------|
| `IllegalArugmentException` | if the uriString is empty or invalid |

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

Returns true if the specified NDEF Record contains identical tnf, type, id and payload fields.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): ByteArray!
```

Returns the variable length ID.

Returns an empty byte array if this record does not have an id field. 

### getPayload

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPayload(): ByteArray!
```

Returns the variable length payload.

Returns an empty byte array if this record does not have a payload field. 

### getTnf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTnf(): Short
```

Returns the 3-bit TNF.

TNF is the top-level type. 

### getType

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): ByteArray!
```

Returns the variable length Type field.

This should be used in conjunction with the TNF field to determine the payload format.

Returns an empty byte array if this record does not have a type field. 

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
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByteArray(): ByteArray!
```

**Deprecated:** *use [NdefMessage.toByteArray()](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray())instead*

Return this NDEF Record as a byte array.

This method is deprecated, use [NdefMessage.toByteArray](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage#toByteArray())instead. This is because the NDEF binary format is not defined for a record outside of the context of a message: the MB and ME flags cannot be set without knowing the location inside a message.

This implementation will attempt to serialize a single record by always setting the MB and ME flags (in other words, assume this is a single-record NDEF Message).

<br />

### toMimeType

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMimeType(): String!
```

Map this record to a MIME type, or return null if it cannot be mapped.

Currently this method considers all [TNF_MIME_MEDIA](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_MIME_MEDIA:kotlin.Short) records to be MIME records, as well as some [TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) records such as [RTD_TEXT](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_TEXT:kotlin.ByteArray). If this is a MIME record then the MIME type as string is returned, otherwise null is returned.

This method does not perform validation that the MIME type is actually valid. It always attempts to return a string containing the type if this is a MIME record.

The returned MIME type will by normalized to lower-case using [Intent.normalizeMimeType](https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String)).

The MIME payload can be obtained using [getPayload](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#getPayload()).

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | MIME type as a string, or null if this is not a MIME record |

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### toUri

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toUri(): Uri!
```

Map this record to a URI, or return null if it cannot be mapped.

Currently this method considers the following to be URI records:

- [TNF_ABSOLUTE_URI](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_ABSOLUTE_URI:kotlin.Short) records.
- [TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) with a type of [RTD_URI](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_URI:kotlin.ByteArray).
- [TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) with a type of [RTD_SMART_POSTER](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#RTD_SMART_POSTER:kotlin.ByteArray) and containing a URI record in the NDEF message nested in the payload.
- [TNF_EXTERNAL_TYPE](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_EXTERNAL_TYPE:kotlin.Short) records.

If this is not a URI record by the above rules, then null is returned.

This method does not perform validation that the URI is actually valid: it always attempts to create and return a URI if this record appears to be a URI record by the above rules.

The returned URI will be normalized to have a lower case scheme using [Uri.normalizeScheme](https://developer.android.com/reference/kotlin/android/net/Uri.html#normalizeScheme()).

<br />

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | URI, or null if this is not a URI record |

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
static val CREATOR: Parcelable.Creator<NdefRecord!>
```  

### RTD_ALTERNATIVE_CARRIER

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTD_ALTERNATIVE_CARRIER: ByteArray!
```

RTD Alternative Carrier type. For use with TNF_WELL_KNOWN. 
**See Also**

- [#TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) 

### RTD_HANDOVER_CARRIER

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTD_HANDOVER_CARRIER: ByteArray!
```

RTD Handover Carrier type. For use with TNF_WELL_KNOWN. 
**See Also**

- [#TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) 

### RTD_HANDOVER_REQUEST

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTD_HANDOVER_REQUEST: ByteArray!
```

RTD Handover Request type. For use with TNF_WELL_KNOWN. 
**See Also**

- [#TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) 

### RTD_HANDOVER_SELECT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTD_HANDOVER_SELECT: ByteArray!
```

RTD Handover Select type. For use with TNF_WELL_KNOWN. 
**See Also**

- [#TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) 

### RTD_SMART_POSTER

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTD_SMART_POSTER: ByteArray!
```

RTD Smart Poster type. For use with TNF_WELL_KNOWN. 
**See Also**

- [#TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) 

### RTD_TEXT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTD_TEXT: ByteArray!
```

RTD Text type. For use with TNF_WELL_KNOWN. 
**See Also**

- [#TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short) 

### RTD_URI

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTD_URI: ByteArray!
```

RTD URI type. For use with TNF_WELL_KNOWN. 
**See Also**

- [#TNF_WELL_KNOWN](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord#TNF_WELL_KNOWN:kotlin.Short)
