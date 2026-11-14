# OnAccountsUpdateListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAccountsUpdateListener

Kotlin| [Java](https://developer.android.com/reference/android/accounts/OnAccountsUpdateListener "View this page in Java") 
| --- | --- |

```
interface OnAccountsUpdateListener
```

| [android.accounts.OnAccountsUpdateListener](https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener#) |

An interface that contains the callback used by the AccountManager

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccountsUpdated](https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener#onAccountsUpdated(kotlin.Array))`(`accounts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!>!`)` This invoked when the AccountManager starts up and whenever the account set changes. |

## Public methods

### onAccountsUpdated

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccountsUpdated(accounts: Array<Account!>!): Unit
```

This invoked when the AccountManager starts up and whenever the account set changes.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accounts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\>!:the current accounts |
