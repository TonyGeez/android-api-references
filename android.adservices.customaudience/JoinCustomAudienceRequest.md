# JoinCustomAudienceRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# JoinCustomAudienceRequest

Kotlin| [Java](../android/adservices/customaudience/JoinCustomAudienceRequest.md) 
| --- | --- |

```
open class JoinCustomAudienceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.JoinCustomAudienceRequest](../android/adservices/customaudience/JoinCustomAudienceRequest.md) |

The request object to join a custom audience.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/customaudience/JoinCustomAudienceRequest.Builder.md) Builder for [JoinCustomAudienceRequest](../android/adservices/customaudience/JoinCustomAudienceRequest.md) objects. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/adservices/customaudience/JoinCustomAudienceRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks whether two [JoinCustomAudienceRequest](../android/adservices/customaudience/JoinCustomAudienceRequest.md) objects contain the same information. |
| open [CustomAudience](../android/adservices/customaudience/CustomAudience.md) | [getCustomAudience](../android/adservices/customaudience/JoinCustomAudienceRequest.md))`()` Returns the custom audience to join. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/adservices/customaudience/JoinCustomAudienceRequest.md))`()` Returns the hash of the [JoinCustomAudienceRequest](../android/adservices/customaudience/JoinCustomAudienceRequest.md) object's data. |
| --- | --- |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Checks whether two [JoinCustomAudienceRequest](../android/adservices/customaudience/JoinCustomAudienceRequest.md) objects contain the same information.

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
| [CustomAudience](../android/adservices/customaudience/CustomAudience.md) | This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash of the [JoinCustomAudienceRequest](../android/adservices/customaudience/JoinCustomAudienceRequest.md) object's data.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
