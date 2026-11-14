# AccountManagerCallback

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccountManagerCallback

Kotlin| [Java](https://developer.android.com/reference/android/accounts/AccountManagerCallback "View this page in Java") 
| --- | --- |

```
interface AccountManagerCallback<V : Any!>
```

| [android.accounts.AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback#) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback#run(android.accounts.AccountManagerFuture))`(`future:` ` [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)<V>!`)` <br /> |

## Public methods

### run

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun run(future: AccountManagerFuture<V>!): Unit
```
