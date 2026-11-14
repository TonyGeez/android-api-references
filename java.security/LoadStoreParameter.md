# KeyStore.LoadStoreParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoadStoreParameter

```
interface LoadStoreParameter
```

| [java.security.KeyStore.LoadStoreParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter#) |

| Known Direct Subclasses [DomainLoadStoreParameter](https://developer.android.com/reference/kotlin/java/security/DomainLoadStoreParameter) |-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------| | [DomainLoadStoreParameter](https://developer.android.com/reference/kotlin/java/security/DomainLoadStoreParameter) | Configuration data that specifies the keystores in a keystore domain. | |

A marker interface for`KeyStore` [load](https://developer.android.com/reference/kotlin/java/security/KeyStore#load(java.security.KeyStore.LoadStoreParameter))and [store](https://developer.android.com/reference/kotlin/java/security/KeyStore#store(java.security.KeyStore.LoadStoreParameter))parameters.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [KeyStore.ProtectionParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter)! | [getProtectionParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter#getProtectionParameter())`()` Gets the parameter used to protect keystore data. |

## Public methods

### getProtectionParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProtectionParameter(): KeyStore.ProtectionParameter!
```

Gets the parameter used to protect keystore data.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [KeyStore.ProtectionParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter)! | the parameter used to protect keystore data, or null |
