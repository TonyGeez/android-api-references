# AbsSavedState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbsSavedState

Kotlin| [Java](AbsSavedState.md) 
| --- | --- |

```
abstract class AbsSavedState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.AbsSavedState](AbsSavedState.md) |

| Known Direct Subclasses [Preference.BaseSavedState](../android/preference/Preference.BaseSavedState.md), [View.BaseSavedState](../android/view/View.BaseSavedState.md) |--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Preference.BaseSavedState](../android/preference/Preference.BaseSavedState.md) | A base class for managing the instance state of a [Preference](../android.preference/Preference.md). | | [View.BaseSavedState](../android/view/View.BaseSavedState.md) | Base class for derived classes that want to save and restore their own state in [android.view.View#onSaveInstanceState()](View.md)). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [TextView.SavedState](../android/widget/TextView.SavedState.md) |----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [TextView.SavedState](../android/widget/TextView.SavedState.md) | User interface state that is stored by TextView for implementing [View.onSaveInstanceState](View.md)). | |
| --- | --- | --- | --- | --- | --- | --- |

A [Parcelable](../android.os/Parcelable.md) implementation that should be used by inheritance hierarchies to ensure the state of all classes along the chain is saved.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbsSavedState](AbsSavedState.md))`(`source:` ` [Parcel](../android.os/Parcel.md)!`)` Constructor used when reading from a parcel. |
| [AbsSavedState](AbsSavedState.md))`(`source:` ` [Parcel](../android.os/Parcel.md)!`, `loader:` ` [ClassLoader](../java.lang/ClassLoader.md)!`)` Constructor used when reading from a parcel using a given class loader. |
| [AbsSavedState](AbsSavedState.md))`(`superState:` ` [Parcelable](../android.os/Parcelable.md)!`)` Constructor called by derived classes when creating their SavedState objects |

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](AbsSavedState.md))`()` <br /> |
| [Parcelable](../android.os/Parcelable.md)! | [getSuperState](AbsSavedState.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](AbsSavedState.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AbsSavedState](AbsSavedState.md)!\> | [CREATOR](AbsSavedState.md) <br /> |
| static [AbsSavedState](AbsSavedState.md)! | [EMPTY_STATE](AbsSavedState.md) <br /> |

## Protected constructors

### AbsSavedState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbsSavedState(source: Parcel!)
```

Constructor used when reading from a parcel. Reads the state of the superclass.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `source` | [Parcel](../android.os/Parcel.md)!:parcel to read from |

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
| `source` | [Parcel](../android.os/Parcel.md)!:parcel to read from |
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)!:ClassLoader to use for reading |

### AbsSavedState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbsSavedState(superState: Parcelable!)
```

Constructor called by derived classes when creating their SavedState objects

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `superState` | [Parcelable](../android.os/Parcelable.md)!:The state of the superclass of this view |

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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
