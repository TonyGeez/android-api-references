# NfcF

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcF

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/NfcF "View this page in Java") 
| --- | --- |

```
class NfcF : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#) |

Provides access to NFC-F (JIS 6319-4) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#).

Acquire a [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#) object using [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#get(android.nfc.Tag)).

The primary NFC-F I/O operation is [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray)). Applications must implement their own protocol stack on top of [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray)).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#connect())`()` <br /> |
| static [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#)! | [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#get(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!`)` Get an instance of [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#) for the given tag. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getManufacturer](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#getManufacturer())`()` Return the Manufacturer bytes from tag discovery. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#getMaxTransceiveLength())`()` Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray)). |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getSystemCode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#getSystemCode())`()` Return the System Code bytes from tag discovery. |
| --- | --- |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#getTag())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeout](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#getTimeout())`()` Get the current [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray))timeout in milliseconds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#isConnected())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeout](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#setTimeout(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray))timeout in milliseconds. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw NFC-F commands to the tag and receive the response. |

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
static fun get(tag: Tag!): NfcF!
```

Get an instance of [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#) for the given tag.

Returns null if [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#) was not enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()). This indicates the tag does not support NFC-F.

Does not cause any RF activity and does not block.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!:an NFC-F compatible tag |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#)! | NFC-F object |

### getManufacturer

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getManufacturer(): ByteArray!
```

Return the Manufacturer bytes from tag discovery.

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | Manufacturer bytes |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray)). |

### getSystemCode

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemCode(): ByteArray!
```

Return the System Code bytes from tag discovery.

Does not cause any RF activity and does not block.

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | System Code bytes |

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

Get the current [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray))timeout in milliseconds.

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

Set the [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray))timeout in milliseconds.

The timeout only applies to [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray))on this object, and is reset to a default value when #close is called.

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

Send raw NFC-F commands to the tag and receive the response.

Applications must not prefix the SoD (preamble and sync code) and/or append the EoD (CRC) to the payload, it will be automatically calculated.

A typical NFC-F frame for this method looks like: 

```kotlin
LENGTH (1 byte) --- CMD (1 byte) -- IDm (8 bytes) -- PARAMS (LENGTH - 10 bytes)
  
```

Use [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#getMaxTransceiveLength())to retrieve the maximum amount of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF#transceive(kotlin.ByteArray)).

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
