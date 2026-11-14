# DomainVerificationManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DomainVerificationManager

Kotlin| [Java](DomainVerificationManager.md) 
| --- | --- |

```
class DomainVerificationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.verify.domain.DomainVerificationManager](DomainVerificationManager.md) |

System service to access domain verification APIs. Applications should use [getDomainVerificationUserState(java.lang.String)](DomainVerificationManager.md))if necessary to check if/how they are verified for a domain, which is required starting from platform [android.os.Build.VERSION_CODES#S](../android/os/Build.VERSION_CODES.md) in order to open [Intent](../android.content/Intent.md) s which declare [Intent.CATEGORY_BROWSABLE](../android.content/Intent.md) or no category and also match against [Intent.CATEGORY_DEFAULT](../android.content/Intent.md) [android.content.IntentFilter](../android.content/IntentFilter.md) s, either through an explicit declaration of [Intent.CATEGORY_DEFAULT](../android.content/Intent.md) or through the use of [android.content.pm.PackageManager#MATCH_DEFAULT_ONLY](../android.content.pm/PackageManager.md), which is usually added for the caller when using [Context.startActivity(Intent)](../android.content/Context.md))and similar. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DomainVerificationUserState](DomainVerificationUserState.md)? | [getDomainVerificationUserState](DomainVerificationManager.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Retrieve the user state for the given package and the [Context](../android.content/Context.md)'s user. |

## Public methods

### getDomainVerificationUserState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDomainVerificationUserState(packageName: String): DomainVerificationUserState?
```

Retrieve the user state for the given package and the [Context](../android.content/Context.md)'s user.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The app to query state for. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [DomainVerificationUserState](DomainVerificationUserState.md)? | The user selection verification data for the given package for the user, or null if the package does not declare any HTTP/HTTPS domains. |
