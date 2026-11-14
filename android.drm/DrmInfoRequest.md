# DrmInfoRequest

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInfoRequest

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmInfoRequest "View this page in Java") 

```
open class DrmInfoRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.drm.DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

An entity class that is used to pass information to an online DRM server. An instance of this class is passed to the [acquireDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#acquireDrmInfo(android.drm.DrmInfoRequest))method to get an instance of a [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_ID](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#ACCOUNT_ID:kotlin.String) Key that is used to pass the unique session ID for the account or the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUBSCRIPTION_ID](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#SUBSCRIPTION_ID:kotlin.String) Key that is used to pass the unique session ID for the subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REGISTRATION_INFO](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#TYPE_REGISTRATION_INFO:kotlin.Int) Acquires DRM server registration information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_ACQUISITION_INFO](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#TYPE_RIGHTS_ACQUISITION_INFO:kotlin.Int) Acquires rights information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RIGHTS_ACQUISITION_PROGRESS_INFO](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#TYPE_RIGHTS_ACQUISITION_PROGRESS_INFO:kotlin.Int) Acquires the progress of the rights acquisition. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNREGISTRATION_INFO](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#TYPE_UNREGISTRATION_INFO:kotlin.Int) Acquires information for unregistering the DRM server. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#DrmInfoRequest(kotlin.Int,%20kotlin.String))`(`infoType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfoRequest`object with type and MIME type. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [get](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#get(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInfoType](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#getInfoType())`()` Retrieves the information type associated with this object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMimeType](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#getMimeType())`()` Retrieves the MIME type associated with this object. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [iterator](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#iterator())`()` Retrieves an iterator object that you can use to iterate over the values associated with this`DrmInfoRequest`object. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [keyIterator](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#keyIterator())`()` Retrieves an iterator object that you can use to iterate over the keys associated with this`DrmInfoRequest`object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest#put(kotlin.String,%20kotlin.Any))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Adds optional information as key-value pairs to this object. |

## Constants

### ACCOUNT_ID

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_ID: String
```

**Deprecated:** *Deprecated in Java.*

Key that is used to pass the unique session ID for the account or the user. 

 Value: "account_id"

### SUBSCRIPTION_ID

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_ID: String
```

**Deprecated:** *Deprecated in Java.*

Key that is used to pass the unique session ID for the subscription. 

 Value: "subscription_id"

### TYPE_REGISTRATION_INFO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REGISTRATION_INFO: Int
```

**Deprecated:** *Deprecated in Java.*

Acquires DRM server registration information. 

 Value: 1

### TYPE_RIGHTS_ACQUISITION_INFO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RIGHTS_ACQUISITION_INFO: Int
```

**Deprecated:** *Deprecated in Java.*

Acquires rights information. 

 Value: 3

### TYPE_RIGHTS_ACQUISITION_PROGRESS_INFO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RIGHTS_ACQUISITION_PROGRESS_INFO: Int
```

**Deprecated:** *Deprecated in Java.*

Acquires the progress of the rights acquisition. 

 Value: 4

### TYPE_UNREGISTRATION_INFO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNREGISTRATION_INFO: Int
```

**Deprecated:** *Deprecated in Java.*

Acquires information for unregistering the DRM server. 

 Value: 2

## Public constructors

### DrmInfoRequest

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmInfoRequest(
    infoType: Int, 
    mimeType: String!)
```

Creates a`DrmInfoRequest`object with type and MIME type.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------|
| `infoType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Type of information. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:MIME type. |

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
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The value of the key that is being retrieved. Returns null if the key cannot be found. |

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

Retrieves an iterator object that you can use to iterate over the values associated with this`DrmInfoRequest`object.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | The iterator object. |

### keyIterator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keyIterator(): MutableIterator<String!>!
```

**Deprecated:** *Deprecated in Java.*

Retrieves an iterator object that you can use to iterate over the keys associated with this`DrmInfoRequest`object.

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

Adds optional information as key-value pairs to this object.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key to add. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The value to add. |
