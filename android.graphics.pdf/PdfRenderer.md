# PdfRenderer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PdfRenderer

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/PdfRenderer "View this page in Java") 
| --- | --- |

```
class PdfRenderer : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.PdfRenderer](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#) |

This class enables rendering a PDF document and selecting, searching, fast scrolling, annotations, etc. from Android V. This class is thread safe and can be called by multiple threads however only one thread will be executed at a time as the access is synchronized by internal locking.

If you want to render a PDF, you create a renderer and for every page you want to render, you open the page, render it, and close the page. After you are done with rendering, you close the renderer. After the renderer is closed it should not be used anymore. Note that the pages are rendered one by one, i.e. you can have only a single page opened at any given time.

A typical use of the APIs to render a PDF looks like this: 

```kotlin
// create a new renderer
  PdfRenderer renderer = new PdfRenderer(getSeekableFileDescriptor());
 
  // let us just render all pages
  final int pageCount = renderer.getPageCount();
  for (int i = 0; i < pageCount; i++) {
      Page page = renderer.openPage(i);
 
      // say we render for showing on the screen
      page.render(mBitmap, null, null, Page.RENDER_MODE_FOR_DISPLAY);
 
      // do stuff with the bitmap
 
      // close the page
      page.close();
  }
 
  // close the renderer
  renderer.close();
  
