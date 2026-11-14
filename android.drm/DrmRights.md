# DrmRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmRights

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmRights "View this page in Java") 
| --- | --- |

```
open class DrmRights
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

An entity class that wraps the license information retrieved from the online DRM server.

A caller can instantiate a [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights#) object by first invoking the [DrmManagerClient.processDrmInfo(DrmInfo)](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo))method and then using the resulting [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData) object to invoke the [DrmRights.DrmRights(ProcessedData, String)](https://developer.android.com/reference/kotlin/android/drm/DrmRights#DrmRights(android.drm.ProcessedData,%20kotlin.String))constructor.

A caller can also instantiate a [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights#) object by using the [DrmRights.DrmRights(String, String)](https://developer.android.com/reference/kotlin/android/drm/DrmRights#DrmRights(kotlin.String,%20kotlin.String))constructor, which takes a path to a file containing rights information instead of a`ProcessedData`.

Please note that the account id and subscription id is not mandatory by all DRM agents or plugins. When account id or subscription id is not required by the specific DRM agent or plugin, they can be either null, or an empty string, or any other don't-care string value.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights#DrmRights(android.drm.ProcessedData,%20kotlin.String))`(`data:` ` [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmRights`object with the given parameters. |
| [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights#DrmRights(java.io.File,%20kotlin.String))`(`rightsFile:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmRights`object with the given parameters. |
| [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights#DrmRights(kotlin.String,%20kotlin.String))`(`rightsFilePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmRights`object with the given parameters. |
| [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights#DrmRights(kotlin.String,%20kotlin.String,%20kotlin.String))`(`rightsFilePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmRights`object with the given parameters. |
| [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights#DrmRights(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`rightsFilePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `subscriptionId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmRights`object with the given parameters. |

| Public methods ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAccountId](https://developer.android.com/reference/kotlin/android/drm/DrmRights#getAccountId())`()` Retrieves the account ID associated with this`DrmRights`object. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getData](https://developer.android.com/reference/kotlin/android/drm/DrmRights#getData())`()` Retrieves the rights data associated with this`DrmRights`object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMimeType](https://developer.android.com/reference/kotlin/android/drm/DrmRights#getMimeType())`()` Retrieves the MIME type associated with this`DrmRights`object. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubscriptionId](https://developer.android.com/reference/kotlin/android/drm/DrmRights#getSubscriptionId())`()` Retrieves the subscription ID associated with this`DrmRights`object. |

## Public constructors

### DrmRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmRights(
    data: ProcessedData!, 
    mimeType: String!)
```

Creates a`DrmRights`object with the given parameters.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData)!:A [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData) object containing rights information. Must not be null. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The MIME type. It must not be null or an empty string. |

### DrmRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmRights(
    rightsFile: File!, 
    mimeType: String!)
```

Creates a`DrmRights`object with the given parameters.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `rightsFile` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:File containing rights information. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:MIME type. Must not be null or an empty string. |

### DrmRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmRights(
    rightsFilePath: String!, 
    mimeType: String!)
```

Creates a`DrmRights`object with the given parameters.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `rightsFilePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Path to the file containing rights information. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:MIME type. Must not be null or an empty string. |

### DrmRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmRights(
    rightsFilePath: String!, 
    mimeType: String!, 
    accountId: String!)
```

Creates a`DrmRights`object with the given parameters.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `rightsFilePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Path to the file containing rights information. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:MIME type. Must not be null or an empty string. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Account ID of the user. |
| --- | --- |

### DrmRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmRights(
    rightsFilePath: String!, 
    mimeType: String!, 
    accountId: String!, 
    subscriptionId: String!)
```

Creates a`DrmRights`object with the given parameters.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `rightsFilePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Path to the file containing rights information. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:MIME type. Must not be null or an empty string. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Account ID of the user. |
| --- | --- |
| `subscriptionId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Subscription ID of the user. |

## Public methods

### getAccountId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAccountId(): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the account ID associated with this`DrmRights`object.

| Return ||
|-----------------------------------------------------------------------------------|-----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The account ID. |

### getData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getData(): ByteArray!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the rights data associated with this`DrmRights`object.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | A`byte`array representing the rights data. |

### getMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMimeType(): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the MIME type associated with this`DrmRights`object.

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The MIME type. |

### getSubscriptionId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubscriptionId(): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the subscription ID associated with this`DrmRights`object.

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The subscription ID. |
