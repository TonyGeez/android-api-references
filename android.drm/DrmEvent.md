# DrmEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmEvent

Kotlin| [Java](DrmEvent.md) 
| --- | --- |

```
open class DrmEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmEvent](DrmEvent.md) |

| Known Direct Subclasses [DrmErrorEvent](DrmErrorEvent.md), [DrmInfoEvent](DrmInfoEvent.md) |-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DrmErrorEvent](DrmErrorEvent.md) | An entity class that is passed to the [onError()](../android/drm/DrmManagerClient.OnErrorListener.md))callback. | | [DrmInfoEvent](DrmInfoEvent.md) | An entity class that is passed to the [onInfo()](../android/drm/DrmManagerClient.OnInfoListener.md))callback. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android.media/MediaDrm.md)

A base class that is used to send asynchronous event information from the DRM framework.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_OBJECT](DrmEvent.md) The key that is used in the`attributes`HashMap to pass the [DrmInfo](DrmInfo.md) object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DRM_INFO_STATUS_OBJECT](DrmEvent.md) The key that is used in the`attributes`HashMap to pass the return status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALL_RIGHTS_REMOVED](DrmEvent.md) All of the rights information associated with all DRM schemes have been successfully removed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DRM_INFO_PROCESSED](DrmEvent.md) The given DRM information has been successfully processed. |

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmEvent](DrmEvent.md))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmEvent`object with the specified parameters. |
| [DrmEvent](DrmEvent.md))`(`uniqueId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [HashMap](../java.util/HashMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Creates a`DrmEvent`object with the specified parameters. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](DrmEvent.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the attribute associated with the specified key. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessage](DrmEvent.md))`()` Retrieves the message description associated with this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](DrmEvent.md))`()` Retrieves the type of information that is associated with this object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](DrmEvent.md))`()` Retrieves the unique session identifier associated with this object. |

## Constants

### DRM_INFO_OBJECT

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_INFO_OBJECT: String
```

**Deprecated:** *Deprecated in Java.*

The key that is used in the`attributes`HashMap to pass the [DrmInfo](DrmInfo.md) object. 

 Value: "drm_info_object"

### DRM_INFO_STATUS_OBJECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_INFO_STATUS_OBJECT: String
```

**Deprecated:** *Deprecated in Java.*

The key that is used in the`attributes`HashMap to pass the return status. 

 Value: "drm_info_status_object"

### TYPE_ALL_RIGHTS_REMOVED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ALL_RIGHTS_REMOVED: Int
```

**Deprecated:** *Deprecated in Java.*

All of the rights information associated with all DRM schemes have been successfully removed. 

 Value: 1001

### TYPE_DRM_INFO_PROCESSED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DRM_INFO_PROCESSED: Int
```

**Deprecated:** *Deprecated in Java.*

The given DRM information has been successfully processed. 

 Value: 1002

## Protected constructors

### DrmEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected DrmEvent(
    uniqueId: Int, 
    type: Int, 
    message: String!)
```

Creates a`DrmEvent`object with the specified parameters.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------|
| `uniqueId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique session identifier. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of information. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Message description. |
| --- | --- |

### DrmEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected DrmEvent(
    uniqueId: Int, 
    type: Int, 
    message: String!, 
    attributes: HashMap<String!, Any!>!)
```

Creates a`DrmEvent`object with the specified parameters.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniqueId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique session identifier. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of information. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Message description. |
| --- | --- |
| `attributes` | [HashMap](../java.util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:Attributes for extensible information. |

## Public methods

### getAttribute

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttribute(key: String!): Any!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the attribute associated with the specified key.

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | One of the attributes or null if no mapping for the key is found. |

### getMessage

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessage(): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the message description associated with this object.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The message description. |

### getType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

**Deprecated:** *Deprecated in Java.*

Retrieves the type of information that is associated with this object.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The type of information. |

### getUniqueId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUniqueId(): Int
```

**Deprecated:** *Deprecated in Java.*

Retrieves the unique session identifier associated with this object.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The unique session identifier. |
