# ReadMedicalResourcesRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# ReadMedicalResourcesRequest

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/ReadMedicalResourcesRequest "View this page in Java") 
| --- | --- |

```
abstract class ReadMedicalResourcesRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.ReadMedicalResourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesRequest#) |

| Known Direct Subclasses [ReadMedicalResourcesInitialRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesInitialRequest), [ReadMedicalResourcesPageRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest) |------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------| | [ReadMedicalResourcesInitialRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesInitialRequest) | An initial read request with specified filters for android. | | [ReadMedicalResourcesPageRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest) | A page read request with specified`pageToken`for android. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A base class to represent a read request for android.health.connect.HealthConnectManager#readMedicalResources.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageSize](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesRequest#getPageSize())`()` Returns maximum number of`MedicalResource`s to be returned by the read operation if set, 1000 otherwise. |

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
