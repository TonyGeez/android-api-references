# CacheResponse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CacheResponse

```
abstract class CacheResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.CacheResponse](CacheResponse.md) |

| Known Direct Subclasses [SecureCacheResponse](SecureCacheResponse.md) |----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [SecureCacheResponse](SecureCacheResponse.md) | Represents a cache response originally retrieved through secure means, such as TLS. | |
| --- | --- | --- | --- | --- | --- | --- |

Represent channels for retrieving resources from the ResponseCache. Instances of such a class provide an InputStream that returns the entity body, and also a getHeaders() method which returns the associated response headers.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [CacheResponse](CacheResponse.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [InputStream](../java.io/InputStream.md)! | [getBody](CacheResponse.md))`()` Returns the response body as an InputStream. |
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | [getHeaders](CacheResponse.md))`()` Returns the response headers as a Map. |

## Public constructors

### CacheResponse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CacheResponse()
```

## Public methods

### getBody

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBody(): InputStream!
```

Returns the response body as an InputStream.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [InputStream](../java.io/InputStream.md)! | an InputStream from which the response body can be accessed |

| Exceptions ||
|-----------------------|--------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while getting the response body |

### getHeaders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHeaders(): MutableMap<String!, MutableList<String!>!>!
```

Returns the response headers as a Map.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | An immutable Map from response header field names to lists of field values. The status line has null as its field name. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while getting the response headers |
