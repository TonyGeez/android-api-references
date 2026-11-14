Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PictureInPictureParams

```
class PictureInPictureParams : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.PictureInPictureParams](PictureInPictureParams.md) |

Represents a set of parameters used to initialize and update an Activity in picture-in-picture mode.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#` objects. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RemoteAction](RemoteAction.md)!\> | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getActions()()` Returns the list of user actions that are associated with the activity when in picture-in-picture mode. |
| --- | --- |
| [Rational](../android.util/Rational.md)? | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getAspectRatio()()` Returns the expected aspect ratio of the picture-in-picture window. |
| [RemoteAction](RemoteAction.md)? | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getCloseAction()()` Returns the action that is to replace the system close action. |
| [Rational](../android.util/Rational.md)? | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getExpandedAspectRatio()()` Returns the desired aspect ratio of the expanded picture-in-picture window. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RemoteAction](RemoteAction.md)!\> | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getOverlayActions()()` Returns the set of overlay actions that are associated with the activity when in picture-in-picture mode. |
| [RemoteAction](RemoteAction.md)? | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getPrimaryAction()()` Returns the action that is to be used as the primary action in the PiP menu. |
| [RemoteAction](RemoteAction.md)? | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getPrimaryOverlayAction()()` Returns the primary overlay action that is associated with the activity when in picture-in-picture mode. |
| --- | --- |
| [Rect](../android.graphics/Rect.md)? | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getSourceRectHint()()` Returns the source rect hint. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getSubtitle()()` Returns the subtitle of the picture-in-picture window that may be displayed to the user. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#getTitle()()` Returns the title of the picture-in-picture window that may be displayed to the user. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#isAutoEnterEnabled()()` Returns whether auto enter picture-in-picture is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#isSeamlessResizeEnabled()()` Returns whether seamless resize is enabled. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PictureInPictureParams](PictureInPictureParams.md)!\> | `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams#CREATOR:android.os.Parcelable.Creator` <br /> |

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
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getActions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getActions(): MutableList<RemoteAction!>
```

Returns the list of user actions that are associated with the activity when in picture-in-picture mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/RemoteAction!>` | the user actions in a new list. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setActions(kotlin.collections.MutableList)`

### getAspectRatio

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAspectRatio(): Rational?
```

Returns the expected aspect ratio of the picture-in-picture window.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Rational.html#?` | aspect ratio as the desired width / height or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setAspectRatio(android.util.Rational)`

### getCloseAction

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCloseAction(): RemoteAction?
```

Returns the action that is to replace the system close action.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/RemoteAction?` | the close action or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setCloseAction(android.app.RemoteAction)`

### getExpandedAspectRatio

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExpandedAspectRatio(): Rational?
```

Returns the desired aspect ratio of the expanded picture-in-picture window.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Rational.html#?` | aspect ratio as the desired width / height or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setExpandedAspectRatio(android.util.Rational)`

### getOverlayActions

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOverlayActions(): MutableList<RemoteAction!>
```

Returns the set of overlay actions that are associated with the activity when in picture-in-picture mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/RemoteAction!>` | the overlay actions in a new list. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setOverlayActions(kotlin.collections.MutableList,%20android.app.RemoteAction)`

### getPrimaryAction

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPrimaryAction(): RemoteAction?
```

Returns the action that is to be used as the primary action in the PiP menu.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/RemoteAction?` | the primary action or `null` if not set. |

**See Also**

### getPrimaryOverlayAction

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPrimaryOverlayAction(): RemoteAction?
```

Returns the primary overlay action that is associated with the activity when in picture-in-picture mode.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/RemoteAction?` | the primary overlay action or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setOverlayActions(kotlin.collections.MutableList,%20android.app.RemoteAction)`

### getSourceRectHint

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSourceRectHint(): Rect?
```

Returns the source rect hint.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?` | the source rect hint also known as launch bounds or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setSourceRectHint(android.graphics.Rect)`

### getSubtitle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubtitle(): CharSequence?
```

Returns the subtitle of the picture-in-picture window that may be displayed to the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | subtitle of the picture-in-picture window. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setSubtitle(kotlin.CharSequence)`

### getTitle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTitle(): CharSequence?
```

Returns the title of the picture-in-picture window that may be displayed to the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | title of the picture-in-picture window. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setTitle(kotlin.CharSequence)`

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

### isAutoEnterEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAutoEnterEnabled(): Boolean
```

Returns whether auto enter picture-in-picture is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the system will automatically put the activity in picture-in-picture mode. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setAutoEnterEnabled(kotlin.Boolean)`

### isSeamlessResizeEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSeamlessResizeEnabled(): Boolean
```

Returns whether seamless resize is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the system can seamlessly resize the window while activity is in picture-in-picture mode. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setSeamlessResizeEnabled(kotlin.Boolean)`

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
    out: Parcel, 
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
static val CREATOR: Parcelable.Creator<PictureInPictureParams!>
```
