# ConversationStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConversationStatus

Kotlin| [Java](https://developer.android.com/reference/android/app/people/ConversationStatus "View this page in Java") 
| --- | --- |

```
class ConversationStatus : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.people.ConversationStatus](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#) |

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus.Builder) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_ANNIVERSARY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_ANNIVERSARY:kotlin.Int) Constant representing that the conversation user and the device user are celebrating and anniversary today. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_AUDIO](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_AUDIO:kotlin.Int) Constant representing that the conversation user is listening to music or other audio like a podcast. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_BIRTHDAY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_BIRTHDAY:kotlin.Int) Constant representing that today is the conversation user's birthday. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_GAME](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_GAME:kotlin.Int) Constant representing that the conversation user is playing a game. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_LOCATION](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_LOCATION:kotlin.Int) Constant representing that the conversation user is sharing status with the device user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_NEW_STORY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_NEW_STORY:kotlin.Int) Constant representing that the conversation user has posted a new story. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_OTHER](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_OTHER:kotlin.Int) Constant representing that the conversation user is engaged in an activity that cannot be more specifically represented by another type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_UPCOMING_BIRTHDAY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_UPCOMING_BIRTHDAY:kotlin.Int) Constant representing that the conversation user's birthday is approaching soon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTIVITY_VIDEO](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_VIDEO:kotlin.Int) Constant representing that the conversation user is watching video content. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABILITY_AVAILABLE](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#AVAILABILITY_AVAILABLE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABILITY_BUSY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#AVAILABILITY_BUSY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABILITY_OFFLINE](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#AVAILABILITY_OFFLINE:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABILITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#AVAILABILITY_UNKNOWN:kotlin.Int) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActivity](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#getActivity())`()` Returns the type of activity represented by this status |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailability](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#getAvailability())`()` Returns the availability of the people behind this conversation while this activity is happening. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDescription](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#getDescription())`()` Returns the description for this activity. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEndTimeMillis](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#getEndTimeMillis())`()` Returns the time at which this status should be expired. |
| --- | --- |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | [getIcon](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#getIcon())`()` Returns the image for this activity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#getId())`()` Returns the unique identifier for the status. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTimeMillis](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#getStartTimeMillis())`()` Returns the time at which this status started |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ConversationStatus](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ACTIVITY_ANNIVERSARY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_ANNIVERSARY: Int
```

Constant representing that the conversation user and the device user are celebrating and anniversary today. 

 Value: 2

### ACTIVITY_AUDIO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_AUDIO: Int
```

Constant representing that the conversation user is listening to music or other audio like a podcast. 

 Value: 4

### ACTIVITY_BIRTHDAY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_BIRTHDAY: Int
```

Constant representing that today is the conversation user's birthday. 

 Value: 1

### ACTIVITY_GAME

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_GAME: Int
```

Constant representing that the conversation user is playing a game. 

 Value: 6

### ACTIVITY_LOCATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_LOCATION: Int
```

Constant representing that the conversation user is sharing status with the device user. Use this to represent a general 'this person is sharing their location with you' status or a more specific 'this is the current location of this person' status. 

 Value: 7

### ACTIVITY_NEW_STORY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_NEW_STORY: Int
```

Constant representing that the conversation user has posted a new story. 

 Value: 3

### ACTIVITY_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_OTHER: Int
```

Constant representing that the conversation user is engaged in an activity that cannot be more specifically represented by another type. 

 Value: 0

### ACTIVITY_UPCOMING_BIRTHDAY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_UPCOMING_BIRTHDAY: Int
```

Constant representing that the conversation user's birthday is approaching soon. 

 Value: 8

### ACTIVITY_VIDEO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTIVITY_VIDEO: Int
```

Constant representing that the conversation user is watching video content. 

 Value: 5

### AVAILABILITY_AVAILABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABILITY_AVAILABLE: Int
```  

 Value: 0

### AVAILABILITY_BUSY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABILITY_BUSY: Int
```  

 Value: 1

### AVAILABILITY_OFFLINE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABILITY_OFFLINE: Int
```  

 Value: 2

### AVAILABILITY_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABILITY_UNKNOWN: Int
```  

 Value: -1

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getActivity

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActivity(): Int
```

Returns the type of activity represented by this status

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.people.ConversationStatus#ACTIVITY_OTHER](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_OTHER:kotlin.Int), [android.app.people.ConversationStatus#ACTIVITY_BIRTHDAY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_BIRTHDAY:kotlin.Int), [android.app.people.ConversationStatus#ACTIVITY_ANNIVERSARY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_ANNIVERSARY:kotlin.Int), [android.app.people.ConversationStatus#ACTIVITY_NEW_STORY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_NEW_STORY:kotlin.Int), [android.app.people.ConversationStatus#ACTIVITY_AUDIO](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_AUDIO:kotlin.Int), [android.app.people.ConversationStatus#ACTIVITY_VIDEO](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_VIDEO:kotlin.Int), [android.app.people.ConversationStatus#ACTIVITY_GAME](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_GAME:kotlin.Int), [android.app.people.ConversationStatus#ACTIVITY_LOCATION](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_LOCATION:kotlin.Int), or [android.app.people.ConversationStatus#ACTIVITY_UPCOMING_BIRTHDAY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#ACTIVITY_UPCOMING_BIRTHDAY:kotlin.Int) |

### getAvailability

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailability(): Int
```

Returns the availability of the people behind this conversation while this activity is happening.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.people.ConversationStatus#AVAILABILITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#AVAILABILITY_UNKNOWN:kotlin.Int), [android.app.people.ConversationStatus#AVAILABILITY_AVAILABLE](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#AVAILABILITY_AVAILABLE:kotlin.Int), [android.app.people.ConversationStatus#AVAILABILITY_BUSY](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#AVAILABILITY_BUSY:kotlin.Int), or [android.app.people.ConversationStatus#AVAILABILITY_OFFLINE](https://developer.android.com/reference/kotlin/android/app/people/ConversationStatus#AVAILABILITY_OFFLINE:kotlin.Int) |

### getDescription

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): CharSequence?
```

Returns the description for this activity.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getEndTimeMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndTimeMillis(): Long
```

Returns the time at which this status should be expired. 

### getIcon

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIcon(): Icon?
```

Returns the image for this activity.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | This value may be`null`. |

### getId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

Returns the unique identifier for the status.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getStartTimeMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTimeMillis(): Long
```

Returns the time at which this status started 

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ConversationStatus!>
```
