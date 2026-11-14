# DrmErrorEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmErrorEvent

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmErrorEvent "View this page in Java") 
| --- | --- |

```
open class DrmErrorEvent : DrmEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.drm.DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) ||
| | ↳ | [android.drm.DrmErrorEvent](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

An entity class that is passed to the [onError()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener#onError(android.drm.DrmManagerClient,%20android.drm.DrmErrorEvent))callback.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ACQUIRE_DRM_INFO_FAILED](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#TYPE_ACQUIRE_DRM_INFO_FAILED:kotlin.Int) Failed to acquire [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#TYPE_NOT_SUPPORTED:kotlin.Int) Response from the server cannot be handled by the DRM plug-in (agent). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_INTERNET_CONNECTION](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#TYPE_NO_INTERNET_CONNECTION:kotlin.Int) An Internet connection is not available and no attempt can be made to renew rights. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OUT_OF_MEMORY](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#TYPE_OUT_OF_MEMORY:kotlin.Int) Memory allocation failed during renewal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_PROCESS_DRM_INFO_FAILED](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#TYPE_PROCESS_DRM_INFO_FAILED:kotlin.Int) Failed to process [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOVE_ALL_RIGHTS_FAILED](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#TYPE_REMOVE_ALL_RIGHTS_FAILED:kotlin.Int) Failed to remove all the rights objects associated with all DRM schemes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_NOT_INSTALLED](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#TYPE_RIGHTS_NOT_INSTALLED:kotlin.Int) Something went wrong installing the rights. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_RENEWAL_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#TYPE_RIGHTS_RENEWAL_NOT_ALLOWED:kotlin.Int) The server rejected the renewal of rights. |

| Inherited constants ||
|---|---|
| From class [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_OBJECT](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#DRM_INFO_OBJECT:kotlin.String) <br /> The key that is used in the`attributes`HashMap to pass the [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo) object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_STATUS_OBJECT](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#DRM_INFO_STATUS_OBJECT:kotlin.String) <br /> The key that is used in the`attributes`HashMap to pass the return status. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALL_RIGHTS_REMOVED](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#TYPE_ALL_RIGHTS_REMOVED:kotlin.Int) <br /> All of the rights information associated with all DRM schemes have been successfully removed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DRM_INFO_PROCESSED](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#TYPE_DRM_INFO_PROCESSED:kotlin.Int) <br /> The given DRM information has been successfully processed. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmErrorEvent](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#DrmErrorEvent(kotlin.Int,%20kotlin.Int,%20kotlin.String))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmErrorEvent`object with the specified parameters. |
| [DrmErrorEvent](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent#DrmErrorEvent(kotlin.Int,%20kotlin.Int,%20kotlin.String,%20java.util.HashMap))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Creates a`DrmErrorEvent`object with the specified parameters. |

| Inherited functions ||
|---|---|
| From class [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) |-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#getAttribute(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the attribute associated with the specified key. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessage](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#getMessage())`()` <br /> Retrieves the message description associated with this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#getType())`()` <br /> Retrieves the type of information that is associated with this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#getUniqueId())`()` <br /> Retrieves the unique session identifier associated with this object. <br /> | ||

## Constants

### TYPE_ACQUIRE_DRM_INFO_FAILED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ACQUIRE_DRM_INFO_FAILED: Int
```

**Deprecated:** *Deprecated in Java.*

Failed to acquire [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo). This error event is sent when an [acquireDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#acquireDrmInfo(android.drm.DrmInfoRequest))call fails. 

 Value: 2008

### TYPE_NOT_SUPPORTED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NOT_SUPPORTED: Int
```

**Deprecated:** *Deprecated in Java.*

Response from the server cannot be handled by the DRM plug-in (agent). 

 Value: 2003

### TYPE_NO_INTERNET_CONNECTION

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NO_INTERNET_CONNECTION: Int
```

**Deprecated:** *Deprecated in Java.*

An Internet connection is not available and no attempt can be made to renew rights. 

 Value: 2005

### TYPE_OUT_OF_MEMORY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OUT_OF_MEMORY: Int
```

**Deprecated:** *Deprecated in Java.*

Memory allocation failed during renewal. Can in the future perhaps be used to trigger garbage collector. 

 Value: 2004

### TYPE_PROCESS_DRM_INFO_FAILED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_PROCESS_DRM_INFO_FAILED: Int
```

**Deprecated:** *Deprecated in Java.*

Failed to process [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo). This error event is sent when a [processDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo))call fails. 

 Value: 2006

### TYPE_REMOVE_ALL_RIGHTS_FAILED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOVE_ALL_RIGHTS_FAILED: Int
```

**Deprecated:** *Deprecated in Java.*

Failed to remove all the rights objects associated with all DRM schemes. 

 Value: 2007

### TYPE_RIGHTS_NOT_INSTALLED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RIGHTS_NOT_INSTALLED: Int
```

**Deprecated:** *Deprecated in Java.*

Something went wrong installing the rights. 

 Value: 2001

### TYPE_RIGHTS_RENEWAL_NOT_ALLOWED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RIGHTS_RENEWAL_NOT_ALLOWED: Int
```

**Deprecated:** *Deprecated in Java.*

The server rejected the renewal of rights. 

 Value: 2002

## Public constructors

### DrmErrorEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmErrorEvent(
    uniqueId: Int, 
    type: Int, 
    message: String!)
```

Creates a`DrmErrorEvent`object with the specified parameters.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `uniqueId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique session identifier. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of the event. Must be any of the event types defined above. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Message description. It can be null. |
| --- | --- |

### DrmErrorEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmErrorEvent(
    uniqueId: Int, 
    type: Int, 
    message: String!, 
    attributes: HashMap<String!, Any!>!)
```

Creates a`DrmErrorEvent`object with the specified parameters.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniqueId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique session identifier. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of the event. Must be any of the event types defined above. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Message description. |
| --- | --- |
| `attributes` | [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:Attributes for extensible information. Could be any information provided by the plug-in. It can be null. |
