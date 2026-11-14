# FileUriExposedException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileUriExposedException

Kotlin| [Java](https://developer.android.com/reference/android/os/FileUriExposedException "View this page in Java") 

```
open class FileUriExposedException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [android.os.FileUriExposedException](https://developer.android.com/reference/kotlin/android/os/FileUriExposedException#) |

The exception that may be thrown when an application exposes a`file://` [android.net.Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) to another app.

This exception is a diagnostic tool for developers to identify situations where`file://`Uris are being exposed. It is not always thrown when a`file://`Uri is exposed, so it must not be relied on for security purposes on any SDK version.

`file://`Uri exposure is discouraged since the receiving app may not have access to the shared path. For example, the receiving app may not have requested the [android.Manifest.permission#READ_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String) runtime permission, or the platform may be sharing the [android.net.Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) across user profile boundaries.

Instead, apps should use`content://`Uris so the platform can extend temporary permission for the receiving app to access the resource.

This is only thrown for applications targeting [Build.VERSION_CODES.N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#N:kotlin.Int) or higher. Applications targeting earlier SDK versions are allowed to share`file://` [android.net.Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#), but it's strongly discouraged.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileUriExposedException](https://developer.android.com/reference/kotlin/android/os/FileUriExposedException#FileUriExposedException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### FileUriExposedException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileUriExposedException(message: String!)
```
