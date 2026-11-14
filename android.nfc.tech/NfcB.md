# NfcB

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcB

Kotlin| [Java](../android/nfc/tech/NfcB.md) 
| --- | --- |

```
class NfcB : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NfcB](../android/nfc/tech/NfcB.md) |

Provides access to NFC-B (ISO 14443-3B) properties and I/O operations on a [Tag](../android/nfc/Tag.md).

Acquire a [NfcB](../android/nfc/tech/NfcB.md) object using [get](../android/nfc/tech/NfcB.md)).

The primary NFC-B I/O operation is [transceive](../android/nfc/tech/NfcB.md)). Applications must implement their own protocol stack on top of [transceive](../android/nfc/tech/NfcB.md)).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/nfc/tech/NfcB.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/nfc/tech/NfcB.md))`()` <br /> |
| static [NfcB](../android/nfc/tech/NfcB.md)! | [get](../android/nfc/tech/NfcB.md))`(`tag:` ` [Tag](../android/nfc/Tag.md)!`)` Get an instance of [NfcB](../android/nfc/tech/NfcB.md) for the given tag. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getApplicationData](../android/nfc/tech/NfcB.md))`()` Return the Application Data bytes from ATQB/SENSB_RES at tag discovery. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](../android/nfc/tech/NfcB.md))`()` Return the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/NfcB.md)). |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getProtocolInfo](../android/nfc/tech/NfcB.md))`()` Return the Protocol Info bytes from ATQB/SENSB_RES at tag discovery. |
| --- | --- |
| [Tag](../android/nfc/Tag.md)! | [getTag](../android/nfc/tech/NfcB.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/nfc/tech/NfcB.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](../android/nfc/tech/NfcB.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw NFC-B commands to the tag and receive the response. |
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
static fun get(tag: Tag!): NfcB!
```

Get an instance of [NfcB](../android/nfc/tech/NfcB.md) for the given tag.

Returns null if [NfcB](../android/nfc/tech/NfcB.md) was not enumerated in [Tag.getTechList](../android/nfc/Tag.md)). This indicates the tag does not support NFC-B.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](../android/nfc/Tag.md)!:an NFC-B compatible tag |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [NfcB](../android/nfc/tech/NfcB.md)! | NFC-B object |

### getApplicationData

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getApplicationData(): ByteArray!
```

Return the Application Data bytes from ATQB/SENSB_RES at tag discovery.

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | Application Data bytes from ATQB/SENSB_RES bytes |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/NfcB.md)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/NfcB.md)). |

### getProtocolInfo

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProtocolInfo(): ByteArray!
```

Return the Protocol Info bytes from ATQB/SENSB_RES at tag discovery.

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | Protocol Info bytes from ATQB/SENSB_RES bytes |

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

Send raw NFC-B commands to the tag and receive the response.

Applications must not append the EoD (CRC) to the payload, it will be automatically calculated.

Applications must not send commands that manage the polling loop and initialization (SENSB_REQ, SLOT_MARKER etc).

Use [getMaxTransceiveLength](../android/nfc/tech/NfcB.md))to retrieve the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/NfcB.md)).

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
