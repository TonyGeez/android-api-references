# DrmInfoEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInfoEvent

Kotlin| [Java](../android/drm/DrmInfoEvent.md) 
| --- | --- |

```
open class DrmInfoEvent : DrmEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.drm.DrmEvent](../android/drm/DrmEvent.md) ||
| | ↳ | [android.drm.DrmInfoEvent](../android/drm/DrmInfoEvent.md) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android/media/MediaDrm.md)

An entity class that is passed to the [onInfo()](../android/drm/DrmManagerClient.OnInfoListener.md))callback.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ACCOUNT_ALREADY_REGISTERED](../android/drm/DrmInfoEvent.md) The registration has already been done for the given account. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALREADY_REGISTERED_BY_ANOTHER_ACCOUNT](../android/drm/DrmInfoEvent.md) The registration has already been done by another account ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOVE_RIGHTS](../android/drm/DrmInfoEvent.md) The rights need to be removed completely. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_INSTALLED](../android/drm/DrmInfoEvent.md) The rights have been successfully downloaded and installed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_REMOVED](../android/drm/DrmInfoEvent.md) The rights have been removed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WAIT_FOR_RIGHTS](../android/drm/DrmInfoEvent.md) The rights object is being delivered to the device. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [DrmEvent](../android/drm/DrmEvent.md) |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_OBJECT](../android/drm/DrmEvent.md) <br /> The key that is used in the`attributes`HashMap to pass the [DrmInfo](../android/drm/DrmInfo.md) object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_STATUS_OBJECT](../android/drm/DrmEvent.md) <br /> The key that is used in the`attributes`HashMap to pass the return status. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALL_RIGHTS_REMOVED](../android/drm/DrmEvent.md) <br /> All of the rights information associated with all DRM schemes have been successfully removed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DRM_INFO_PROCESSED](../android/drm/DrmEvent.md) <br /> The given DRM information has been successfully processed. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmInfoEvent](../android/drm/DrmInfoEvent.md))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfoEvent`object with the specified parameters. |
| [DrmInfoEvent](../android/drm/DrmInfoEvent.md))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [HashMap](../java/util/HashMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Creates a`DrmInfoEvent`object with the specified parameters. |

| Inherited functions ||
|---|---|
| From class [DrmEvent](../android/drm/DrmEvent.md) |-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](../android/drm/DrmEvent.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the attribute associated with the specified key. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessage](../android/drm/DrmEvent.md))`()` <br /> Retrieves the message description associated with this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/drm/DrmEvent.md))`()` <br /> Retrieves the type of information that is associated with this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](../android/drm/DrmEvent.md))`()` <br /> Retrieves the unique session identifier associated with this object. <br /> | ||

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

The rights object is being delivered to the device. You must wait before calling [acquireRights()](../android/drm/DrmManagerClient.md))again. 

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
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of the event. Must be any of the event types defined above, or the constants defined in [DrmEvent](../android/drm/DrmEvent.md). |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Message description. It can be null. |
| --- | --- |

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
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of the event. Must be any of the event types defined above, or the constants defined in [DrmEvent](../android/drm/DrmEvent.md) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Message description. It can be null. |
| --- | --- |
| `attributes` | [HashMap](../java/util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:Attributes for extensible information. Could be any information provided by the plug-in. |
