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
| NotProvisionedException <br /> |

| Inherited functions ||
|---|---|
| From class MediaDrmException |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getErrorContext Returns MediaDrm plugin vendor defined error context associated with this MediaDrmThrowable. Please consult the MediaDrm plugin vendor for details on the error context. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getOemError Returns OEM or SOC specific error code associated with this MediaDrmThrowable. Please consult the MediaDrm plugin, chip, or device vendor for details on the error code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getVendorError Returns MediaDrm plugin vendor defined error code associated with this MediaDrmThrowable. Please consult the MediaDrm plugin vendor for details on the error code. <br /> | ||

## Public constructors

### NotProvisionedException

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
NotProvisionedException(detailMessage: String!)
```
