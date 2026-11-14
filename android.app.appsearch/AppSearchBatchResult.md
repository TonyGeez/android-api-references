# AppSearchBatchResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchBatchResult

Kotlin| [Java](AppSearchBatchResult.md) 
| --- | --- |

```
class AppSearchBatchResult<KeyType : Any!, ValueType : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.AppSearchBatchResult](AppSearchBatchResult.md) |

Provides results for AppSearch batch operations which encompass multiple documents.

Individual results of a batch operation are separated into two maps: one for successes and one for failures. For successes, [getSuccesses()](AppSearchBatchResult.md))will return a map of keys to instances of the value type. For failures, [getFailures()](AppSearchBatchResult.md))will return a map of keys to [AppSearchResult](AppSearchResult.md) objects.

Alternatively, [getAll()](AppSearchBatchResult.md))returns a map of keys to [AppSearchResult](AppSearchResult.md) objects for both successes and failures.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/app/appsearch/AppSearchBatchResult.Builder.md) Builder for [AppSearchBatchResult](AppSearchBatchResult.md) objects. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType, [AppSearchResult](AppSearchResult.md)\<ValueType\>!\> | [getAll](AppSearchBatchResult.md))`()` Returns a [Map](../java.util/Map.md) of keys mapped to instances of [AppSearchResult](AppSearchResult.md) for all individual results. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType, [AppSearchResult](AppSearchResult.md)\<ValueType\>!\> | [getFailures](AppSearchBatchResult.md))`()` Returns a [Map](../java.util/Map.md) of keys mapped to instances of [AppSearchResult](AppSearchResult.md) for all failed individual results. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<KeyType,ValueType\> | [getSuccesses](AppSearchBatchResult.md))`()` Returns a [Map](../java.util/Map.md) of keys mapped to instances of the value type for all successful individual results. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSuccess](AppSearchBatchResult.md))`()` Returns`true`if this [AppSearchBatchResult](AppSearchBatchResult.md) has no failures. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AppSearchBatchResult.md))`()` Returns a string representation of the object. |

## Public methods

### getAll

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAll(): MutableMap<KeyType, AppSearchResult<ValueType>!>
```

Returns a [Map](../java.util/Map.md) of keys mapped to instances of [AppSearchResult](AppSearchResult.md) for all individual results.

The values of the [Map](../java.util/Map.md) will not be`null`. 

### getFailures

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFailures(): MutableMap<KeyType, AppSearchResult<ValueType>!>
```

Returns a [Map](../java.util/Map.md) of keys mapped to instances of [AppSearchResult](AppSearchResult.md) for all failed individual results.

The values of the [Map](../java.util/Map.md) will not be`null`. 

### getSuccesses

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuccesses(): MutableMap<KeyType, ValueType>
```

Returns a [Map](../java.util/Map.md) of keys mapped to instances of the value type for all successful individual results.

Example: [AppSearchSession.getByDocumentId](AppSearchSession.md))returns an [AppSearchBatchResult](AppSearchBatchResult.md). Each key (the document ID, of`String`type) will map to a [GenericDocument](GenericDocument.md) object.

The values of the [Map](../java.util/Map.md) will not be`null`. 

### isSuccess

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSuccess(): Boolean
```

Returns`true`if this [AppSearchBatchResult](AppSearchBatchResult.md) has no failures. 

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |
