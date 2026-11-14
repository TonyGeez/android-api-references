# DrmInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInfo

Kotlin| [Java](DrmInfo.md) 
| --- | --- |

```
open class DrmInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmInfo](DrmInfo.md) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android.media/MediaDrm.md)

An entity class that describes the information required to send transactions between a device and an online DRM server. The DRM framework achieves server registration, license acquisition, and any other server-related transactions by passing an instance of this class to [DrmManagerClient.processDrmInfo](DrmManagerClient.md)).

The caller can retrieve the [DrmInfo](DrmInfo.md) instance by passing a [DrmInfoRequest](DrmInfoRequest.md) instance to [DrmManagerClient.acquireDrmInfo](DrmManagerClient.md)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmInfo](DrmInfo.md))`(`infoType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfo`object with the given parameters. |
| [DrmInfo](DrmInfo.md))`(`infoType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfo`object with the given parameters. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [get](DrmInfo.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a given key. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getData](DrmInfo.md))`()` Retrieves the trigger data associated with this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInfoType](DrmInfo.md))`()` Retrieves the information type associated with this object. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMimeType](DrmInfo.md))`()` Retrieves the MIME type associated with this object. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [iterator](DrmInfo.md))`()` Retrieves an iterator object that you can use to iterate over the values associated with this`DrmInfo`object. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [keyIterator](DrmInfo.md))`()` Retrieves an iterator object that you can use to iterate over the keys associated with this`DrmInfo`object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](DrmInfo.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Adds optional information as key-value pairs to this object. |

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

Adds optional information as key-value pairs to this object. To add a custom object to the`DrmInfo`object, you must override the [toString](../java.lang/Object.md))implementation.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Key to add. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Value to add. |
