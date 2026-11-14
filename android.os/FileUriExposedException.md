# FileUriExposedException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileUriExposedException

Kotlin| [Java](FileUriExposedException.md) 
| --- | --- |

```
open class FileUriExposedException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.FileUriExposedException](FileUriExposedException.md) |

The exception that may be thrown when an application exposes a`file://` [android.net.Uri](../android.net/Uri.md) to another app.

This exception is a diagnostic tool for developers to identify situations where`file://`Uris are being exposed. It is not always thrown when a`file://`Uri is exposed, so it must not be relied on for security purposes on any SDK version.

`file://`Uri exposure is discouraged since the receiving app may not have access to the shared path. For example, the receiving app may not have requested the [android.Manifest.permission#READ_EXTERNAL_STORAGE](../android/Manifest.permission.md) runtime permission, or the platform may be sharing the [android.net.Uri](../android.net/Uri.md) across user profile boundaries.

Instead, apps should use`content://`Uris so the platform can extend temporary permission for the receiving app to access the resource.

This is only thrown for applications targeting [Build.VERSION_CODES.N](../android/os/Build.VERSION_CODES.md) or higher. Applications targeting earlier SDK versions are allowed to share`file://` [android.net.Uri](../android.net/Uri.md), but it's strongly discouraged.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileUriExposedException](FileUriExposedException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### FileUriExposedException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileUriExposedException(message: String!)
```
