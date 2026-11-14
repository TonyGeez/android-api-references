# CacheRequest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CacheRequest

```
abstract class CacheRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.CacheRequest](https://developer.android.com/reference/kotlin/java/net/CacheRequest#) |

Represents channels for storing resources in the ResponseCache. Instances of such a class provide an OutputStream object which is called by protocol handlers to store the resource data into the cache, and also an abort() method which allows a cache store operation to be interrupted and abandoned. If an IOException is encountered while reading the response or writing to the cache, the current cache store operation will be aborted.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------|---|
| [CacheRequest](https://developer.android.com/reference/kotlin/java/net/CacheRequest#CacheRequest())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abort](https://developer.android.com/reference/kotlin/java/net/CacheRequest#abort())`()` Aborts the attempt to cache the response. |
| abstract [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [getBody](https://developer.android.com/reference/kotlin/java/net/CacheRequest#getBody())`()` Returns an OutputStream to which the response body can be written. |

## Public constructors

### CacheRequest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CacheRequest()
```

## Public methods

### abort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun abort(): Unit
```

Aborts the attempt to cache the response. If an IOException is encountered while reading the response or writing to the cache, the current cache store operation will be abandoned. 

### getBody

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBody(): OutputStream!
```

Returns an OutputStream to which the response body can be written.

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | an OutputStream to which the response body can be written |

| Exceptions ||
|-----------------------|--------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while writing the response body |
