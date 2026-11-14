# EasyEditSpan

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EasyEditSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/EasyEditSpan "View this page in Java") 

```
open class EasyEditSpan : ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.style.EasyEditSpan](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#) |

Provides an easy way to edit a portion of text.

The [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) uses this span to allow the user to delete a chuck of text in one click.

[TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) removes the span when the user deletes the whole text or modifies it.

This span can be also used to receive notification when the user deletes or modifies the text;

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TEXT_CHANGED_TYPE](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EXTRA_TEXT_CHANGED_TYPE:kotlin.String) The extra key field in the pending intent that describes how the text changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEXT_DELETED](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#TEXT_DELETED:kotlin.Int) The value of [EXTRA_TEXT_CHANGED_TYPE](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EXTRA_TEXT_CHANGED_TYPE:kotlin.String) when the text wrapped by this span is deleted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEXT_MODIFIED](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#TEXT_MODIFIED:kotlin.Int) The value of [EXTRA_TEXT_CHANGED_TYPE](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EXTRA_TEXT_CHANGED_TYPE:kotlin.String) when the text wrapped by this span is modified. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EasyEditSpan](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EasyEditSpan())`()` Creates the span. |
| [EasyEditSpan](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EasyEditSpan(android.app.PendingIntent))`(`pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!`)` <br /> |
| [EasyEditSpan](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EasyEditSpan(android.os.Parcel))`(`source:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`)` Constructor called from [TextUtils](https://developer.android.com/reference/kotlin/android/text/TextUtils.html#) to restore the span. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#getSpanTypeId())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

## Constants

### EXTRA_TEXT_CHANGED_TYPE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TEXT_CHANGED_TYPE: String
```

The extra key field in the pending intent that describes how the text changed. 

 Value: "android.text.style.EXTRA_TEXT_CHANGED_TYPE"

**See Also**

- [#TEXT_DELETED](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#TEXT_DELETED:kotlin.Int)
- [#TEXT_MODIFIED](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#TEXT_MODIFIED:kotlin.Int) 

### TEXT_DELETED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEXT_DELETED: Int
```

The value of [EXTRA_TEXT_CHANGED_TYPE](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EXTRA_TEXT_CHANGED_TYPE:kotlin.String) when the text wrapped by this span is deleted. 

 Value: 1

### TEXT_MODIFIED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEXT_MODIFIED: Int
```

The value of [EXTRA_TEXT_CHANGED_TYPE](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EXTRA_TEXT_CHANGED_TYPE:kotlin.String) when the text wrapped by this span is modified. 

 Value: 2

## Public constructors

### EasyEditSpan

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EasyEditSpan()
```

Creates the span. No intent is sent when the wrapped text is modified or deleted. 

### EasyEditSpan

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EasyEditSpan(pendingIntent: PendingIntent!)
```

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!:The intent will be sent when the wrapped text is deleted or modified. When the pending intent is sent, [EXTRA_TEXT_CHANGED_TYPE](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan#EXTRA_TEXT_CHANGED_TYPE:kotlin.String) is added in the intent to describe how the text changed. |

### EasyEditSpan

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EasyEditSpan(source: Parcel)
```

Constructor called from [TextUtils](https://developer.android.com/reference/kotlin/android/text/TextUtils.html#) to restore the span.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `source` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getSpanTypeId

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanTypeId(): Int
```  

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
