# GetTopicsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# GetTopicsResponse

Kotlin| [Java](GetTopicsResponse.md) 
| --- | --- |

```
class GetTopicsResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.topics.GetTopicsResponse](GetTopicsResponse.md) |

Represent the result from the getTopics API.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/topics/GetTopicsResponse.Builder.md) Builder for [GetTopicsResponse](GetTopicsResponse.md) objects. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](GetTopicsResponse.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EncryptedTopic](EncryptedTopic.md)!\> | [getEncryptedTopics](GetTopicsResponse.md))`()` Returns a [List](../java.util/List.md) of [EncryptedTopic](EncryptedTopic.md) objects returned by getTopics API. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Topic](Topic.md)!\> | [getTopics](GetTopicsResponse.md))`()` Returns a [List](../java.util/List.md) of [Topic](Topic.md) objects returned by getTopics API. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](GetTopicsResponse.md))`()` <br /> |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getEncryptedTopics

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 11](https://developer.android.com/sdkExtensions) 

```
fun getEncryptedTopics(): MutableList<EncryptedTopic!>
```

Returns a [List](../java.util/List.md) of [EncryptedTopic](EncryptedTopic.md) objects returned by getTopics API.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [EncryptedTopic](EncryptedTopic.md)!> | This value cannot be`null`. |

### getTopics

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getTopics(): MutableList<Topic!>
```

Returns a [List](../java.util/List.md) of [Topic](Topic.md) objects returned by getTopics API.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Topic](Topic.md)!> | This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
