# EasyEditSpan

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EasyEditSpan

Kotlin| [Java](../android/text/style/EasyEditSpan.md) 
| --- | --- |

```
open class EasyEditSpan : ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.EasyEditSpan](../android/text/style/EasyEditSpan.md) |

Provides an easy way to edit a portion of text.

The [TextView](../android/widget/TextView.md) uses this span to allow the user to delete a chuck of text in one click.

[TextView](../android/widget/TextView.md) removes the span when the user deletes the whole text or modifies it.

This span can be also used to receive notification when the user deletes or modifies the text;

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TEXT_CHANGED_TYPE](../android/text/style/EasyEditSpan.md) The extra key field in the pending intent that describes how the text changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEXT_DELETED](../android/text/style/EasyEditSpan.md) The value of [EXTRA_TEXT_CHANGED_TYPE](../android/text/style/EasyEditSpan.md) when the text wrapped by this span is deleted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEXT_MODIFIED](../android/text/style/EasyEditSpan.md) The value of [EXTRA_TEXT_CHANGED_TYPE](../android/text/style/EasyEditSpan.md) when the text wrapped by this span is modified. |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EasyEditSpan](../android/text/style/EasyEditSpan.md))`()` Creates the span. |
| [EasyEditSpan](../android/text/style/EasyEditSpan.md))`(`pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)!`)` <br /> |
| [EasyEditSpan](../android/text/style/EasyEditSpan.md))`(`source:` ` [Parcel](../android/os/Parcel.md)`)` Constructor called from [TextUtils](../android/text/TextUtils.md) to restore the span. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/text/style/EasyEditSpan.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](../android/text/style/EasyEditSpan.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/text/style/EasyEditSpan.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

## Constants

### EXTRA_TEXT_CHANGED_TYPE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TEXT_CHANGED_TYPE: String
```

The extra key field in the pending intent that describes how the text changed. 

 Value: "android.text.style.EXTRA_TEXT_CHANGED_TYPE"

**See Also**

- [#TEXT_DELETED](../android/text/style/EasyEditSpan.md)
- [#TEXT_MODIFIED](../android/text/style/EasyEditSpan.md) 

### TEXT_DELETED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEXT_DELETED: Int
```

The value of [EXTRA_TEXT_CHANGED_TYPE](../android/text/style/EasyEditSpan.md) when the text wrapped by this span is deleted. 

 Value: 1

### TEXT_MODIFIED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEXT_MODIFIED: Int
```

The value of [EXTRA_TEXT_CHANGED_TYPE](../android/text/style/EasyEditSpan.md) when the text wrapped by this span is modified. 

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
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md)!:The intent will be sent when the wrapped text is deleted or modified. When the pending intent is sent, [EXTRA_TEXT_CHANGED_TYPE](../android/text/style/EasyEditSpan.md) is added in the intent to describe how the text changed. |

### EasyEditSpan

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EasyEditSpan(source: Parcel)
```

Constructor called from [TextUtils](../android/text/TextUtils.md) to restore the span.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `source` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
