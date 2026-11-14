# FormWidgetInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# FormWidgetInfo

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/models/FormWidgetInfo "View this page in Java") 

```
class FormWidgetInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.pdf.models.FormWidgetInfo](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#) |

Information about a form widget of a PDF document.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo.Builder) Builder for [FormWidgetInfo](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#) |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_CHECKBOX](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_CHECKBOX:kotlin.Int) Represents a checkbox type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_COMBOBOX](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_COMBOBOX:kotlin.Int) Represents a combobox type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_LISTBOX](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_LISTBOX:kotlin.Int) Represents a listbox type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_PUSHBUTTON](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_PUSHBUTTON:kotlin.Int) Represents a push button type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_RADIOBUTTON](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_RADIOBUTTON:kotlin.Int) Represents a radio button type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_SIGNATURE](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_SIGNATURE:kotlin.Int) Represents a signature type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_TEXTFIELD](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_TEXTFIELD:kotlin.Int) Represents a text field type form widget |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDGET_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_UNKNOWN:kotlin.Int) Represents a form widget type that is unknown |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getAccessibilityLabel](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#getAccessibilityLabel())`()` Returns the field's accessibility label, if present |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFontSize](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#getFontSize())`()` Returns the font size in pixels for text input, or 0 for text inputs without a specified font size and widgets that are not text inputs. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ListItem](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/ListItem)!\> | [getListItems](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#getListItems())`()` Returns the list of choice options in the order that it was passed in, or an empty list for widgets without choice options. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxLength](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#getMaxLength())`()` Returns the maximum length of text supported by a text input widget, or -1 for text inputs without a maximum length and widgets that are not text inputs. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTextValue](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#getTextValue())`()` Returns the field's text value, if present |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetIndex](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#getWidgetIndex())`()` Returns the index of the widget within the page's "Annot" array in the PDF document |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getWidgetRect](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#getWidgetRect())`()` Returns the [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) in page coordinates occupied by the widget |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetType](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#getWidgetType())`()` Returns the type of this widget |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEditableText](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#isEditableText())`()` Returns`true`if the widget is editable text |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMultiLineText](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#isMultiLineText())`()` Returns true if the widget supports multiple lines of text input |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMultiSelect](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#isMultiSelect())`()` Returns`true`if the widget supports selecting multiple values |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#isReadOnly())`()` Returns`true`if the widget is read-only |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [FormWidgetInfo](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ListItem](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/ListItem)!> | This value cannot be`null`. |

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

Returns the [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) in page coordinates occupied by the widget

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | This value cannot be`null`. |

### getWidgetType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getWidgetType(): Int
```

Returns the type of this widget

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_UNKNOWN:kotlin.Int), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_PUSHBUTTON](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_PUSHBUTTON:kotlin.Int), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_CHECKBOX](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_CHECKBOX:kotlin.Int), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_RADIOBUTTON](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_RADIOBUTTON:kotlin.Int), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_COMBOBOX](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_COMBOBOX:kotlin.Int), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_LISTBOX](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_LISTBOX:kotlin.Int), [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_TEXTFIELD](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_TEXTFIELD:kotlin.Int), or [android.graphics.pdf.models.FormWidgetInfo#WIDGET_TYPE_SIGNATURE](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/FormWidgetInfo#WIDGET_TYPE_SIGNATURE:kotlin.Int) |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<FormWidgetInfo!>
```
