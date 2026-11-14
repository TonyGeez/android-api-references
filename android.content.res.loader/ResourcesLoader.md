Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResourcesLoader

Kotlin | [Java](ResourcesLoader.md)
| --- | --- |

```
open class ResourcesLoader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.res.loader.ResourcesLoader](ResourcesLoader.md) |

A container for supplying `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider` to `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` objects.

`https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader#` are added to Resources objects to supply additional resources and assets or modify the values of existing resources and assets. Multiple Resources objects can share the same ResourcesLoaders and ResourcesProviders. Changes to the list of `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider` a loader contains propagates to all Resources objects that use the loader.

Loaders must be added to Resources objects in increasing precedence order. A loader will override the resources and assets of loaders added before itself.

Providers retrieved with `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader#getProviders()` are listed in increasing precedence order. A provider will override the resources and assets of providers listed before itself.

Modifying the list of providers a loader contains or the list of loaders a Resources object contains can cause lock contention with the UI thread. APIs that modify the lists of loaders or providers should only be used on the UI thread. Providers can be instantiated on any thread without causing lock contention.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader#ResourcesLoader()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader#addProvider(android.content.res.loader.ResourcesProvider)(resourcesProvider: https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider)` Appends a provider to the end of the provider list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader#clearProviders()()` Removes all `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider`. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResourcesProvider](ResourcesProvider.md)!\> | `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader#getProviders()()` Retrieves the list of providers loaded into this instance. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader#removeProvider(android.content.res.loader.ResourcesProvider)(resourcesProvider: https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider)` Removes a provider from the provider list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader#setProviders(kotlin.collections.MutableList)(resourcesProviders: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider!>)` Sets the list of providers. |

## Public constructors

### ResourcesLoader

```
ResourcesLoader()
```

## Public methods

### addProvider

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addProvider(resourcesProvider: ResourcesProvider): Unit
```

Appends a provider to the end of the provider list. If the provider is already present in the loader list, the list will not be modified.

This should only be called from the UI thread to avoid lock contention when propagating provider changes.

| Parameters ||
|---|---|
| `resourcesProvider` | [ResourcesProvider](ResourcesProvider.md): the provider to add. This value cannot be `null`. |

### clearProviders

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearProviders(): Unit
```

Removes all `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider`.

This should only be called from the UI thread to avoid lock contention when propagating provider changes.

### getProviders

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProviders(): MutableList<ResourcesProvider!>
```

Retrieves the list of providers loaded into this instance. Providers are listed in increasing precedence order. A provider will override the values of providers listed before itself.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider!>` | This value cannot be `null`. |

### removeProvider

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeProvider(resourcesProvider: ResourcesProvider): Unit
```

Removes a provider from the provider list. If the provider is not present in the provider list, the list will not be modified.

This should only be called from the UI thread to avoid lock contention when propagating provider changes.

| Parameters ||
|---|---|
| `resourcesProvider` | [ResourcesProvider](ResourcesProvider.md): the provider to remove. This value cannot be `null`. |

### setProviders

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setProviders(resourcesProviders: MutableList<ResourcesProvider!>): Unit
```

Sets the list of providers.

This should only be called from the UI thread to avoid lock contention when propagating provider changes.

| Parameters ||
|---|---|
| `resourcesProviders` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResourcesProvider](ResourcesProvider.md)!\>: the new providers. This value cannot be `null`. |
