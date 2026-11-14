# InputMethodSubtype

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMethodSubtype

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/InputMethodSubtype "View this page in Java") 

```
class InputMethodSubtype : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.inputmethod.InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#) |

This class is used to specify meta information of a subtype contained in an input method editor (IME). Subtype can describe locale (e.g. en_US, fr_FR...) and mode (e.g. voice, keyboard...), and is used for IME switch and settings. The input method subtype allows the system to bring up the specified subtype of the designated IME directly.

It should be defined in an XML resource file of the input method with the`<subtype>`element, which resides within an`<input-method>`element. For more information, see the guide to [Creating an Input Method](https://developer.android.com/guide/topics/text/creating-input-method.html).

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [InputMethodSubtypeBuilder](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.InputMethodSubtypeBuilder) InputMethodSubtypeBuilder is a builder class of InputMethodSubtype. |

| XML attributes ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [`android:icon`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | The icon of the subtype. |
| [`android:imeSubtypeExtraValue`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | The extra value of the subtype. |
| [`android:imeSubtypeLocale`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | The locale of the subtype. |
| [`android:imeSubtypeMode`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | The mode of the subtype. |
| [`android:isAsciiCapable`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | Set to true if this subtype is ASCII capable. |
| [`android:isAuxiliary`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | Set true if the subtype is auxiliary. |
| [`android:label`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | The name of the subtype. |
| [`android:languageTag`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | The BCP-47 Language Tag of the subtype. |
| [`android:overridesImplicitlyEnabledSubtype`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | Set true when this subtype should be selected by default if no other subtypes are selected explicitly. |
| [`android:subtypeId`](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#attr_InputMethodSubtype) | The unique id for the subtype. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#InputMethodSubtype(kotlin.Int,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Boolean,%20kotlin.Boolean))`(`nameId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `iconId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extraValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isAuxiliary:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `overridesImplicitlyEnabledSubtype:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructor with no subtype ID specified. |
| [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#InputMethodSubtype(kotlin.Int,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Int))`(`nameId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `iconId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extraValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isAuxiliary:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `overridesImplicitlyEnabledSubtype:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsExtraValueKey](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#containsExtraValueKey(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The string of ExtraValue in subtype should be defined as follows: example: key0,key1=value1,key2,key3,key4=value4 |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getDisplayName](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getDisplayName(android.content.Context,%20kotlin.String,%20android.content.pm.ApplicationInfo))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `appInfo:` ` [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)!`)` Returns a display name for this subtype. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExtraValue](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getExtraValue())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExtraValueOf](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getExtraValueOf(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The string of ExtraValue in subtype should be defined as follows: example: key0,key1=value1,key2,key3,key4=value4 |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIconResId](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getIconResId())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getLanguageTag](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getLanguageTag())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getLayoutDisplayName](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getLayoutDisplayName(android.content.Context,%20android.content.pm.ApplicationInfo))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `imeAppInfo:` ` [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)`)` Returns the layout display name. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getLayoutLabelNonLocalized](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getLayoutLabelNonLocalized())`()` Returns the non-localized layout label. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutLabelResource](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getLayoutLabelResource())`()` Returns the layout label string resource identifier. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getLocale](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getLocale())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMode](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getMode())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getNameOverride](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getNameOverride())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNameResId](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getNameResId())`()` <br /> |
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)? | [getPhysicalKeyboardHintLanguageTag](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getPhysicalKeyboardHintLanguageTag())`()` Returns the physical keyboard BCP-47 language tag. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPhysicalKeyboardHintLayoutType](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getPhysicalKeyboardHintLayoutType())`()` Returns the physical keyboard layout type string. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAsciiCapable](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#isAsciiCapable())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAuxiliary](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#isAuxiliary())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [overridesImplicitlyEnabledSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#overridesImplicitlyEnabledSubtype())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `parcelableFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#CREATOR:android.os.Parcelable.Creator) <br /> |

