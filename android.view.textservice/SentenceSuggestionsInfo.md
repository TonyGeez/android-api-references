# SentenceSuggestionsInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SentenceSuggestionsInfo

Kotlin| [Java](SentenceSuggestionsInfo.md) 
| --- | --- |

```
class SentenceSuggestionsInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textservice.SentenceSuggestionsInfo](SentenceSuggestionsInfo.md) |

This class contains a metadata of suggestions returned from a text service (e.g. [android.service.textservice.SpellCheckerService](../android.service.textservice/SpellCheckerService.md)). The text service uses this class to return the suggestions for a sentence. See [SuggestionsInfo](SuggestionsInfo.md) which is used for suggestions for a word. This class extends the functionality of [SuggestionsInfo](SuggestionsInfo.md) as far as this class enables you to put multiple [SuggestionsInfo](SuggestionsInfo.md) s on a sentence with the offsets and the lengths of all [SuggestionsInfo](SuggestionsInfo.md) s.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SentenceSuggestionsInfo](SentenceSuggestionsInfo.md))`(`source:` ` [Parcel](../android.os/Parcel.md)!`)` <br /> |
| [SentenceSuggestionsInfo](SentenceSuggestionsInfo.md))`(`suggestionsInfos:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [SuggestionsInfo](SuggestionsInfo.md)!>!`, `offsets:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `lengths:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SentenceSuggestionsInfo.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLengthAt](SentenceSuggestionsInfo.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetAt](SentenceSuggestionsInfo.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSuggestionsCount](SentenceSuggestionsInfo.md))`()` <br /> |
| [SuggestionsInfo](SuggestionsInfo.md)! | [getSuggestionsInfoAt](SentenceSuggestionsInfo.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SentenceSuggestionsInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android.os/Parcel.md). |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SentenceSuggestionsInfo](SentenceSuggestionsInfo.md)!\> | [CREATOR](SentenceSuggestionsInfo.md) Used to make this class parcelable. |

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
| `suggestionsInfos` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [SuggestionsInfo](SuggestionsInfo.md)!\>!:from the text service |
| `offsets` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the array of offsets of suggestions |
| `lengths` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the array of lengths of suggestions |
| --- | --- |

## Public methods

### describeContents

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getLengthAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLengthAt(i: Int): Int
```

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id of [SuggestionsInfo](SuggestionsInfo.md) s this instance holds |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the specified [SuggestionsInfo](SuggestionsInfo.md) |

### getOffsetAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffsetAt(i: Int): Int
```

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id of [SuggestionsInfo](SuggestionsInfo.md) s this instance holds |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offset of the specified [SuggestionsInfo](SuggestionsInfo.md) |

### getSuggestionsCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuggestionsCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the count of [SuggestionsInfo](SuggestionsInfo.md) s this instance holds. |

### getSuggestionsInfoAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuggestionsInfoAt(i: Int): SuggestionsInfo!
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id of [SuggestionsInfo](SuggestionsInfo.md) s this instance holds. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [SuggestionsInfo](SuggestionsInfo.md)! | a [SuggestionsInfo](SuggestionsInfo.md) at the specified id |

### writeToParcel

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](../android.os/Parcel.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The [Parcel](../android.os/Parcel.md) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SentenceSuggestionsInfo!>
```

Used to make this class parcelable.
