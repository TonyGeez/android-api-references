# GetTopicsRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# GetTopicsRequest

Kotlin| [Java](https://developer.android.com/reference/android/adservices/topics/GetTopicsRequest "View this page in Java") 

```
class GetTopicsRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.topics.GetTopicsRequest](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsRequest#) |

Get Topics Request.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsRequest.Builder) Builder for [GetTopicsRequest](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsRequest#) objects. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getAdsSdkName](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsRequest#getAdsSdkName())`()` Get the Sdk Name. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldRecordObservation](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsRequest#shouldRecordObservation())`()` Get Record Observation. |

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
