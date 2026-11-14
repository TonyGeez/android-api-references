# MediaDrmException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDrmException

Kotlin| [Java](../android/media/MediaDrmException.md) 
| --- | --- |

```
open class MediaDrmException : Exception, MediaDrmThrowable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.media.MediaDrmException](../android/media/MediaDrmException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [DeniedByServerException](../android/media/DeniedByServerException.md), [MediaPlayer.NoDrmSchemeException](../android/media/MediaPlayer.NoDrmSchemeException.md), [MediaPlayer.ProvisioningNetworkErrorException](../android/media/MediaPlayer.ProvisioningNetworkErrorException.md), [MediaPlayer.ProvisioningServerErrorException](../android/media/MediaPlayer.ProvisioningServerErrorException.md), [NotProvisionedException](../android/media/NotProvisionedException.md), [ResourceBusyException](../android/media/ResourceBusyException.md), [UnsupportedSchemeException](../android/media/UnsupportedSchemeException.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [DeniedByServerException](../android/media/DeniedByServerException.md) | Exception thrown when the provisioning server or key server denies a certficate or license for a device. | | [MediaPlayer.NoDrmSchemeException](../android/media/MediaPlayer.NoDrmSchemeException.md) | Thrown when a DRM method is called before preparing a DRM scheme through prepareDrm(). | | [MediaPlayer.ProvisioningNetworkErrorException](../android/media/MediaPlayer.ProvisioningNetworkErrorException.md) | Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to a network error (Internet reachability, timeout, etc.). | | [MediaPlayer.ProvisioningServerErrorException](../android/media/MediaPlayer.ProvisioningServerErrorException.md) | Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to the provisioning server denying the request. | | [NotProvisionedException](../android/media/NotProvisionedException.md) | Exception thrown when an operation on a MediaDrm object is attempted and the device does not have a certificate. | | [ResourceBusyException](../android/media/ResourceBusyException.md) | Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use. | | [UnsupportedSchemeException](../android/media/UnsupportedSchemeException.md) | Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for MediaDrm exceptions

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaDrmException](../android/media/MediaDrmException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](../android/media/MediaDrmException.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](../android/media/MediaDrmException.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](../android/media/MediaDrmException.md))`()` <br /> |
| --- | --- |

## Public constructors

### MediaDrmException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaDrmException(detailMessage: String!)
```

## Public methods

### getErrorContext

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorContext(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an opaque integer that would help the @ [MediaDrm](../android/media/MediaDrm.md) vendor locate the source of the error if available, otherwise 0. |

### getOemError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOemError(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an OEM or SOC specific error code if available, otherwise 0. |

### getVendorError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVendorError(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an error code defined by the [MediaDrm](../android/media/MediaDrm.md) plugin vendor if available, otherwise 0. |
