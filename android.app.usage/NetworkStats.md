# NetworkStats

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkStats

Kotlin| [Java](NetworkStats.md) 
| --- | --- |

```
class NetworkStats : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.NetworkStats](NetworkStats.md) |

Class providing enumeration over buckets of network usage statistics. [NetworkStats](NetworkStats.md) objects are returned as results to various queries in [NetworkStatsManager](NetworkStatsManager.md).

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Bucket](../android/app/usage/NetworkStats.Bucket.md) Buckets are the smallest elements of a query result. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](NetworkStats.md))`()` Closes the enumeration. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getNextBucket](NetworkStats.md))`(`bucketOut:` ` [NetworkStats.Bucket](../android/app/usage/NetworkStats.Bucket.md)?`)` Fills the recycled bucket with data of the next bin in the enumeration. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNextBucket](NetworkStats.md))`()` Check if it is possible to ask for a next bucket in the enumeration. |
| --- | --- |

| Protected methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](NetworkStats.md))`()` <br /> |

## Public methods

### close

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Closes the enumeration. Call this method before this object gets out of scope.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### getNextBucket

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNextBucket(bucketOut: NetworkStats.Bucket?): Boolean
```

Fills the recycled bucket with data of the next bin in the enumeration.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bucketOut` | [NetworkStats.Bucket](../android/app/usage/NetworkStats.Bucket.md)?:Bucket to be filled with data. If null, the method does nothing and returning false. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if successfully filled the bucket, false otherwise. |

### hasNextBucket

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasNextBucket(): Boolean
```

Check if it is possible to ask for a next bucket in the enumeration.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there is at least one more bucket. |

## Protected methods

### finalize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
