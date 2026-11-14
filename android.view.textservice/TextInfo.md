# TextInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextInfo

Kotlin| [Java](TextInfo.md) 
| --- | --- |

```
class TextInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textservice.TextInfo](TextInfo.md) |

This class contains a metadata of the input of TextService

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextInfo](TextInfo.md))`(`source:` ` [Parcel](../android.os/Parcel.md)!`)` <br /> |
| [TextInfo](TextInfo.md))`(`charSequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cookie:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequenceNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |
| [TextInfo](TextInfo.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor. |
| [TextInfo](TextInfo.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cookie:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequenceNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](TextInfo.md))`()` Used to make this class parcelable. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getCharSequence](TextInfo.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCookie](TextInfo.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequence](TextInfo.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getText](TextInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](TextInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android.os/Parcel.md). |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TextInfo](TextInfo.md)!\> | [CREATOR](TextInfo.md) Used to make this class parcelable. |

## Public constructors

### TextInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextInfo(source: Parcel!)
```  

### TextInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextInfo(
    charSequence: CharSequence!, 
    start: Int, 
    end: Int, 
    cookie: Int, 
    sequenceNumber: Int)
```

Constructor.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `charSequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text which will be input to TextService. Attached spans that implement [ParcelableSpan](../android.text/ParcelableSpan.md) will also be marshaled alongside with the text. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the beginning of the range of text (inclusive). |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end of the range of text (exclusive). |
| --- | --- |
| `cookie` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the cookie for this TextInfo |
| `sequenceNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sequence number for this TextInfo |

### TextInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextInfo(text: String!)
```

Constructor.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the text which will be input to TextService |

### TextInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextInfo(
    text: String!, 
    cookie: Int, 
    sequenceNumber: Int)
```

Constructor.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the text which will be input to TextService |
| `cookie` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the cookie for this TextInfo |
| `sequenceNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sequence number for this TextInfo |
| --- | --- |

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Used to make this class parcelable.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getCharSequence

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCharSequence(): CharSequence!
```

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | the charSequence which is an input of a text service. This may have some parcelable spans. |

### getCookie

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCookie(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the cookie of TextInfo |

### getSequence

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSequence(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the sequence of TextInfo |

### getText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getText(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the text which is an input of a text service |

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TextInfo!>
```

Used to make this class parcelable.
