# NetworkStats

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkStats

Kotlin| [Java](https://developer.android.com/reference/android/app/usage/NetworkStats "View this page in Java") 

```
class NetworkStats : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.usage.NetworkStats](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats#) |

Class providing enumeration over buckets of network usage statistics. [NetworkStats](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats#) objects are returned as results to various queries in [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager).

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Bucket](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats.Bucket) Buckets are the smallest elements of a query result. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats#close())`()` Closes the enumeration. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getNextBucket](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats#getNextBucket(android.app.usage.NetworkStats.Bucket))`(`bucketOut:` ` [NetworkStats.Bucket](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats.Bucket)?`)` Fills the recycled bucket with data of the next bin in the enumeration. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNextBucket](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats#hasNextBucket())`()` Check if it is possible to ask for a next bucket in the enumeration. |

| Protected methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats#finalize())`()` <br /> |

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
| `bucketOut` | [NetworkStats.Bucket](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStats.Bucket)?:Bucket to be filled with data. If null, the method does nothing and returning false. |

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
