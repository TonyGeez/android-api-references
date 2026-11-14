# LocaleList

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocaleList

Kotlin| [Java](../android/os/LocaleList.md) 
| --- | --- |

```
class LocaleList : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.LocaleList](../android/os/LocaleList.md) |

LocaleList is an immutable list of Locales, typically used to keep an ordered list of user preferences for locales.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocaleList](../android/os/LocaleList.md))`(`vararg` `list:` ` [Locale](../java/util/Locale.md)!`)` Creates a new [LocaleList](../android/os/LocaleList.md). |

| Public methods ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/os/LocaleList.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/os/LocaleList.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [LocaleList](../android/os/LocaleList.md) | [forLanguageTags](../android/os/LocaleList.md))`(`list:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Generates a new LocaleList with the given language tags. |
| --- | --- |
| [Locale](../java/util/Locale.md)! | [get](../android/os/LocaleList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the [Locale](../java/util/Locale.md) at the specified index. |
| static [LocaleList](../android/os/LocaleList.md) | [getAdjustedDefault](../android/os/LocaleList.md))`()` Returns the default locale list, adjusted by moving the default locale to its first position. |
| static [LocaleList](../android/os/LocaleList.md) | [getDefault](../android/os/LocaleList.md))`()` The result is guaranteed to include the default Locale returned by Locale. |
| --- | --- |
| static [LocaleList](../android/os/LocaleList.md) | [getEmptyLocaleList](../android/os/LocaleList.md))`()` Retrieve an empty instance of [LocaleList](../android/os/LocaleList.md). |
| [Locale](../java/util/Locale.md)? | [getFirstMatch](../android/os/LocaleList.md))`(`supportedLocales:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Returns the first match in the locale list given an unordered array of supported locales in BCP 47 format. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/os/LocaleList.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../android/os/LocaleList.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Searches this [LocaleList](../android/os/LocaleList.md) for the specified [Locale](../java/util/Locale.md) and returns the index of the first occurrence. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/os/LocaleList.md))`()` Returns whether the [LocaleList](../android/os/LocaleList.md) contains no [Locale](../java/util/Locale.md) items. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPseudoLocale](../android/os/LocaleList.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)?`)` Returns true if locale is a pseudo-locale, false otherwise. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matchesLanguageAndScript](../android/os/LocaleList.md))`(`supported:` ` [Locale](../java/util/Locale.md)`, `desired:` ` [Locale](../java/util/Locale.md)`)` Determine whether two locales are considered a match, even if they are not exactly equal. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](../android/os/LocaleList.md))`(`locales:` ` [LocaleList](../android/os/LocaleList.md)`)` Also sets the default locale by calling Locale. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../android/os/LocaleList.md))`()` Returns the number of [Locale](../java/util/Locale.md) items in this [LocaleList](../android/os/LocaleList.md). |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toLanguageTags](../android/os/LocaleList.md))`()` Retrieves a String representation of the language tags in this list. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/os/LocaleList.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/os/LocaleList.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `parcelableFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [LocaleList](../android/os/LocaleList.md)!\> | [CREATOR](../android/os/LocaleList.md) <br /> |

## Public constructors

### LocaleList

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocaleList(vararg list: Locale!)
```

Creates a new [LocaleList](../android/os/LocaleList.md). If two or more same locales are passed, the repeated locales will be dropped.

For empty lists of [Locale](../java/util/Locale.md) items it is better to use [getEmptyLocaleList()](../android/os/LocaleList.md)), which returns a pre-constructed empty list.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `list` | [Locale](../java/util/Locale.md)!:This value cannot be`null`. |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if any of the input locales is`null`. |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### forLanguageTags

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun forLanguageTags(list: String?): LocaleList
```

Generates a new LocaleList with the given language tags.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The language tags to be included as a single [String](../java/lang/String.md) separated by commas. This value may be`null`. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocaleList](../android/os/LocaleList.md) | A new instance with the [Locale](../java/util/Locale.md) items identified by the given tags. This value cannot be`null`. |

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(index: Int): Locale!
```

Retrieves the [Locale](../java/util/Locale.md) at the specified index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position to retrieve. |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Locale](../java/util/Locale.md)! | The [Locale](../java/util/Locale.md) in the given index. |

### getAdjustedDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAdjustedDefault(): LocaleList
```

Returns the default locale list, adjusted by moving the default locale to its first position.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------|
| [LocaleList](../android/os/LocaleList.md) | This value cannot be`null`. |

### getDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefault(): LocaleList
```

The result is guaranteed to include the default Locale returned by Locale.getDefault(), but not necessarily at the top of the list. The default locale not being at the top of the list is an indication that the system has set the default locale to one of the user's other preferred locales, having concluded that the primary preference is not supported but a secondary preference is.

Note that the default LocaleList would change if Locale.setDefault() is called. This method takes that into account by always checking the output of Locale.getDefault() and recalculating the default LocaleList if needed.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------|
| [LocaleList](../android/os/LocaleList.md) | This value cannot be`null`. |

### getEmptyLocaleList

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getEmptyLocaleList(): LocaleList
```

Retrieve an empty instance of [LocaleList](../android/os/LocaleList.md).

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------|
| [LocaleList](../android/os/LocaleList.md) | This value cannot be`null`. |

### getFirstMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFirstMatch(supportedLocales: Array<String!>!): Locale?
```

Returns the first match in the locale list given an unordered array of supported locales in BCP 47 format.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Locale](../java/util/Locale.md)? | The first [Locale](../java/util/Locale.md) from this list that appears in the given array, or`null`if the [LocaleList](../android/os/LocaleList.md) is empty. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### indexOf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun indexOf(locale: Locale!): Int
```

Searches this [LocaleList](../android/os/LocaleList.md) for the specified [Locale](../java/util/Locale.md) and returns the index of the first occurrence.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:The [Locale](../java/util/Locale.md) to search for. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the first occurrence of the [Locale](../java/util/Locale.md) or`-1`if the item wasn't found. Value is -1 or greater |

### isEmpty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEmpty(): Boolean
```

Returns whether the [LocaleList](../android/os/LocaleList.md) contains no [Locale](../java/util/Locale.md) items.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this [LocaleList](../android/os/LocaleList.md) has no [Locale](../java/util/Locale.md) items,`false`otherwise. |

### isPseudoLocale

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isPseudoLocale(locale: ULocale?): Boolean
```

Returns true if locale is a pseudo-locale, false otherwise.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)?:This value may be`null`. |

### matchesLanguageAndScript

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun matchesLanguageAndScript(
    supported: Locale, 
    desired: Locale
): Boolean
```

Determine whether two locales are considered a match, even if they are not exactly equal. They are considered as a match when both of their languages and scripts (explicit or inferred) are identical. This means that a user would be able to understand the content written in the supported locale even if they say they prefer the desired locale. E.g. \[zh-HK\] matches \[zh-Hant\]; \[en-US\] matches \[en-CA\]

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supported` | [Locale](../java/util/Locale.md):The supported [Locale](../java/util/Locale.md) to be compared. This value cannot be`null`. |
| `desired` | [Locale](../java/util/Locale.md):The desired [Locale](../java/util/Locale.md) to be compared. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if they match, false otherwise. |

### setDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setDefault(locales: LocaleList): Unit
```

Also sets the default locale by calling Locale.setDefault() with the first locale in the list.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `locales` | [LocaleList](../android/os/LocaleList.md):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.NullPointerException` | if the input is`null`. |
| `java.lang.IllegalArgumentException` | if the input is empty. |

### size

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun size(): Int
```

Returns the number of [Locale](../java/util/Locale.md) items in this [LocaleList](../android/os/LocaleList.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### toLanguageTags

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLanguageTags(): String
```

Retrieves a String representation of the language tags in this list.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LocaleList!>
```
