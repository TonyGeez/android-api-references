# Ndef

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Ndef

Kotlin| [Java](Ndef.md) 
| --- | --- |

```
class Ndef : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.Ndef](Ndef.md) |

Provides access to NDEF content and operations on a [Tag](../android.nfc/Tag.md).

Acquire a [Ndef](Ndef.md) object using [get](Ndef.md)).

NDEF is an NFC Forum data format. The data formats are implemented in [android.nfc.NdefMessage](../android.nfc/NdefMessage.md) and [android.nfc.NdefRecord](../android.nfc/NdefRecord.md). This class provides methods to retrieve and modify the [android.nfc.NdefMessage](../android.nfc/NdefMessage.md) on a tag.

There are currently four NFC Forum standardized tag types that can be formatted to contain NDEF data.

- NFC Forum Type 1 Tag ([NFC_FORUM_TYPE_1](Ndef.md)), such as the Innovision Topaz
- NFC Forum Type 2 Tag ([NFC_FORUM_TYPE_2](Ndef.md)), such as the NXP MIFARE Ultralight
- NFC Forum Type 3 Tag ([NFC_FORUM_TYPE_3](Ndef.md)), such as Sony Felica
- NFC Forum Type 4 Tag ([NFC_FORUM_TYPE_4](Ndef.md)), such as NXP MIFARE Desfire

It is mandatory for all Android devices with NFC to correctly enumerate [Ndef](Ndef.md) on NFC Forum Tag Types 1-4, and implement all NDEF operations as defined in this class.

Some vendors have their own well defined specifications for storing NDEF data on tags that do not fall into the above categories. Android devices with NFC should enumerate and implement [Ndef](Ndef.md) under these vendor specifications where possible, but it is not mandatory. [getType](Ndef.md))returns a String describing this specification, for example [MIFARE_CLASSIC](Ndef.md) is`com.nxp.ndef.mifareclassic`.

Android devices that support MIFARE Classic must also correctly implement [Ndef](Ndef.md) on MIFARE Classic tags formatted to NDEF.

For guaranteed compatibility across all Android devices with NFC, it is recommended to use NFC Forum Types 1-4 in new deployments of NFC tags with NDEF payload. Vendor NDEF formats will not work on all Android devices.

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MIFARE_CLASSIC](Ndef.md) NDEF on MIFARE Classic |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NFC_FORUM_TYPE_1](Ndef.md) NFC Forum Tag Type 1 |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NFC_FORUM_TYPE_2](Ndef.md) NFC Forum Tag Type 2 |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NFC_FORUM_TYPE_3](Ndef.md) NFC Forum Tag Type 3 |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NFC_FORUM_TYPE_4](Ndef.md) NFC Forum Tag Type 4 |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canMakeReadOnly](Ndef.md))`()` Indicates whether a tag can be made read-only with [makeReadOnly()](Ndef.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](Ndef.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](Ndef.md))`()` <br /> |
| --- | --- |
| static [Ndef](Ndef.md)! | [get](Ndef.md))`(`tag:` ` [Tag](../android.nfc/Tag.md)!`)` Get an instance of [Ndef](Ndef.md) for the given tag. |
| [NdefMessage](../android.nfc/NdefMessage.md)! | [getCachedNdefMessage](Ndef.md))`()` Get the [NdefMessage](../android.nfc/NdefMessage.md) that was read from the tag at discovery time. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSize](Ndef.md))`()` Get the maximum NDEF message size in bytes. |
| --- | --- |
| [NdefMessage](../android.nfc/NdefMessage.md)! | [getNdefMessage](Ndef.md))`()` Read the current [android.nfc.NdefMessage](../android.nfc/NdefMessage.md) on this tag. |
| [Tag](../android.nfc/Tag.md)! | [getTag](Ndef.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](Ndef.md))`()` Get the NDEF tag type. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](Ndef.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWritable](Ndef.md))`()` Determine if the tag is writable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [makeReadOnly](Ndef.md))`()` Make a tag read-only. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNdefMessage](Ndef.md))`(`msg:` ` [NdefMessage](../android.nfc/NdefMessage.md)!`)` Overwrite the [NdefMessage](../android.nfc/NdefMessage.md) on this tag. |

## Constants

### MIFARE_CLASSIC

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIFARE_CLASSIC: String
```

NDEF on MIFARE Classic 

 Value: "com.nxp.ndef.mifareclassic"

### NFC_FORUM_TYPE_1

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFC_FORUM_TYPE_1: String
```

NFC Forum Tag Type 1 

 Value: "org.nfcforum.ndef.type1"

### NFC_FORUM_TYPE_2

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFC_FORUM_TYPE_2: String
```

