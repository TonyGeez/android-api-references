# AssistStructure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssistStructure

Kotlin| [Java](https://developer.android.com/reference/android/app/assist/AssistStructure "View this page in Java") 
| --- | --- |

```
open class AssistStructure : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.assist.AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#) |

This API automatically creates assist data from the platform's implementation of assist and autofill.

The structure is used for assist purposes when created by [android.app.Activity#onProvideAssistData](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistData(android.os.Bundle)), [View.onProvideStructure(ViewStructure)](https://developer.android.com/reference/kotlin/android/view/View.html#onProvideStructure(android.view.ViewStructure)), or [View.onProvideVirtualStructure(ViewStructure)](https://developer.android.com/reference/kotlin/android/view/View.html#onProvideVirtualStructure(android.view.ViewStructure)).

The structure is also used for autofill purposes when created by [View.onProvideAutofillStructure(ViewStructure, int)](https://developer.android.com/reference/kotlin/android/view/View.html#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int)), or [View.onProvideAutofillVirtualStructure(ViewStructure, int)](https://developer.android.com/reference/kotlin/android/view/View.html#onProvideAutofillVirtualStructure(android.view.ViewStructure,%20kotlin.Int)).

For performance reasons, some properties of the assist data might only be available for assist or autofill purposes. In those cases, a property's availability will be documented in its javadoc.

To learn about using Autofill in your app, read the [Autofill Framework](https://developer.android.com/reference/kotlin/guide/topics/text/autofill) guides.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [ViewNode](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.ViewNode) Describes a single view in the assist data. |
| open | [WindowNode](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.WindowNode) Describes a window in the assist data. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------|---|
| [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#AssistStructure())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#describeContents())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAcquisitionEndTime](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#getAcquisitionEndTime())`()` Returns the time when the activity finished generating assist data to build the AssistStructure. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAcquisitionStartTime](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#getAcquisitionStartTime())`()` Returns the time when the activity started generating assist data to build the AssistStructure. |
| --- | --- |
| open [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)! | [getActivityComponent](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#getActivityComponent())`()` Return the activity this AssistStructure came from. |
| open [AssistStructure.WindowNode](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.WindowNode)! | [getWindowNodeAt](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#getWindowNodeAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return one of the windows in the assist data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWindowNodeCount](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#getWindowNodeCount())`()` Return the number of window contents that have been collected in this assist data. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHomeActivity](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#isHomeActivity())`()` Returns whether the activity associated with this AssistStructure was the home activity (Launcher) at the time the assist data was acquired. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### AssistStructure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssistStructure()
```

## Public methods

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAcquisitionEndTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAcquisitionEndTime(): Long
```

Returns the time when the activity finished generating assist data to build the AssistStructure. The time is as specified by [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()).

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns the acquisition end time of the assist data, in milliseconds. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#getAcquisitionStartTime()> 

### getAcquisitionStartTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAcquisitionStartTime(): Long
```

Returns the time when the activity started generating assist data to build the AssistStructure. The time is as specified by [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()).

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns the acquisition start time of the assist data, in milliseconds. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#getAcquisitionEndTime()> 

### getActivityComponent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActivityComponent(): ComponentName!
```

Return the activity this AssistStructure came from. 

### getWindowNodeAt

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindowNodeAt(index: Int): AssistStructure.WindowNode!
```

Return one of the windows in the assist data.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which window to retrieve, may be 0 to [getWindowNodeCount()](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure#getWindowNodeCount())-1. |

### getWindowNodeCount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindowNodeCount(): Int
```

Return the number of window contents that have been collected in this assist data. 

### isHomeActivity

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isHomeActivity(): Boolean
```

Returns whether the activity associated with this AssistStructure was the home activity (Launcher) at the time the assist data was acquired.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the activity was the home activity. |

**See Also**

- [android.content.Intent#CATEGORY_HOME](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String) 

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AssistStructure!>
```
