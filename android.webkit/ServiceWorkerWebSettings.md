# ServiceWorkerWebSettings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceWorkerWebSettings

Kotlin| [Java](ServiceWorkerWebSettings.md) 
| --- | --- |

```
abstract class ServiceWorkerWebSettings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ServiceWorkerWebSettings](ServiceWorkerWebSettings.md) |

Manages settings state for all Service Workers. These settings are not tied to the lifetime of any WebView because service workers can outlive WebView instances. The settings are similar to [WebSettings](WebSettings.md) but only settings relevant to Service Workers are supported.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceWorkerWebSettings](ServiceWorkerWebSettings.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowContentAccess](ServiceWorkerWebSettings.md))`()` Gets whether Service Workers support content URL access. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowFileAccess](ServiceWorkerWebSettings.md))`()` Gets whether Service Workers support file access. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBlockNetworkLoads](ServiceWorkerWebSettings.md))`()` Gets whether Service Workers are prohibited from loading any resources from the network. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCacheMode](ServiceWorkerWebSettings.md))`()` Gets the current setting for overriding the cache mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowContentAccess](ServiceWorkerWebSettings.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables content URL access from Service Workers, see [WebSettings.setAllowContentAccess](WebSettings.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowFileAccess](ServiceWorkerWebSettings.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables file access within Service Workers, see [WebSettings.setAllowFileAccess](WebSettings.md)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlockNetworkLoads](ServiceWorkerWebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Service Workers should not load resources from the network, see [WebSettings.setBlockNetworkLoads](WebSettings.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCacheMode](ServiceWorkerWebSettings.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Overrides the way the cache is used, see [WebSettings.setCacheMode](WebSettings.md)). |

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

- [#setAllowContentAccess](ServiceWorkerWebSettings.md)) 

### getAllowFileAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllowFileAccess(): Boolean
```

Gets whether Service Workers support file access. 
**See Also**

- [#setAllowFileAccess](ServiceWorkerWebSettings.md)) 

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

- [#setBlockNetworkLoads](ServiceWorkerWebSettings.md)) 

### getCacheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCacheMode(): Int
```

Gets the current setting for overriding the cache mode.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current setting for overriding the cache mode Value is [android.webkit.WebSettings#LOAD_DEFAULT](WebSettings.md), [android.webkit.WebSettings#LOAD_NORMAL](WebSettings.md), [android.webkit.WebSettings#LOAD_CACHE_ELSE_NETWORK](WebSettings.md), [android.webkit.WebSettings#LOAD_NO_CACHE](WebSettings.md), or [android.webkit.WebSettings#LOAD_CACHE_ONLY](WebSettings.md) |

**See Also**

- [#setCacheMode](ServiceWorkerWebSettings.md)) 

### setAllowContentAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowContentAccess(allow: Boolean): Unit
```

Enables or disables content URL access from Service Workers, see [WebSettings.setAllowContentAccess](WebSettings.md)). 

### setAllowFileAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowFileAccess(allow: Boolean): Unit
```

Enables or disables file access within Service Workers, see [WebSettings.setAllowFileAccess](WebSettings.md)). 

### setBlockNetworkLoads

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlockNetworkLoads(flag: Boolean): Unit
```

Sets whether Service Workers should not load resources from the network, see [WebSettings.setBlockNetworkLoads](WebSettings.md)).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`means block network loads by the Service Workers |

### setCacheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCacheMode(mode: Int): Unit
```

Overrides the way the cache is used, see [WebSettings.setCacheMode](WebSettings.md)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode to use. One of [WebSettings.LOAD_DEFAULT](WebSettings.md), [WebSettings.LOAD_CACHE_ELSE_NETWORK](WebSettings.md), [WebSettings.LOAD_NO_CACHE](WebSettings.md) or [WebSettings.LOAD_CACHE_ONLY](WebSettings.md). The default value is [WebSettings.LOAD_DEFAULT](WebSettings.md). Value is [android.webkit.WebSettings#LOAD_DEFAULT](WebSettings.md), [android.webkit.WebSettings#LOAD_NORMAL](WebSettings.md), [android.webkit.WebSettings#LOAD_CACHE_ELSE_NETWORK](WebSettings.md), [android.webkit.WebSettings#LOAD_NO_CACHE](WebSettings.md), or [android.webkit.WebSettings#LOAD_CACHE_ONLY](WebSettings.md) |
