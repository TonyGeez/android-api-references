# AmbientBacklightEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AmbientBacklightEvent

Kotlin| [Java](https://developer.android.com/reference/android/media/quality/AmbientBacklightEvent "View this page in Java") 

```
class AmbientBacklightEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.quality.AmbientBacklightEvent](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#) |

Ambient backlight event

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AMBIENT_BACKLIGHT_EVENT_DISABLED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_DISABLED:kotlin.Int) Event type for ambient backlight events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AMBIENT_BACKLIGHT_EVENT_ENABLED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_ENABLED:kotlin.Int) Event type for ambient backlight events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AMBIENT_BACKLIGHT_EVENT_INTERRUPTED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_INTERRUPTED:kotlin.Int) Event type for ambient backlight events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE:kotlin.Int) Event type for ambient backlight events. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AmbientBacklightEvent](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AmbientBacklightEvent(kotlin.Int,%20android.media.quality.AmbientBacklightMetadata))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metadata:` ` [AmbientBacklightMetadata](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata)?`)` Constructs AmbientBacklightEvent. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventType](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#getEventType())`()` Gets event type. |
| [AmbientBacklightMetadata](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata)? | [getMetadata](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#getMetadata())`()` Gets ambient backlight metadata. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AmbientBacklightEvent](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### AMBIENT_BACKLIGHT_EVENT_DISABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AMBIENT_BACKLIGHT_EVENT_DISABLED: Int
```

Event type for ambient backlight events. The ambient backlight is disabled. 

 Value: 2

### AMBIENT_BACKLIGHT_EVENT_ENABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AMBIENT_BACKLIGHT_EVENT_ENABLED: Int
```

Event type for ambient backlight events. The ambient backlight is enabled. 

 Value: 1

### AMBIENT_BACKLIGHT_EVENT_INTERRUPTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AMBIENT_BACKLIGHT_EVENT_INTERRUPTED: Int
```

Event type for ambient backlight events. The ambient backlight event is preempted by another application. 

 Value: 4

### AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE: Int
```

Event type for ambient backlight events. The ambient backlight metadata is available. 

 Value: 3

## Public constructors

### AmbientBacklightEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AmbientBacklightEvent(
    eventType: Int, 
    metadata: AmbientBacklightMetadata?)
```

Constructs AmbientBacklightEvent.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_ENABLED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_ENABLED:kotlin.Int), [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_DISABLED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_DISABLED:kotlin.Int), [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE:kotlin.Int), or [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_INTERRUPTED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_INTERRUPTED:kotlin.Int) |
| `metadata` | [AmbientBacklightMetadata](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata)?:This value may be`null`. |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getEventType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventType(): Int
```

Gets event type.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_ENABLED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_ENABLED:kotlin.Int), [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_DISABLED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_DISABLED:kotlin.Int), [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE:kotlin.Int), or [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_INTERRUPTED](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_INTERRUPTED:kotlin.Int) |

### getMetadata

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetadata(): AmbientBacklightMetadata?
```

Gets ambient backlight metadata.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AmbientBacklightMetadata](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightMetadata)? | the metadata of the event. It's non-null only for [AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE:kotlin.Int). |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AmbientBacklightEvent!>
```
