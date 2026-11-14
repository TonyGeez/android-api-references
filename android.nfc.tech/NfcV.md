# NfcV

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcV

Kotlin| [Java](../android/nfc/tech/NfcV.md) 
| --- | --- |

```
class NfcV : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NfcV](../android/nfc/tech/NfcV.md) |

Provides access to NFC-V (ISO 15693) properties and I/O operations on a [Tag](../android/nfc/Tag.md).

Acquire a [NfcV](../android/nfc/tech/NfcV.md) object using [get](../android/nfc/tech/NfcV.md)).

The primary NFC-V I/O operation is [transceive](../android/nfc/tech/NfcV.md)). Applications must implement their own protocol stack on top of [transceive](../android/nfc/tech/NfcV.md)).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/nfc/tech/NfcV.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/nfc/tech/NfcV.md))`()` <br /> |
| static [NfcV](../android/nfc/tech/NfcV.md)! | [get](../android/nfc/tech/NfcV.md))`(`tag:` ` [Tag](../android/nfc/Tag.md)!`)` Get an instance of [NfcV](../android/nfc/tech/NfcV.md) for the given tag. |
| --- | --- |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getDsfId](../android/nfc/tech/NfcV.md))`()` Return the DSF ID bytes from tag discovery. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](../android/nfc/tech/NfcV.md))`()` Return the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/NfcV.md)). |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getResponseFlags](../android/nfc/tech/NfcV.md))`()` Return the Response Flag bytes from tag discovery. |
| --- | --- |
| [Tag](../android/nfc/Tag.md)! | [getTag](../android/nfc/tech/NfcV.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/nfc/tech/NfcV.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](../android/nfc/tech/NfcV.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw NFC-V commands to the tag and receive the response. |
| --- | --- |

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
static fun get(tag: Tag!): NfcV!
```

Get an instance of [NfcV](../android/nfc/tech/NfcV.md) for the given tag.

Returns null if [NfcV](../android/nfc/tech/NfcV.md) was not enumerated in [Tag.getTechList](../android/nfc/Tag.md)). This indicates the tag does not support NFC-V.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](../android/nfc/Tag.md)!:an NFC-V compatible tag |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [NfcV](../android/nfc/tech/NfcV.md)! | NFC-V object |

### getDsfId

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDsfId(): Byte
```

Return the DSF ID bytes from tag discovery.

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | DSF ID bytes |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/NfcV.md)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/NfcV.md)). |

### getResponseFlags

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResponseFlags(): Byte
```

Return the Response Flag bytes from tag discovery.

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | Response Flag bytes |

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): Tag!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](../android/nfc/Tag.md)! | the [Tag](../android/nfc/Tag.md) backing this [TagTechnology](../android/nfc/tech/TagTechnology.md) object. |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |

### transceive

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun transceive(data: ByteArray!): ByteArray!
```

Send raw NFC-V commands to the tag and receive the response.

Applications must not append the CRC to the payload, it will be automatically calculated. The application does provide FLAGS, CMD and PARAMETER bytes.

Use [getMaxTransceiveLength](../android/nfc/tech/NfcV.md))to retrieve the maximum amount of bytes that can be sent with [transceive](../android/nfc/tech/NfcV.md)).

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java/io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:bytes to send |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | bytes received in response |

| Exceptions ||
|-----------------------|-----------------------------------------------------------|
| `TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or this operation is canceled |
