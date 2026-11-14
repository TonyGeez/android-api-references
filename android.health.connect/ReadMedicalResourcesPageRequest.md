# ReadMedicalResourcesPageRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# ReadMedicalResourcesPageRequest

Kotlin| [Java](ReadMedicalResourcesPageRequest.md) 
| --- | --- |

```
class ReadMedicalResourcesPageRequest : ReadMedicalResourcesRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.health.connect.ReadMedicalResourcesRequest](ReadMedicalResourcesRequest.md) ||
| | ↳ | [android.health.connect.ReadMedicalResourcesPageRequest](ReadMedicalResourcesPageRequest.md) |

A page read request with specified`pageToken`for android.health.connect.HealthConnectManager#readMedicalResources.

When making a new initial request with new filters, use [ReadMedicalResourcesInitialRequest](ReadMedicalResourcesInitialRequest.md).

Example usage: 

```kotlin
<code>ReadMedicalResourcesInitialRequest initialRequest
      = new ReadMedicalResourcesInitialRequest.Builder(...).build();
  ReadMedicalResourcesResponse response = makeRequest(initialRequest);
  String pageToken = response.getNextPageToken();
 
  while (pageToken != null) {
      ReadMedicalResourcesPageRequest pageRequest = new ReadMedicalResourcesPageRequest(pageToken);
      response = makeRequest(pageRequest);
      pageToken = response.getNextPageToken();
  }
  </code>
```

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/ReadMedicalResourcesPageRequest.Builder.md) Builder class for [ReadMedicalResourcesPageRequest](ReadMedicalResourcesPageRequest.md). |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ReadMedicalResourcesPageRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPageToken](ReadMedicalResourcesPageRequest.md))`()` Returns the page token to read the requested page. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](ReadMedicalResourcesPageRequest.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ReadMedicalResourcesPageRequest.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ReadMedicalResourcesRequest](ReadMedicalResourcesRequest.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageSize](ReadMedicalResourcesRequest.md))`()` <br /> Returns maximum number of`MedicalResource`s to be returned by the read operation if set, 1000 otherwise. <br /> | ||

## Public methods

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getPageToken

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getPageToken(): String
```

Returns the page token to read the requested page.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
