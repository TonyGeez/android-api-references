# GetTopicsRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# GetTopicsRequest

Kotlin| [Java](../android/adservices/topics/GetTopicsRequest.md) 
| --- | --- |

```
class GetTopicsRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.topics.GetTopicsRequest](../android/adservices/topics/GetTopicsRequest.md) |

Get Topics Request.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/topics/GetTopicsRequest.Builder.md) Builder for [GetTopicsRequest](../android/adservices/topics/GetTopicsRequest.md) objects. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getAdsSdkName](../android/adservices/topics/GetTopicsRequest.md))`()` Get the Sdk Name. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldRecordObservation](../android/adservices/topics/GetTopicsRequest.md))`()` Get Record Observation. |

## Public methods

### getAdsSdkName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getAdsSdkName(): String
```

Get the Sdk Name.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### shouldRecordObservation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 

```
fun shouldRecordObservation(): Boolean
```

Get Record Observation.
