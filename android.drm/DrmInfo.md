# DrmInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInfo

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmInfo "View this page in Java") 
| --- | --- |

```
open class DrmInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

An entity class that describes the information required to send transactions between a device and an online DRM server. The DRM framework achieves server registration, license acquisition, and any other server-related transactions by passing an instance of this class to [DrmManagerClient.processDrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo)).

The caller can retrieve the [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#) instance by passing a [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest) instance to [DrmManagerClient.acquireDrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#acquireDrmInfo(android.drm.DrmInfoRequest)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#DrmInfo(kotlin.Int,%20kotlin.ByteArray,%20kotlin.String))`(`infoType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfo`object with the given parameters. |
| [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#DrmInfo(kotlin.Int,%20kotlin.String,%20kotlin.String))`(`infoType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfo`object with the given parameters. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [get](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#get(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a given key. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getData](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#getData())`()` Retrieves the trigger data associated with this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInfoType](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#getInfoType())`()` Retrieves the information type associated with this object. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMimeType](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#getMimeType())`()` Retrieves the MIME type associated with this object. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [iterator](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#iterator())`()` Retrieves an iterator object that you can use to iterate over the values associated with this`DrmInfo`object. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [keyIterator](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#keyIterator())`()` Retrieves an iterator object that you can use to iterate over the keys associated with this`DrmInfo`object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/android/drm/DrmInfo#put(kotlin.String,%20kotlin.Any))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Adds optional information as key-value pairs to this object. |

## Public constructors

### DrmInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmInfo(
    infoType: Int, 
    data: ByteArray!, 
    mimeType: String!)
```

Creates a`DrmInfo`object with the given parameters.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------|
| `infoType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of information. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The trigger data. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The MIME type. |
| --- | --- |

### DrmInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmInfo(
    infoType: Int, 
    path: String!, 
    mimeType: String!)
```

Creates a`DrmInfo`object with the given parameters.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------|
| `infoType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of information. |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The trigger data. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The MIME type. |
| --- | --- |

## Public methods

### get

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: String!): Any!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the value of a given key.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key whose value is being retrieved. |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The value of the key being retrieved. Returns null if the key cannot be found. |

### getData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getData(): ByteArray!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the trigger data associated with this object.

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | The trigger data. |

### getInfoType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInfoType(): Int
```

**Deprecated:** *Deprecated in Java.*

Retrieves the information type associated with this object.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The information type. |

### getMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMimeType(): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the MIME type associated with this object.

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The MIME type. |

### iterator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<Any!>!
```

**Deprecated:** *Deprecated in Java.*

Retrieves an iterator object that you can use to iterate over the values associated with this`DrmInfo`object.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | The iterator object. |

### keyIterator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keyIterator(): MutableIterator<String!>!
```

**Deprecated:** *Deprecated in Java.*

Retrieves an iterator object that you can use to iterate over the keys associated with this`DrmInfo`object.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The iterator object. |

### put

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    key: String!, 
    value: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds optional information as key-value pairs to this object. To add a custom object to the`DrmInfo`object, you must override the [toString](https://developer.android.com/reference/kotlin/java/lang/Object.html#toString())implementation.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Key to add. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Value to add. |
