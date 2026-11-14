# GetTopicsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# GetTopicsResponse

Kotlin| [Java](https://developer.android.com/reference/android/adservices/topics/GetTopicsResponse "View this page in Java") 
| --- | --- |

```
class GetTopicsResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.topics.GetTopicsResponse](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse#) |

Represent the result from the getTopics API.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse.Builder) Builder for [GetTopicsResponse](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse#) objects. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EncryptedTopic](https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic)!\> | [getEncryptedTopics](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse#getEncryptedTopics())`()` Returns a [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [EncryptedTopic](https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic) objects returned by getTopics API. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Topic](https://developer.android.com/reference/kotlin/android/adservices/topics/Topic)!\> | [getTopics](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse#getTopics())`()` Returns a [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [Topic](https://developer.android.com/reference/kotlin/android/adservices/topics/Topic) objects returned by getTopics API. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse#hashCode())`()` <br /> |

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

Returns a [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [EncryptedTopic](https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic) objects returned by getTopics API.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [EncryptedTopic](https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic)!> | This value cannot be`null`. |

### getTopics

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getTopics(): MutableList<Topic!>
```

Returns a [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [Topic](https://developer.android.com/reference/kotlin/android/adservices/topics/Topic) objects returned by getTopics API.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Topic](https://developer.android.com/reference/kotlin/android/adservices/topics/Topic)!> | This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
