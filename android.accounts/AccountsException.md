# AccountsException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccountsException

Kotlin| [Java](https://developer.android.com/reference/android/accounts/AccountsException "View this page in Java") 
| --- | --- |

```
open class AccountsException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.accounts.AccountsException](https://developer.android.com/reference/kotlin/android/accounts/AccountsException#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [AuthenticatorException](https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException), [NetworkErrorException](https://developer.android.com/reference/kotlin/android/accounts/NetworkErrorException), [OperationCanceledException](https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException) |--------------------------------------------------------------------------------------------------------------------------|--------| | [AuthenticatorException](https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException) | <br /> | | [NetworkErrorException](https://developer.android.com/reference/kotlin/android/accounts/NetworkErrorException) | <br /> | | [OperationCanceledException](https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccountsException](https://developer.android.com/reference/kotlin/android/accounts/AccountsException#AccountsException())`()` <br /> |
| [AccountsException](https://developer.android.com/reference/kotlin/android/accounts/AccountsException#AccountsException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [AccountsException](https://developer.android.com/reference/kotlin/android/accounts/AccountsException#AccountsException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [AccountsException](https://developer.android.com/reference/kotlin/android/accounts/AccountsException#AccountsException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

## Public constructors

### AccountsException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccountsException()
```  

### AccountsException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccountsException(message: String!)
```  

### AccountsException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccountsException(
    message: String!, 
    cause: Throwable!)
```  

### AccountsException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccountsException(cause: Throwable!)
```
