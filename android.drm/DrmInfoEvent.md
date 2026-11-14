# DrmInfoEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInfoEvent

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmInfoEvent "View this page in Java") 

```
open class DrmInfoEvent : DrmEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.drm.DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) ||
| | ↳ | [android.drm.DrmInfoEvent](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

An entity class that is passed to the [onInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener#onInfo(android.drm.DrmManagerClient,%20android.drm.DrmInfoEvent))callback.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ACCOUNT_ALREADY_REGISTERED](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#TYPE_ACCOUNT_ALREADY_REGISTERED:kotlin.Int) The registration has already been done for the given account. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALREADY_REGISTERED_BY_ANOTHER_ACCOUNT](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#TYPE_ALREADY_REGISTERED_BY_ANOTHER_ACCOUNT:kotlin.Int) The registration has already been done by another account ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOVE_RIGHTS](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#TYPE_REMOVE_RIGHTS:kotlin.Int) The rights need to be removed completely. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_INSTALLED](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#TYPE_RIGHTS_INSTALLED:kotlin.Int) The rights have been successfully downloaded and installed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_REMOVED](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#TYPE_RIGHTS_REMOVED:kotlin.Int) The rights have been removed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WAIT_FOR_RIGHTS](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#TYPE_WAIT_FOR_RIGHTS:kotlin.Int) The rights object is being delivered to the device. |

| Inherited constants ||
|---|---|
| From class [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_OBJECT](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#DRM_INFO_OBJECT:kotlin.String) <br /> The key that is used in the`attributes`HashMap to pass the [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo) object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_STATUS_OBJECT](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#DRM_INFO_STATUS_OBJECT:kotlin.String) <br /> The key that is used in the`attributes`HashMap to pass the return status. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALL_RIGHTS_REMOVED](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#TYPE_ALL_RIGHTS_REMOVED:kotlin.Int) <br /> All of the rights information associated with all DRM schemes have been successfully removed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DRM_INFO_PROCESSED](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#TYPE_DRM_INFO_PROCESSED:kotlin.Int) <br /> The given DRM information has been successfully processed. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmInfoEvent](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#DrmInfoEvent(kotlin.Int,%20kotlin.Int,%20kotlin.String))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfoEvent`object with the specified parameters. |
| [DrmInfoEvent](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent#DrmInfoEvent(kotlin.Int,%20kotlin.Int,%20kotlin.String,%20java.util.HashMap))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Creates a`DrmInfoEvent`object with the specified parameters. |

| Inherited functions ||
|---|---|
| From class [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) |-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#getAttribute(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the attribute associated with the specified key. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessage](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#getMessage())`()` <br /> Retrieves the message description associated with this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#getType())`()` <br /> Retrieves the type of information that is associated with this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](https://developer.android.com/reference/kotlin/android/drm/DrmEvent#getUniqueId())`()` <br /> Retrieves the unique session identifier associated with this object. <br /> | ||

## Constants

### TYPE_ACCOUNT_ALREADY_REGISTERED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ACCOUNT_ALREADY_REGISTERED: Int
```

**Deprecated:** *Deprecated in Java.*

The registration has already been done for the given account. 

 Value: 5

### TYPE_ALREADY_REGISTERED_BY_ANOTHER_ACCOUNT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ALREADY_REGISTERED_BY_ANOTHER_ACCOUNT: Int
```

**Deprecated:** *Deprecated in Java.*

The registration has already been done by another account ID. 

 Value: 1

### TYPE_REMOVE_RIGHTS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOVE_RIGHTS: Int
```

**Deprecated:** *Deprecated in Java.*

The rights need to be removed completely. 

 Value: 2

### TYPE_RIGHTS_INSTALLED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RIGHTS_INSTALLED: Int
```

**Deprecated:** *Deprecated in Java.*

The rights have been successfully downloaded and installed. 

 Value: 3

### TYPE_RIGHTS_REMOVED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RIGHTS_REMOVED: Int
```

**Deprecated:** *Deprecated in Java.*

The rights have been removed. 

 Value: 6

### TYPE_WAIT_FOR_RIGHTS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WAIT_FOR_RIGHTS: Int
```

**Deprecated:** *Deprecated in Java.*

The rights object is being delivered to the device. You must wait before calling [acquireRights()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#acquireRights(android.drm.DrmInfoRequest))again. 

 Value: 4

## Public constructors

### DrmInfoEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmInfoEvent(
    uniqueId: Int, 
    type: Int, 
    message: String!)
```

Creates a`DrmInfoEvent`object with the specified parameters.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniqueId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique session identifier. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of the event. Must be any of the event types defined above, or the constants defined in [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent). |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Message description. It can be null. |

### DrmInfoEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmInfoEvent(
    uniqueId: Int, 
    type: Int, 
    message: String!, 
    attributes: HashMap<String!, Any!>!)
```

Creates a`DrmInfoEvent`object with the specified parameters.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniqueId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique session identifier. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of the event. Must be any of the event types defined above, or the constants defined in [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Message description. It can be null. |
| `attributes` | [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:Attributes for extensible information. Could be any information provided by the plug-in. |
