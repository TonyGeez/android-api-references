Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutofillValue

Kotlin | [Java](https://developer.android.com/reference/android/view/autofill/AutofillValue "View this page in Java")
| --- | --- |

```
class AutofillValue : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.autofill.AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#) |

Abstracts how a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be autofilled by an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#`.

Each `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` is associated with a `type`, as defined by `https://developer.android.com/reference/kotlin/android/view/View.html#getAutofillType()`.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| static [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#)! | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forDate(kotlin.Long)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` representing a date. |
| --- | --- |
| static [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#)! | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forList(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` representing a selection list. |
| static [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#)! | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forText(kotlin.CharSequence)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` representing a text field. |
| static [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#)! | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#forToggle(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` representing a toggable field. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#getDateValue()()` Gets the value to autofill a date field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#getListValue()()` Gets the value to autofill a selection list field. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#getTextValue()()` Gets the value to autofill a text field. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#getToggleValue()()` Gets the value to autofill a toggable field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#isDate()()` Checks if this is a date value. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#isList()()` Checks if this is a list value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#isText()()` Checks if this is a text value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#isToggle()()` Checks if this is a toggle value. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#)!\> | `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
|---|---|
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### forDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun forDate(value: Long): AutofillValue!
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` representing a date.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_DATE:kotlin.Int` for more info.

### forList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun forList(value: Int): AutofillValue!
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` representing a selection list.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_LIST:kotlin.Int` for more info.

### forText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun forText(value: CharSequence?): AutofillValue!
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` representing a text field.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_TEXT:kotlin.Int` for more info.

**Note:** This method is not thread safe and can throw an exception if the `value` is modified by a different thread before it returns.

| Parameters ||
|---|---|
| `value` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: This value may be `null`. |

### forToggle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun forToggle(value: Boolean): AutofillValue!
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue#` to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` representing a toggable field.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_TOGGLE:kotlin.Int` for more info.

### getDateValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDateValue(): Long
```

Gets the value to autofill a date field.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_DATE:kotlin.Int` for more info.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the value is not a date value |

### getListValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getListValue(): Int
```

Gets the value to autofill a selection list field.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_LIST:kotlin.Int` for more info.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the value is not a list value |

### getTextValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextValue(): CharSequence
```

Gets the value to autofill a text field.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_TEXT:kotlin.Int` for more info.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the value is not a text value |

### getToggleValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getToggleValue(): Boolean
```

Gets the value to autofill a toggable field.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_TOGGLE:kotlin.Int` for more info.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the value is not a toggle value |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDate(): Boolean
```

Checks if this is a date value.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_DATE:kotlin.Int` for more info.

### isList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isList(): Boolean
```

Checks if this is a list value.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_LIST:kotlin.Int` for more info.

### isText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isText(): Boolean
```

Checks if this is a text value.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_TEXT:kotlin.Int` for more info.

### isToggle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isToggle(): Boolean
```

Checks if this is a toggle value.

See `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_TOGGLE:kotlin.Int` for more info.

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AutofillValue!>
```
