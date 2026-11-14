# WebStorage

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebStorage

Kotlin| [Java](../android/webkit/WebStorage.md) 
| --- | --- |

```
open class WebStorage
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebStorage](../android/webkit/WebStorage.md) |

This class is used to manage the JavaScript storage APIs provided by the [WebView](../android/webkit/WebView.md). It manages the Web SQL Database API and the HTML5 Web Storage API. The Web SQL Database API provides storage which is private to a given origin. Use of the Web SQL Database can be attributed to an origin. It is also possible to set per-origin quotas.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Origin](../android/webkit/WebStorage.Origin.md) This class encapsulates information about the amount of storage currently used by an origin for the JavaScript storage APIs. |
| abstract | [QuotaUpdater](../android/webkit/WebStorage.QuotaUpdater.md) Encapsulates a callback function which is used to provide a new quota for a JavaScript storage API. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteAllData](../android/webkit/WebStorage.md))`()` Clears all storage currently being used by the JavaScript storage APIs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteOrigin](../android/webkit/WebStorage.md))`(`origin:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Clears the storage currently being used by the Web SQL Database APIs by the given origin. |
| openstatic [WebStorage](../android/webkit/WebStorage.md)! | [getInstance](../android/webkit/WebStorage.md))`()` Gets the singleton instance of this class. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOrigins](../android/webkit/WebStorage.md))`(`callback:` ` [ValueCallback](../android/webkit/ValueCallback.md)< [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>!>!`)` Gets the origins currently using the Web SQL Database APIs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getQuotaForOrigin](../android/webkit/WebStorage.md))`(`origin:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `callback:` ` [ValueCallback](../android/webkit/ValueCallback.md)< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!>!`)` Gets the storage quota for the Web SQL Database API for the given origin. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getUsageForOrigin](../android/webkit/WebStorage.md))`(`origin:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `callback:` ` [ValueCallback](../android/webkit/ValueCallback.md)< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!>!`)` Gets the amount of storage currently being used by the Web SQL Database APIs by the given origin. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQuotaForOrigin](../android/webkit/WebStorage.md))`(`origin:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `quota:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the storage quota for the Web SQL Database API for the given origin. |

## Public methods

### deleteAllData

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteAllData(): Unit
```

Clears all storage currently being used by the JavaScript storage APIs. This includes Web SQL Database and the HTML5 Web Storage APIs. 

### deleteOrigin

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteOrigin(origin: String!): Unit
```

Clears the storage currently being used by the Web SQL Database APIs by the given origin. The origin is specified using its string representation. 

### getInstance

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): WebStorage!
```

Gets the singleton instance of this class.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [WebStorage](../android/webkit/WebStorage.md)! | the singleton [WebStorage](../android/webkit/WebStorage.md) instance |

### getOrigins

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrigins(callback: ValueCallback<MutableMap<Any?, Any?>!>!): Unit
```

Gets the origins currently using the Web SQL Database APIs. This method operates asynchronously, with the result being provided via a [ValueCallback](../android/webkit/ValueCallback.md). The origins are provided as a map, of type`Map<String, WebStorage.Origin>`, from the string representation of the origin to a [WebStorage.Origin](../android/webkit/WebStorage.Origin.md) object. 

### getQuotaForOrigin

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQuotaForOrigin(
    origin: String!, 
    callback: ValueCallback<Long!>!
): Unit
```

Gets the storage quota for the Web SQL Database API for the given origin. The quota is given in bytes and the origin is specified using its string representation. This method operates asynchronously, with the result being provided via a [ValueCallback](../android/webkit/ValueCallback.md). 

### getUsageForOrigin

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUsageForOrigin(
    origin: String!, 
    callback: ValueCallback<Long!>!
): Unit
```

Gets the amount of storage currently being used by the Web SQL Database APIs by the given origin. The amount is given in bytes and the origin is specified using its string representation. This method operates asynchronously, with the result being provided via a [ValueCallback](../android/webkit/ValueCallback.md). 

### setQuotaForOrigin

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setQuotaForOrigin(
    origin: String!, 
    quota: Long
): Unit
```

**Deprecated:** *Controlling quota per-origin will not be supported in future.*

Sets the storage quota for the Web SQL Database API for the given origin. The quota is specified in bytes and the origin is specified using its string representation.
