# DomainVerificationManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DomainVerificationManager

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/verify/domain/DomainVerificationManager "View this page in Java") 
| --- | --- |

```
class DomainVerificationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.verify.domain.DomainVerificationManager](https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager#) |

System service to access domain verification APIs. Applications should use [getDomainVerificationUserState(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager#getDomainVerificationUserState(kotlin.String))if necessary to check if/how they are verified for a domain, which is required starting from platform [android.os.Build.VERSION_CODES#S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) in order to open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) s which declare [Intent.CATEGORY_BROWSABLE](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_BROWSABLE:kotlin.String) or no category and also match against [Intent.CATEGORY_DEFAULT](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String) [android.content.IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#) s, either through an explicit declaration of [Intent.CATEGORY_DEFAULT](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String) or through the use of [android.content.pm.PackageManager#MATCH_DEFAULT_ONLY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DEFAULT_ONLY:kotlin.Int), which is usually added for the caller when using [Context.startActivity(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent))and similar. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DomainVerificationUserState](https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationUserState)? | [getDomainVerificationUserState](https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager#getDomainVerificationUserState(kotlin.String))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Retrieve the user state for the given package and the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)'s user. |

## Public methods

### getDomainVerificationUserState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDomainVerificationUserState(packageName: String): DomainVerificationUserState?
```

Retrieve the user state for the given package and the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)'s user.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The app to query state for. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [DomainVerificationUserState](https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationUserState)? | The user selection verification data for the given package for the user, or null if the package does not declare any HTTP/HTTPS domains. |
