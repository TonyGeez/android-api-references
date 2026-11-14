# MediaSyncEvent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaSyncEvent

Kotlin| [Java](MediaSyncEvent.md) 
| --- | --- |

```
open class MediaSyncEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaSyncEvent](MediaSyncEvent.md) |

The MediaSyncEvent class defines events that can be used to synchronize playback or capture actions between different players and recorders.

For instance, [AudioRecord.startRecording(MediaSyncEvent)](AudioRecord.md))is used to start capture only when the playback on a particular audio session is complete. The audio session ID is retrieved from a player (e.g [MediaPlayer](MediaPlayer.md), [AudioTrack](AudioTrack.md) or [ToneGenerator](ToneGenerator.md)) by use of the getAudioSessionId() method.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_EVENT_NONE](MediaSyncEvent.md) No sync event specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_EVENT_PRESENTATION_COMPLETE](MediaSyncEvent.md) The corresponding action is triggered only when the presentation is completed (meaning the media has been presented to the user) on the specified session. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [MediaSyncEvent](MediaSyncEvent.md)! | [createEvent](MediaSyncEvent.md))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a synchronization event of the sepcified type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](MediaSyncEvent.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](MediaSyncEvent.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSessionId](MediaSyncEvent.md))`()` Gets the synchronization event audio session ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](MediaSyncEvent.md))`()` Gets the synchronization event type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](MediaSyncEvent.md))`()` <br /> |
| --- | --- |
| open [MediaSyncEvent](MediaSyncEvent.md)! | [setAudioSessionId](MediaSyncEvent.md))`(`audioSessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the event source audio session ID. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](MediaSyncEvent.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](MediaSyncEvent.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [MediaSyncEvent](MediaSyncEvent.md)!\> | [CREATOR](MediaSyncEvent.md) <br /> |

## Constants

### SYNC_EVENT_NONE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EVENT_NONE: Int
```

No sync event specified. When used with a synchronized playback or capture method, the behavior is equivalent to calling the corresponding non synchronized method. 

 Value: 0

### SYNC_EVENT_PRESENTATION_COMPLETE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EVENT_PRESENTATION_COMPLETE: Int
```

The corresponding action is triggered only when the presentation is completed (meaning the media has been presented to the user) on the specified session. A synchronization of this type requires a source audio session ID to be set via [setAudioSessionId(int)](MediaSyncEvent.md))method. 

 Value: 1

## Public methods

### createEvent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createEvent(eventType: Int): MediaSyncEvent!
```

Creates a synchronization event of the sepcified type.

The type specifies which kind of event is monitored. For instance, event [SYNC_EVENT_PRESENTATION_COMPLETE](MediaSyncEvent.md) corresponds to the audio being presented to the user on a particular audio session.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the synchronization event type. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [MediaSyncEvent](MediaSyncEvent.md)! | the MediaSyncEvent created. |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAudioSessionId

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAudioSessionId(): Int
```

Gets the synchronization event audio session ID.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the synchronization audio session ID. The returned audio session ID is 0 if it has not been set. |

### getType

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

Gets the synchronization event type.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the synchronization event type. |

### hashCode

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setAudioSessionId

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioSessionId(audioSessionId: Int): MediaSyncEvent!
```

Sets the event source audio session ID.

The audio session ID specifies on which audio session the synchronization event should be monitored. It is mandatory for certain event types (e.g. [SYNC_EVENT_PRESENTATION_COMPLETE](MediaSyncEvent.md)). For instance, the audio session ID can be retrieved via [MediaPlayer.getAudioSessionId()](MediaPlayer.md))when monitoring an event on a particular MediaPlayer.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `audioSessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the audio session ID of the event source being monitored. |

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| [MediaSyncEvent](MediaSyncEvent.md)! | the MediaSyncEvent the method is called on. |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### toString

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MediaSyncEvent!>
```