NFC Forum Tag Type 2 

 Value: "org.nfcforum.ndef.type2"

### NFC_FORUM_TYPE_3

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFC_FORUM_TYPE_3: String
```

NFC Forum Tag Type 3 

 Value: "org.nfcforum.ndef.type3"

### NFC_FORUM_TYPE_4

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFC_FORUM_TYPE_4: String
```

NFC Forum Tag Type 4 

 Value: "org.nfcforum.ndef.type4"

## Public methods

### canMakeReadOnly

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canMakeReadOnly(): Boolean
```

Indicates whether a tag can be made read-only with [makeReadOnly()](Ndef.md)).

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if it is possible to make this tag read-only |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### close

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

### connect

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(): Unit
```

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or connect is canceled |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

### get

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun get(tag: Tag!): Ndef!
```

Get an instance of [Ndef](Ndef.md) for the given tag.

Returns null if [Ndef](Ndef.md) was not enumerated in [Tag.getTechList](../android.nfc/Tag.md)). This indicates the tag is not NDEF formatted, or that this tag is NDEF formatted but under a vendor specification that this Android device does not implement.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `tag` | [Tag](../android.nfc/Tag.md)!:an NDEF compatible tag |

| Return ||
|--------------------------------------------------------------------------------|-------------|
| [Ndef](Ndef.md)! | Ndef object |

### getCachedNdefMessage

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCachedNdefMessage(): NdefMessage!
```

Get the [NdefMessage](../android.nfc/NdefMessage.md) that was read from the tag at discovery time.

If the NDEF Message is modified by an I/O operation then it will not be updated here, this function only returns what was discovered when the tag entered the field.

Note that this method may return null if the tag was in the INITIALIZED state as defined by NFC Forum, as in this state the tag is formatted to support NDEF but does not contain a message yet.

Does not cause any RF activity and does not block.

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [NdefMessage](../android.nfc/NdefMessage.md)! | NDEF Message read from the tag at discovery time, can be null |

### getMaxSize

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxSize(): Int
```

Get the maximum NDEF message size in bytes.

Does not cause any RF activity and does not block.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | size in bytes |

### getNdefMessage

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNdefMessage(): NdefMessage!
```

Read the current [android.nfc.NdefMessage](../android.nfc/NdefMessage.md) on this tag.

This always reads the current NDEF Message stored on the tag.

Note that this method may return null if the tag was in the INITIALIZED state as defined by NFC Forum, as in that state the tag is formatted to support NDEF but does not contain a message yet.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------|
| [NdefMessage](../android.nfc/NdefMessage.md)! | the NDEF Message, can be null |

| Exceptions ||
|--------------------------------|--------------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |
| `android.nfc.FormatException` | if the NDEF Message on the tag is malformed |
| --- | --- |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): Tag!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](../android.nfc/Tag.md)! | the [Tag](../android.nfc/Tag.md) backing this [TagTechnology](TagTechnology.md) object. |

### getType

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String!
```

Get the NDEF tag type.

Returns one of [NFC_FORUM_TYPE_1](Ndef.md), [NFC_FORUM_TYPE_2](Ndef.md), [NFC_FORUM_TYPE_3](Ndef.md), [NFC_FORUM_TYPE_4](Ndef.md), [MIFARE_CLASSIC](Ndef.md) or another NDEF tag type that has not yet been formalized in this Android API.

Does not cause any RF activity and does not block.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representing the NDEF tag type |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |

### isWritable

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isWritable(): Boolean
```

Determine if the tag is writable.

NFC Forum tags can be in read-only or read-write states.

Does not cause any RF activity and does not block.

Requires [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the tag is writable |

### makeReadOnly

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun makeReadOnly(): Boolean
```

Make a tag read-only.

This sets the CC field to indicate the tag is read-only, and where possible permanently sets the lock bits to prevent any further modification of the memory.

This is a one-way process and cannot be reverted!

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true on success, false if it is not possible to make this tag read-only |

| Exceptions ||
|--------------------------------|--------------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

### writeNdefMessage

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeNdefMessage(msg: NdefMessage!): Unit
```

Overwrite the [NdefMessage](../android.nfc/NdefMessage.md) on this tag.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [NdefMessage](../android.nfc/NdefMessage.md)!:the NDEF Message to write, must not be null |

| Exceptions ||
|--------------------------------|--------------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |
| `android.nfc.FormatException` | if the NDEF Message to write is malformed |
| --- | --- |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
