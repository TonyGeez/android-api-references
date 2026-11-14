# FormWidgetInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# FormWidgetInfo

Kotlin| [Java](../android/graphics/pdf/models/FormWidgetInfo.md) 
| --- | --- |

```
class FormWidgetInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.models.FormWidgetInfo](../android/graphics/pdf/models/FormWidgetInfo.md) |

Information about a form widget of a PDF document.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/graphics/pdf/models/FormWidgetInfo.Builder.md) Builder for [FormWidgetInfo](../android/graphics/pdf/models/FormWidgetInfo.md) |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_CHECKBOX](../android/graphics/pdf/models/FormWidgetInfo.md) Represents a checkbox type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_COMBOBOX](../android/graphics/pdf/models/FormWidgetInfo.md) Represents a combobox type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_LISTBOX](../android/graphics/pdf/models/FormWidgetInfo.md) Represents a listbox type form widget |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_PUSHBUTTON](../android/graphics/pdf/models/FormWidgetInfo.md) Represents a push button type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_RADIOBUTTON](../android/graphics/pdf/models/FormWidgetInfo.md) Represents a radio button type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_SIGNATURE](../android/graphics/pdf/models/FormWidgetInfo.md) Represents a signature type form widget |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_TEXTFIELD](../android/graphics/pdf/models/FormWidgetInfo.md) Represents a text field type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_UNKNOWN](../android/graphics/pdf/models/FormWidgetInfo.md) Represents a form widget type that is unknown |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/graphics/pdf/models/FormWidgetInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/pdf/models/FormWidgetInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getAccessibilityLabel](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns the field's accessibility label, if present |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFontSize](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns the font size in pixels for text input, or 0 for text inputs without a specified font size and widgets that are not text inputs. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ListItem](../android/graphics/pdf/models/ListItem.md)!\> | [getListItems](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns the list of choice options in the order that it was passed in, or an empty list for widgets without choice options. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxLength](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns the maximum length of text supported by a text input widget, or -1 for text inputs without a maximum length and widgets that are not text inputs. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTextValue](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns the field's text value, if present |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetIndex](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns the index of the widget within the page's "Annot" array in the PDF document |
| [Rect](../android/graphics/Rect.md) | [getWidgetRect](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns the [Rect](../android/graphics/Rect.md) in page coordinates occupied by the widget |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetType](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns the type of this widget |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/pdf/models/FormWidgetInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEditableText](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns`true`if the widget is editable text |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMultiLineText](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns true if the widget supports multiple lines of text input |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMultiSelect](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns`true`if the widget supports selecting multiple values |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](../android/graphics/pdf/models/FormWidgetInfo.md))`()` Returns`true`if the widget is read-only |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/graphics/pdf/models/FormWidgetInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/graphics/pdf/models/FormWidgetInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [FormWidgetInfo](../android/graphics/pdf/models/FormWidgetInfo.md)!\> | [CREATOR](../android/graphics/pdf/models/FormWidgetInfo.md) <br /> |

## Constants

### WIDGET_TYPE_CHECKBOX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val WIDGET_TYPE_CHECKBOX: Int
```

Represents a checkbox type form widget 

 Value: 2

### WIDGET_TYPE_COMBOBOX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val WIDGET_TYPE_COMBOBOX: Int
```

Represents a combobox type form widget 

 Value: 4

### WIDGET_TYPE_LISTBOX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val WIDGET_TYPE_LISTBOX: Int
```

Represents a listbox type form widget 

 Value: 5

### WIDGET_TYPE_PUSHBUTTON

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val WIDGET_TYPE_PUSHBUTTON: Int
```

Represents a push button type form widget 

 Value: 1

### WIDGET_TYPE_RADIOBUTTON

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val WIDGET_TYPE_RADIOBUTTON: Int
```

Represents a radio button type form widget 

 Value: 3

### WIDGET_TYPE_SIGNATURE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val WIDGET_TYPE_SIGNATURE: Int
```

Represents a signature type form widget 

 Value: 7

### WIDGET_TYPE_TEXTFIELD

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val WIDGET_TYPE_TEXTFIELD: Int
```

Represents a text field type form widget 

 Value: 6

### WIDGET_TYPE_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val WIDGET_TYPE_UNKNOWN: Int
```

Represents a form widget type that is unknown 

 Value: 0

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAccessibilityLabel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getAccessibilityLabel(): String?
```

Returns the field's accessibility label, if present

**Note:**Comes from the "TU" value in the annotation dictionary, if present, or else the "T" value. See PDF Spec 1.7 Table 8.69

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getFontSize

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getFontSize(): Float
```

Returns the font size in pixels for text input, or 0 for text inputs without a specified font size and widgets that are not text inputs.

| Return ||
|--------------------------------------------------------------------------------|--------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is 0.0f or greater |

### getListItems

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getListItems(): MutableList<ListItem!>
```

Returns the list of choice options in the order that it was passed in, or an empty list for widgets without choice options.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ListItem](../android/graphics/pdf/models/ListItem.md)!> | This value cannot be`null`. |

### getMaxLength

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getMaxLength(): Int
```

Returns the maximum length of text supported by a text input widget, or -1 for text inputs without a maximum length and widgets that are not text inputs.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is -1 or greater |

### getTextValue

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getTextValue(): String?
```

Returns the field's text value, if present

**Note:** Comes from the "V" value in the annotation dictionary. See [PDF Spec 1.7 Table 8.69](https://opensource.adobe.com/dc-acrobat-sdk-docs/pdfstandards/pdfreference1.7old .pdf) Table 8.69

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getWidgetIndex

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getWidgetIndex(): Int
```

Returns the index of the widget within the page's "Annot" array in the PDF document

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### getWidgetRect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getWidgetRect(): Rect
```

Returns the [Rect](../android/graphics/Rect.md) in page coordinates occupied by the widget

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Rect](../android/graphics/Rect.md) | This value cannot be`null`. |

### getWidgetType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getWidgetType(): Int
```

Returns the type of this widget

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_UNKNOWN](../android/graphics/pdf/models/FormWidgetInfo.md), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_PUSHBUTTON](../android/graphics/pdf/models/FormWidgetInfo.md), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_CHECKBOX](../android/graphics/pdf/models/FormWidgetInfo.md), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_RADIOBUTTON](../android/graphics/pdf/models/FormWidgetInfo.md), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_COMBOBOX](../android/graphics/pdf/models/FormWidgetInfo.md), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_LISTBOX](../android/graphics/pdf/models/FormWidgetInfo.md), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_TEXTFIELD](../android/graphics/pdf/models/FormWidgetInfo.md), or [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_SIGNATURE](../android/graphics/pdf/models/FormWidgetInfo.md) |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isEditableText

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun isEditableText(): Boolean
```

Returns`true`if the widget is editable text 

### isMultiLineText

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun isMultiLineText(): Boolean
```

Returns true if the widget supports multiple lines of text input 

### isMultiSelect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun isMultiSelect(): Boolean
```

Returns`true`if the widget supports selecting multiple values 

### isReadOnly

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun isReadOnly(): Boolean
```

Returns`true`if the widget is read-only 

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<FormWidgetInfo!>
```
