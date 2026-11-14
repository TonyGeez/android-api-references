# AbsSavedState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbsSavedState

Kotlin| [Java](https://developer.android.com/reference/android/view/AbsSavedState "View this page in Java") 
| --- | --- |

```
abstract class AbsSavedState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.AbsSavedState](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#) |

| Known Direct Subclasses [Preference.BaseSavedState](https://developer.android.com/reference/kotlin/android/preference/Preference.BaseSavedState.html#), [View.BaseSavedState](https://developer.android.com/reference/kotlin/android/view/View.BaseSavedState) |--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Preference.BaseSavedState](https://developer.android.com/reference/kotlin/android/preference/Preference.BaseSavedState.html#) | A base class for managing the instance state of a [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference.html#). | | [View.BaseSavedState](https://developer.android.com/reference/kotlin/android/view/View.BaseSavedState) | Base class for derived classes that want to save and restore their own state in [android.view.View#onSaveInstanceState()](https://developer.android.com/reference/kotlin/android/view/View#onSaveInstanceState()). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [TextView.SavedState](https://developer.android.com/reference/kotlin/android/widget/TextView.SavedState.html#) |----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [TextView.SavedState](https://developer.android.com/reference/kotlin/android/widget/TextView.SavedState.html#) | User interface state that is stored by TextView for implementing [View.onSaveInstanceState](https://developer.android.com/reference/kotlin/android/view/View#onSaveInstanceState()). | |
| --- | --- | --- | --- | --- | --- | --- |

A [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) implementation that should be used by inheritance hierarchies to ensure the state of all classes along the chain is saved.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbsSavedState](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#AbsSavedState(android.os.Parcel))`(`source:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` Constructor used when reading from a parcel. |
| [AbsSavedState](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#AbsSavedState(android.os.Parcel,%20java.lang.ClassLoader))`(`source:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`, `loader:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`)` Constructor used when reading from a parcel using a given class loader. |
| [AbsSavedState](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#AbsSavedState(android.os.Parcelable))`(`superState:` ` [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!`)` Constructor called by derived classes when creating their SavedState objects |

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#describeContents())`()` <br /> |
| [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)! | [getSuperState](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#getSuperState())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AbsSavedState](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#CREATOR:android.os.Parcelable.Creator) <br /> |
| static [AbsSavedState](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#)! | [EMPTY_STATE](https://developer.android.com/reference/kotlin/android/view/AbsSavedState#EMPTY_STATE:android.view.AbsSavedState) <br /> |

## Protected constructors

### AbsSavedState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbsSavedState(source: Parcel!)
```

Constructor used when reading from a parcel. Reads the state of the superclass.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `source` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!:parcel to read from |

### AbsSavedState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbsSavedState(
    source: Parcel!, 
    loader: ClassLoader!)
```

Constructor used when reading from a parcel using a given class loader. Reads the state of the superclass.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `source` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!:parcel to read from |
| `loader` | [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!:ClassLoader to use for reading |

### AbsSavedState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbsSavedState(superState: Parcelable!)
```

Constructor called by derived classes when creating their SavedState objects

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `superState` | [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!:The state of the superclass of this view |

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getSuperState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuperState(): Parcelable!
```  

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AbsSavedState!>
```  

### EMPTY_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMPTY_STATE: AbsSavedState!
```
