Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NotProvisionedException

Kotlin | [Java](NotProvisionedException.md)
| --- | --- |

```
class NotProvisionedException : MediaDrmException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.media.MediaDrmException](MediaDrmException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.media.NotProvisionedException](NotProvisionedException.md) |

Exception thrown when an operation on a MediaDrm object is attempted and the device does not have a certificate. The app should obtain and install a certificate using the MediaDrm provisioning methods then retry the operation.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/NotProvisionedException#NotProvisionedException(kotlin.String)(detailMessage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/media/MediaDrmException` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getErrorContext()()` Returns `https://developer.android.com/reference/kotlin/android/media/MediaDrm` plugin vendor defined error context associated with this `https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable`. Please consult the `https://developer.android.com/reference/kotlin/android/media/MediaDrm` plugin vendor for details on the error context. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getOemError()()` Returns OEM or SOC specific error code associated with this `https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable`. Please consult the `https://developer.android.com/reference/kotlin/android/media/MediaDrm` plugin, chip, or device vendor for details on the error code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/MediaDrmException#getVendorError()()` Returns `https://developer.android.com/reference/kotlin/android/media/MediaDrm` plugin vendor defined error code associated with this `https://developer.android.com/reference/kotlin/android/media/MediaDrmThrowable`. Please consult the `https://developer.android.com/reference/kotlin/android/media/MediaDrm` plugin vendor for details on the error code. <br /> | ||

## Public constructors

### NotProvisionedException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
NotProvisionedException(detailMessage: String!)
```
