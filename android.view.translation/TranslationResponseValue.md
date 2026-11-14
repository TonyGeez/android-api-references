# TranslationResponseValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationResponseValue

Kotlin | [Java](https://developer.android.com/reference/android/view/translation/TranslationResponseValue "View this page in Java") 

```
class TranslationResponseValue : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.translation.TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#) |

A translated response value from translation service.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue.Builder) A builder for [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#) |

| Constants ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEFINITIONS](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#EXTRA_DEFINITIONS:kotlin.String) Name in the result of [getExtras()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#getExtras()) to pass dictionary definitions of the text categorized by parts of speech. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ERROR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#STATUS_ERROR:kotlin.Int) This value was not successfully translated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#STATUS_SUCCESS:kotlin.Int) This value was successfully translated. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#) | [forError](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#forError())`()` Creates a [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#) with the [STATUS_ERROR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#STATUS_ERROR:kotlin.Int) result; |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getExtras](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#getExtras())`()` Extra results associated with the translated text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatusCode](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#getStatusCode())`()` The status code of this [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#). |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getText](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#getText())`()` The translated text result. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTransliteration](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#getTransliteration())`()` The transliteration result of the translated text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### EXTRA_DEFINITIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEFINITIONS: String
```

Name in the result of [getExtras()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#getExtras()) to pass dictionary definitions of the text categorized by parts of speech.

The dictionary definitions consists of groups of terms keyed by their corresponding parts of speech. This map-like structure is stored in a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#). The individual parts of speech can be traversed by [Bundle.keySet()](https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#keySet()) and used to get the corresponding list of terms as [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) s.

- "noun" -\> \["def1", "def2", ...\]
- "verb" -\> \["def3", "def4", ...\]
- ...

The set of parts of speech can then be used by [Bundle.getCharSequenceArrayList(String)](https://developer.android.com/reference/kotlin/android/os/Bundle.html#getCharSequenceArrayList(kotlin.String)) to get the list of terms. **Example** : `for (String partOfSpeech : extras.getBundle(EXTRA_DEFINITIONS).keySet()) { ArrayList<CharSequence> terms = extras.getBundle(EXTRA_DEFINITIONS).getCharSequenceArrayList(partOfSpeech); ... }`

<br />

 Value: "android.view.translation.extra.DEFINITIONS"

### STATUS_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ERROR: Int
```

This value was not successfully translated. No value can be obtained with [getText()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#getText()). 

 Value: 1

### STATUS_SUCCESS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_SUCCESS: Int
```

This value was successfully translated. 

 Value: 0

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### forError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun forError(): TranslationResponseValue
```

Creates a [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#) with the [STATUS_ERROR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#STATUS_ERROR:kotlin.Int) result;

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#) | This value cannot be `null`. |

### getExtras

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle
```

Extra results associated with the translated text.

The bundle includes [EXTRA_DEFINITIONS](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#EXTRA_DEFINITIONS:kotlin.String), obtained by [Bundle.getBundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#getBundle(kotlin.String)).

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be `null`. |

### getStatusCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatusCode(): Int
```

The status code of this [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#).

If the status code is [STATUS_ERROR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#STATUS_ERROR:kotlin.Int), no values are attached, and all getters will return `null`.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.translation.TranslationResponseValue#STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#STATUS_SUCCESS:kotlin.Int), or [android.view.translation.TranslationResponseValue#STATUS_ERROR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#STATUS_ERROR:kotlin.Int) |

### getText

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getText(): CharSequence?
```

The translated text result.

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be `null`. |

### getTransliteration

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransliteration(): CharSequence?
```

The transliteration result of the translated text.

This returns a CharSequence representation of the transliteration of the translated text.

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be `null`. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TranslationResponseValue!>
```
