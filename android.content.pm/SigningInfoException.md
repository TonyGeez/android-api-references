# SigningInfoException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SigningInfoException

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/SigningInfoException "View this page in Java") 

```
open class SigningInfoException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.content.pm.SigningInfoException](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfoException#) |

Indicates an error when verifying the [app signing](https://source.android.com/docs/security/features/apksigning) information.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCode](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfoException#getCode())`()` Returns a code representing the cause, in one of the installation parse return codes in [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager). |

## Public methods

### getCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCode(): Int
```

Returns a code representing the cause, in one of the installation parse return codes in [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager).
