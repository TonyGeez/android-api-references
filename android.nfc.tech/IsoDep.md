# IsoDep

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IsoDep

Kotlin| [Java](../android/nfc/tech/IsoDep.md) 
| --- | --- |

```
class IsoDep : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.IsoDep](../android/nfc/tech/IsoDep.md) |

Provides access to ISO-DEP (ISO 14443-4) properties and I/O operations on a [Tag](../android/nfc/Tag.md).

Acquire an [IsoDep](../android/nfc/tech/IsoDep.md) object using [get](../android/nfc/tech/IsoDep.md)).

The primary ISO-DEP I/O operation is [transceive](../android/nfc/tech/IsoDep.md)). Applications must implement their own protocol stack on top of [transceive](../android/nfc/tech/IsoDep.md)).

Tags that enumerate the [IsoDep](../android/nfc/tech/IsoDep.md) technology in [Tag.getTechList](../android/nfc/Tag.md))will also enumerate [NfcA](../android/nfc/tech/NfcA.md) or [NfcB](../android/nfc/tech/NfcB.md)(since IsoDep builds on top of either of these).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/nfc/tech/IsoDep.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/nfc/tech/IsoDep.md))`()` <br /> |
| static [IsoDep](../android/nfc/tech/IsoDep.md)! | [get](../android/nfc/tech/IsoDep.md))`(`tag:` ` [Tag](../android/nfc/Tag.md)!`)` Get an instance of [IsoDep](../android/nfc/tech/IsoDep.md) for the given tag. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getHiLayerResponse](../android/nfc/tech/IsoDep.md))`()` Return the higher layer response bytes for [NfcB](../android/nfc/tech/NfcB.md) tags. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getHistoricalBytes](../android/nfc/tech/IsoDep.md))`()` Return the ISO-DEP historical bytes for [NfcA](../android/nfc/tech/NfcA.md) tags. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransceiveLength](../android/nfc/tech/IsoDep.md))`()` Return the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/IsoDep.md)). |
| --- | --- |
| [Tag](../android/nfc/Tag.md)! | [getTag](../android/nfc/tech/IsoDep.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeout](../android/nfc/tech/IsoDep.md))`()` Get the current timeout for [transceive](../android/nfc/tech/IsoDep.md))in milliseconds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/nfc/tech/IsoDep.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExtendedLengthApduSupported](../android/nfc/tech/IsoDep.md))`()` Standard APDUs have a 1-byte length field, allowing a maximum of 255 payload bytes, which results in a maximum APDU length of 261 bytes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeout](../android/nfc/tech/IsoDep.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the timeout of [transceive](../android/nfc/tech/IsoDep.md))in milliseconds. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [transceive](../android/nfc/tech/IsoDep.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send raw ISO-DEP data to the tag and receive the response. |
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

Get an instance of [IsoDep](../android/nfc/tech/IsoDep.md) for the given tag.

Does not cause any RF activity and does not block.

Returns null if [IsoDep](../android/nfc/tech/IsoDep.md) was not enumerated in [Tag.getTechList](../android/nfc/Tag.md)). This indicates the tag does not support ISO-DEP.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `tag` | [Tag](../android/nfc/Tag.md)!:an ISO-DEP compatible tag |

| Return ||
|------------------------------------------------------------------------------------|----------------|
| [IsoDep](../android/nfc/tech/IsoDep.md)! | ISO-DEP object |

### getHiLayerResponse

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHiLayerResponse(): ByteArray!
```

Return the higher layer response bytes for [NfcB](../android/nfc/tech/NfcB.md) tags.

Does not cause any RF activity and does not block.

The higher layer response bytes can be used to help identify a tag. They are present only on [IsoDep](../android/nfc/tech/IsoDep.md) tags that are based on [NfcB](../android/nfc/tech/NfcB.md) RF technology. If this tag is not [NfcB](../android/nfc/tech/NfcB.md) then null is returned.

In ISO 14443-4 terminology, the higher layer bytes are a subset of the ATTRIB response.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | ISO-DEP historical bytes, or null if this is not a [NfcB](../android/nfc/tech/NfcB.md) tag |

### getHistoricalBytes

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalBytes(): ByteArray!
```

Return the ISO-DEP historical bytes for [NfcA](../android/nfc/tech/NfcA.md) tags.

Does not cause any RF activity and does not block.

The historical bytes can be used to help identify a tag. They are present only on [IsoDep](../android/nfc/tech/IsoDep.md) tags that are based on [NfcA](../android/nfc/tech/NfcA.md) RF technology. If this tag is not [NfcA](../android/nfc/tech/NfcA.md) then null is returned.

In ISO 14443-4 terminology, the historical bytes are a subset of the RATS response.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | ISO-DEP historical bytes, or null if this is not a [NfcA](../android/nfc/tech/NfcA.md) tag |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/IsoDep.md)).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/IsoDep.md)). |

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): Tag!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](../android/nfc/Tag.md)! | the [Tag](../android/nfc/Tag.md) backing this [TagTechnology](../android/nfc/tech/TagTechnology.md) object. |

### getTimeout

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeout(): Int
```

Get the current timeout for [transceive](../android/nfc/tech/IsoDep.md))in milliseconds.

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

Set the timeout of [transceive](../android/nfc/tech/IsoDep.md))in milliseconds.

The timeout only applies to ISO-DEP [transceive](../android/nfc/tech/IsoDep.md)), and is reset to a default value when #close is called.

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

Send raw ISO-DEP data to the tag and receive the response.

Applications must only send the INF payload, and not the start of frame and end of frame indicators. Applications do not need to fragment the payload, it will be automatically fragmented and defragmented by [transceive](../android/nfc/tech/IsoDep.md))if it exceeds FSD/FSC limits.

Use [getMaxTransceiveLength](../android/nfc/tech/IsoDep.md))to retrieve the maximum number of bytes that can be sent with [transceive](../android/nfc/tech/IsoDep.md)).

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java/io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

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
