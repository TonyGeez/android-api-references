# AmbientBacklightEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AmbientBacklightEvent

Kotlin| [Java](../android/media/quality/AmbientBacklightEvent.md) 
| --- | --- |

```
class AmbientBacklightEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.quality.AmbientBacklightEvent](../android/media/quality/AmbientBacklightEvent.md) |

Ambient backlight event

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AMBIENT_BACKLIGHT_EVENT_DISABLED](../android/media/quality/AmbientBacklightEvent.md) Event type for ambient backlight events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AMBIENT_BACKLIGHT_EVENT_ENABLED](../android/media/quality/AmbientBacklightEvent.md) Event type for ambient backlight events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AMBIENT_BACKLIGHT_EVENT_INTERRUPTED](../android/media/quality/AmbientBacklightEvent.md) Event type for ambient backlight events. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE](../android/media/quality/AmbientBacklightEvent.md) Event type for ambient backlight events. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AmbientBacklightEvent](../android/media/quality/AmbientBacklightEvent.md))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metadata:` ` [AmbientBacklightMetadata](../android/media/quality/AmbientBacklightMetadata.md)?`)` Constructs AmbientBacklightEvent. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/quality/AmbientBacklightEvent.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/media/quality/AmbientBacklightEvent.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventType](../android/media/quality/AmbientBacklightEvent.md))`()` Gets event type. |
| --- | --- |
| [AmbientBacklightMetadata](../android/media/quality/AmbientBacklightMetadata.md)? | [getMetadata](../android/media/quality/AmbientBacklightEvent.md))`()` Gets ambient backlight metadata. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/media/quality/AmbientBacklightEvent.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/media/quality/AmbientBacklightEvent.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/quality/AmbientBacklightEvent.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AmbientBacklightEvent](../android/media/quality/AmbientBacklightEvent.md)!\> | [CREATOR](../android/media/quality/AmbientBacklightEvent.md) <br /> |

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
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_ENABLED](../android/media/quality/AmbientBacklightEvent.md), [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_DISABLED](../android/media/quality/AmbientBacklightEvent.md), [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE](../android/media/quality/AmbientBacklightEvent.md), or [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_INTERRUPTED](../android/media/quality/AmbientBacklightEvent.md) |
| `metadata` | [AmbientBacklightMetadata](../android/media/quality/AmbientBacklightMetadata.md)?:This value may be`null`. |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_ENABLED](../android/media/quality/AmbientBacklightEvent.md), [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_DISABLED](../android/media/quality/AmbientBacklightEvent.md), [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE](../android/media/quality/AmbientBacklightEvent.md), or [android.media.quality.AmbientBacklightEvent#AMBIENT_BACKLIGHT_EVENT_INTERRUPTED](../android/media/quality/AmbientBacklightEvent.md) |

### getMetadata

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetadata(): AmbientBacklightMetadata?
```

Gets ambient backlight metadata.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AmbientBacklightMetadata](../android/media/quality/AmbientBacklightMetadata.md)? | the metadata of the event. It's non-null only for [AMBIENT_BACKLIGHT_EVENT_METADATA_AVAILABLE](../android/media/quality/AmbientBacklightEvent.md). |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AmbientBacklightEvent!>
```
