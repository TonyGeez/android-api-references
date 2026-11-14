# NfcA

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcA

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/NfcA "View this page in Java") 
| --- | --- |

```
class NfcA : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#) |

Provides access to NFC-A (ISO 14443-3A) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#).

Acquire a [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#) object using [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#get(android.nfc.Tag)).

The primary NFC-A I/O operation is [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)). Applications must implement their own protocol stack on top of [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#connect())`()` <br /> |
| static [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#)! | [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#get(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!`)` Get an instance of [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#) for the given tag. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getAtqa](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#getAtqa())`()` Return the ATQA/SENS_RES bytes from tag discovery. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#getMaxTransceiveLength())`()` Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)). |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getSak](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#getSak())`()` Return the SAK/SEL_RES bytes from tag discovery. |
| --- | --- |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#getTag())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeout](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#getTimeout())`()` Get the current [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray))timeout in milliseconds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#isConnected())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeout](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#setTimeout(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray))timeout in milliseconds. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw NFC-A commands to the tag and receive the response. |

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

Get an instance of [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#) for the given tag.

Returns null if [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#) was not enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()). This indicates the tag does not support NFC-A.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!:an NFC-A compatible tag |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#)! | NFC-A object |

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

Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)). |

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
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology) object. |

### getTimeout

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeout(): Int
```

Get the current [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray))timeout in milliseconds.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

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

Set the [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray))timeout in milliseconds.

The timeout only applies to [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray))on this object, and is reset to a default value when #close is called.

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

Send raw NFC-A commands to the tag and receive the response.

Applications must not append the EoD (CRC) to the payload, it will be automatically calculated.

Applications must only send commands that are complete bytes, for example a SENS_REQ is not possible (these are used to manage tag polling and initialization).

Use [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#getMaxTransceiveLength())to retrieve the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)).

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
