# DrmManagerClient

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmManagerClient

Kotlin | [Java](DrmManagerClient.md) 
| --- | --- |

```
open class DrmManagerClient : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmManagerClient](DrmManagerClient.md) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android.media/MediaDrm.md)

The main programming interface for the DRM framework. An application must instantiate this class to access DRM agents through the DRM framework.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnErrorListener](../android/drm/DrmManagerClient.OnErrorListener.md) Interface definition for a callback that receives information about DRM framework errors. |
| abstract | [OnEventListener](../android/drm/DrmManagerClient.OnEventListener.md) Interface definition for a callback that receives information about DRM processing events. |
| abstract | [OnInfoListener](../android/drm/DrmManagerClient.OnInfoListener.md) Interface definition for a callback that receives status messages and warnings during registration and rights acquisition. |
| --- | --- |

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NONE](DrmManagerClient.md) Indicates that a request was successful or that no error occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](DrmManagerClient.md) Indicates that an error occurred and the reason is not known. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmManagerClient](DrmManagerClient.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Creates a `DrmManagerClient`. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [DrmInfo](DrmInfo.md)! | [acquireDrmInfo](DrmManagerClient.md))`(`drmInfoRequest:` ` [DrmInfoRequest](DrmInfoRequest.md)!`)` Retrieves information for registering, unregistering, or acquiring rights. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [acquireRights](DrmManagerClient.md))`(`drmInfoRequest:` ` [DrmInfoRequest](DrmInfoRequest.md)!`)` Processes a given [DrmInfoRequest](DrmInfoRequest.md) and returns the rights information asynchronously. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canHandle](DrmManagerClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks whether the given MIME type or URI can be handled. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canHandle](DrmManagerClient.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks whether the given MIME type or path can be handled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkRightsStatus](DrmManagerClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`)` Check whether the given content has valid rights. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkRightsStatus](DrmManagerClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks whether the given rights-protected content has valid rights for the specified [DrmStore.Action](../android/drm/DrmStore.Action.md). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkRightsStatus](DrmManagerClient.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks whether the given content has valid rights. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkRightsStatus](DrmManagerClient.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks whether the given rights-protected content has valid rights for the specified [DrmStore.Action](../android/drm/DrmStore.Action.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](DrmManagerClient.md))`()` Releases resources associated with the current session of DrmManagerClient. |
| --- | --- |
| open [DrmConvertedStatus](DrmConvertedStatus.md)! | [closeConvertSession](DrmManagerClient.md))`(`convertId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Informs the DRM plug-in (agent) that there is no more data to convert or that an error has occurred. |
| open [DrmConvertedStatus](DrmConvertedStatus.md)! | [convertData](DrmManagerClient.md))`(`convertId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Converts the input data (content) that is part of a rights-protected file. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableDrmEngines](DrmManagerClient.md))`()` Retrieves information about all the DRM plug-ins (agents) that are registered with the DRM framework. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [DrmSupportInfo](DrmSupportInfo.md)!\> | [getAvailableDrmSupportInfo](DrmManagerClient.md))`()` Retrieves information about all the DRM plug-ins (agents) that are registered with the DRM framework. |
| open [ContentValues](../android.content/ContentValues.md)! | [getConstraints](DrmManagerClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves constraint information for rights-protected content. |
| open [ContentValues](../android.content/ContentValues.md)! | [getConstraints](DrmManagerClient.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves constraint information for rights-protected content. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDrmObjectType](DrmManagerClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the type of rights-protected object (for example, content object, rights object, and so on) using the specified URI or MIME type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDrmObjectType](DrmManagerClient.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the type of rights-protected object (for example, content object, rights object, and so on) using the specified path or MIME type. |
| open [ContentValues](../android.content/ContentValues.md)! | [getMetadata](DrmManagerClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`)` Retrieves metadata information for rights-protected content. |
| --- | --- |
| open [ContentValues](../android.content/ContentValues.md)! | [getMetadata](DrmManagerClient.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves metadata information for rights-protected content. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOriginalMimeType](DrmManagerClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`)` Retrieves the MIME type embedded in the original content. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOriginalMimeType](DrmManagerClient.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the MIME type embedded in the original content. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [openConvertSession](DrmManagerClient.md))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Initiates a new conversion session. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [processDrmInfo](DrmManagerClient.md))`(`drmInfo:` ` [DrmInfo](DrmInfo.md)!`)` Processes the given DRM information based on the information type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](DrmManagerClient.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [removeAllRights](DrmManagerClient.md))`()` Removes all the rights information of every DRM plug-in (agent) associated with the DRM framework. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [removeRights](DrmManagerClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`)` Removes the rights associated with the given rights-protected content. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [removeRights](DrmManagerClient.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes the rights associated with the given rights-protected content. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveRights](DrmManagerClient.md))`(`drmRights:` ` [DrmRights](DrmRights.md)!`, `rightsPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `contentPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Saves rights to a specified path and associates that path with the content path. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnErrorListener](DrmManagerClient.md))`(`errorListener:` ` [DrmManagerClient.OnErrorListener](../android/drm/DrmManagerClient.OnErrorListener.md)!`)` Registers an [DrmManagerClient.OnErrorListener](../android/drm/DrmManagerClient.OnErrorListener.md) callback, which is invoked when the DRM framework sends error information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnEventListener](DrmManagerClient.md))`(`eventListener:` ` [DrmManagerClient.OnEventListener](../android/drm/DrmManagerClient.OnEventListener.md)!`)` Registers an [DrmManagerClient.OnEventListener](../android/drm/DrmManagerClient.OnEventListener.md) callback, which is invoked when the DRM framework sends information about DRM processing. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnInfoListener](DrmManagerClient.md))`(`infoListener:` ` [DrmManagerClient.OnInfoListener](../android/drm/DrmManagerClient.OnInfoListener.md)!`)` Registers an [DrmManagerClient.OnInfoListener](../android/drm/DrmManagerClient.OnInfoListener.md) callback, which is invoked when the DRM framework sends status or warning information during registration or rights acquisition. |

