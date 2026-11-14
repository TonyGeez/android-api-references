# PrintDocumentInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintDocumentInfo

Kotlin| [Java](https://developer.android.com/reference/android/print/PrintDocumentInfo "View this page in Java") 

```
class PrintDocumentInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.print.PrintDocumentInfo](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#) |

This class encapsulates information about a document for printing purposes. This meta-data is used by the platform and print services, components that interact with printers. For example, this class contains the number of pages contained in the document it describes and this number of pages is shown to the user allowing them to select the range to print. Also a print service may optimize the printing process based on the content type, such as document or photo.

Instances of this class are created by the printing application and passed to the [PrintDocumentInfo, boolean)](https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.LayoutResultCallback#onLayoutFinished(android.print.PrintDocumentInfo,%20kotlin.Boolean))callback after successfully laying out the content which is performed in [PrintDocumentAdapter.LayoutResultCallback, android.os.Bundle)](https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)).

An example usage looks like this: 

```kotlin
. . .
 
  public void onLayout(PrintAttributes oldAttributes, PrintAttributes newAttributes,
          CancellationSignal cancellationSignal, LayoutResultCallback callback,
          Bundle metadata) {
 
         // Assume the app defined a LayoutResult class which contains
         // the layout result data and that the content is a document.
         LayoutResult result = doSomeLayoutWork();
 
         PrintDocumentInfo info = new PrintDocumentInfo
                 .Builder("printed_file.pdf")
                 .setContentType(PrintDocumentInfo.CONTENT_TYPE_DOCUMENT)
                 .setPageCount(result.getPageCount())
                 .build();
 
        callback.onLayoutFinished(info, result.getContentChanged());
    }
 
    . . .
 
  
```

<br />

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo.Builder) Builder for creating a [PrintDocumentInfo](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#). |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_DOCUMENT](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#CONTENT_TYPE_DOCUMENT:kotlin.Int) Content type: document. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_PHOTO](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#CONTENT_TYPE_PHOTO:kotlin.Int) Content type: photo. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#CONTENT_TYPE_UNKNOWN:kotlin.Int) Content type: unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAGE_COUNT_UNKNOWN](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#PAGE_COUNT_UNKNOWN:kotlin.Int) Constant for unknown page count. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContentType](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#getContentType())`()` Gets the content type. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDataSize](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#getDataSize())`()` Gets the document data size in bytes. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#getName())`()` Gets the document name. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageCount](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#getPageCount())`()` Gets the total number of pages. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PrintDocumentInfo](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CONTENT_TYPE_DOCUMENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_DOCUMENT: Int
```

Content type: document.

A print service may use normal paper to print the content instead of dedicated photo paper. Also it may use a lower quality printing process as the content is not as sensitive to print quality variation as a photo is. 

 Value: 0

### CONTENT_TYPE_PHOTO

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_PHOTO: Int
```

Content type: photo.

A print service may use dedicated photo paper to print the content instead of normal paper. Also it may use a higher quality printing process as the content is more sensitive to print quality variation than a document. 

 Value: 1

### CONTENT_TYPE_UNKNOWN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_UNKNOWN: Int
```

Content type: unknown. 

 Value: -1

### PAGE_COUNT_UNKNOWN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAGE_COUNT_UNKNOWN: Int
```

Constant for unknown page count. 

 Value: -1

## Public methods

### describeContents

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getContentType

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentType(): Int
```

Gets the content type.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The content type. |

**See Also**

- [#CONTENT_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#CONTENT_TYPE_UNKNOWN:kotlin.Int)
- [#CONTENT_TYPE_DOCUMENT](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#CONTENT_TYPE_DOCUMENT:kotlin.Int)
- [#CONTENT_TYPE_PHOTO](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#CONTENT_TYPE_PHOTO:kotlin.Int) 

### getDataSize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataSize(): Long
```

Gets the document data size in bytes.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The data size. Value is 0 or greater |

### getName

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Gets the document name. This name may be shown to the user.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The document name. This value cannot be`null`. |

### getPageCount

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPageCount(): Int
```

Gets the total number of pages.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of pages. Value is -1 or greater |

**See Also**

- [#PAGE_COUNT_UNKNOWN](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo#PAGE_COUNT_UNKNOWN:kotlin.Int) 

### hashCode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PrintDocumentInfo!>
```
