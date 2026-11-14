# PictureInPictureUiState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PictureInPictureUiState

Kotlin| [Java](https://developer.android.com/reference/android/app/PictureInPictureUiState "View this page in Java") 
| --- | --- |

```
class PictureInPictureUiState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.PictureInPictureUiState](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#) |

Used by [Activity.onPictureInPictureUiStateChanged(PictureInPictureUiState)](https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureUiStateChanged(android.app.PictureInPictureUiState)).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#hashCode())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStashed](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#isStashed())`()` Returns whether Picture-in-Picture is stashed or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTransitioningToPip](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#isTransitioningToPip())`()` Returns`true`if the app is going to enter Picture-in-Picture (PiP) mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PictureInPictureUiState](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#CREATOR:android.os.Parcelable.Creator) <br /> |

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

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isStashed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isStashed(): Boolean
```

Returns whether Picture-in-Picture is stashed or not. A stashed PiP means it is only partially visible to the user, with some parts of it being off-screen. This is usually a UI state that is triggered by the user, such as flinging the PiP to the edge or letting go of PiP while dragging partially off-screen. Developers can use this in conjunction with [Activity.onPictureInPictureUiStateChanged(PictureInPictureUiState)](https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureUiStateChanged(android.app.PictureInPictureUiState))to get a signal when the PiP stash state has changed. For example, if the state changed from`false`to`true`, developers can choose to temporarily pause video playback if PiP is of video content. Vice versa, if changing from`true`to`false`and video content is paused, developers can resume video playback. 
**See Also**

### isTransitioningToPip

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isTransitioningToPip(): Boolean
```

Returns`true`if the app is going to enter Picture-in-Picture (PiP) mode. This state is associated with the entering PiP animation. When that animation starts, whether via auto enter PiP or calling [Activity.enterPictureInPictureMode(PictureInPictureParams)](https://developer.android.com/reference/kotlin/android/app/Activity#enterPictureInPictureMode(android.app.PictureInPictureParams))explicitly, app can expect [Activity.onPictureInPictureUiStateChanged(PictureInPictureUiState)](https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureUiStateChanged(android.app.PictureInPictureUiState))callback with [isTransitioningToPip()](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#isTransitioningToPip())to be`true`first, followed by [Activity.onPictureInPictureModeChanged(boolean, Configuration)](https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration))when it fully settles in PiP mode. When app receives the [Activity.onPictureInPictureUiStateChanged(PictureInPictureUiState)](https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureUiStateChanged(android.app.PictureInPictureUiState))callback with [isTransitioningToPip()](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#isTransitioningToPip())being`true`, it's recommended to hide certain UI elements, such as video controls, to archive a clean entering PiP animation. In case an application wants to restore the previously hidden UI elements when exiting PiP, it is recommended to do that in`onPictureInPictureModeChanged(isInPictureInPictureMode=false)`callback rather than the beginning of exit PiP animation. 

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PictureInPictureUiState!>
```
