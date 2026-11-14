# KeyStoreBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStoreBuilderParameters

```
open class KeyStoreBuilderParameters : ManagerFactoryParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.KeyStoreBuilderParameters](../javax/net/ssl/KeyStoreBuilderParameters.md) |

A parameters object for X509KeyManagers that encapsulates a List of KeyStore.Builders.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyStoreBuilderParameters](../javax/net/ssl/KeyStoreBuilderParameters.md))`(`builder:` ` [KeyStore.Builder](../java/security/KeyStore.Builder.md)!`)` Construct new KeyStoreBuilderParameters from the specified [java.security.KeyStore.Builder](../java/security/KeyStore.Builder.md). |
| [KeyStoreBuilderParameters](../javax/net/ssl/KeyStoreBuilderParameters.md))`(`parameters:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [KeyStore.Builder](../java/security/KeyStore.Builder.md)!>!`)` Construct new KeyStoreBuilderParameters from a List of [java.security.KeyStore.Builder](../java/security/KeyStore.Builder.md) s. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [KeyStore.Builder](../java/security/KeyStore.Builder.md)!\>! | [getParameters](../javax/net/ssl/KeyStoreBuilderParameters.md))`()` Return the unmodifiable List of the [java.security.KeyStore.Builder](../java/security/KeyStore.Builder.md) s encapsulated by this object. |

## Public constructors

### KeyStoreBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreBuilderParameters(builder: KeyStore.Builder!)
```

Construct new KeyStoreBuilderParameters from the specified [java.security.KeyStore.Builder](../java/security/KeyStore.Builder.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `builder` | [KeyStore.Builder](../java/security/KeyStore.Builder.md)!:the Builder object |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if builder is null |

### KeyStoreBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreBuilderParameters(parameters: MutableList<KeyStore.Builder!>!)
```

Construct new KeyStoreBuilderParameters from a List of [java.security.KeyStore.Builder](../java/security/KeyStore.Builder.md) s. Note that the list is cloned to protect against subsequent modification.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [KeyStore.Builder](../java/security/KeyStore.Builder.md)!\>!:the List of Builder objects |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.NullPointerException` | if parameters is null |
| `java.lang.IllegalArgumentException` | if parameters is an empty list |

## Public methods

### getParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameters(): MutableList<KeyStore.Builder!>!
```

Return the unmodifiable List of the [java.security.KeyStore.Builder](../java/security/KeyStore.Builder.md) s encapsulated by this object.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [KeyStore.Builder](../java/security/KeyStore.Builder.md)!>! | the unmodifiable List of the [java.security.KeyStore.Builder](../java/security/KeyStore.Builder.md) s encapsulated by this object. |
