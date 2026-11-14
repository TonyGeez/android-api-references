# Ndef

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Ndef

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/Ndef "View this page in Java") 
| --- | --- |

```
class Ndef : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#) |

Provides access to NDEF content and operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#).

Acquire a [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#) object using [get](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#get(android.nfc.Tag)).

NDEF is an NFC Forum data format. The data formats are implemented in [android.nfc.NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#) and [android.nfc.NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord.html#). This class provides methods to retrieve and modify the [android.nfc.NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#) on a tag.

There are currently four NFC Forum standardized tag types that can be formatted to contain NDEF data.

- NFC Forum Type 1 Tag ([NFC_FORUM_TYPE_1](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_1:kotlin.String)), such as the Innovision Topaz
- NFC Forum Type 2 Tag ([NFC_FORUM_TYPE_2](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_2:kotlin.String)), such as the NXP MIFARE Ultralight
- NFC Forum Type 3 Tag ([NFC_FORUM_TYPE_3](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_3:kotlin.String)), such as Sony Felica
- NFC Forum Type 4 Tag ([NFC_FORUM_TYPE_4](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_4:kotlin.String)), such as NXP MIFARE Desfire

It is mandatory for all Android devices with NFC to correctly enumerate [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#) on NFC Forum Tag Types 1-4, and implement all NDEF operations as defined in this class.

Some vendors have their own well defined specifications for storing NDEF data on tags that do not fall into the above categories. Android devices with NFC should enumerate and implement [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#) under these vendor specifications where possible, but it is not mandatory. [getType](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#getType())returns a String describing this specification, for example [MIFARE_CLASSIC](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#MIFARE_CLASSIC:kotlin.String) is`com.nxp.ndef.mifareclassic`.

Android devices that support MIFARE Classic must also correctly implement [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#) on MIFARE Classic tags formatted to NDEF.

For guaranteed compatibility across all Android devices with NFC, it is recommended to use NFC Forum Types 1-4 in new deployments of NFC tags with NDEF payload. Vendor NDEF formats will not work on all Android devices.

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MIFARE_CLASSIC](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#MIFARE_CLASSIC:kotlin.String) NDEF on MIFARE Classic |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NFC_FORUM_TYPE_1](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_1:kotlin.String) NFC Forum Tag Type 1 |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NFC_FORUM_TYPE_2](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_2:kotlin.String) NFC Forum Tag Type 2 |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NFC_FORUM_TYPE_3](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_3:kotlin.String) NFC Forum Tag Type 3 |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NFC_FORUM_TYPE_4](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_4:kotlin.String) NFC Forum Tag Type 4 |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canMakeReadOnly](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#canMakeReadOnly())`()` Indicates whether a tag can be made read-only with [makeReadOnly()](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#makeReadOnly()). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#connect())`()` <br /> |
| --- | --- |
| static [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#)! | [get](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#get(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!`)` Get an instance of [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#) for the given tag. |
| [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)! | [getCachedNdefMessage](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#getCachedNdefMessage())`()` Get the [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#) that was read from the tag at discovery time. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSize](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#getMaxSize())`()` Get the maximum NDEF message size in bytes. |
| --- | --- |
| [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)! | [getNdefMessage](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#getNdefMessage())`()` Read the current [android.nfc.NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#) on this tag. |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#getTag())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#getType())`()` Get the NDEF tag type. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#isConnected())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWritable](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#isWritable())`()` Determine if the tag is writable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [makeReadOnly](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#makeReadOnly())`()` Make a tag read-only. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNdefMessage](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#writeNdefMessage(android.nfc.NdefMessage))`(`msg:` ` [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)!`)` Overwrite the [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#) on this tag. |

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

Indicates whether a tag can be made read-only with [makeReadOnly()](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#makeReadOnly()).

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

Get an instance of [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#) for the given tag.

Returns null if [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#) was not enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()). This indicates the tag is not NDEF formatted, or that this tag is NDEF formatted but under a vendor specification that this Android device does not implement.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!:an NDEF compatible tag |

| Return ||
|--------------------------------------------------------------------------------|-------------|
| [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#)! | Ndef object |

### getCachedNdefMessage

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCachedNdefMessage(): NdefMessage!
```

Get the [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#) that was read from the tag at discovery time.

If the NDEF Message is modified by an I/O operation then it will not be updated here, this function only returns what was discovered when the tag entered the field.

Note that this method may return null if the tag was in the INITIALIZED state as defined by NFC Forum, as in this state the tag is formatted to support NDEF but does not contain a message yet.

Does not cause any RF activity and does not block.

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)! | NDEF Message read from the tag at discovery time, can be null |

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

Read the current [android.nfc.NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#) on this tag.

This always reads the current NDEF Message stored on the tag.

Note that this method may return null if the tag was in the INITIALIZED state as defined by NFC Forum, as in that state the tag is formatted to support NDEF but does not contain a message yet.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------|
| [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)! | the NDEF Message, can be null |

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
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology) object. |

### getType

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String!
```

Get the NDEF tag type.

Returns one of [NFC_FORUM_TYPE_1](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_1:kotlin.String), [NFC_FORUM_TYPE_2](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_2:kotlin.String), [NFC_FORUM_TYPE_3](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_3:kotlin.String), [NFC_FORUM_TYPE_4](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#NFC_FORUM_TYPE_4:kotlin.String), [MIFARE_CLASSIC](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#MIFARE_CLASSIC:kotlin.String) or another NDEF tag type that has not yet been formalized in this Android API.

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

Requires [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

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

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

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

Overwrite the [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#) on this tag.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)!:the NDEF Message to write, must not be null |

| Exceptions ||
|--------------------------------|--------------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |
| `android.nfc.FormatException` | if the NDEF Message to write is malformed |
| --- | --- |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
