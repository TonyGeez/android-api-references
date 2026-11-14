# InlinePresentation

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InlinePresentation

Kotlin| [Java](InlinePresentation.md) 
| --- | --- |

```
class InlinePresentation : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.InlinePresentation](InlinePresentation.md) |

Wrapper class holding a [Slice](../android.app.slice/Slice.md) and an [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md) for rendering UI for an Inline Suggestion.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InlinePresentation](InlinePresentation.md))`(`slice:` ` [Slice](../android.app.slice/Slice.md)`, `inlinePresentationSpec:` ` [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md)`, `pinned:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new InlinePresentation. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [InlinePresentation](InlinePresentation.md) | [createTooltipPresentation](InlinePresentation.md))`(`slice:` ` [Slice](../android.app.slice/Slice.md)`, `spec:` ` [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md)`)` Creates a presentation for the inline suggestion tooltip |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](InlinePresentation.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](InlinePresentation.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md) | [getInlinePresentationSpec](InlinePresentation.md))`()` Specifies the UI specification for the inline suggestion. |
| [Slice](../android.app.slice/Slice.md) | [getSlice](InlinePresentation.md))`()` Represents the UI content and the action for the inline suggestion. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](InlinePresentation.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPinned](InlinePresentation.md))`()` Indicates whether the UI should be pinned, hence non-scrollable and non-filterable, in the host. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](InlinePresentation.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](InlinePresentation.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InlinePresentation](InlinePresentation.md)!\> | [CREATOR](InlinePresentation.md) <br /> |

## Public constructors

### InlinePresentation

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InlinePresentation(
    slice: Slice, 
    inlinePresentationSpec: InlinePresentationSpec, 
    pinned: Boolean)
```

Creates a new InlinePresentation.

| Parameters ||
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `slice` | [Slice](../android.app.slice/Slice.md):Represents the UI content and the action for the inline suggestion. The Slice should be constructed using the Content builder provided in the androidx autofill library e.g.`androidx.autofill.inline.v1.InlineSuggestionUi.Content.Builder`and then converted to a Slice with`androidx.autofill.inline.UiVersions.Content#getSlice()`. This value cannot be`null`. |
| `inlinePresentationSpec` | [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md):Specifies the UI specification for the inline suggestion. This value cannot be`null`. |
| `pinned` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Indicates whether the UI should be pinned, hence non-scrollable and non-filterable, in the host. However, it's eventually up to the host whether the UI is pinned or not. Also a [Dataset](Dataset.md) with a pinned inline presentation will not be replaced by the new data set returned from authentication intent. See [Dataset.Builder.setAuthentication(android.content.IntentSender)](../android/service/autofill/Dataset.Builder.md))for more information. |
| --- | --- |

## Public methods

### createTooltipPresentation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createTooltipPresentation(
    slice: Slice, 
    spec: InlinePresentationSpec
): InlinePresentation
```

Creates a presentation for the inline suggestion tooltip

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `slice` | [Slice](../android.app.slice/Slice.md):Represents the UI content and the action for the inline suggestion tooltip. This value cannot be`null`. |
| `spec` | [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md):Specifies the UI specification for the inline suggestion tooltip. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InlinePresentation](InlinePresentation.md) | An [InlinePresentation](InlinePresentation.md) for the inline suggestion tooltip This value cannot be`null`. |

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

### getInlinePresentationSpec

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInlinePresentationSpec(): InlinePresentationSpec
```

Specifies the UI specification for the inline suggestion.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md) | This value cannot be`null`. |

### getSlice

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlice(): Slice
```

Represents the UI content and the action for the inline suggestion.

The Slice should be constructed using the Content builder provided in the androidx autofill library e.g.`androidx.autofill.inline.v1.InlineSuggestionUi.Content.Builder`and then converted to a Slice with`androidx.autofill.inline.UiVersions.Content#getSlice()`.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [Slice](../android.app.slice/Slice.md) | This value cannot be`null`. |

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

Indicates whether the UI should be pinned, hence non-scrollable and non-filterable, in the host. However, it's eventually up to the host whether the UI is pinned or not.

Also a [Dataset](Dataset.md) with a pinned inline presentation will not be replaced by the new data set returned from authentication intent. See [Dataset.Builder.setAuthentication(android.content.IntentSender)](../android/service/autofill/Dataset.Builder.md))for more information. 

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
static val CREATOR: Parcelable.Creator<InlinePresentation!>
```
