# SentenceSuggestionsInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SentenceSuggestionsInfo

Kotlin| [Java](https://developer.android.com/reference/android/view/textservice/SentenceSuggestionsInfo "View this page in Java") 

```
class SentenceSuggestionsInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.textservice.SentenceSuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#) |

This class contains a metadata of suggestions returned from a text service (e.g. [android.service.textservice.SpellCheckerService](https://developer.android.com/reference/kotlin/android/service/textservice/SpellCheckerService.html#)). The text service uses this class to return the suggestions for a sentence. See [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) which is used for suggestions for a word. This class extends the functionality of [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) as far as this class enables you to put multiple [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) s on a sentence with the offsets and the lengths of all [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) s.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SentenceSuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#SentenceSuggestionsInfo(android.os.Parcel))`(`source:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| [SentenceSuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#SentenceSuggestionsInfo(kotlin.Array,%20kotlin.IntArray,%20kotlin.IntArray))`(`suggestionsInfos:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo)!>!`, `offsets:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `lengths:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLengthAt](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#getLengthAt(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetAt](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#getOffsetAt(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSuggestionsCount](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#getSuggestionsCount())`()` <br /> |
| [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo)! | [getSuggestionsInfoAt](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#getSuggestionsInfoAt(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SentenceSuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/textservice/SentenceSuggestionsInfo#CREATOR:android.os.Parcelable.Creator) Used to make this class parcelable. |

## Public constructors

### SentenceSuggestionsInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SentenceSuggestionsInfo(source: Parcel!)
```  

### SentenceSuggestionsInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SentenceSuggestionsInfo(
    suggestionsInfos: Array<SuggestionsInfo!>!, 
    offsets: IntArray!, 
    lengths: IntArray!)
```

Constructor.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `suggestionsInfos` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo)!\>!:from the text service |
| `offsets` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the array of offsets of suggestions |
| `lengths` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the array of lengths of suggestions |

## Public methods

### describeContents

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getLengthAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLengthAt(i: Int): Int
```

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id of [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) s this instance holds |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the specified [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) |

### getOffsetAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffsetAt(i: Int): Int
```

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id of [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) s this instance holds |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offset of the specified [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) |

### getSuggestionsCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuggestionsCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the count of [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) s this instance holds. |

### getSuggestionsInfoAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuggestionsInfoAt(i: Int): SuggestionsInfo!
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id of [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) s this instance holds. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo)! | a [SuggestionsInfo](https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo) at the specified id |

### writeToParcel

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SentenceSuggestionsInfo!>
```

Used to make this class parcelable.
