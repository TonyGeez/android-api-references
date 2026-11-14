# ReadMedicalResourcesPageRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# ReadMedicalResourcesPageRequest

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/ReadMedicalResourcesPageRequest "View this page in Java") 
| --- | --- |

```
class ReadMedicalResourcesPageRequest : ReadMedicalResourcesRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.health.connect.ReadMedicalResourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesRequest) ||
| | ↳ | [android.health.connect.ReadMedicalResourcesPageRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest#) |

A page read request with specified`pageToken`for android.health.connect.HealthConnectManager#readMedicalResources.

When making a new initial request with new filters, use [ReadMedicalResourcesInitialRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesInitialRequest).

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
| | [Builder](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest.Builder) Builder class for [ReadMedicalResourcesPageRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest#). |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPageToken](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest#getPageToken())`()` Returns the page token to read the requested page. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest#hashCode())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest#toString())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ReadMedicalResourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesRequest) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageSize](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesRequest#getPageSize())`()` <br /> Returns maximum number of`MedicalResource`s to be returned by the read operation if set, 1000 otherwise. <br /> | ||

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
