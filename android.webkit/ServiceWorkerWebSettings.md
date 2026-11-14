# ServiceWorkerWebSettings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceWorkerWebSettings

Kotlin| [Java](https://developer.android.com/reference/android/webkit/ServiceWorkerWebSettings "View this page in Java") 

```
abstract class ServiceWorkerWebSettings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.webkit.ServiceWorkerWebSettings](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#) |

Manages settings state for all Service Workers. These settings are not tied to the lifetime of any WebView because service workers can outlive WebView instances. The settings are similar to [WebSettings](https://developer.android.com/reference/kotlin/android/webkit/WebSettings) but only settings relevant to Service Workers are supported.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceWorkerWebSettings](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#ServiceWorkerWebSettings())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowContentAccess](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#getAllowContentAccess())`()` Gets whether Service Workers support content URL access. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowFileAccess](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#getAllowFileAccess())`()` Gets whether Service Workers support file access. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBlockNetworkLoads](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#getBlockNetworkLoads())`()` Gets whether Service Workers are prohibited from loading any resources from the network. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCacheMode](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#getCacheMode())`()` Gets the current setting for overriding the cache mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowContentAccess](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#setAllowContentAccess(kotlin.Boolean))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables content URL access from Service Workers, see [WebSettings.setAllowContentAccess](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setAllowContentAccess(kotlin.Boolean)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowFileAccess](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#setAllowFileAccess(kotlin.Boolean))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables file access within Service Workers, see [WebSettings.setAllowFileAccess](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setAllowFileAccess(kotlin.Boolean)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlockNetworkLoads](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#setBlockNetworkLoads(kotlin.Boolean))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Service Workers should not load resources from the network, see [WebSettings.setBlockNetworkLoads](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setBlockNetworkLoads(kotlin.Boolean)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCacheMode](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#setCacheMode(kotlin.Int))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Overrides the way the cache is used, see [WebSettings.setCacheMode](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setCacheMode(kotlin.Int)). |

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

- [#setAllowContentAccess](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#setAllowContentAccess(kotlin.Boolean)) 

### getAllowFileAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllowFileAccess(): Boolean
```

Gets whether Service Workers support file access. 
**See Also**

- [#setAllowFileAccess](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#setAllowFileAccess(kotlin.Boolean)) 

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

- [#setBlockNetworkLoads](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#setBlockNetworkLoads(kotlin.Boolean)) 

### getCacheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCacheMode(): Int
```

Gets the current setting for overriding the cache mode.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current setting for overriding the cache mode Value is [android.webkit.WebSettings#LOAD_DEFAULT](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_DEFAULT:kotlin.Int), [android.webkit.WebSettings#LOAD_NORMAL](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_NORMAL:kotlin.Int), [android.webkit.WebSettings#LOAD_CACHE_ELSE_NETWORK](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_CACHE_ELSE_NETWORK:kotlin.Int), [android.webkit.WebSettings#LOAD_NO_CACHE](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_NO_CACHE:kotlin.Int), or [android.webkit.WebSettings#LOAD_CACHE_ONLY](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_CACHE_ONLY:kotlin.Int) |

**See Also**

- [#setCacheMode](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings#setCacheMode(kotlin.Int)) 

### setAllowContentAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowContentAccess(allow: Boolean): Unit
```

Enables or disables content URL access from Service Workers, see [WebSettings.setAllowContentAccess](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setAllowContentAccess(kotlin.Boolean)). 

### setAllowFileAccess

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowFileAccess(allow: Boolean): Unit
```

Enables or disables file access within Service Workers, see [WebSettings.setAllowFileAccess](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setAllowFileAccess(kotlin.Boolean)). 

### setBlockNetworkLoads

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlockNetworkLoads(flag: Boolean): Unit
```

Sets whether Service Workers should not load resources from the network, see [WebSettings.setBlockNetworkLoads](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setBlockNetworkLoads(kotlin.Boolean)).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`means block network loads by the Service Workers |

### setCacheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCacheMode(mode: Int): Unit
```

Overrides the way the cache is used, see [WebSettings.setCacheMode](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setCacheMode(kotlin.Int)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode to use. One of [WebSettings.LOAD_DEFAULT](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_DEFAULT:kotlin.Int), [WebSettings.LOAD_CACHE_ELSE_NETWORK](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_CACHE_ELSE_NETWORK:kotlin.Int), [WebSettings.LOAD_NO_CACHE](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_NO_CACHE:kotlin.Int) or [WebSettings.LOAD_CACHE_ONLY](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_CACHE_ONLY:kotlin.Int). The default value is [WebSettings.LOAD_DEFAULT](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_DEFAULT:kotlin.Int). Value is [android.webkit.WebSettings#LOAD_DEFAULT](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_DEFAULT:kotlin.Int), [android.webkit.WebSettings#LOAD_NORMAL](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_NORMAL:kotlin.Int), [android.webkit.WebSettings#LOAD_CACHE_ELSE_NETWORK](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_CACHE_ELSE_NETWORK:kotlin.Int), [android.webkit.WebSettings#LOAD_NO_CACHE](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_NO_CACHE:kotlin.Int), or [android.webkit.WebSettings#LOAD_CACHE_ONLY](https://developer.android.com/reference/kotlin/android/webkit/WebSettings#LOAD_CACHE_ONLY:kotlin.Int) |
