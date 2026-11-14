Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassificationContext

Kotlin | [Java](../android/view/textclassifier/TextClassificationContext.md)
| --- | --- |

```
class TextClassificationContext : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.TextClassificationContext](../android/view/textclassifier/TextClassificationContext.md) |

A representation of the context in which text classification would be performed.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext.Builder` A builder for building a TextClassification context. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext#getPackageName()()` Returns the package name of the app that this context originated in. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext#getWidgetType()()` Returns the widget type for this classification context. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext#getWidgetVersion()()` Returns a custom version string for the widget type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TextClassificationContext](../android/view/textclassifier/TextClassificationContext.md)!\> | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getPackageName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String
```

Returns the package name of the app that this context originated in.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getWidgetType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidgetType(): String
```

Returns the widget type for this classification context.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_TEXTVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_EDITTEXT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_UNSELECTABLE_TEXTVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_WEBVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_EDIT_WEBVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_TEXTVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_EDITTEXT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_UNSELECTABLE_TEXTVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_NOTIFICATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CLIPBOARD:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_UNKNOWN:kotlin.String` |

### getWidgetVersion

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidgetVersion(): String?
```

Returns a custom version string for the widget type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext#getWidgetType()`

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TextClassificationContext!>
```
