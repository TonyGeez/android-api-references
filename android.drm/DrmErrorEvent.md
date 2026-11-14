# DrmErrorEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmErrorEvent

Kotlin| [Java](DrmErrorEvent.md) 
| --- | --- |

```
open class DrmErrorEvent : DrmEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.drm.DrmEvent](DrmEvent.md) ||
| | ↳ | [android.drm.DrmErrorEvent](DrmErrorEvent.md) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android.media/MediaDrm.md)

An entity class that is passed to the [onError()](../android/drm/DrmManagerClient.OnErrorListener.md))callback.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ACQUIRE_DRM_INFO_FAILED](DrmErrorEvent.md) Failed to acquire [DrmInfo](DrmInfo.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NOT_SUPPORTED](DrmErrorEvent.md) Response from the server cannot be handled by the DRM plug-in (agent). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_INTERNET_CONNECTION](DrmErrorEvent.md) An Internet connection is not available and no attempt can be made to renew rights. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OUT_OF_MEMORY](DrmErrorEvent.md) Memory allocation failed during renewal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_PROCESS_DRM_INFO_FAILED](DrmErrorEvent.md) Failed to process [DrmInfo](DrmInfo.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOVE_ALL_RIGHTS_FAILED](DrmErrorEvent.md) Failed to remove all the rights objects associated with all DRM schemes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_NOT_INSTALLED](DrmErrorEvent.md) Something went wrong installing the rights. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_RENEWAL_NOT_ALLOWED](DrmErrorEvent.md) The server rejected the renewal of rights. |

| Inherited constants ||
|---|---|
| From class [DrmEvent](DrmEvent.md) |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_OBJECT](DrmEvent.md) <br /> The key that is used in the`attributes`HashMap to pass the [DrmInfo](DrmInfo.md) object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_STATUS_OBJECT](DrmEvent.md) <br /> The key that is used in the`attributes`HashMap to pass the return status. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALL_RIGHTS_REMOVED](DrmEvent.md) <br /> All of the rights information associated with all DRM schemes have been successfully removed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DRM_INFO_PROCESSED](DrmEvent.md) <br /> The given DRM information has been successfully processed. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmErrorEvent](DrmErrorEvent.md))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmErrorEvent`object with the specified parameters. |
| [DrmErrorEvent](DrmErrorEvent.md))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [HashMap](../java.util/HashMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Creates a`DrmErrorEvent`object with the specified parameters. |

| Inherited functions ||
|---|---|
| From class [DrmEvent](DrmEvent.md) |-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](DrmEvent.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the attribute associated with the specified key. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessage](DrmEvent.md))`()` <br /> Retrieves the message description associated with this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](DrmEvent.md))`()` <br /> Retrieves the type of information that is associated with this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](DrmEvent.md))`()` <br /> Retrieves the unique session identifier associated with this object. <br /> | ||

## Constants

### TYPE_ACQUIRE_DRM_INFO_FAILED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ACQUIRE_DRM_INFO_FAILED: Int
```

**Deprecated:** *Deprecated in Java.*

Failed to acquire [DrmInfo](DrmInfo.md). This error event is sent when an [acquireDrmInfo()](DrmManagerClient.md))call fails. 

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

Failed to process [DrmInfo](DrmInfo.md). This error event is sent when a [processDrmInfo()](DrmManagerClient.md))call fails. 

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
| `attributes` | [HashMap](../java.util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:Attributes for extensible information. Could be any information provided by the plug-in. It can be null. |
