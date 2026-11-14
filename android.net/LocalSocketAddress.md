# LocalSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalSocketAddress

Kotlin | [Java](LocalSocketAddress.md) 
| --- | --- |

```
open class LocalSocketAddress
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.LocalSocketAddress](LocalSocketAddress.md) |

A UNIX-domain (AF_LOCAL) socket address. For use with android.net.LocalSocket and android.net.LocalServerSocket. On the Android system, these names refer to names in the Linux abstract (non-filesystem) UNIX domain namespace.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Namespace](../android/net/LocalSocketAddress.Namespace.md) The namespace that this address exists in. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocalSocketAddress](LocalSocketAddress.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an instance with a given name in the [Namespace.ABSTRACT](../android/net/LocalSocketAddress.Namespace.md) namespace |
| [LocalSocketAddress](LocalSocketAddress.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `namespace:` ` [LocalSocketAddress.Namespace](../android/net/LocalSocketAddress.Namespace.md)!`)` Creates an instance with a given name. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](LocalSocketAddress.md))`()` Retrieves the string name of this address |
| open [LocalSocketAddress.Namespace](../android/net/LocalSocketAddress.Namespace.md)! | [getNamespace](LocalSocketAddress.md))`()` Returns the namespace used by this address. |

## Public constructors

### LocalSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocalSocketAddress(name: String!)
```

Creates an instance with a given name in the [Namespace.ABSTRACT](../android/net/LocalSocketAddress.Namespace.md) namespace

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: non-null name |

### LocalSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocalSocketAddress(
    name: String!, 
    namespace: LocalSocketAddress.Namespace!)
```

Creates an instance with a given name.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: non-null name |
| `namespace` | [LocalSocketAddress.Namespace](../android/net/LocalSocketAddress.Namespace.md)!: namespace the name should be created in. |

## Public methods

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Retrieves the string name of this address

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | string name |

### getNamespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNamespace(): LocalSocketAddress.Namespace!
```

Returns the namespace used by this address.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------|
| [LocalSocketAddress.Namespace](../android/net/LocalSocketAddress.Namespace.md)! | non-null a namespace |
