# AppSearchBatchResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchBatchResult

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/AppSearchBatchResult "View this page in Java") 

```
class AppSearchBatchResult<KeyType : Any!, ValueType : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appsearch.AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#) |

Provides results for AppSearch batch operations which encompass multiple documents.

Individual results of a batch operation are separated into two maps: one for successes and one for failures. For successes, [getSuccesses()](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#getSuccesses())will return a map of keys to instances of the value type. For failures, [getFailures()](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#getFailures())will return a map of keys to [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) objects.

Alternatively, [getAll()](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#getAll())returns a map of keys to [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) objects for both successes and failures.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult.Builder) Builder for [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#) objects. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType, [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\<ValueType\>!\> | [getAll](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#getAll())`()` Returns a [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) of keys mapped to instances of [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) for all individual results. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType, [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult)\<ValueType\>!\> | [getFailures](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#getFailures())`()` Returns a [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) of keys mapped to instances of [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) for all failed individual results. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType,ValueType\> | [getSuccesses](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#getSuccesses())`()` Returns a [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) of keys mapped to instances of the value type for all successful individual results. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSuccess](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#isSuccess())`()` Returns`true`if this [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#) has no failures. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#toString())`()` Returns a string representation of the object. |

## Public methods

### getAll

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAll(): MutableMap<KeyType, AppSearchResult<ValueType>!>
```

Returns a [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) of keys mapped to instances of [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) for all individual results.

The values of the [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) will not be`null`. 

### getFailures

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFailures(): MutableMap<KeyType, AppSearchResult<ValueType>!>
```

Returns a [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) of keys mapped to instances of [AppSearchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult) for all failed individual results.

The values of the [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) will not be`null`. 

### getSuccesses

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuccesses(): MutableMap<KeyType, ValueType>
```

Returns a [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) of keys mapped to instances of the value type for all successful individual results.

Example: [AppSearchSession.getByDocumentId](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#getByDocumentId(android.app.appsearch.GetByDocumentIdRequest,%20java.util.concurrent.Executor,%20android.app.appsearch.BatchResultCallback))returns an [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#). Each key (the document ID, of`String`type) will map to a [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) object.

The values of the [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) will not be`null`. 

### isSuccess

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSuccess(): Boolean
```

Returns`true`if this [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult#) has no failures. 

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |
