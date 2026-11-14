# InlineSuggestionInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InlineSuggestionInfo

Kotlin| [Java](InlineSuggestionInfo.md) 
| --- | --- |

```
class InlineSuggestionInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.InlineSuggestionInfo](InlineSuggestionInfo.md) |

This class represents the description of an inline suggestion. It contains information to help the IME to decide where and when to show the suggestions. See [InlineSuggestion](InlineSuggestion.md) for more information.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SOURCE_AUTOFILL](InlineSuggestionInfo.md) Suggestion source: the suggestion is made by the user selected autofill service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SOURCE_PLATFORM](InlineSuggestionInfo.md) Suggestion source: the suggestion is made by the platform. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_ACTION](InlineSuggestionInfo.md) UI type: the UI contains an widget that will launch an intent when tapped. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_SUGGESTION](InlineSuggestionInfo.md) UI type: the UI contains an Autofill suggestion that will autofill the fields when tapped. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](InlineSuggestionInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](InlineSuggestionInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getAutofillHints](InlineSuggestionInfo.md))`()` Hints for the type of data being suggested. |
| --- | --- |
| [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md) | [getInlinePresentationSpec](InlineSuggestionInfo.md))`()` The presentation spec to which the inflated suggestion view abides. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getSource](InlineSuggestionInfo.md))`()` The source from which the suggestion is provided. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](InlineSuggestionInfo.md))`()` The type of the UI. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](InlineSuggestionInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPinned](InlineSuggestionInfo.md))`()` Whether the suggestion should be pinned or not. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](InlineSuggestionInfo.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](InlineSuggestionInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InlineSuggestionInfo](InlineSuggestionInfo.md)!\> | [CREATOR](InlineSuggestionInfo.md) <br /> |

## Constants

### SOURCE_AUTOFILL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_AUTOFILL: String
```

Suggestion source: the suggestion is made by the user selected autofill service. 
Value is [android.view.inputmethod.InlineSuggestionInfo#SOURCE_AUTOFILL](InlineSuggestionInfo.md), or [android.view.inputmethod.InlineSuggestionInfo#SOURCE_PLATFORM](InlineSuggestionInfo.md) 

 Value: "android:autofill"

### SOURCE_PLATFORM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_PLATFORM: String
```

Suggestion source: the suggestion is made by the platform. 
Value is [android.view.inputmethod.InlineSuggestionInfo#SOURCE_AUTOFILL](InlineSuggestionInfo.md), or [android.view.inputmethod.InlineSuggestionInfo#SOURCE_PLATFORM](InlineSuggestionInfo.md) 

 Value: "android:platform"

### TYPE_ACTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ACTION: String
```

UI type: the UI contains an widget that will launch an intent when tapped. 
Value is [android.view.inputmethod.InlineSuggestionInfo#TYPE_SUGGESTION](InlineSuggestionInfo.md), or [android.view.inputmethod.InlineSuggestionInfo#TYPE_ACTION](InlineSuggestionInfo.md) 

 Value: "android:autofill:action"

### TYPE_SUGGESTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SUGGESTION: String
```

UI type: the UI contains an Autofill suggestion that will autofill the fields when tapped. 
Value is [android.view.inputmethod.InlineSuggestionInfo#TYPE_SUGGESTION](InlineSuggestionInfo.md), or [android.view.inputmethod.InlineSuggestionInfo#TYPE_ACTION](InlineSuggestionInfo.md) 

 Value: "android:autofill:suggestion"

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getAutofillHints

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAutofillHints(): Array<String!>?
```

Hints for the type of data being suggested.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be`null`. |

### getInlinePresentationSpec

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInlinePresentationSpec(): InlinePresentationSpec
```

The presentation spec to which the inflated suggestion view abides.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md) | This value cannot be`null`. |

### getSource

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSource(): String
```

The source from which the suggestion is provided.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. Value is [android.view.inputmethod.InlineSuggestionInfo#SOURCE_AUTOFILL](InlineSuggestionInfo.md), or [android.view.inputmethod.InlineSuggestionInfo#SOURCE_PLATFORM](InlineSuggestionInfo.md) |

### getType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String
```

The type of the UI.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. Value is [android.view.inputmethod.InlineSuggestionInfo#TYPE_SUGGESTION](InlineSuggestionInfo.md), or [android.view.inputmethod.InlineSuggestionInfo#TYPE_ACTION](InlineSuggestionInfo.md) |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isPinned

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPinned(): Boolean
```

Whether the suggestion should be pinned or not. 

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InlineSuggestionInfo!>
```
