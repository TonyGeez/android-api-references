# HeaderBlock

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# HeaderBlock

Kotlin| [Java](HeaderBlock.md) 
| --- | --- |

```
abstract class HeaderBlock
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.HeaderBlock](HeaderBlock.md) |

Unmodifiable container of headers or trailers.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [HeaderBlock](HeaderBlock.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | [getAsList](HeaderBlock.md))`()` Returns an unmodifiable list of the header field and value pairs. |
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | [getAsMap](HeaderBlock.md))`()` Returns an unmodifiable map from header field names to lists of values. |

## Public constructors

### HeaderBlock

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
HeaderBlock()
```

## Public methods

### getAsList

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getAsList(): MutableList<MutableEntry<String!, String!>!>
```

Returns an unmodifiable list of the header field and value pairs. For response, the headers are in the same order they are received over the wire. For request, the headers are in the same order they are added.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!> | an unmodifiable list of header field and value pairs This value cannot be`null`. |

### getAsMap

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getAsMap(): MutableMap<String!, MutableList<String!>!>
```

Returns an unmodifiable map from header field names to lists of values. Order of each list of values for a single header field is: For response, the same order they were received over the wire. For request, the same order they were added. The iteration order of keys is unspecified.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!> | an unmodifiable map from header field names to lists of values This value cannot be`null`. |