| Protected methods ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](DrmManagerClient.md))`()` <br /> |

## Constants

### ERROR_NONE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NONE: Int
```

**Deprecated:** *Deprecated in Java.*

Indicates that a request was successful or that no error occurred. 

 Value: 0

### ERROR_UNKNOWN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN: Int
```

**Deprecated:** *Deprecated in Java.*

Indicates that an error occurred and the reason is not known. 

 Value: -2000

## Public constructors

### DrmManagerClient

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmManagerClient(context: Context!)
```

Creates a `DrmManagerClient`.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: Context of the caller. |

## Public methods

### acquireDrmInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquireDrmInfo(drmInfoRequest: DrmInfoRequest!): DrmInfo!
```

**Deprecated:** *Deprecated in Java.*

Retrieves information for registering, unregistering, or acquiring rights.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `drmInfoRequest` | [DrmInfoRequest](DrmInfoRequest.md)!: The [DrmInfoRequest](DrmInfoRequest.md) that specifies the type of DRM information being retrieved. |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [DrmInfo](DrmInfo.md)! | A [DrmInfo](DrmInfo.md) instance. |

### acquireRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquireRights(drmInfoRequest: DrmInfoRequest!): Int
```

**Deprecated:** *Deprecated in Java.*

Processes a given [DrmInfoRequest](DrmInfoRequest.md) and returns the rights information asynchronously.

This is a utility method that consists of an [acquireDrmInfo()](DrmManagerClient.md)) and a [processDrmInfo()](DrmManagerClient.md)) method call. This utility method can be used only if the selected DRM plug-in (agent) supports this sequence of calls. Some DRM agents, such as OMA, do not support this utility method, in which case an application must invoke [acquireDrmInfo()](DrmManagerClient.md)) and [processDrmInfo()](DrmManagerClient.md)) separately.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `drmInfoRequest` | [DrmInfoRequest](DrmInfoRequest.md)!: The [DrmInfoRequest](DrmInfoRequest.md) used to acquire the rights. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | ERROR_NONE for success; ERROR_UNKNOWN for failure. |

### canHandle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canHandle(
    uri: Uri!, 
    mimeType: String!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether the given MIME type or URI can be handled.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!: URI for the content to be handled. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: MIME type of the object to be handled |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the given MIME type or URI can be handled; false if they cannot be handled. |

### canHandle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canHandle(
    path: String!, 
    mimeType: String!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether the given MIME type or path can be handled.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path of the content to be handled. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: MIME type of the object to be handled. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the given MIME type or path can be handled; false if they cannot be handled. |

### checkRightsStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRightsStatus(uri: Uri!): Int
```

