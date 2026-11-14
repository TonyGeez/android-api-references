# ReadRecordsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadRecordsResponse

Kotlin| [Java](../android/health/connect/ReadRecordsResponse.md) 
| --- | --- |

```
open class ReadRecordsResponse<T : Record!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.ReadRecordsResponse](../android/health/connect/ReadRecordsResponse.md) |

Response containing list of Records for [HealthConnectManager.readRecords](../android/health/connect/HealthConnectManager.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNextPageToken](../android/health/connect/ReadRecordsResponse.md))`()` Returns a page token to read the next page of the result. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [getRecords](../android/health/connect/ReadRecordsResponse.md))`()` <br /> |

## Public methods

### getNextPageToken

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNextPageToken(): Long
```

Returns a page token to read the next page of the result. -1 if there are no more pages available. 

### getRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecords(): MutableList<T>
```

| Return ||
|------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | This value cannot be`null`. |
