# MifareUltralight

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MifareUltralight

Kotlin| [Java](MifareUltralight.md) 
| --- | --- |

```
class MifareUltralight : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.MifareUltralight](MifareUltralight.md) |

Provides access to MIFARE Ultralight properties and I/O operations on a [Tag](../android.nfc/Tag.md).

Acquire a [MifareUltralight](MifareUltralight.md) object using [get](MifareUltralight.md)).

MIFARE Ultralight compatible tags have 4 byte pages [PAGE_SIZE](MifareUltralight.md). The primary operations on an Ultralight tag are [readPages](MifareUltralight.md))and [writePage](MifareUltralight.md)).

The original MIFARE Ultralight consists of a 64 byte EEPROM. The first 4 pages are for the OTP area, manufacturer data, and locking bits. They are readable and some bits are writable. The final 12 pages are the user read/write area. For more information see the NXP data sheet MF0ICU1.

The MIFARE Ultralight C consists of a 192 byte EEPROM. The first 4 pages are for OTP, manufacturer data, and locking bits. The next 36 pages are the user read/write area. The next 4 pages are additional locking bits, counters and authentication configuration and are readable. The final 4 pages are for the authentication key and are not readable. For more information see the NXP data sheet MF0ICU2.

Implementation of this class on a Android NFC device is optional. If it is not implemented, then [MifareUltralight](MifareUltralight.md) will never be enumerated in [Tag.getTechList](../android.nfc/Tag.md)). If it is enumerated, then all [MifareUltralight](MifareUltralight.md) I/O operations will be supported. In either case, [NfcA](NfcA.md) will also be enumerated on the tag, because all MIFARE Ultralight tags are also [NfcA](NfcA.md) tags.

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAGE_SIZE](MifareUltralight.md) Size of a MIFARE Ultralight page in bytes |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ULTRALIGHT](MifareUltralight.md) A MIFARE Ultralight tag |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ULTRALIGHT_C](MifareUltralight.md) A MIFARE Ultralight C tag |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNKNOWN](MifareUltralight.md) A MIFARE Ultralight compatible tag of unknown type |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](MifareUltralight.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](MifareUltralight.md))`()` <br /> |
| static [MifareUltralight](MifareUltralight.md)! | [get](MifareUltralight.md))`(`tag:` ` [Tag](../android.nfc/Tag.md)!`)` Get an instance of [MifareUltralight](MifareUltralight.md) for the given tag. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](MifareUltralight.md))`()` Return the maximum number of bytes that can be sent with [transceive](MifareUltralight.md)). |
| [Tag](../android.nfc/Tag.md)! | [getTag](MifareUltralight.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeout](MifareUltralight.md))`()` Get the current [transceive](MifareUltralight.md))timeout in milliseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](MifareUltralight.md))`()` Return the MIFARE Ultralight type of the tag. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](MifareUltralight.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readPages](MifareUltralight.md))`(`pageOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read 4 pages (16 bytes). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeout](MifareUltralight.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the [transceive](MifareUltralight.md))timeout in milliseconds. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](MifareUltralight.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw NfcA data to a tag and receive the response. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writePage](MifareUltralight.md))`(`pageOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Write 1 page (4 bytes). |
| --- | --- |

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
static fun get(tag: Tag!): MifareUltralight!
```

Get an instance of [MifareUltralight](MifareUltralight.md) for the given tag.

Returns null if [MifareUltralight](MifareUltralight.md) was not enumerated in [Tag.getTechList](../android.nfc/Tag.md))- this indicates the tag is not MIFARE Ultralight compatible, or that this Android device does not implement MIFARE Ultralight.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](../android.nfc/Tag.md)!:an MIFARE Ultralight compatible tag |

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------|
| [MifareUltralight](MifareUltralight.md)! | MIFARE Ultralight object |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with [transceive](MifareUltralight.md)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](MifareUltralight.md)). |

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): Tag!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](../android.nfc/Tag.md)! | the [Tag](../android.nfc/Tag.md) backing this [TagTechnology](TagTechnology.md) object. |

### getTimeout

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeout(): Int
```

Get the current [transceive](MifareUltralight.md))timeout in milliseconds.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

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

One of [TYPE_ULTRALIGHT](MifareUltralight.md) or [TYPE_ULTRALIGHT_C](MifareUltralight.md) or [TYPE_UNKNOWN](MifareUltralight.md).

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

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

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

Set the [transceive](MifareUltralight.md))timeout in milliseconds.

The timeout only applies to [transceive](MifareUltralight.md))on this object, and is reset to a default value when #close is called.

Setting a longer timeout may be useful when performing transactions that require a long processing time on the tag such as key generation.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

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

This is equivalent to connecting to this tag via [NfcA](NfcA.md) and calling [NfcA.transceive](NfcA.md)). Note that all MIFARE Classic tags are based on [NfcA](NfcA.md) technology.

Use [getMaxTransceiveLength](MifareUltralight.md))to retrieve the maximum number of bytes that can be sent with [transceive](MifareUltralight.md)).

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission. 
**See Also**

- [android.nfc.tech.NfcA#transceive](NfcA.md)) 

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

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------|
| `pageOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of page to write, starting from 0 |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:4 bytes to write |

| Exceptions ||
|--------------------------------|----------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |
