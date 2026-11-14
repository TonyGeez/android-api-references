# LocaleSpan

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocaleSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/LocaleSpan "View this page in Java") 
| --- | --- |

```
open class LocaleSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |||
| | ↳ | [android.text.style.MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) ||
| | | ↳ | [android.text.style.LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#) |
| --- | --- | --- | --- |

Changes the [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) of the text to which the span is attached.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#LocaleSpan(android.os.LocaleList))`(`locales:` ` [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)`)` Creates a [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#) from [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#). |
| [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#LocaleSpan(android.os.Parcel))`(`source:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#LocaleSpan(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)?`)` Creates a [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#) from a well-formed [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#describeContents())`()` <br /> |
| open [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)? | [getLocale](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#getLocale())`()` <br /> |
| open [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | [getLocales](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#getLocales())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#getSpanTypeId())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#updateDrawState(android.text.TextPaint))`(`ds:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#updateMeasureState(android.text.TextPaint))`(`paint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying())`()` <br /> Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying MetricAffectingSpan. <br /> | ||
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint))`(`tp:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### LocaleSpan

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocaleSpan(locales: LocaleList)
```

Creates a [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#) from [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locales` | [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#):The [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) of the text to which the span is attached. This value cannot be`null`. |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`locales`is null |

### LocaleSpan

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocaleSpan(source: Parcel!)
```  

### LocaleSpan

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocaleSpan(locale: Locale?)
```

Creates a [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#) from a well-formed [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). Note that only [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) objects that can be created by [Locale.forLanguageTag(String)](https://developer.android.com/reference/kotlin/java/util/Locale.html#forLanguageTag(kotlin.String))are supported.

**Caveat:** Do not specify any [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) object that cannot be created by [Locale.forLanguageTag(String)](https://developer.android.com/reference/kotlin/java/util/Locale.html#forLanguageTag(kotlin.String)).`new Locale(" a ", " b c", " d")`is an example of such a malformed [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) object.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)?:The [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) of the text to which the span is attached. This value may be`null`. |

**See Also**

- [#LocaleSpan(LocaleList)](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#LocaleSpan(android.os.LocaleList))

## Public methods

### describeContents

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getLocale

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocale(): Locale?
```

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)? | The [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) for this span. If multiple locales are associated with this span, only the first locale is returned.`null`if no [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) is specified. |

**See Also**

- [android.os.LocaleList#get(int)](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#get(kotlin.Int))
- <https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan#getLocales()> 

### getLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocales(): LocaleList
```

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | The entire list of locales that are associated with this span. This value cannot be`null`. |

### getSpanTypeId

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanTypeId(): Int
```  

### toString

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### updateDrawState

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateDrawState(ds: TextPaint!): Unit
```  

### updateMeasureState

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateMeasureState(paint: TextPaint): Unit
```

| Parameters ||
|-------------|-----------------------------------------------------------------|
| `textPaint` | the paint used for drawing the text This value cannot be`null`. |

### writeToParcel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