**Deprecated:** *Deprecated in Java.*

Check whether the given content has valid rights.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!: URI of the rights-protected content. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` representing the [DrmStore.RightsStatus](../android/drm/DrmStore.RightsStatus.md) of the content. |

### checkRightsStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRightsStatus(
    uri: Uri!, 
    action: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Checks whether the given rights-protected content has valid rights for the specified [DrmStore.Action](../android/drm/DrmStore.Action.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!: URI for the rights-protected content. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The [DrmStore.Action](../android/drm/DrmStore.Action.md) to perform. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` representing the [DrmStore.RightsStatus](../android/drm/DrmStore.RightsStatus.md) of the content. |

### checkRightsStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRightsStatus(path: String!): Int
```

**Deprecated:** *Deprecated in Java.*

Checks whether the given content has valid rights.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path to the rights-protected content. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` representing the [DrmStore.RightsStatus](../android/drm/DrmStore.RightsStatus.md) of the content. |

### checkRightsStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRightsStatus(
    path: String!, 
    action: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Checks whether the given rights-protected content has valid rights for the specified [DrmStore.Action](../android/drm/DrmStore.Action.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path to the rights-protected content. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The [DrmStore.Action](../android/drm/DrmStore.Action.md) to perform. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` representing the [DrmStore.RightsStatus](../android/drm/DrmStore.RightsStatus.md) of the content. |

### close

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

**Deprecated:** *Deprecated in Java.*

Releases resources associated with the current session of DrmManagerClient. It is considered good practice to call this method when the [DrmManagerClient](DrmManagerClient.md) object is no longer needed in your application. After this method is called, [DrmManagerClient](DrmManagerClient.md) is no longer usable since it has lost all of its required resource. This method was added in API 24. In API versions 16 through 23, release() should be called instead. There is no need to do anything for API versions prior to 16.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### closeConvertSession

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeConvertSession(convertId: Int): DrmConvertedStatus!
```

**Deprecated:** *Deprecated in Java.*

Informs the DRM plug-in (agent) that there is no more data to convert or that an error has occurred. Upon successful conversion of the data, the DRM agent will provide an offset value indicating where the header and body signature should be added. Appending the signature is necessary to protect the integrity of the converted file.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------|
| `convertId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Handle for the conversion session. |

| Return ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DrmConvertedStatus](DrmConvertedStatus.md)! | A [DrmConvertedStatus](DrmConvertedStatus.md) object that contains the status of the data conversion, the converted data, and the offset for the header and body signature. |

### convertData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun convertData(
    convertId: Int, 
    inputData: ByteArray!
): DrmConvertedStatus!
```

**Deprecated:** *Deprecated in Java.*

Converts the input data (content) that is part of a rights-protected file. The converted data and status is returned in a [DrmConvertedStatus](DrmConvertedStatus.md) object. This method should be called each time there is a new block of data received by the application.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `convertId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Handle for the conversion session. |
| `inputData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Input data that needs to be converted. |

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DrmConvertedStatus](DrmConvertedStatus.md)! | A [DrmConvertedStatus](DrmConvertedStatus.md) object that contains the status of the data conversion, the converted data, and offset for the header and body signature. An application can ignore the offset because it is only relevant to the [closeConvertSession()](DrmManagerClient.md)) method. |

### getAvailableDrmEngines

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAvailableDrmEngines(): Array<String!>!
```

**Deprecated:** *Deprecated in Java.*

Retrieves information about all the DRM plug-ins (agents) that are registered with the DRM framework.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | A `String` array of DRM plug-in descriptions. |

### getAvailableDrmSupportInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAvailableDrmSupportInfo(): MutableCollection<DrmSupportInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieves information about all the DRM plug-ins (agents) that are registered with the DRM framework.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [DrmSupportInfo](DrmSupportInfo.md)!> | List of all the DRM plug-ins (agents) that are registered with the DRM framework. This value cannot be `null`. |

### getConstraints

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConstraints(
    uri: Uri!, 
    action: Int
): ContentValues!
```

**Deprecated:** *Deprecated in Java.*

Retrieves constraint information for rights-protected content.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!: URI for the content from which you are retrieving DRM constraints. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action defined in [DrmStore.Action](../android/drm/DrmStore.Action.md). |

| Return ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentValues](../android.content/ContentValues.md)! | A [android.content.ContentValues](../android.content/ContentValues.md) instance that contains key-value pairs representing the constraints. Null in case of failure. |

### getConstraints

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConstraints(
    path: String!, 
    action: Int
): ContentValues!
```

**Deprecated:** *Deprecated in Java.*

Retrieves constraint information for rights-protected content.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path to the content from which you are retrieving DRM constraints. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action defined in [DrmStore.Action](../android/drm/DrmStore.Action.md). |

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentValues](../android.content/ContentValues.md)! | A [android.content.ContentValues](../android.content/ContentValues.md) instance that contains key-value pairs representing the constraints. Null in case of failure. The keys are defined in [DrmStore.ConstraintsColumns](../android/drm/DrmStore.ConstraintsColumns.md). |

### getDrmObjectType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDrmObjectType(
    uri: Uri!, 
    mimeType: String!
): Int
```

**Deprecated:** *Deprecated in Java.*

Retrieves the type of rights-protected object (for example, content object, rights object, and so on) using the specified URI or MIME type. At least one parameter must be specified to retrieve the DRM object type.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!: URI for the content or null. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: MIME type of the content or null. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` that corresponds to a [DrmStore.DrmObjectType](../android/drm/DrmStore.DrmObjectType.md). |

### getDrmObjectType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDrmObjectType(
    path: String!, 
    mimeType: String!
): Int
```

**Deprecated:** *Deprecated in Java.*

Retrieves the type of rights-protected object (for example, content object, rights object, and so on) using the specified path or MIME type. At least one parameter must be specified to retrieve the DRM object type.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path to the content or null. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: MIME type of the content or null. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` that corresponds to a [DrmStore.DrmObjectType](../android/drm/DrmStore.DrmObjectType.md). |

### getMetadata

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetadata(uri: Uri!): ContentValues!
```

**Deprecated:** *Deprecated in Java.*

Retrieves metadata information for rights-protected content.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!: URI for the content from which you are retrieving metadata information. |

| Return ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentValues](../android.content/ContentValues.md)! | A [android.content.ContentValues](../android.content/ContentValues.md) instance that contains key-value pairs representing the constraints. Null in case of failure. |

### getMetadata

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetadata(path: String!): ContentValues!
```

**Deprecated:** *Deprecated in Java.*

Retrieves metadata information for rights-protected content.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path to the content from which you are retrieving metadata information. |

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentValues](../android.content/ContentValues.md)! | A [android.content.ContentValues](../android.content/ContentValues.md) instance that contains key-value pairs representing the metadata. Null in case of failure. |

### getOriginalMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOriginalMimeType(uri: Uri!): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the MIME type embedded in the original content.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!: URI of the rights-protected content. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | MIME type of the original content, such as `video/mpeg`. |

### getOriginalMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOriginalMimeType(path: String!): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the MIME type embedded in the original content.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path to the rights-protected content. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The MIME type of the original content, such as `video/mpeg`. |

### openConvertSession

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openConvertSession(mimeType: String!): Int
```

**Deprecated:** *Deprecated in Java.*

Initiates a new conversion session. An application must initiate a conversion session with this method each time it downloads a rights-protected file that needs to be converted.

This method applies only to forward-locking (copy protection) DRM schemes.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: MIME type of the input data packet. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A convert ID that is used used to maintain the conversion session. |

### processDrmInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun processDrmInfo(drmInfo: DrmInfo!): Int
```

**Deprecated:** *Deprecated in Java.*

Processes the given DRM information based on the information type.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `drmInfo` | [DrmInfo](DrmInfo.md)!: The [DrmInfo](DrmInfo.md) to be processed. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | ERROR_NONE for success; ERROR_UNKNOWN for failure. |

### release

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

**Deprecated:** *replaced by [close()](DrmManagerClient.md)).* 

### removeAllRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAllRights(): Int
```

**Deprecated:** *Deprecated in Java.*

Removes all the rights information of every DRM plug-in (agent) associated with the DRM framework.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | ERROR_NONE for success; ERROR_UNKNOWN for failure. |

### removeRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeRights(uri: Uri!): Int
```

**Deprecated:** *Deprecated in Java.*

Removes the rights associated with the given rights-protected content.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!: URI for the rights-protected content. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | ERROR_NONE for success; ERROR_UNKNOWN for failure. |

### removeRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeRights(path: String!): Int
```

**Deprecated:** *Deprecated in Java.*

Removes the rights associated with the given rights-protected content.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path to the rights-protected content. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | ERROR_NONE for success; ERROR_UNKNOWN for failure. |

### saveRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveRights(
    drmRights: DrmRights!, 
    rightsPath: String!, 
    contentPath: String!
): Int
```

**Deprecated:** *Deprecated in Java.*

Saves rights to a specified path and associates that path with the content path.

**Note:** For OMA or WM-DRM, `rightsPath` and `contentPath` can be null.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `drmRights` | [DrmRights](DrmRights.md)!: The [DrmRights](DrmRights.md) to be saved. |
| `rightsPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: File path where rights will be saved. |
| `contentPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: File path where content is saved. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | ERROR_NONE for success; ERROR_UNKNOWN for failure. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------|
| `java.io.IOException` | If the call failed to save rights information at the given `rightsPath`. |

### setOnErrorListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnErrorListener(errorListener: DrmManagerClient.OnErrorListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an [DrmManagerClient.OnErrorListener](../android/drm/DrmManagerClient.OnErrorListener.md) callback, which is invoked when the DRM framework sends error information.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorListener` | [DrmManagerClient.OnErrorListener](../android/drm/DrmManagerClient.OnErrorListener.md)!: Interface definition for the callback. |

### setOnEventListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnEventListener(eventListener: DrmManagerClient.OnEventListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an [DrmManagerClient.OnEventListener](../android/drm/DrmManagerClient.OnEventListener.md) callback, which is invoked when the DRM framework sends information about DRM processing.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eventListener` | [DrmManagerClient.OnEventListener](../android/drm/DrmManagerClient.OnEventListener.md)!: Interface definition for the callback. |

### setOnInfoListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnInfoListener(infoListener: DrmManagerClient.OnInfoListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an [DrmManagerClient.OnInfoListener](../android/drm/DrmManagerClient.OnInfoListener.md) callback, which is invoked when the DRM framework sends status or warning information during registration or rights acquisition.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `infoListener` | [DrmManagerClient.OnInfoListener](../android/drm/DrmManagerClient.OnInfoListener.md)!: Interface definition for the callback. |

## Protected methods

### finalize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|---------------------------------------|
| `java.lang.Throwable` | the `Exception` raised by this method |
