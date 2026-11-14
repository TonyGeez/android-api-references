# NfcBarcode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcBarcode

Kotlin| [Java](NfcBarcode.md) 
| --- | --- |

```
class NfcBarcode : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NfcBarcode](NfcBarcode.md) |

Provides access to tags containing just a barcode.

Acquire an [NfcBarcode](NfcBarcode.md) object using [get](NfcBarcode.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_KOVIO](NfcBarcode.md) Kovio Tags |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNKNOWN](NfcBarcode.md) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](NfcBarcode.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](NfcBarcode.md))`()` <br /> |
| static [NfcBarcode](NfcBarcode.md)! | [get](NfcBarcode.md))`(`tag:` ` [Tag](../android.nfc/Tag.md)!`)` Get an instance of [NfcBarcode](NfcBarcode.md) for the given tag. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBarcode](NfcBarcode.md))`()` Returns the barcode of an NfcBarcode tag. |
| [Tag](../android.nfc/Tag.md)! | [getTag](NfcBarcode.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](NfcBarcode.md))`()` Returns the NFC Barcode tag type. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](NfcBarcode.md))`()` <br /> |

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
| --- | --- |

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
| --- | --- |

### get

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun get(tag: Tag!): NfcBarcode!
```

Get an instance of [NfcBarcode](NfcBarcode.md) for the given tag.

Returns null if [NfcBarcode](NfcBarcode.md) was not enumerated in [Tag.getTechList](../android.nfc/Tag.md)).

Does not cause any RF activity and does not block.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](../android.nfc/Tag.md)!:an NfcBarcode compatible tag |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------|
| [NfcBarcode](NfcBarcode.md)! | NfcBarcode object |

### getBarcode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBarcode(): ByteArray!
```

Returns the barcode of an NfcBarcode tag.

Tags of [TYPE_KOVIO](NfcBarcode.md) return 16 bytes:

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
| [Tag](../android.nfc/Tag.md)! | the [Tag](../android.nfc/Tag.md) backing this [TagTechnology](TagTechnology.md) object. |

### getType

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the NFC Barcode tag type.

Currently only one of [TYPE_KOVIO](NfcBarcode.md) or [TYPE_UNKNOWN](NfcBarcode.md).

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
