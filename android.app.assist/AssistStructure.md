# AssistStructure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssistStructure

Kotlin| [Java](../android/app/assist/AssistStructure.md) 
| --- | --- |

```
open class AssistStructure : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.assist.AssistStructure](../android/app/assist/AssistStructure.md) |

This API automatically creates assist data from the platform's implementation of assist and autofill.

The structure is used for assist purposes when created by [android.app.Activity#onProvideAssistData](../android/app/Activity.md)), [View.onProvideStructure(ViewStructure)](../android/view/View.md)), or [View.onProvideVirtualStructure(ViewStructure)](../android/view/View.md)).

The structure is also used for autofill purposes when created by [View.onProvideAutofillStructure(ViewStructure, int)](../android/view/View.md)), or [View.onProvideAutofillVirtualStructure(ViewStructure, int)](../android/view/View.md)).

For performance reasons, some properties of the assist data might only be available for assist or autofill purposes. In those cases, a property's availability will be documented in its javadoc.

To learn about using Autofill in your app, read the [Autofill Framework](../guide/topics/text/autofill.md) guides.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [ViewNode](../android/app/assist/AssistStructure.ViewNode.md) Describes a single view in the assist data. |
| open | [WindowNode](../android/app/assist/AssistStructure.WindowNode.md) Describes a window in the assist data. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------|---|
| [AssistStructure](../android/app/assist/AssistStructure.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/app/assist/AssistStructure.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAcquisitionEndTime](../android/app/assist/AssistStructure.md))`()` Returns the time when the activity finished generating assist data to build the AssistStructure. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAcquisitionStartTime](../android/app/assist/AssistStructure.md))`()` Returns the time when the activity started generating assist data to build the AssistStructure. |
| --- | --- |
| open [ComponentName](../android/content/ComponentName.md)! | [getActivityComponent](../android/app/assist/AssistStructure.md))`()` Return the activity this AssistStructure came from. |
| open [AssistStructure.WindowNode](../android/app/assist/AssistStructure.WindowNode.md)! | [getWindowNodeAt](../android/app/assist/AssistStructure.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return one of the windows in the assist data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWindowNodeCount](../android/app/assist/AssistStructure.md))`()` Return the number of window contents that have been collected in this assist data. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHomeActivity](../android/app/assist/AssistStructure.md))`()` Returns whether the activity associated with this AssistStructure was the home activity (Launcher) at the time the assist data was acquired. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/app/assist/AssistStructure.md))`(`out:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AssistStructure](../android/app/assist/AssistStructure.md)!\> | [CREATOR](../android/app/assist/AssistStructure.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getAcquisitionEndTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAcquisitionEndTime(): Long
```

Returns the time when the activity finished generating assist data to build the AssistStructure. The time is as specified by [SystemClock.uptimeMillis()](../android/os/SystemClock.md)).

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

Returns the time when the activity started generating assist data to build the AssistStructure. The time is as specified by [SystemClock.uptimeMillis()](../android/os/SystemClock.md)).

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
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which window to retrieve, may be 0 to [getWindowNodeCount()](../android/app/assist/AssistStructure.md))-1. |

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

- [android.content.Intent#CATEGORY_HOME](../android/content/Intent.md) 

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AssistStructure!>
```
