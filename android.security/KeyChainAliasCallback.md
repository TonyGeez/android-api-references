# KeyChainAliasCallback

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyChainAliasCallback

Kotlin | [Java](https://developer.android.com/reference/android/security/KeyChainAliasCallback "View this page in Java") 
| --- | --- |

```
interface KeyChainAliasCallback
```

| [android.security.KeyChainAliasCallback](https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback#) |

The KeyChainAliasCallback is the callback for android.security.KeyChain#choosePrivateKeyAlias.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [alias](https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback#alias(kotlin.String))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Called with the alias of the certificate chosen by the user, or null if no value was chosen. |

## Public methods

### alias

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun alias(alias: String?): Unit
```

Called with the alias of the certificate chosen by the user, or null if no value was chosen.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
