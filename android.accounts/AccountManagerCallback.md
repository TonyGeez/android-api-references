# AccountManagerCallback

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccountManagerCallback

Kotlin| [Java](AccountManagerCallback.md) 
| --- | --- |

```
interface AccountManagerCallback<V : Any!>
```

| [android.accounts.AccountManagerCallback](AccountManagerCallback.md) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](AccountManagerCallback.md))`(`future:` ` [AccountManagerFuture](AccountManagerFuture.md)<V>!`)` <br /> |

## Public methods

### run

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun run(future: AccountManagerFuture<V>!): Unit
```
