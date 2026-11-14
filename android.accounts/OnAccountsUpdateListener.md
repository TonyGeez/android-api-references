# OnAccountsUpdateListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAccountsUpdateListener

Kotlin| [Java](OnAccountsUpdateListener.md) 
| --- | --- |

```
interface OnAccountsUpdateListener
```

| [android.accounts.OnAccountsUpdateListener](OnAccountsUpdateListener.md) |

An interface that contains the callback used by the AccountManager

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccountsUpdated](OnAccountsUpdateListener.md))`(`accounts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Account](Account.md)!>!`)` This invoked when the AccountManager starts up and whenever the account set changes. |

## Public methods

### onAccountsUpdated

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccountsUpdated(accounts: Array<Account!>!): Unit
```

This invoked when the AccountManager starts up and whenever the account set changes.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accounts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Account](Account.md)!\>!:the current accounts |
