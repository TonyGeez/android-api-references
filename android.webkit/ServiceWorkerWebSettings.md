# ServiceWorkerWebSettings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceWorkerWebSettings

Kotlin| [Java](../android/webkit/ServiceWorkerWebSettings.md) 
| --- | --- |

```
abstract class ServiceWorkerWebSettings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ServiceWorkerWebSettings](../android/webkit/ServiceWorkerWebSettings.md) |

Manages settings state for all Service Workers. These settings are not tied to the lifetime of any WebView because service workers can outlive WebView instances. The settings are similar to [WebSettings](../android/webkit/WebSettings.md) but only settings relevant to Service Workers are supported.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceWorkerWebSettings](../android/webkit/ServiceWorkerWebSettings.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowContentAccess](../android/webkit/ServiceWorkerWebSettings.md))`()` Gets whether Service Workers support content URL access. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowFileAccess](../android/webkit/ServiceWorkerWebSettings.md))`()` Gets whether Service Workers support file access. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBlockNetworkLoads](../android/webkit/ServiceWorkerWebSettings.md))`()` Gets whether Service Workers are prohibited from loading any resources from the network. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCacheMode](../android/webkit/ServiceWorkerWebSettings.md))`()` Gets the current setting for overriding the cache mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowContentAccess](../android/webkit/ServiceWorkerWebSettings.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables content URL access from Service Workers, see [WebSettings.setAllowContentAccess](../android/webkit/WebSettings.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowFileAccess](../android/webkit/ServiceWorkerWebSettings.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables file access within Service Workers, see [WebSettings.setAllowFileAccess](../android/webkit/WebSettings.md)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlockNetworkLoads](../android/webkit/ServiceWorkerWebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Service Workers should not load resources from the network, see [WebSettings.setBlockNetworkLoads](../android/webkit/WebSettings.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCacheMode](../android/webkit/ServiceWorkerWebSettings.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Overrides the way the cache is used, see [WebSettings.setCacheMode](../android/webkit/WebSettings.md)). |

## Public constructors

### ServiceWorkerWebSettings

```
ServiceWorkerWebSettings()
```

## Public methods

### getAllowContentAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllowContentAccess(): Boolean
```

Gets whether Service Workers support content URL access. 
**See Also**

- [#setAllowContentAccess](../android/webkit/ServiceWorkerWebSettings.md)) 

### getAllowFileAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllowFileAccess(): Boolean
```

Gets whether Service Workers support file access. 
**See Also**

- [#setAllowFileAccess](../android/webkit/ServiceWorkerWebSettings.md)) 

### getBlockNetworkLoads

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBlockNetworkLoads(): Boolean
```

Gets whether Service Workers are prohibited from loading any resources from the network.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the Service Workers are not allowed to load any resources from the network |

**See Also**

- [#setBlockNetworkLoads](../android/webkit/ServiceWorkerWebSettings.md)) 

### getCacheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCacheMode(): Int
```

Gets the current setting for overriding the cache mode.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current setting for overriding the cache mode Value is [android.webkit.WebSettings#LOAD_DEFAULT](../android/webkit/WebSettings.md), [android.webkit.WebSettings#LOAD_NORMAL](../android/webkit/WebSettings.md), [android.webkit.WebSettings#LOAD_CACHE_ELSE_NETWORK](../android/webkit/WebSettings.md), [android.webkit.WebSettings#LOAD_NO_CACHE](../android/webkit/WebSettings.md), or [android.webkit.WebSettings#LOAD_CACHE_ONLY](../android/webkit/WebSettings.md) |

**See Also**

- [#setCacheMode](../android/webkit/ServiceWorkerWebSettings.md)) 

### setAllowContentAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowContentAccess(allow: Boolean): Unit
```

Enables or disables content URL access from Service Workers, see [WebSettings.setAllowContentAccess](../android/webkit/WebSettings.md)). 

### setAllowFileAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowFileAccess(allow: Boolean): Unit
```

Enables or disables file access within Service Workers, see [WebSettings.setAllowFileAccess](../android/webkit/WebSettings.md)). 

### setBlockNetworkLoads

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlockNetworkLoads(flag: Boolean): Unit
```

Sets whether Service Workers should not load resources from the network, see [WebSettings.setBlockNetworkLoads](../android/webkit/WebSettings.md)).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`means block network loads by the Service Workers |

### setCacheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCacheMode(mode: Int): Unit
```

Overrides the way the cache is used, see [WebSettings.setCacheMode](../android/webkit/WebSettings.md)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode to use. One of [WebSettings.LOAD_DEFAULT](../android/webkit/WebSettings.md), [WebSettings.LOAD_CACHE_ELSE_NETWORK](../android/webkit/WebSettings.md), [WebSettings.LOAD_NO_CACHE](../android/webkit/WebSettings.md) or [WebSettings.LOAD_CACHE_ONLY](../android/webkit/WebSettings.md). The default value is [WebSettings.LOAD_DEFAULT](../android/webkit/WebSettings.md). Value is [android.webkit.WebSettings#LOAD_DEFAULT](../android/webkit/WebSettings.md), [android.webkit.WebSettings#LOAD_NORMAL](../android/webkit/WebSettings.md), [android.webkit.WebSettings#LOAD_CACHE_ELSE_NETWORK](../android/webkit/WebSettings.md), [android.webkit.WebSettings#LOAD_NO_CACHE](../android/webkit/WebSettings.md), or [android.webkit.WebSettings#LOAD_CACHE_ONLY](../android/webkit/WebSettings.md) |
