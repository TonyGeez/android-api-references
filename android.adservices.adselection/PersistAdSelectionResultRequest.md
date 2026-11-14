# PersistAdSelectionResultRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# PersistAdSelectionResultRequest

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/PersistAdSelectionResultRequest "View this page in Java") 
| --- | --- |

```
class PersistAdSelectionResultRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.PersistAdSelectionResultRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#) |

Represents a request containing the seller, the ad selection data id and data.

Instances of this class are created by SDKs to be provided as arguments to the [android.adservices.adselection.AdSelectionManager#persistAdSelectionResult](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#persistAdSelectionResult(android.adservices.adselection.PersistAdSelectionResultRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))methods in [AdSelectionManager](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest.Builder) Builder for [PersistAdSelectionResultRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#) objects. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionDataId](https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#getAdSelectionDataId())`()` Returns the id that identifies the [android.adservices.adselection.AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))payload that generated this result. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionId](https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#getAdSelectionId())`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAdSelectionResult](https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#getAdSelectionResult())`()` <br /> |
| --- | --- |
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)? | [getSeller](https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#getSeller())`()` <br /> |

## Public methods

### getAdSelectionDataId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getAdSelectionDataId(): Long
```

Returns the id that identifies the [android.adservices.adselection.AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))payload that generated this result. 

### getAdSelectionId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdSelectionId(): Long
```

**Deprecated:** *Use the [getAdSelectionDataId()](https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#getAdSelectionDataId())instead, the underlying value is enforced to be the same.*

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | an ad selection id. |

### getAdSelectionResult

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getAdSelectionResult(): ByteArray?
```

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | an ad selection result. This value may be`null`. |

### getSeller

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getSeller(): AdTechIdentifier?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)? | a seller. This value may be`null`. |
