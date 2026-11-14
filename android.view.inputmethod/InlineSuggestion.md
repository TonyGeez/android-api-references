Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InlineSuggestion

Kotlin | [Java](https://developer.android.com/reference/android/view/inputmethod/InlineSuggestion "View this page in Java")
| --- | --- |

```
class InlineSuggestion : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.InlineSuggestion](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#) |

This class represents an inline suggestion which is made by one app and can be embedded into the UI of another. Suggestions may contain sensitive information not known to the host app which needs to be protected from spoofing. To address that the suggestion view inflated on demand for embedding is created in such a way that the hosting app cannot introspect its content and cannot interact with it.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [InlineSuggestionInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionInfo) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#getInfo()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#hashCode()()` Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#inflate(android.content.Context,%20android.util.Size,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, size: https://developer.android.com/reference/kotlin/android/util/Size.html#, callbackExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/widget/inline/InlineContentView.html#!>)` Inflates a view with the content of this suggestion at a specific size. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [InlineSuggestion](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInfo(): InlineSuggestionInfo
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionInfo` | This value cannot be `null`. |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### inflate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun inflate(
    context: Context, 
    size: Size, 
    callbackExecutor: Executor, 
    callback: Consumer<InlineContentView!>
): Unit
```

Inflates a view with the content of this suggestion at a specific size.

Each dimension of the size must satisfy one of the following conditions:

1. between `https://developer.android.com/reference/kotlin/android/widget/inline/InlinePresentationSpec.html#getMinSize()` and `https://developer.android.com/reference/kotlin/android/widget/inline/InlinePresentationSpec.html#getMaxSize()` of the presentation spec from `mInfo`
2. `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int`

If the size is set to `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int`, then the size of the inflated view will be just large enough to fit the content, while still conforming to the min / max size specified by the `https://developer.android.com/reference/kotlin/android/widget/inline/InlinePresentationSpec.html#`.

The caller can attach an `https://developer.android.com/reference/kotlin/android/view/View.OnClickListener.html#` and/or an `https://developer.android.com/reference/kotlin/android/view/View.OnLongClickListener.html#` to the view in the `callback` to receive click and long click events on the view.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): Context in which to inflate the view. This value cannot be `null`. |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#): The size at which to inflate the suggestion. For each dimension, it maybe an exact value or `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int`. This value cannot be `null`. |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [InlineContentView](https://developer.android.com/reference/kotlin/android/widget/inline/InlineContentView.html#)!\>: Callback for receiving the inflated view, where the `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#` of the view is set as the actual size of the underlying remote view. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If an invalid argument is passed. |
| `java.lang.IllegalStateException` | If this method is already called. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

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
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<InlineSuggestion!>
```
