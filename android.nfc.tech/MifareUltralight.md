# MifareUltralight

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MifareUltralight

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/MifareUltralight "View this page in Java") 

```
class MifareUltralight : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.nfc.tech.MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#) |

Provides access to MIFARE Ultralight properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#).

Acquire a [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#) object using [get](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#get(android.nfc.Tag)).

MIFARE Ultralight compatible tags have 4 byte pages [PAGE_SIZE](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#PAGE_SIZE:kotlin.Int). The primary operations on an Ultralight tag are [readPages](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#readPages(kotlin.Int))and [writePage](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#writePage(kotlin.Int,%20kotlin.ByteArray)).

The original MIFARE Ultralight consists of a 64 byte EEPROM. The first 4 pages are for the OTP area, manufacturer data, and locking bits. They are readable and some bits are writable. The final 12 pages are the user read/write area. For more information see the NXP data sheet MF0ICU1.

The MIFARE Ultralight C consists of a 192 byte EEPROM. The first 4 pages are for OTP, manufacturer data, and locking bits. The next 36 pages are the user read/write area. The next 4 pages are additional locking bits, counters and authentication configuration and are readable. The final 4 pages are for the authentication key and are not readable. For more information see the NXP data sheet MF0ICU2.

Implementation of this class on a Android NFC device is optional. If it is not implemented, then [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#) will never be enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()). If it is enumerated, then all [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#) I/O operations will be supported. In either case, [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) will also be enumerated on the tag, because all MIFARE Ultralight tags are also [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) tags.

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAGE_SIZE](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#PAGE_SIZE:kotlin.Int) Size of a MIFARE Ultralight page in bytes |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ULTRALIGHT](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#TYPE_ULTRALIGHT:kotlin.Int) A MIFARE Ultralight tag |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ULTRALIGHT_C](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#TYPE_ULTRALIGHT_C:kotlin.Int) A MIFARE Ultralight C tag |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#TYPE_UNKNOWN:kotlin.Int) A MIFARE Ultralight compatible tag of unknown type |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#connect())`()` <br /> |
| static [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#)! | [get](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#get(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!`)` Get an instance of [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#) for the given tag. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#getMaxTransceiveLength())`()` Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray)). |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#getTag())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeout](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#getTimeout())`()` Get the current [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray))timeout in milliseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#getType())`()` Return the MIFARE Ultralight type of the tag. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#isConnected())`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readPages](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#readPages(kotlin.Int))`(`pageOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read 4 pages (16 bytes). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeout](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#setTimeout(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray))timeout in milliseconds. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw NfcA data to a tag and receive the response. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writePage](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#writePage(kotlin.Int,%20kotlin.ByteArray))`(`pageOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Write 1 page (4 bytes). |

## Constants

### PAGE_SIZE

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAGE_SIZE: Int
```

Size of a MIFARE Ultralight page in bytes 

 Value: 4

### TYPE_ULTRALIGHT

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ULTRALIGHT: Int
```

A MIFARE Ultralight tag 

 Value: 1

### TYPE_ULTRALIGHT_C

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ULTRALIGHT_C: Int
```

A MIFARE Ultralight C tag 

 Value: 2

### TYPE_UNKNOWN

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: Int
```

A MIFARE Ultralight compatible tag of unknown type 

 Value: -1

## Public methods

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

### get

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun get(tag: Tag!): MifareUltralight!
```

Get an instance of [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#) for the given tag.

Returns null if [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#) was not enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList())- this indicates the tag is not MIFARE Ultralight compatible, or that this Android device does not implement MIFARE Ultralight.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!:an MIFARE Ultralight compatible tag |

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------|
| [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#)! | MIFARE Ultralight object |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray)). |

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): Tag!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology) object. |

### getTimeout

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeout(): Int
```

Get the current [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray))timeout in milliseconds.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | timeout value in milliseconds |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### getType

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Return the MIFARE Ultralight type of the tag.

One of [TYPE_ULTRALIGHT](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#TYPE_ULTRALIGHT:kotlin.Int) or [TYPE_ULTRALIGHT_C](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#TYPE_ULTRALIGHT_C:kotlin.Int) or [TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#TYPE_UNKNOWN:kotlin.Int).

Depending on how the tag has been formatted, it can be impossible to accurately classify between original MIFARE Ultralight and Ultralight C. So treat this method as a hint.

Does not cause any RF activity and does not block.

| Return ||
|----------------------------------------------------------------------------|----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the type |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |

### readPages

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readPages(pageOffset: Int): ByteArray!
```

Read 4 pages (16 bytes).

The MIFARE Ultralight protocol always reads 4 pages at a time, to reduce the number of commands required to read an entire tag.

If a read spans past the last readable block, then the tag will return pages that have been wrapped back to the first blocks. MIFARE Ultralight tags have readable blocks 0x00 through 0x0F. So a read to block offset 0x0E would return blocks 0x0E, 0x0F, 0x00, 0x01. MIFARE Ultralight C tags have readable blocks 0x00 through 0x2B. So a read to block 0x2A would return blocks 0x2A, 0x2B, 0x00, 0x01.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------|
| `pageOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of first page to read, starting from 0 |

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | 4 pages (16 bytes) |

| Exceptions ||
|--------------------------------|----------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

### setTimeout

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTimeout(timeout: Int): Unit
```

Set the [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray))timeout in milliseconds.

The timeout only applies to [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray))on this object, and is reset to a default value when #close is called.

Setting a longer timeout may be useful when performing transactions that require a long processing time on the tag such as key generation.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):timeout value in milliseconds |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### transceive

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun transceive(data: ByteArray!): ByteArray!
```

Send raw NfcA data to a tag and receive the response.

This is equivalent to connecting to this tag via [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) and calling [NfcA.transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)). Note that all MIFARE Classic tags are based on [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) technology.

Use [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#getMaxTransceiveLength())to retrieve the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight#transceive(kotlin.ByteArray)).

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission. 
**See Also**

- [android.nfc.tech.NfcA#transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)) 

### writePage

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writePage(
    pageOffset: Int, 
    data: ByteArray!
): Unit
```

Write 1 page (4 bytes).

The MIFARE Ultralight protocol always writes 1 page at a time, to minimize EEPROM write cycles.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------|
| `pageOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of page to write, starting from 0 |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:4 bytes to write |

| Exceptions ||
|--------------------------------|----------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |
