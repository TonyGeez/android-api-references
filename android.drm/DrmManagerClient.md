# DrmManagerClient

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmManagerClient

Kotlin | [Java](https://developer.android.com/reference/android/drm/DrmManagerClient "View this page in Java") 
| --- | --- |

```
open class DrmManagerClient : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

The main programming interface for the DRM framework. An application must instantiate this class to access DRM agents through the DRM framework.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnErrorListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener) Interface definition for a callback that receives information about DRM framework errors. |
| abstract | [OnEventListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnEventListener) Interface definition for a callback that receives information about DRM processing events. |
| abstract | [OnInfoListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener) Interface definition for a callback that receives status messages and warnings during registration and rights acquisition. |
| --- | --- |

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NONE](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#ERROR_NONE:kotlin.Int) Indicates that a request was successful or that no error occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#ERROR_UNKNOWN:kotlin.Int) Indicates that an error occurred and the reason is not known. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#DrmManagerClient(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Creates a `DrmManagerClient`. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo)! | [acquireDrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#acquireDrmInfo(android.drm.DrmInfoRequest))`(`drmInfoRequest:` ` [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest)!`)` Retrieves information for registering, unregistering, or acquiring rights. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [acquireRights](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#acquireRights(android.drm.DrmInfoRequest))`(`drmInfoRequest:` ` [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest)!`)` Processes a given [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest) and returns the rights information asynchronously. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canHandle](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#canHandle(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks whether the given MIME type or URI can be handled. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canHandle](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#canHandle(kotlin.String,%20kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks whether the given MIME type or path can be handled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkRightsStatus](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#checkRightsStatus(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Check whether the given content has valid rights. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkRightsStatus](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#checkRightsStatus(android.net.Uri,%20kotlin.Int))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks whether the given rights-protected content has valid rights for the specified [DrmStore.Action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkRightsStatus](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#checkRightsStatus(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks whether the given content has valid rights. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkRightsStatus](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#checkRightsStatus(kotlin.String,%20kotlin.Int))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks whether the given rights-protected content has valid rights for the specified [DrmStore.Action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#close())`()` Releases resources associated with the current session of DrmManagerClient. |
| --- | --- |
| open [DrmConvertedStatus](https://developer.android.com/reference/kotlin/android/drm/DrmConvertedStatus)! | [closeConvertSession](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#closeConvertSession(kotlin.Int))`(`convertId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Informs the DRM plug-in (agent) that there is no more data to convert or that an error has occurred. |
| open [DrmConvertedStatus](https://developer.android.com/reference/kotlin/android/drm/DrmConvertedStatus)! | [convertData](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#convertData(kotlin.Int,%20kotlin.ByteArray))`(`convertId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Converts the input data (content) that is part of a rights-protected file. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableDrmEngines](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getAvailableDrmEngines())`()` Retrieves information about all the DRM plug-ins (agents) that are registered with the DRM framework. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [DrmSupportInfo](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo)!\> | [getAvailableDrmSupportInfo](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getAvailableDrmSupportInfo())`()` Retrieves information about all the DRM plug-ins (agents) that are registered with the DRM framework. |
| open [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)! | [getConstraints](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getConstraints(android.net.Uri,%20kotlin.Int))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves constraint information for rights-protected content. |
| open [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)! | [getConstraints](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getConstraints(kotlin.String,%20kotlin.Int))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves constraint information for rights-protected content. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDrmObjectType](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getDrmObjectType(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the type of rights-protected object (for example, content object, rights object, and so on) using the specified URI or MIME type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDrmObjectType](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getDrmObjectType(kotlin.String,%20kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the type of rights-protected object (for example, content object, rights object, and so on) using the specified path or MIME type. |
| open [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)! | [getMetadata](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getMetadata(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Retrieves metadata information for rights-protected content. |
| --- | --- |
| open [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)! | [getMetadata](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getMetadata(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves metadata information for rights-protected content. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOriginalMimeType](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getOriginalMimeType(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Retrieves the MIME type embedded in the original content. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOriginalMimeType](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#getOriginalMimeType(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the MIME type embedded in the original content. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [openConvertSession](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#openConvertSession(kotlin.String))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Initiates a new conversion session. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [processDrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo))`(`drmInfo:` ` [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo)!`)` Processes the given DRM information based on the information type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#release())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [removeAllRights](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#removeAllRights())`()` Removes all the rights information of every DRM plug-in (agent) associated with the DRM framework. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [removeRights](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#removeRights(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Removes the rights associated with the given rights-protected content. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [removeRights](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#removeRights(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes the rights associated with the given rights-protected content. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveRights](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#saveRights(android.drm.DrmRights,%20kotlin.String,%20kotlin.String))`(`drmRights:` ` [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights)!`, `rightsPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `contentPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Saves rights to a specified path and associates that path with the content path. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnErrorListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#setOnErrorListener(android.drm.DrmManagerClient.OnErrorListener))`(`errorListener:` ` [DrmManagerClient.OnErrorListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener)!`)` Registers an [DrmManagerClient.OnErrorListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener) callback, which is invoked when the DRM framework sends error information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnEventListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#setOnEventListener(android.drm.DrmManagerClient.OnEventListener))`(`eventListener:` ` [DrmManagerClient.OnEventListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnEventListener)!`)` Registers an [DrmManagerClient.OnEventListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnEventListener) callback, which is invoked when the DRM framework sends information about DRM processing. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnInfoListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#setOnInfoListener(android.drm.DrmManagerClient.OnInfoListener))`(`infoListener:` ` [DrmManagerClient.OnInfoListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener)!`)` Registers an [DrmManagerClient.OnInfoListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener) callback, which is invoked when the DRM framework sends status or warning information during registration or rights acquisition. |

| Protected methods ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#finalize())`()` <br /> |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Context of the caller. |

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
| `drmInfoRequest` | [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest)!: The [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest) that specifies the type of DRM information being retrieved. |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo)! | A [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo) instance. |

### acquireRights

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquireRights(drmInfoRequest: DrmInfoRequest!): Int
```

**Deprecated:** *Deprecated in Java.*

Processes a given [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest) and returns the rights information asynchronously.

This is a utility method that consists of an [acquireDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#acquireDrmInfo(android.drm.DrmInfoRequest)) and a [processDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo)) method call. This utility method can be used only if the selected DRM plug-in (agent) supports this sequence of calls. Some DRM agents, such as OMA, do not support this utility method, in which case an application must invoke [acquireDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#acquireDrmInfo(android.drm.DrmInfoRequest)) and [processDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo)) separately.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `drmInfoRequest` | [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest)!: The [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest) used to acquire the rights. |

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: URI for the content to be handled. |
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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: URI of the rights-protected content. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` representing the [DrmStore.RightsStatus](https://developer.android.com/reference/kotlin/android/drm/DrmStore.RightsStatus) of the content. |

### checkRightsStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRightsStatus(
    uri: Uri!, 
    action: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Checks whether the given rights-protected content has valid rights for the specified [DrmStore.Action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: URI for the rights-protected content. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The [DrmStore.Action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action) to perform. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` representing the [DrmStore.RightsStatus](https://developer.android.com/reference/kotlin/android/drm/DrmStore.RightsStatus) of the content. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` representing the [DrmStore.RightsStatus](https://developer.android.com/reference/kotlin/android/drm/DrmStore.RightsStatus) of the content. |

### checkRightsStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRightsStatus(
    path: String!, 
    action: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Checks whether the given rights-protected content has valid rights for the specified [DrmStore.Action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Path to the rights-protected content. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The [DrmStore.Action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action) to perform. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` representing the [DrmStore.RightsStatus](https://developer.android.com/reference/kotlin/android/drm/DrmStore.RightsStatus) of the content. |

### close

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

**Deprecated:** *Deprecated in Java.*

Releases resources associated with the current session of DrmManagerClient. It is considered good practice to call this method when the [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#) object is no longer needed in your application. After this method is called, [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#) is no longer usable since it has lost all of its required resource. This method was added in API 24. In API versions 16 through 23, release() should be called instead. There is no need to do anything for API versions prior to 16.

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
| [DrmConvertedStatus](https://developer.android.com/reference/kotlin/android/drm/DrmConvertedStatus)! | A [DrmConvertedStatus](https://developer.android.com/reference/kotlin/android/drm/DrmConvertedStatus) object that contains the status of the data conversion, the converted data, and the offset for the header and body signature. |

### convertData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun convertData(
    convertId: Int, 
    inputData: ByteArray!
): DrmConvertedStatus!
```

**Deprecated:** *Deprecated in Java.*

Converts the input data (content) that is part of a rights-protected file. The converted data and status is returned in a [DrmConvertedStatus](https://developer.android.com/reference/kotlin/android/drm/DrmConvertedStatus) object. This method should be called each time there is a new block of data received by the application.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `convertId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Handle for the conversion session. |
| `inputData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Input data that needs to be converted. |

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DrmConvertedStatus](https://developer.android.com/reference/kotlin/android/drm/DrmConvertedStatus)! | A [DrmConvertedStatus](https://developer.android.com/reference/kotlin/android/drm/DrmConvertedStatus) object that contains the status of the data conversion, the converted data, and offset for the header and body signature. An application can ignore the offset because it is only relevant to the [closeConvertSession()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#closeConvertSession(kotlin.Int)) method. |

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
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [DrmSupportInfo](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo)!> | List of all the DRM plug-ins (agents) that are registered with the DRM framework. This value cannot be `null`. |

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: URI for the content from which you are retrieving DRM constraints. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action defined in [DrmStore.Action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action). |

| Return ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)! | A [android.content.ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#) instance that contains key-value pairs representing the constraints. Null in case of failure. |

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
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action defined in [DrmStore.Action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action). |

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)! | A [android.content.ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#) instance that contains key-value pairs representing the constraints. Null in case of failure. The keys are defined in [DrmStore.ConstraintsColumns](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns). |

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: URI for the content or null. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: MIME type of the content or null. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` that corresponds to a [DrmStore.DrmObjectType](https://developer.android.com/reference/kotlin/android/drm/DrmStore.DrmObjectType). |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An `int` that corresponds to a [DrmStore.DrmObjectType](https://developer.android.com/reference/kotlin/android/drm/DrmStore.DrmObjectType). |

### getMetadata

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetadata(uri: Uri!): ContentValues!
```

**Deprecated:** *Deprecated in Java.*

Retrieves metadata information for rights-protected content.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: URI for the content from which you are retrieving metadata information. |

| Return ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)! | A [android.content.ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#) instance that contains key-value pairs representing the constraints. Null in case of failure. |

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
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)! | A [android.content.ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#) instance that contains key-value pairs representing the metadata. Null in case of failure. |

### getOriginalMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOriginalMimeType(uri: Uri!): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the MIME type embedded in the original content.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: URI of the rights-protected content. |

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
| `drmInfo` | [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo)!: The [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo) to be processed. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | ERROR_NONE for success; ERROR_UNKNOWN for failure. |

### release

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

**Deprecated:** *replaced by [close()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#close()).* 

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: URI for the rights-protected content. |

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
| `drmRights` | [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights)!: The [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights) to be saved. |
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

Registers an [DrmManagerClient.OnErrorListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener) callback, which is invoked when the DRM framework sends error information.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorListener` | [DrmManagerClient.OnErrorListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener)!: Interface definition for the callback. |

### setOnEventListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnEventListener(eventListener: DrmManagerClient.OnEventListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an [DrmManagerClient.OnEventListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnEventListener) callback, which is invoked when the DRM framework sends information about DRM processing.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eventListener` | [DrmManagerClient.OnEventListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnEventListener)!: Interface definition for the callback. |

### setOnInfoListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnInfoListener(infoListener: DrmManagerClient.OnInfoListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an [DrmManagerClient.OnInfoListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener) callback, which is invoked when the DRM framework sends status or warning information during registration or rights acquisition.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `infoListener` | [DrmManagerClient.OnInfoListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener)!: Interface definition for the callback. |

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
