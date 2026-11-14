# ReportSystemUsageRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReportSystemUsageRequest

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/ReportSystemUsageRequest "View this page in Java") 
| --- | --- |

```
class ReportSystemUsageRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.ReportSystemUsageRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest#) |

A request to report usage of a document owned by another app from a system UI surface.

Usage reported in this way is measured separately from usage reported via [android.app.appsearch.AppSearchSession#reportUsage](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#reportUsage(android.app.appsearch.ReportUsageRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer)).

See [GlobalSearchSession.reportSystemUsage](https://developer.android.com/reference/kotlin/android/app/appsearch/GlobalSearchSession#reportSystemUsage(android.app.appsearch.ReportSystemUsageRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer))for a detailed description of usage reporting.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest.Builder) Builder for [ReportSystemUsageRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest#) objects. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDatabaseName](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest#getDatabaseName())`()` Returns the database in which the document that was used resides. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDocumentId](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest#getDocumentId())`()` Returns the ID of document that was used. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getNamespace](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest#getNamespace())`()` Returns the namespace of the document that was used. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest#getPackageName())`()` Returns the package name of the app which owns the document that was used. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUsageTimestampMillis](https://developer.android.com/reference/kotlin/android/app/appsearch/ReportSystemUsageRequest#getUsageTimestampMillis())`()` Returns the timestamp in milliseconds of the usage report (the time at which the document was used). |

## Public methods

### getDatabaseName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDatabaseName(): String
```

Returns the database in which the document that was used resides.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getDocumentId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDocumentId(): String
```

Returns the ID of document that was used.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getNamespace

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNamespace(): String
```

Returns the namespace of the document that was used.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getPackageName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String
```

Returns the package name of the app which owns the document that was used.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getUsageTimestampMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUsageTimestampMillis(): Long
```

Returns the timestamp in milliseconds of the usage report (the time at which the document was used).

The value is in the [System.currentTimeMillis](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())time base. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |
