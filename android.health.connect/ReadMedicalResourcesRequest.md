# ReadMedicalResourcesRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# ReadMedicalResourcesRequest

Kotlin| [Java](ReadMedicalResourcesRequest.md) 
| --- | --- |

```
abstract class ReadMedicalResourcesRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.ReadMedicalResourcesRequest](ReadMedicalResourcesRequest.md) |

| Known Direct Subclasses [ReadMedicalResourcesInitialRequest](ReadMedicalResourcesInitialRequest.md), [ReadMedicalResourcesPageRequest](ReadMedicalResourcesPageRequest.md) |------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------| | [ReadMedicalResourcesInitialRequest](ReadMedicalResourcesInitialRequest.md) | An initial read request with specified filters for android. | | [ReadMedicalResourcesPageRequest](ReadMedicalResourcesPageRequest.md) | A page read request with specified`pageToken`for android. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A base class to represent a read request for android.health.connect.HealthConnectManager#readMedicalResources.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageSize](ReadMedicalResourcesRequest.md))`()` Returns maximum number of`MedicalResource`s to be returned by the read operation if set, 1000 otherwise. |

## Public methods

### getPageSize

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
open fun getPageSize(): Int
```

Returns maximum number of`MedicalResource`s to be returned by the read operation if set, 1000 otherwise.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between android.health.connect.Constants#MINIMUM_PAGE_SIZE and android.health.connect.Constants#MAXIMUM_PAGE_SIZE inclusive |
