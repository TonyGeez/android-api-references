# JoinCustomAudienceRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# JoinCustomAudienceRequest

Kotlin| [Java](https://developer.android.com/reference/android/adservices/customaudience/JoinCustomAudienceRequest "View this page in Java") 

```
open class JoinCustomAudienceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.customaudience.JoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#) |

The request object to join a custom audience.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest.Builder) Builder for [JoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#) objects. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks whether two [JoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#) objects contain the same information. |
| open [CustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience) | [getCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#getCustomAudience())`()` Returns the custom audience to join. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#hashCode())`()` Returns the hash of the [JoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#) object's data. |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Checks whether two [JoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#) objects contain the same information.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCustomAudience

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getCustomAudience(): CustomAudience
```

Returns the custom audience to join.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [CustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience) | This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash of the [JoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/JoinCustomAudienceRequest#) object's data.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