## XML attributes

### android:icon

```
android:icon
```
The icon of the subtype.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:imeSubtypeExtraValue

```
android:imeSubtypeExtraValue
```
The extra value of the subtype. This string can be any string and will be passed to the IME when the framework calls the IME with the subtype.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:imeSubtypeLocale

```
android:imeSubtypeLocale
```
The locale of the subtype. This string should be a locale (for example en_US and fr_FR) and will be passed to the IME when the framework calls the IME with the subtype. This is also used by the framework to know the supported locales of the IME.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:imeSubtypeMode

```
android:imeSubtypeMode
```
The mode of the subtype. This string can be a mode (for example, voice and keyboard) and this string will be passed to the IME when the framework calls the IME with the subtype. [android.view.inputmethod.InputMethodSubtype#getLocale()](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getLocale())returns the value specified in this attribute.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:isAsciiCapable

```
android:isAsciiCapable
```
Set to`true`if this subtype is ASCII capable. If the subtype is ASCII capable, it should guarantee that the user can input ASCII characters with this subtype. This is important because many password fields only allow ASCII-characters.

Note: In order to avoid some known system issues on [android.os.Build.VERSION_CODES#P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int) and prior OSes, you may want to include`"AsciiCapable"`in [android.R.styleable#InputMethod_Subtype_imeSubtypeExtraValue](https://developer.android.com/reference/kotlin/android/R.styleable.html#InputMethod_Subtype_imeSubtypeExtraValue:kotlin.Int) when you specify`true`to this attribute.

May be a boolean value, such as "`true`" or "`false`". 

### android:isAuxiliary

```
android:isAuxiliary
```
Set true if the subtype is auxiliary. An auxiliary subtype won't be shown in the input method selection list in the settings app. InputMethodManager#switchToLastInputMethod will ignore auxiliary subtypes when it chooses a target subtype.

May be a boolean value, such as "`true`" or "`false`". 

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
The BCP-47 Language Tag of the subtype. This replaces [android.R.styleable#InputMethod_Subtype_imeSubtypeLocale](https://developer.android.com/reference/kotlin/android/R.styleable.html#InputMethod_Subtype_imeSubtypeLocale:kotlin.Int).

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:overridesImplicitlyEnabledSubtype

```
android:overridesImplicitlyEnabledSubtype
```
Set true when this subtype should be selected by default if no other subtypes are selected explicitly. Note that a subtype with this parameter being true will not be shown in the subtypes list.

May be a boolean value, such as "`true`" or "`false`". 

### android:subtypeId

```
android:subtypeId
```
The unique id for the subtype. The input method framework keeps track of enabled subtypes by ID. When the IME package gets upgraded, enabled IDs will stay enabled even if other attributes are different. If the ID is unspecified (by calling the other constructor or 0. Arrays.hashCode(new Object\[\] {locale, mode, extraValue, isAuxiliary, overridesImplicitlyEnabledSubtype}) will be used instead.

May be an integer value, such as "`100`".

## Public constructors

### InputMethodSubtype

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputMethodSubtype(
    nameId: Int, 
    iconId: Int, 
    locale: String!, 
    mode: String!, 
    extraValue: String!, 
    isAuxiliary: Boolean, 
    overridesImplicitlyEnabledSubtype: Boolean)
```

**Deprecated:** *use [InputMethodSubtypeBuilder](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.InputMethodSubtypeBuilder) instead. Arguments for this constructor have the same meanings as [InputMethodSubtype.InputMethodSubtype(int, int, String, String, String, boolean,](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#InputMethodSubtype(kotlin.Int,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Int))except "id".*

Constructor with no subtype ID specified. 

### InputMethodSubtype

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputMethodSubtype(
    nameId: Int, 
    iconId: Int, 
    locale: String!, 
    mode: String!, 
    extraValue: String!, 
    isAuxiliary: Boolean, 
    overridesImplicitlyEnabledSubtype: Boolean, 
    id: Int)
```

**Deprecated:** *use [InputMethodSubtypeBuilder](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.InputMethodSubtypeBuilder) instead. "isAsciiCapable" is "false" in this constructor.*

Constructor.

| Parameters ||
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `nameId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource ID of the subtype name string. The string resource may have exactly one %s in it. If there is, the %s part will be replaced with the locale's display name by the formatter. Please refer to [getDisplayName](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getDisplayName(android.content.Context,%20kotlin.String,%20android.content.pm.ApplicationInfo))for details. |
| `iconId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource ID of the subtype icon drawable. |
| `locale` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The locale supported by the subtype |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The mode supported by the subtype |
| `extraValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The extra value of the subtype. This string is free-form, but the API supplies tools to deal with a key-value comma-separated list; see [containsExtraValueKey](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#containsExtraValueKey(kotlin.String))and [getExtraValueOf](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getExtraValueOf(kotlin.String)). |
| `isAuxiliary` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true when this subtype is auxiliary, false otherwise. An auxiliary subtype will not be shown in the list of enabled IMEs for choosing the current IME in the Settings even when this subtype is enabled. Please note that this subtype will still be shown in the list of IMEs in the IME switcher to allow the user to tentatively switch to this subtype while an IME is shown. The framework will never switch the current IME to this subtype by [android.view.inputmethod.InputMethodManager#switchToLastInputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#switchToLastInputMethod(android.os.IBinder)). The intent of having this flag is to allow for IMEs that are invoked in a one-shot way as auxiliary input mode, and return to the previous IME once it is finished (e.g. voice input). |
| `overridesImplicitlyEnabledSubtype` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true when this subtype should be enabled by default if no other subtypes in the IME are enabled explicitly. Note that a subtype with this parameter being true will not be shown in the list of subtypes in each IME's subtype enabler. Having an "automatic" subtype is an example use of this flag. |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unique ID for the subtype. The input method framework keeps track of enabled subtypes by ID. When the IME package gets upgraded, enabled IDs will stay enabled even if other attributes are different. If the ID is unspecified or 0, Arrays.hashCode(new Object\[\] {locale, mode, extraValue, isAuxiliary, overridesImplicitlyEnabledSubtype, isAsciiCapable}) will be used instead. |

## Public methods

### containsExtraValueKey

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun containsExtraValueKey(key: String!): Boolean
```

The string of ExtraValue in subtype should be defined as follows: example: key0,key1=value1,key2,key3,key4=value4

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key of extra value |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The subtype contains specified the extra value |

### describeContents

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
): CharSequence
```

Returns a display name for this subtype.

If`subtypeNameResId`is specified (!= 0) text generated from that resource will be returned. The localized string resource of the label should be capitalized for inclusion in UI lists. The string resource may contain at most one`%s`. If present, the`%s`will be replaced with the display name of the subtype locale in the user's locale.

If`subtypeNameResId`is not specified (== 0) the framework returns the display name of the subtype locale, as capitalized for use in UI lists, in the user's locale.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) will be used for getting [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) and [android.content.pm.PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#). |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package name of the input method. |
| `appInfo` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)!:The [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#) of the input method. |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | a display name for this subtype. This value cannot be`null`. |

### getExtraValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtraValue(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The extra value of the subtype. |

### getExtraValueOf

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtraValueOf(key: String!): String!
```

The string of ExtraValue in subtype should be defined as follows: example: key0,key1=value1,key2,key3,key4=value4

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key of extra value |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The value of the specified key |

### getIconResId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIconResId(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Resource ID of the subtype icon drawable. |

### getLanguageTag

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLanguageTag(): String
```

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the BCP-47 Language Tag of the subtype. Returns an empty string when no Language Tag is specified. This value cannot be`null`. |

**See Also**

- [java.util.Locale#forLanguageTag(String)](https://developer.android.com/reference/kotlin/java/util/Locale.html#forLanguageTag(kotlin.String)) 

### getLayoutDisplayName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLayoutDisplayName(
    context: Context, 
    imeAppInfo: ApplicationInfo
): CharSequence
```

Returns the layout display name.

If`layoutLabelResource`is non-zero (specified through [setLayoutLabelResource](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.InputMethodSubtypeBuilder#setLayoutLabelResource(kotlin.Int))), the text generated from that resource will be returned. The localized string resource of the label should be capitalized for inclusion in UI lists.

If`layoutLabelResource`is zero, the framework returns the non-localized layout label, if specified through [setLayoutLabelNonLocalized](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.InputMethodSubtypeBuilder#setLayoutLabelNonLocalized(kotlin.CharSequence)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The context used for getting the [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#). This value cannot be`null`. |
| `imeAppInfo` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#):The [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#) of the input method. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the layout display name. This value cannot be`null`. |

### getLayoutLabelNonLocalized

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLayoutLabelNonLocalized(): CharSequence
```

Returns the non-localized layout label.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | This value cannot be`null`. |

### getLayoutLabelResource

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLayoutLabelResource(): Int
```

Returns the layout label string resource identifier. 

### getLocale

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocale(): String
```

**Deprecated:** *Use [getLanguageTag()](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype#getLanguageTag())instead.*

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The locale of the subtype. This method returns the "locale" string parameter passed to the constructor. This value cannot be`null`. |

### getMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMode(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The mode of the subtype. |

### getNameOverride

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNameOverride(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | The subtype's untranslatable name string. This value cannot be`null`. |

### getNameResId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNameResId(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Resource ID of the subtype name string. |

### getPhysicalKeyboardHintLanguageTag

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhysicalKeyboardHintLanguageTag(): ULocale?
```

Returns the physical keyboard BCP-47 language tag.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)? | This value may be`null`. |

**See Also**

- [android.view.inputmethod.InputMethodSubtype.InputMethodSubtypeBuilder#setPhysicalKeyboardHint](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.InputMethodSubtypeBuilder#setPhysicalKeyboardHint(android.icu.util.ULocale,%20kotlin.String)) 

### getPhysicalKeyboardHintLayoutType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhysicalKeyboardHintLayoutType(): String
```

Returns the physical keyboard layout type string.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

**See Also**

- [android.view.inputmethod.InputMethodSubtype.InputMethodSubtypeBuilder#setPhysicalKeyboardHint](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype.InputMethodSubtypeBuilder#setPhysicalKeyboardHint(android.icu.util.ULocale,%20kotlin.String)) 

### hashCode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isAsciiCapable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAsciiCapable(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this subtype is Ascii capable, false otherwise. If the subtype is ASCII capable, it should guarantee that the user can input ASCII characters with this subtype. This is important because many password fields only allow ASCII-characters. |

### isAuxiliary

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAuxiliary(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this subtype is auxiliary, false otherwise. An auxiliary subtype will not be shown in the list of enabled IMEs for choosing the current IME in the Settings even when this subtype is enabled. Please note that this subtype will still be shown in the list of IMEs in the IME switcher to allow the user to tentatively switch to this subtype while an IME is shown. The framework will never switch the current IME to this subtype by [android.view.inputmethod.InputMethodManager#switchToLastInputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#switchToLastInputMethod(android.os.IBinder)). The intent of having this flag is to allow for IMEs that are invoked in a one-shot way as auxiliary input mode, and return to the previous IME once it is finished (e.g. voice input). |

### overridesImplicitlyEnabledSubtype

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun overridesImplicitlyEnabledSubtype(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true when this subtype will be enabled by default if no other subtypes in the IME are enabled explicitly, false otherwise. Note that a subtype with this method returning true will not be shown in the list of subtypes in each IME's subtype enabler. Having an "automatic" subtype is an example use of this flag. |

### writeToParcel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InputMethodSubtype!>
```
