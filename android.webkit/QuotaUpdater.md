# WebStorage.QuotaUpdater

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# QuotaUpdater

Kotlin| [Java](../android/webkit/WebStorage.QuotaUpdater.md) 
| --- | --- |

```
interface QuotaUpdater
```

| [android.webkit.WebStorage.QuotaUpdater](../android/webkit/WebStorage.QuotaUpdater.md) |

| **This interface was deprecated in API level 19.**
|
| This class is obsolete and no longer used.

Encapsulates a callback function which is used to provide a new quota for a JavaScript storage API. See [WebChromeClient.onExceededDatabaseQuota](WebChromeClient.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateQuota](../android/webkit/WebStorage.QuotaUpdater.md))`(`newQuota:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Provides a new quota, specified in bytes. |

## Public methods

### updateQuota

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateQuota(newQuota: Long): Unit
```

**Deprecated:** *Deprecated in Java.*

Provides a new quota, specified in bytes.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------|
| `newQuota` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new quota, in bytes |
