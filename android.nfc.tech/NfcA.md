# NfcA

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcA

Kotlin| [Java](NfcA.md) 
| --- | --- |

```
class NfcA : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NfcA](NfcA.md) |

Provides access to NFC-A (ISO 14443-3A) properties and I/O operations on a [Tag](../android.nfc/Tag.md).

Acquire a [NfcA](NfcA.md) object using [get](NfcA.md)).

The primary NFC-A I/O operation is [transceive](NfcA.md)). Applications must implement their own protocol stack on top of [transceive](NfcA.md)).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](NfcA.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](NfcA.md))`()` <br /> |
| static [NfcA](NfcA.md)! | [get](NfcA.md))`(`tag:` ` [Tag](../android.nfc/Tag.md)!`)` Get an instance of [NfcA](NfcA.md) for the given tag. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getAtqa](NfcA.md))`()` Return the ATQA/SENS_RES bytes from tag discovery. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](NfcA.md))`()` Return the maximum number of bytes that can be sent with [transceive](NfcA.md)). |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getSak](NfcA.md))`()` Return the SAK/SEL_RES bytes from tag discovery. |
| --- | --- |
| [Tag](../android.nfc/Tag.md)! | [getTag](NfcA.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeout](NfcA.md))`()` Get the current [transceive](NfcA.md))timeout in milliseconds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](NfcA.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeout](NfcA.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the [transceive](NfcA.md))timeout in milliseconds. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](NfcA.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw NFC-A commands to the tag and receive the response. |

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
static fun get(tag: Tag!): NfcA!
```

Get an instance of [NfcA](NfcA.md) for the given tag.

Returns null if [NfcA](NfcA.md) was not enumerated in [Tag.getTechList](../android.nfc/Tag.md)). This indicates the tag does not support NFC-A.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](../android.nfc/Tag.md)!:an NFC-A compatible tag |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [NfcA](NfcA.md)! | NFC-A object |

### getAtqa

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAtqa(): ByteArray!
```

Return the ATQA/SENS_RES bytes from tag discovery.

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | ATQA/SENS_RES bytes |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with [transceive](NfcA.md)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](NfcA.md)). |

### getSak

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSak(): Short
```

Return the SAK/SEL_RES bytes from tag discovery.

Does not cause any RF activity and does not block.

| Return ||
|--------------------------------------------------------------------------------|-----------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | SAK bytes |

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

Get the current [transceive](NfcA.md))timeout in milliseconds.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | timeout value in milliseconds |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |

### setTimeout

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTimeout(timeout: Int): Unit
```

Set the [transceive](NfcA.md))timeout in milliseconds.

The timeout only applies to [transceive](NfcA.md))on this object, and is reset to a default value when #close is called.

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

Send raw NFC-A commands to the tag and receive the response.

Applications must not append the EoD (CRC) to the payload, it will be automatically calculated.

Applications must only send commands that are complete bytes, for example a SENS_REQ is not possible (these are used to manage tag polling and initialization).

Use [getMaxTransceiveLength](NfcA.md))to retrieve the maximum number of bytes that can be sent with [transceive](NfcA.md)).

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

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
