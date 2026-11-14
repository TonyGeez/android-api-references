# NfcB

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcB

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/NfcB "View this page in Java") 
| --- | --- |

```
class NfcB : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#) |

Provides access to NFC-B (ISO 14443-3B) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#).

Acquire a [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#) object using [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#get(android.nfc.Tag)).

The primary NFC-B I/O operation is [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#transceive(kotlin.ByteArray)). Applications must implement their own protocol stack on top of [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#transceive(kotlin.ByteArray)).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#connect())`()` <br /> |
| static [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#)! | [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#get(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!`)` Get an instance of [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#) for the given tag. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getApplicationData](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#getApplicationData())`()` Return the Application Data bytes from ATQB/SENSB_RES at tag discovery. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#getMaxTransceiveLength())`()` Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#transceive(kotlin.ByteArray)). |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getProtocolInfo](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#getProtocolInfo())`()` Return the Protocol Info bytes from ATQB/SENSB_RES at tag discovery. |
| --- | --- |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#getTag())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#isConnected())`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#transceive(kotlin.ByteArray))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw NFC-B commands to the tag and receive the response. |
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

Get an instance of [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#) for the given tag.

Returns null if [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#) was not enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()). This indicates the tag does not support NFC-B.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!:an NFC-B compatible tag |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#)! | NFC-B object |

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

Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#transceive(kotlin.ByteArray)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#transceive(kotlin.ByteArray)). |

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
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology) object. |

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

Use [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#getMaxTransceiveLength())to retrieve the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB#transceive(kotlin.ByteArray)).

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

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
