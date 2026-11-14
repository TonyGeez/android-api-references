# NfcBarcode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcBarcode

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/NfcBarcode "View this page in Java") 

```
class NfcBarcode : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.nfc.tech.NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#) |

Provides access to tags containing just a barcode.

Acquire an [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#) object using [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#get(android.nfc.Tag)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_KOVIO](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#TYPE_KOVIO:kotlin.Int) Kovio Tags |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#TYPE_UNKNOWN:kotlin.Int) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#connect())`()` <br /> |
| static [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#)! | [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#get(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!`)` Get an instance of [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#) for the given tag. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#getBarcode())`()` Returns the barcode of an NfcBarcode tag. |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#getTag())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#getType())`()` Returns the NFC Barcode tag type. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#isConnected())`()` <br /> |

## Constants

### TYPE_KOVIO

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_KOVIO: Int
```

Kovio Tags 

 Value: 1

### TYPE_UNKNOWN

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: Int
```  

 Value: -1

## Public methods

### close

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### connect

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(): Unit
```

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or connect is canceled |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### get

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun get(tag: Tag!): NfcBarcode!
```

Get an instance of [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#) for the given tag.

Returns null if [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#) was not enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()).

Does not cause any RF activity and does not block.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!:an NfcBarcode compatible tag |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------|
| [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#)! | NfcBarcode object |

### getBarcode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBarcode(): ByteArray!
```

Returns the barcode of an NfcBarcode tag.

Tags of [TYPE_KOVIO](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#TYPE_KOVIO:kotlin.Int) return 16 bytes:

- The first byte is 0x80 ORd with a manufacturer ID, corresponding to ISO/IEC 7816-6.
- The second byte describes the payload data format. Defined data format types include the following:
- 0x00: Reserved for manufacturer assignment
- 0x01: 96-bit URL with "http://www." prefix
- 0x02: 96-bit URL with "https://www." prefix
- 0x03: 96-bit URL with "http://" prefix
- 0x04: 96-bit URL with "https://" prefix
- 0x05: 96-bit GS1 EPC
- 0x06-0xFF: reserved
- The following 12 bytes are payload:
- In case of a URL payload, the payload is encoded in US-ASCII, following the limitations defined in RFC3987. {@see [RFC 3987](http://www.ietf.org/rfc/rfc3987.txt)}
- In case of GS1 EPC data, see [GS1 Electronic Product Code (EPC) Tag Data Standard (TDS)](http://www.gs1.org/gsmp/kc/epcglobal/tds/) for more details.
- The last 2 bytes comprise the CRC.

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing the barcode |

**See Also**

### getTag

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): Tag!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology) object. |

### getType

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the NFC Barcode tag type.

Currently only one of [TYPE_KOVIO](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#TYPE_KOVIO:kotlin.Int) or [TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode#TYPE_UNKNOWN:kotlin.Int).

Does not cause any RF activity and does not block.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the NFC Barcode tag type |

### isConnected

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |
