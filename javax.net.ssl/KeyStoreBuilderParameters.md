# KeyStoreBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStoreBuilderParameters

```
open class KeyStoreBuilderParameters : ManagerFactoryParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.net.ssl.KeyStoreBuilderParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyStoreBuilderParameters#) |

A parameters object for X509KeyManagers that encapsulates a List of KeyStore.Builders.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyStoreBuilderParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyStoreBuilderParameters#KeyStoreBuilderParameters(java.security.KeyStore.Builder))`(`builder:` ` [KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#)!`)` Construct new KeyStoreBuilderParameters from the specified [java.security.KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#). |
| [KeyStoreBuilderParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyStoreBuilderParameters#KeyStoreBuilderParameters(kotlin.collections.MutableList))`(`parameters:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#)!>!`)` Construct new KeyStoreBuilderParameters from a List of [java.security.KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#) s. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#)!\>! | [getParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyStoreBuilderParameters#getParameters())`()` Return the unmodifiable List of the [java.security.KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#) s encapsulated by this object. |

## Public constructors

### KeyStoreBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreBuilderParameters(builder: KeyStore.Builder!)
```

Construct new KeyStoreBuilderParameters from the specified [java.security.KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `builder` | [KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#)!:the Builder object |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if builder is null |

### KeyStoreBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreBuilderParameters(parameters: MutableList<KeyStore.Builder!>!)
```

Construct new KeyStoreBuilderParameters from a List of [java.security.KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#) s. Note that the list is cloned to protect against subsequent modification.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#)!\>!:the List of Builder objects |

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

Return the unmodifiable List of the [java.security.KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#) s encapsulated by this object.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#)!>! | the unmodifiable List of the [java.security.KeyStore.Builder](https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder.html#) s encapsulated by this object. |