```

### Print preview and print output

If you are using this class to rasterize a PDF for printing or show a print preview, it is recommended that you respect the following contract in order to provide a consistent user experience when seeing a preview and printing, i.e. the user sees a preview that is the same as the printout.

- Respect the property whether the document would like to be scaled for printing as per [shouldScaleForPrinting()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#shouldScaleForPrinting()).
- When scaling a document for printing the aspect ratio should be preserved.
- Do not inset the content with any margins from the [android.print.PrintAttributes](https://developer.android.com/reference/kotlin/android/print/PrintAttributes.html#) as the application is responsible to render it such that the margins are respected.
- If document page size is greater than the printed media size the content should be anchored to the upper left corner of the page for left-to-right locales and top right corner for right-to-left locales.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Page](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer.Page) This class represents a PDF document page for rendering. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOCUMENT_LINEARIZED_TYPE_LINEARIZED](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#DOCUMENT_LINEARIZED_TYPE_LINEARIZED:kotlin.Int) Represents a linearized PDF document. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED:kotlin.Int) Represents a non-linearized PDF document. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDF_FORM_TYPE_ACRO_FORM](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PDF_FORM_TYPE_ACRO_FORM:kotlin.Int) Represents a PDF with form fields specified using the AcroForm spec |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDF_FORM_TYPE_NONE](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PDF_FORM_TYPE_NONE:kotlin.Int) Represents a PDF without form fields |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDF_FORM_TYPE_XFA_FOREGROUND](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PDF_FORM_TYPE_XFA_FOREGROUND:kotlin.Int) Represents a PDF with form fields specified using the XFAF subset of the XFA spec |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDF_FORM_TYPE_XFA_FULL](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PDF_FORM_TYPE_XFA_FULL:kotlin.Int) Represents a PDF with form fields specified using the entire XFA spec |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfRenderer](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PdfRenderer(android.os.ParcelFileDescriptor))`(`fileDescriptor:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`)` Creates a new instance. |
| [PdfRenderer](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PdfRenderer(android.os.ParcelFileDescriptor,%20android.graphics.pdf.LoadParams))`(`fileDescriptor:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`, `params:` ` [LoadParams](https://developer.android.com/reference/kotlin/android/graphics/pdf/LoadParams)`)` Creates a new instance of PdfRenderer class. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#close())`()` Closes this renderer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDocumentLinearizationType](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#getDocumentLinearizationType())`()` Gets the type of the PDF document. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageCount](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#getPageCount())`()` Gets the number of pages in the document. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPdfFormType](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#getPdfFormType())`()` Returns the form type of the loaded PDF |
| [PdfRenderer.Page](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer.Page) | [openPage](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#openPage(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Opens a page for rendering. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldScaleForPrinting](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#shouldScaleForPrinting())`()` Gets whether the document prefers to be scaled for printing. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#write(android.os.ParcelFileDescriptor,%20kotlin.Boolean))`(`destination:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`, `removePasswordProtection:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Saves the current state of the loaded PDF document to the given writable [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#). |

| Protected methods ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#finalize())`()` <br /> |

## Constants

### DOCUMENT_LINEARIZED_TYPE_LINEARIZED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_LINEARIZED_TYPE_LINEARIZED: Int
```

Represents a linearized PDF document. 

 Value: 1

### DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED: Int
```

Represents a non-linearized PDF document. 

 Value: 0

### PDF_FORM_TYPE_ACRO_FORM

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDF_FORM_TYPE_ACRO_FORM: Int
```

Represents a PDF with form fields specified using the AcroForm spec 

 Value: 1

### PDF_FORM_TYPE_NONE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDF_FORM_TYPE_NONE: Int
```

Represents a PDF without form fields 

 Value: 0

### PDF_FORM_TYPE_XFA_FOREGROUND

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDF_FORM_TYPE_XFA_FOREGROUND: Int
```

Represents a PDF with form fields specified using the XFAF subset of the XFA spec 

 Value: 3

### PDF_FORM_TYPE_XFA_FULL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PDF_FORM_TYPE_XFA_FULL: Int
```

Represents a PDF with form fields specified using the entire XFA spec 

 Value: 2

## Public constructors

### PdfRenderer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PdfRenderer(fileDescriptor: ParcelFileDescriptor)
```

Creates a new instance.

**Note:** The provided file descriptor must be**seekable**, i.e. its data being randomly accessed, e.g. pointing to a file.

**Note:**This class takes ownership of the passed in file descriptor and is responsible for closing it when the renderer is closed.

If the file is from an untrusted source it is recommended to run the renderer in a separate, isolated process with minimal permissions to limit the impact of security exploits.**Note:** The constructor should be instantiated on the [android.annotation.WorkerThread](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#) as it can be long-running while loading the document.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileDescriptor` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):Seekable file descriptor to read from. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If an error occurs while reading the file. |
| `java.lang.SecurityException` | If the file requires a password or the security scheme is not supported. |
| `java.lang.IllegalArgumentException` | If the [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) is not seekable. |
| --- | --- |
| `java.lang.NullPointerException` | If the file descriptor is null. |

### PdfRenderer

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PdfRenderer(
    fileDescriptor: ParcelFileDescriptor, 
    params: LoadParams)
```

Creates a new instance of PdfRenderer class.

**Note:** The provided file descriptor must be**seekable** , i.e. its data being randomly accessed, e.g. pointing to a file. If the password passed in [android.graphics.pdf.LoadParams](https://developer.android.com/reference/kotlin/android/graphics/pdf/LoadParams) is incorrect, the [android.graphics.pdf.PdfRenderer](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#) will throw a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#).

**Note:**This class takes ownership of the passed in file descriptor and is responsible for closing it when the renderer is closed.

If the file is from an untrusted source it is recommended to run the renderer in a separate, isolated process with minimal permissions to limit the impact of security exploits.**Note:** The constructor should be instantiated on the [android.annotation.WorkerThread](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#) as it can be long-running while loading the document.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileDescriptor` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):Seekable file descriptor to read from. This value cannot be`null`. |
| `params` | [LoadParams](https://developer.android.com/reference/kotlin/android/graphics/pdf/LoadParams):Instance of [LoadParams](https://developer.android.com/reference/kotlin/android/graphics/pdf/LoadParams) specifying params for loading PDF document. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If an error occurs while reading the file. |
| `java.lang.SecurityException` | If the file requires a password or the security scheme is not supported by the renderer. |
| `java.lang.IllegalArgumentException` | If the [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) is not seekable. |
| --- | --- |
| `java.lang.NullPointerException` | If the file descriptor or load params is null. |

## Public methods

### close

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Closes this renderer. You should not use this instance after this method is called.

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.lang.IllegalStateException` | If [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#close())is called before invoking this or if any page is opened and not closed |

**See Also**

- [android.graphics.pdf.PdfRenderer.Page#close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer.Page#close()) 

### getDocumentLinearizationType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDocumentLinearizationType(): Int
```

Gets the type of the PDF document.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The PDF document type. Value is [android.graphics.pdf.PdfRenderer#DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED:kotlin.Int), or [android.graphics.pdf.PdfRenderer#DOCUMENT_LINEARIZED_TYPE_LINEARIZED](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#DOCUMENT_LINEARIZED_TYPE_LINEARIZED:kotlin.Int) |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#close())is called before invoking this. |

### getPageCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPageCount(): Int
```

Gets the number of pages in the document.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The page count. Value is 0 or greater |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#close())is called before invoking this. |

### getPdfFormType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPdfFormType(): Int
```

Returns the form type of the loaded PDF

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.pdf.PdfRenderer#PDF_FORM_TYPE_NONE](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PDF_FORM_TYPE_NONE:kotlin.Int), [android.graphics.pdf.PdfRenderer#PDF_FORM_TYPE_ACRO_FORM](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PDF_FORM_TYPE_ACRO_FORM:kotlin.Int), [android.graphics.pdf.PdfRenderer#PDF_FORM_TYPE_XFA_FULL](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PDF_FORM_TYPE_XFA_FULL:kotlin.Int), or [android.graphics.pdf.PdfRenderer#PDF_FORM_TYPE_XFA_FOREGROUND](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#PDF_FORM_TYPE_XFA_FOREGROUND:kotlin.Int) |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalStateException` | if the renderer is closed |
| `java.lang.IllegalArgumentException` | if an unexpected PDF form type is returned |

### openPage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openPage(index: Int): PdfRenderer.Page
```

Opens a page for rendering.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The page index to open, starting from index 0. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [PdfRenderer.Page](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer.Page) | A page that can be rendered. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#close())is called before invoking this. |
| `java.lang.IllegalArgumentException` | If the page number is less than 0 or greater than or equal to the total page count. |

**See Also**

- [android.graphics.pdf.PdfRenderer.Page#close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer.Page#close()) 

### shouldScaleForPrinting

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shouldScaleForPrinting(): Boolean
```

Gets whether the document prefers to be scaled for printing. You should take this info account if the document is rendered for printing and the target media size differs from the page size.

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If to scale the document. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#close())is called before invoking this. |

### write

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(
    destination: ParcelFileDescriptor, 
    removePasswordProtection: Boolean
): Unit
```

Saves the current state of the loaded PDF document to the given writable [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#). If the document is password-protected then setting`removePasswordProtection`removes the protection before saving. The PDF document should already be decrypted with the correct password before writing. Useful for printing or sharing.**Note:**This method closes the provided file descriptor.

| Parameters ||
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):The writable [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) This value cannot be`null`. |
| `removePasswordProtection` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, removes password protection from the PDF before saving. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If there's a write error, or if 'removePasswordSecurity' is`true`but the document remains encrypted. |
| `java.lang.IllegalStateException` | If [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer#close())is called before invoking this. |

## Protected methods

### finalize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
