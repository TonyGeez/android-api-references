# PersistAdSelectionResultRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# PersistAdSelectionResultRequest

Kotlin| [Java](PersistAdSelectionResultRequest.md) 
| --- | --- |

```
class PersistAdSelectionResultRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.PersistAdSelectionResultRequest](PersistAdSelectionResultRequest.md) |

Represents a request containing the seller, the ad selection data id and data.

Instances of this class are created by SDKs to be provided as arguments to the [android.adservices.adselection.AdSelectionManager#persistAdSelectionResult](AdSelectionManager.md))methods in [AdSelectionManager](AdSelectionManager.md).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/adselection/PersistAdSelectionResultRequest.Builder.md) Builder for [PersistAdSelectionResultRequest](PersistAdSelectionResultRequest.md) objects. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionDataId](PersistAdSelectionResultRequest.md))`()` Returns the id that identifies the [android.adservices.adselection.AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](AdSelectionManager.md))payload that generated this result. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionId](PersistAdSelectionResultRequest.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAdSelectionResult](PersistAdSelectionResultRequest.md))`()` <br /> |
| --- | --- |
| [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md)? | [getSeller](PersistAdSelectionResultRequest.md))`()` <br /> |

## Public methods

### getAdSelectionDataId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getAdSelectionDataId(): Long
```

Returns the id that identifies the [android.adservices.adselection.AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](AdSelectionManager.md))payload that generated this result. 

### getAdSelectionId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdSelectionId(): Long
```

**Deprecated:** *Use the [getAdSelectionDataId()](PersistAdSelectionResultRequest.md))instead, the underlying value is enforced to be the same.*

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
| [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md)? | a seller. This value may be`null`. |
