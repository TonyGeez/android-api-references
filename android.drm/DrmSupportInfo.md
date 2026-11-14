# DrmSupportInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmSupportInfo

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmSupportInfo "View this page in Java") 

```
open class DrmSupportInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.drm.DrmSupportInfo](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

An entity class that wraps the capability of each DRM plug-in (agent), such as the MIME type and file suffix the DRM plug-in can handle.

Plug-in developers can expose the capability of their plug-in by passing an instance of this class to an application.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [DrmSupportInfo](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#DrmSupportInfo())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFileSuffix](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#addFileSuffix(kotlin.String))`(`fileSuffix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds the specified file suffix to the list of file suffixes this DRM plug-in supports. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addMimeType](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#addMimeType(kotlin.String))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds the specified MIME type to the list of MIME types this DRM plug-in supports. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Overridden`equals`implementation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescriprition](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#getDescriprition())`()` Retrieves the DRM plug-in (agent) description. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescription](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#getDescription())`()` Retrieves the DRM plug-in (agent) description. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getFileSuffixIterator](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#getFileSuffixIterator())`()` Retrieves an iterator object that you can use to iterate over the file suffixes that this DRM plug-in supports. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getMimeTypeIterator](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#getMimeTypeIterator())`()` Retrieves an iterator object that you can use to iterate over the MIME types that this DRM plug-in supports. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#hashCode())`()` Overridden hash code implementation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDescription](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#setDescription(kotlin.String))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets a description for the DRM plug-in (agent). |

## Public constructors

### DrmSupportInfo

```
DrmSupportInfo()
```

## Public methods

### addFileSuffix

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFileSuffix(fileSuffix: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds the specified file suffix to the list of file suffixes this DRM plug-in supports.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileSuffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:File suffix that can be handled by this DRM plug-in. it could be null but not an empty string. When it is null, it indicates that some DRM content comes with no file suffix. |

### addMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addMimeType(mimeType: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds the specified MIME type to the list of MIME types this DRM plug-in supports.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:MIME type that can be handles by this DRM plug-in. Must not be null or an empty string. |

### equals

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Overridden`equals`implementation. Two DrmSupportInfo objects are considered being equal if they support exactly the same set of mime types, file suffixes, and has exactly the same description.

| Parameters ||
|----------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `object` | The object to be compared. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if equal; false if not equal. |

### getDescriprition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescriprition(): String!
```

**Deprecated:** *The method name is mis-spelled, and it is replaced by [getDescription()](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#getDescription()).*

Retrieves the DRM plug-in (agent) description.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The plug-in description. |

### getDescription

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescription(): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the DRM plug-in (agent) description. Even if null or an empty string is not allowed in [setDescription(java.lang.String)](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#setDescription(kotlin.String)), if [setDescription(java.lang.String)](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo#setDescription(kotlin.String))is not called, description returned from this method is an empty string.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The plug-in description. |

### getFileSuffixIterator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFileSuffixIterator(): MutableIterator<String!>!
```

**Deprecated:** *Deprecated in Java.*

Retrieves an iterator object that you can use to iterate over the file suffixes that this DRM plug-in supports.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The iterator object. |

### getMimeTypeIterator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMimeTypeIterator(): MutableIterator<String!>!
```

**Deprecated:** *Deprecated in Java.*

Retrieves an iterator object that you can use to iterate over the MIME types that this DRM plug-in supports.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The iterator object |

### hashCode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Overridden hash code implementation.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The hash code value. |

### setDescription

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDescription(description: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets a description for the DRM plug-in (agent).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Unique description of plug-in. Must not be null or an empty string. |
