# MediaDrmThrowable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDrmThrowable

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaDrmThrowable "View this page in Java") 
| --- | --- |

```
interface MediaDrmThrowable
```

| [android.media.MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#) |

| Known Direct Subclasses [MediaCodec.CryptoException](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoException), [MediaCryptoException](https://developer.android.com/reference/kotlin/android/media/MediaCryptoException), [MediaDrm.MediaDrmStateException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MediaDrmStateException), [MediaDrm.SessionException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.SessionException), [MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException), [MediaDrmResetException](https://developer.android.com/reference/kotlin/android/media/MediaDrmResetException) |---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MediaCodec.CryptoException](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoException) | Thrown when a crypto error occurs while queueing a secure input buffer. | | [MediaCryptoException](https://developer.android.com/reference/kotlin/android/media/MediaCryptoException) | Exception thrown if MediaCrypto object could not be instantiated or if unable to perform an operation on the MediaCrypto object. | | [MediaDrm.MediaDrmStateException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MediaDrmStateException) | Thrown when a general failure occurs during a MediaDrm operation. | | [MediaDrm.SessionException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.SessionException) | [SessionException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.SessionException) is a misnomer because it may occur in methods**without**a session context. | | [MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException) | Base class for MediaDrm exceptions | | [MediaDrmResetException](https://developer.android.com/reference/kotlin/android/media/MediaDrmResetException) | This exception is thrown when the MediaDrm instance has become unusable due to a restart of the mediaserver process. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/DeniedByServerException), [MediaPlayer.NoDrmSchemeException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.NoDrmSchemeException), [MediaPlayer.ProvisioningNetworkErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningNetworkErrorException), [MediaPlayer.ProvisioningServerErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningServerErrorException), [NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/NotProvisionedException), [ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/ResourceBusyException), [UnsupportedSchemeException](https://developer.android.com/reference/kotlin/android/media/UnsupportedSchemeException) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/DeniedByServerException) | Exception thrown when the provisioning server or key server denies a certficate or license for a device. | | [MediaPlayer.NoDrmSchemeException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.NoDrmSchemeException) | Thrown when a DRM method is called before preparing a DRM scheme through prepareDrm(). | | [MediaPlayer.ProvisioningNetworkErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningNetworkErrorException) | Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to a network error (Internet reachability, timeout, etc.). | | [MediaPlayer.ProvisioningServerErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningServerErrorException) | Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to the provisioning server denying the request. | | [NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/NotProvisionedException) | Exception thrown when an operation on a MediaDrm object is attempted and the device does not have a certificate. | | [ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/ResourceBusyException) | Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use. | | [UnsupportedSchemeException](https://developer.android.com/reference/kotlin/android/media/UnsupportedSchemeException) | Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A @ [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#) thrown from [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) or @ [MediaCrypto](https://developer.android.com/reference/kotlin/android/media/MediaCrypto) APIs

## Summary

| Public methods ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#getErrorContext())`()` Returns [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor defined error context associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#getOemError())`()` Returns OEM or SOC specific error code associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#getVendorError())`()` Returns [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor defined error code associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#). |
| --- | --- |

## Public methods

### getErrorContext

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorContext(): Int
```

Returns [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor defined error context associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#).

Please consult the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor for details on the error context.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an opaque integer that would help the @ [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) vendor locate the source of the error if available, otherwise 0. |

### getOemError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOemError(): Int
```

Returns OEM or SOC specific error code associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#).

Please consult the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin, chip, or device vendor for details on the error code.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an OEM or SOC specific error code if available, otherwise 0. |

### getVendorError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVendorError(): Int
```

Returns [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor defined error code associated with this [MediaDrmThrowable](https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable#).

Please consult the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor for details on the error code.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an error code defined by the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor if available, otherwise 0. |
