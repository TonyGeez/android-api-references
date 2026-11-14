# KeyStore.LoadStoreParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoadStoreParameter

```
interface LoadStoreParameter
```

| [java.security.KeyStore.LoadStoreParameter](../java/security/KeyStore.LoadStoreParameter.md) |

| Known Direct Subclasses [DomainLoadStoreParameter](DomainLoadStoreParameter.md) |-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------| | [DomainLoadStoreParameter](DomainLoadStoreParameter.md) | Configuration data that specifies the keystores in a keystore domain. | |
| --- | --- | --- | --- | --- | --- | --- |

A marker interface for`KeyStore` [load](KeyStore.md))and [store](KeyStore.md))parameters.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)! | [getProtectionParameter](../java/security/KeyStore.LoadStoreParameter.md))`()` Gets the parameter used to protect keystore data. |

## Public methods

### getProtectionParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProtectionParameter(): KeyStore.ProtectionParameter!
```

Gets the parameter used to protect keystore data.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)! | the parameter used to protect keystore data, or null |
