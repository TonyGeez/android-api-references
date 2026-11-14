# MediaDrmException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDrmException

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaDrmException "View this page in Java") 
| --- | --- |

```
open class MediaDrmException : Exception, MediaDrmThrowable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.media.MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/DeniedByServerException), [MediaPlayer.NoDrmSchemeException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.NoDrmSchemeException), [MediaPlayer.ProvisioningNetworkErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningNetworkErrorException), [MediaPlayer.ProvisioningServerErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningServerErrorException), [NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/NotProvisionedException), [ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/ResourceBusyException), [UnsupportedSchemeException](https://developer.android.com/reference/kotlin/android/media/UnsupportedSchemeException) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/DeniedByServerException) | Exception thrown when the provisioning server or key server denies a certficate or license for a device. | | [MediaPlayer.NoDrmSchemeException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.NoDrmSchemeException) | Thrown when a DRM method is called before preparing a DRM scheme through prepareDrm(). | | [MediaPlayer.ProvisioningNetworkErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningNetworkErrorException) | Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to a network error (Internet reachability, timeout, etc.). | | [MediaPlayer.ProvisioningServerErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningServerErrorException) | Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to the provisioning server denying the request. | | [NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/NotProvisionedException) | Exception thrown when an operation on a MediaDrm object is attempted and the device does not have a certificate. | | [ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/ResourceBusyException) | Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use. | | [UnsupportedSchemeException](https://developer.android.com/reference/kotlin/android/media/UnsupportedSchemeException) | Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for MediaDrm exceptions

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#MediaDrmException(kotlin.String))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorContext](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getErrorContext())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOemError](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getOemError())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorError](https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getVendorError())`()` <br /> |
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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an opaque integer that would help the @ [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) vendor locate the source of the error if available, otherwise 0. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an error code defined by the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) plugin vendor if available, otherwise 0. |
