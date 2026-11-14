# InsertRecordsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InsertRecordsResponse

Kotlin| [Java](InsertRecordsResponse.md) 
| --- | --- |

```
open class InsertRecordsResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.InsertRecordsResponse](InsertRecordsResponse.md) |

Response for [HealthConnectManager.insertRecords](HealthConnectManager.md)). The response contains records in same order as records in [HealthConnectManager.insertRecords](HealthConnectManager.md))

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Record](../android.health.connect.datatypes/Record.md)!\> | [getRecords](InsertRecordsResponse.md))`()` <br /> |

## Public methods

### getRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecords(): MutableList<Record!>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Record](../android.health.connect.datatypes/Record.md)!> | This value cannot be`null`. |
