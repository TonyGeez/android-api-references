# AppSearchBatchResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchBatchResult

Kotlin| [Java](../android/app/appsearch/AppSearchBatchResult.md) 
| --- | --- |

```
class AppSearchBatchResult<KeyType : Any!, ValueType : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md) |

Provides results for AppSearch batch operations which encompass multiple documents.

Individual results of a batch operation are separated into two maps: one for successes and one for failures. For successes, [getSuccesses()](../android/app/appsearch/AppSearchBatchResult.md))will return a map of keys to instances of the value type. For failures, [getFailures()](../android/app/appsearch/AppSearchBatchResult.md))will return a map of keys to [AppSearchResult](../android/app/appsearch/AppSearchResult.md) objects.

Alternatively, [getAll()](../android/app/appsearch/AppSearchBatchResult.md))returns a map of keys to [AppSearchResult](../android/app/appsearch/AppSearchResult.md) objects for both successes and failures.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/app/appsearch/AppSearchBatchResult.Builder.md) Builder for [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md) objects. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType, [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\<ValueType\>!\> | [getAll](../android/app/appsearch/AppSearchBatchResult.md))`()` Returns a [Map](../java/util/Map.md) of keys mapped to instances of [AppSearchResult](../android/app/appsearch/AppSearchResult.md) for all individual results. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType, [AppSearchResult](../android/app/appsearch/AppSearchResult.md)\<ValueType\>!\> | [getFailures](../android/app/appsearch/AppSearchBatchResult.md))`()` Returns a [Map](../java/util/Map.md) of keys mapped to instances of [AppSearchResult](../android/app/appsearch/AppSearchResult.md) for all failed individual results. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType,ValueType\> | [getSuccesses](../android/app/appsearch/AppSearchBatchResult.md))`()` Returns a [Map](../java/util/Map.md) of keys mapped to instances of the value type for all successful individual results. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSuccess](../android/app/appsearch/AppSearchBatchResult.md))`()` Returns`true`if this [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md) has no failures. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/app/appsearch/AppSearchBatchResult.md))`()` Returns a string representation of the object. |

## Public methods

### getAll

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAll(): MutableMap<KeyType, AppSearchResult<ValueType>!>
```

Returns a [Map](../java/util/Map.md) of keys mapped to instances of [AppSearchResult](../android/app/appsearch/AppSearchResult.md) for all individual results.

The values of the [Map](../java/util/Map.md) will not be`null`. 

### getFailures

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFailures(): MutableMap<KeyType, AppSearchResult<ValueType>!>
```

Returns a [Map](../java/util/Map.md) of keys mapped to instances of [AppSearchResult](../android/app/appsearch/AppSearchResult.md) for all failed individual results.

The values of the [Map](../java/util/Map.md) will not be`null`. 

### getSuccesses

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuccesses(): MutableMap<KeyType, ValueType>
```

Returns a [Map](../java/util/Map.md) of keys mapped to instances of the value type for all successful individual results.

Example: [AppSearchSession.getByDocumentId](../android/app/appsearch/AppSearchSession.md))returns an [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md). Each key (the document ID, of`String`type) will map to a [GenericDocument](../android/app/appsearch/GenericDocument.md) object.

The values of the [Map](../java/util/Map.md) will not be`null`. 

### isSuccess

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSuccess(): Boolean
```

Returns`true`if this [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md) has no failures. 

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |
