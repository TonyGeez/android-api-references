# MediaCrypto

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCrypto

Kotlin| [Java](MediaCrypto.md) 
| --- | --- |

```
class MediaCrypto
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaCrypto](MediaCrypto.md) |

MediaCrypto class can be used in conjunction with [android.media.MediaCodec](MediaCodec.md) to decode encrypted media data. Crypto schemes are assigned 16 byte UUIDs, the method [isCryptoSchemeSupported](MediaCrypto.md))can be used to query if a given scheme is supported on the device.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaCrypto](MediaCrypto.md))`(`uuid:` ` [UUID](../java.util/UUID.md)`, `sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Instantiate a MediaCrypto object and associate it with a MediaDrm session |

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCryptoSchemeSupported](MediaCrypto.md))`(`uuid:` ` [UUID](../java.util/UUID.md)`)` Query if the given scheme identified by its UUID is supported on this device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](MediaCrypto.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresSecureDecoderComponent](MediaCrypto.md))`(`mime:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query if the crypto scheme requires the use of a secure decoder to decode data of the given mime type. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMediaDrmSession](MediaCrypto.md))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Associate a new MediaDrm session with this MediaCrypto instance. |

| Protected methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](MediaCrypto.md))`()` <br /> |

## Public constructors

### MediaCrypto

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaCrypto(
    uuid: UUID, 
    sessionId: ByteArray)
```

Instantiate a MediaCrypto object and associate it with a MediaDrm session

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](../java.util/UUID.md):The UUID of the crypto scheme. This value cannot be`null`. |
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):The MediaDrm sessionId to associate with this MediaCrypto session. The sessionId may be changed after the MediaCrypto is created using [setMediaDrmSession](MediaCrypto.md))This value cannot be`null`. |

## Public methods

### isCryptoSchemeSupported

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isCryptoSchemeSupported(uuid: UUID): Boolean
```

Query if the given scheme identified by its UUID is supported on this device.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](../java.util/UUID.md):The UUID of the crypto scheme. This value cannot be`null`. |

### release

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun release(): Unit
```  

### requiresSecureDecoderComponent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requiresSecureDecoderComponent(mime: String): Boolean
```

Query if the crypto scheme requires the use of a secure decoder to decode data of the given mime type.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `mime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The mime type of the media data This value cannot be`null`. |

### setMediaDrmSession

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMediaDrmSession(sessionId: ByteArray): Unit
```

Associate a new MediaDrm session with this MediaCrypto instance.

The MediaDrm session is used to securely load decryption keys for a crypto scheme. The crypto keys loaded through the MediaDrm session may be selected for use during the decryption operation performed by [android.media.MediaCodec#queueSecureInputBuffer](MediaCodec.md))by specifying their key IDs in the [android.media.MediaCodec.CryptoInfo#key](../android/media/MediaCodec.CryptoInfo.md) field.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):The MediaDrm sessionId to associate with this MediaCrypto instance. The session's scheme must match the scheme UUID used when constructing this MediaCrypto instance. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `android.media.MediaCryptoException` | on failure to set the sessionId |

## Protected methods

### finalize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
