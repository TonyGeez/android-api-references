# SpellCheckerSubtype

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpellCheckerSubtype

Kotlin| [Java](../android/view/textservice/SpellCheckerSubtype.md) 
| --- | --- |

```
class SpellCheckerSubtype : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textservice.SpellCheckerSubtype](../android/view/textservice/SpellCheckerSubtype.md) |

This class is used to specify meta information of a subtype contained in a spell checker. Subtype can describe locale (e.g. en_US, fr_FR...) used for settings.

## Summary

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [`android:label`](../android/view/textservice/SpellCheckerSubtype.md) | The name of the subtype. |
| [`android:languageTag`](../android/view/textservice/SpellCheckerSubtype.md) | The BCP-47 Language Tag of the subtype. |
| [`android:subtypeExtraValue`](../android/view/textservice/SpellCheckerSubtype.md) | The extra value of the subtype. |
| --- | --- |
| [`android:subtypeId`](../android/view/textservice/SpellCheckerSubtype.md) | The unique id for the subtype. |
| [`android:subtypeLocale`](../android/view/textservice/SpellCheckerSubtype.md) | The locale of the subtype. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SpellCheckerSubtype](../android/view/textservice/SpellCheckerSubtype.md))`(`nameId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extraValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsExtraValueKey](../android/view/textservice/SpellCheckerSubtype.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The string of ExtraValue in subtype should be defined as follows: example: key0,key1=value1,key2,key3,key4=value4 |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/textservice/SpellCheckerSubtype.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/view/textservice/SpellCheckerSubtype.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getDisplayName](../android/view/textservice/SpellCheckerSubtype.md))`(`context:` ` [Context](../android/content/Context.md)!`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `appInfo:` ` [ApplicationInfo](../android/content/pm/ApplicationInfo.md)!`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExtraValue](../android/view/textservice/SpellCheckerSubtype.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExtraValueOf](../android/view/textservice/SpellCheckerSubtype.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The string of ExtraValue in subtype should be defined as follows: example: key0,key1=value1,key2,key3,key4=value4 |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getLanguageTag](../android/view/textservice/SpellCheckerSubtype.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getLocale](../android/view/textservice/SpellCheckerSubtype.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNameResId](../android/view/textservice/SpellCheckerSubtype.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/view/textservice/SpellCheckerSubtype.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/textservice/SpellCheckerSubtype.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `parcelableFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SpellCheckerSubtype](../android/view/textservice/SpellCheckerSubtype.md)!\> | [CREATOR](../android/view/textservice/SpellCheckerSubtype.md) <br /> |

## XML attributes

### android:label

```
android:label
```
The name of the subtype.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:languageTag

```
android:languageTag
```
The BCP-47 Language Tag of the subtype. This replaces [android.R.styleable#SpellChecker_Subtype_subtypeLocale](../android/R.styleable.md).

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:subtypeExtraValue

```
android:subtypeExtraValue
```
The extra value of the subtype. This string can be any string and will be passed to the SpellChecker.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:subtypeId

```
android:subtypeId
```
The unique id for the subtype. The text service (spell checker) framework keeps track of enabled subtypes by ID. When the spell checker package gets upgraded, enabled IDs will stay enabled even if other attributes are different. If the ID is unspecified or explicitly specified to 0 in XML resources,`Arrays.hashCode(new Object[] {subtypeLocale, extraValue})`will be used instead.

May be an integer value, such as "`100`". 

### android:subtypeLocale

```
android:subtypeLocale
```
The locale of the subtype. This string should be a locale (for example, en_US and fr_FR). This is also used by the framework to know the supported locales of the spell checker. [android.view.textservice.SpellCheckerSubtype#getLocale()](../android/view/textservice/SpellCheckerSubtype.md))returns the value specified in this attribute.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

## Public constructors

### SpellCheckerSubtype

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SpellCheckerSubtype(
    nameId: Int, 
    locale: String!, 
    extraValue: String!)
```

**Deprecated:** *There is no public API that requires developers to directly instantiate custom [SpellCheckerSubtype](../android/view/textservice/SpellCheckerSubtype.md) objects right now. Hence only the system is expected to be able to instantiate [SpellCheckerSubtype](../android/view/textservice/SpellCheckerSubtype.md) object.*

Constructor.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| `nameId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The name of the subtype |
| `locale` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The locale supported by the subtype |
| `extraValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The extra value of the subtype |
| --- | --- |

## Public methods

### containsExtraValueKey

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun containsExtraValueKey(key: String!): Boolean
```

The string of ExtraValue in subtype should be defined as follows: example: key0,key1=value1,key2,key3,key4=value4

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key of extra value |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the subtype contains specified the extra value |

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDisplayName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(
    context: Context!, 
    packageName: String!, 
    appInfo: ApplicationInfo!
): CharSequence!
```

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:Context will be used for getting Locale and PackageManager. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package name of the spell checker |
| `appInfo` | [ApplicationInfo](../android/content/pm/ApplicationInfo.md)!:The application info of the spell checker |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a display name for this subtype. The string resource of the label (mSubtypeNameResId) can have only one %s in it. If there is, the %s part will be replaced with the locale's display name by the formatter. If there is not, this method simply returns the string specified by mSubtypeNameResId. If mSubtypeNameResId is not specified (== 0), it's up to the framework to generate an appropriate display name. |

### getExtraValue

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtraValue(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the extra value of the subtype |

### getExtraValueOf

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtraValueOf(key: String!): String!
```

The string of ExtraValue in subtype should be defined as follows: example: key0,key1=value1,key2,key3,key4=value4

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key of extra value |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the specified key |

### getLanguageTag

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLanguageTag(): String
```

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the BCP-47 Language Tag of the subtype. Returns an empty string when no Language Tag is specified. This value cannot be`null`. |

**See Also**

- [java.util.Locale#forLanguageTag(String)](../java/util/Locale.md)) 

### getLocale

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocale(): String
```

**Deprecated:** *Use [getLanguageTag()](../android/view/textservice/SpellCheckerSubtype.md))instead.*

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the locale of the subtype This value cannot be`null`. |

### getNameResId

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNameResId(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the name of the subtype |

### hashCode

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SpellCheckerSubtype!>
```
