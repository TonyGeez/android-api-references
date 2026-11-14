# MediaDrmThrowable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDrmThrowable

Kotlin| [Java](../android/media/MediaDrmThrowable.md) 
| --- | --- |

```
interface MediaDrmThrowable
```

| [android.media.MediaDrmThrowable](../android/media/MediaDrmThrowable.md) |

| Known Direct Subclasses [MediaCodec.CryptoException](../android/media/MediaCodec.CryptoException.md), [MediaCryptoException](../android/media/MediaCryptoException.md), [MediaDrm.MediaDrmStateException](../android/media/MediaDrm.MediaDrmStateException.md), [MediaDrm.SessionException](../android/media/MediaDrm.SessionException.md), [MediaDrmException](../android/media/MediaDrmException.md), [MediaDrmResetException](../android/media/MediaDrmResetException.md) |---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MediaCodec.CryptoException](../android/media/MediaCodec.CryptoException.md) | Thrown when a crypto error occurs while queueing a secure input buffer. | | [MediaCryptoException](../android/media/MediaCryptoException.md) | Exception thrown if MediaCrypto object could not be instantiated or if unable to perform an operation on the MediaCrypto object. | | [MediaDrm.MediaDrmStateException](../android/media/MediaDrm.MediaDrmStateException.md) | Thrown when a general failure occurs during a MediaDrm operation. | | [MediaDrm.SessionException](../android/media/MediaDrm.SessionException.md) | [SessionException](../android/media/MediaDrm.SessionException.md) is a misnomer because it may occur in methods**without**a session context. | | [MediaDrmException](../android/media/MediaDrmException.md) | Base class for MediaDrm exceptions | | [MediaDrmResetException](../android/media/MediaDrmResetException.md) | This exception is thrown when the MediaDrm instance has become unusable due to a restart of the mediaserver process. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DeniedByServerException](../android/media/DeniedByServerException.md), [MediaPlayer.NoDrmSchemeException](../android/media/MediaPlayer.NoDrmSchemeException.md), [MediaPlayer.ProvisioningNetworkErrorException](../android/media/MediaPlayer.ProvisioningNetworkErrorException.md), [MediaPlayer.ProvisioningServerErrorException](../android/media/MediaPlayer.ProvisioningServerErrorException.md), [NotProvisionedException](../android/media/NotProvisionedException.md), [ResourceBusyException](../android/media/ResourceBusyException.md), [UnsupportedSchemeException](../android/media/UnsupportedSchemeException.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [DeniedByServerException](../android/media/DeniedByServerException.md) | Exception thrown when the provisioning server or key server denies a certficate or license for a device. | | [MediaPlayer.NoDrmSchemeException](../android/media/MediaPlayer.NoDrmSchemeException.md) | Thrown when a DRM method is called before preparing a DRM scheme through prepareDrm(). | | [MediaPlayer.ProvisioningNetworkErrorException](../android/media/MediaPlayer.ProvisioningNetworkErrorException.md) | Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to a network error (Internet reachability, timeout, etc.). | | [MediaPlayer.ProvisioningServerErrorException](../android/media/MediaPlayer.ProvisioningServerErrorException.md) | Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to the provisioning server denying the request. | | [NotProvisionedException](../android/media/NotProvisionedException.md) | Exception thrown when an operation on a MediaDrm object is attempted and the device does not have a certificate. | | [ResourceBusyException](../android/media/ResourceBusyException.md) | Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use. | | [UnsupportedSchemeException](../android/media/UnsupportedSchemeException.md) | Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A @ [Throwable](../java/lang/Throwable.md) thrown from [MediaDrm](../android/media/MediaDrm.md) or @ [MediaCrypto](../android/media/MediaCrypto.md) APIs

## Summary

| Public methods ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](../android/media/MediaDrmThrowable.md))`()` Returns [MediaDrm](../android/media/MediaDrm.md) plugin vendor defined error context associated with this [MediaDrmThrowable](../android/media/MediaDrmThrowable.md). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](../android/media/MediaDrmThrowable.md))`()` Returns OEM or SOC specific error code associated with this [MediaDrmThrowable](../android/media/MediaDrmThrowable.md). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](../android/media/MediaDrmThrowable.md))`()` Returns [MediaDrm](../android/media/MediaDrm.md) plugin vendor defined error code associated with this [MediaDrmThrowable](../android/media/MediaDrmThrowable.md). |
| --- | --- |

## Public methods

### getErrorContext

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorContext(): Int
```

Returns [MediaDrm](../android/media/MediaDrm.md) plugin vendor defined error context associated with this [MediaDrmThrowable](../android/media/MediaDrmThrowable.md).

Please consult the [MediaDrm](../android/media/MediaDrm.md) plugin vendor for details on the error context.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an opaque integer that would help the @ [MediaDrm](../android/media/MediaDrm.md) vendor locate the source of the error if available, otherwise 0. |

### getOemError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOemError(): Int
```

Returns OEM or SOC specific error code associated with this [MediaDrmThrowable](../android/media/MediaDrmThrowable.md).

Please consult the [MediaDrm](../android/media/MediaDrm.md) plugin, chip, or device vendor for details on the error code.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an OEM or SOC specific error code if available, otherwise 0. |

### getVendorError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVendorError(): Int
```

Returns [MediaDrm](../android/media/MediaDrm.md) plugin vendor defined error code associated with this [MediaDrmThrowable](../android/media/MediaDrmThrowable.md).

Please consult the [MediaDrm](../android/media/MediaDrm.md) plugin vendor for details on the error code.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an error code defined by the [MediaDrm](../android/media/MediaDrm.md) plugin vendor if available, otherwise 0. |
