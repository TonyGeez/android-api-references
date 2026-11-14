# IsoDep

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IsoDep

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/IsoDep "View this page in Java") 
| --- | --- |

```
class IsoDep : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#) |

Provides access to ISO-DEP (ISO 14443-4) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#).

Acquire an [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#) object using [get](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#get(android.nfc.Tag)).

The primary ISO-DEP I/O operation is [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray)). Applications must implement their own protocol stack on top of [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray)).

Tags that enumerate the [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#) technology in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList())will also enumerate [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) or [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB)(since IsoDep builds on top of either of these).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#connect())`()` <br /> |
| static [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#)! | [get](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#get(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!`)` Get an instance of [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#) for the given tag. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getHiLayerResponse](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#getHiLayerResponse())`()` Return the higher layer response bytes for [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB) tags. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getHistoricalBytes](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#getHistoricalBytes())`()` Return the ISO-DEP historical bytes for [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) tags. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#getMaxTransceiveLength())`()` Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray)). |
| --- | --- |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#getTag())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeout](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#getTimeout())`()` Get the current timeout for [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray))in milliseconds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#isConnected())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExtendedLengthApduSupported](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#isExtendedLengthApduSupported())`()` Standard APDUs have a 1-byte length field, allowing a maximum of 255 payload bytes, which results in a maximum APDU length of 261 bytes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeout](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#setTimeout(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the timeout of [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray))in milliseconds. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw ISO-DEP data to the tag and receive the response. |
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
static fun get(tag: Tag!): IsoDep!
```

Get an instance of [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#) for the given tag.

Does not cause any RF activity and does not block.

Returns null if [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#) was not enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()). This indicates the tag does not support ISO-DEP.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!:an ISO-DEP compatible tag |

| Return ||
|------------------------------------------------------------------------------------|----------------|
| [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#)! | ISO-DEP object |

### getHiLayerResponse

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHiLayerResponse(): ByteArray!
```

Return the higher layer response bytes for [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB) tags.

Does not cause any RF activity and does not block.

The higher layer response bytes can be used to help identify a tag. They are present only on [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#) tags that are based on [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB) RF technology. If this tag is not [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB) then null is returned.

In ISO 14443-4 terminology, the higher layer bytes are a subset of the ATTRIB response.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | ISO-DEP historical bytes, or null if this is not a [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB) tag |

### getHistoricalBytes

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalBytes(): ByteArray!
```

Return the ISO-DEP historical bytes for [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) tags.

Does not cause any RF activity and does not block.

The historical bytes can be used to help identify a tag. They are present only on [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#) tags that are based on [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) RF technology. If this tag is not [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) then null is returned.

In ISO 14443-4 terminology, the historical bytes are a subset of the RATS response.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | ISO-DEP historical bytes, or null if this is not a [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) tag |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray)).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray)). |

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

Get the current timeout for [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray))in milliseconds.

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

### isExtendedLengthApduSupported

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isExtendedLengthApduSupported(): Boolean
```

Standard APDUs have a 1-byte length field, allowing a maximum of 255 payload bytes, which results in a maximum APDU length of 261 bytes.

Extended length APDUs have a 3-byte length field, allowing 65535 payload bytes.

Some NFC adapters, like the one used in the Nexus S and the Galaxy Nexus do not support extended length APDUs. They are expected to be well-supported in the future though. Use this method to check for extended length APDU support.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the NFC adapter on this device supports extended length APDUs. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### setTimeout

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTimeout(timeout: Int): Unit
```

Set the timeout of [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray))in milliseconds.

The timeout only applies to ISO-DEP [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray)), and is reset to a default value when #close is called.

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

Send raw ISO-DEP data to the tag and receive the response.

Applications must only send the INF payload, and not the start of frame and end of frame indicators. Applications do not need to fragment the payload, it will be automatically fragmented and defragmented by [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray))if it exceeds FSD/FSC limits.

Use [getMaxTransceiveLength](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#getMaxTransceiveLength())to retrieve the maximum number of bytes that can be sent with [transceive](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep#transceive(kotlin.ByteArray)).

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:command bytes to send, must not be null |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | response bytes received, will not be null |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or this operation is canceled |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |
