# PdfRendererPreV

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# PdfRendererPreV

Kotlin| [Java](PdfRendererPreV.md) 
| --- | --- |

```
class PdfRendererPreV : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.PdfRendererPreV](PdfRendererPreV.md) |

This class enables rendering a PDF document and selecting, searching, fast scrolling, annotations, etc from Android R till Android U. This class is thread safe and can be called by multiple threads however only one thread will be executed at a time as the access is synchronized by internal locking.

If you want to render a PDF, you will need to create a new instance of renderer for each document. To render each page, you open the page using the renderer instance created earlier, render it, and close the page. After you are done with rendering, you close the renderer. After the renderer is closed it should not be used anymore. Note that the pages are rendered one by one, i.e. you can have only a single page opened at any given time.

A typical use of the APIs to render a PDF looks like this: 

```kotlin
// create a new renderer
  try (PdfRendererPreV renderer = new PdfRendererPreV(getSeekableFileDescriptor(), loadParams)) {
       // let us just render all pages
       final int pageCount = renderer.getPageCount();
       for (int i = 0; i < pageCount; i++) {
           Page page = renderer.openPage(i);
           RenderParams params = new RenderParams.Builder(Page.RENDER_MODE_FOR_DISPLAY).build();
 
           // say we render for showing on the screen
           page.render(mBitmap, params, null, null);
 
           // do stuff with the bitmap
 
           // close the page
           page.close();
       }
  }
  
```

### Print preview and print output

Please refer to [PdfRenderer](PdfRenderer.md) for fulfilling this usecase.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Page](../android/graphics/pdf/PdfRendererPreV.Page.md) This class represents a PDF document page for rendering. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOCUMENT_LINEARIZED_TYPE_LINEARIZED](PdfRendererPreV.md) Represents a linearized PDF document. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED](PdfRendererPreV.md) Represents a non-linearized PDF document. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDF_FORM_TYPE_ACRO_FORM](PdfRendererPreV.md) Represents a PDF with form fields specified using the AcroForm spec |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDF_FORM_TYPE_NONE](PdfRendererPreV.md) Represents a PDF without form fields |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDF_FORM_TYPE_XFA_FOREGROUND](PdfRendererPreV.md) Represents a PDF with form fields specified using the XFAF subset of the XFA spec |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PDF_FORM_TYPE_XFA_FULL](PdfRendererPreV.md) Represents a PDF with form fields specified using the entire XFA spec |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfRendererPreV](PdfRendererPreV.md))`(`fileDescriptor:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`)` Creates a new instance of PdfRendererPreV class. |
| [PdfRendererPreV](PdfRendererPreV.md))`(`fileDescriptor:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`, `params:` ` [LoadParams](LoadParams.md)`)` Creates a new instance of PdfRendererPreV class. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](PdfRendererPreV.md))`()` Closes this renderer and destroys any cached instance of the document. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDocumentLinearizationType](PdfRendererPreV.md))`()` Gets the type of the PDF document. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageCount](PdfRendererPreV.md))`()` Gets the number of pages in the document. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPdfFormType](PdfRendererPreV.md))`()` Returns the form type of the loaded PDF |
| [PdfRendererPreV.Page](../android/graphics/pdf/PdfRendererPreV.Page.md) | [openPage](PdfRendererPreV.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Opens a [Page](../android/graphics/pdf/PdfRendererPreV.Page.md) for rendering. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](PdfRendererPreV.md))`(`destination:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`, `removePasswordProtection:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Saves the current state of the loaded PDF document to the given writable [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md). |
| --- | --- |

| Protected methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](PdfRendererPreV.md))`()` <br /> |

## Constants

### DOCUMENT_LINEARIZED_TYPE_LINEARIZED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val DOCUMENT_LINEARIZED_TYPE_LINEARIZED: Int
```

Represents a linearized PDF document. 

 Value: 1

### DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED: Int
```

Represents a non-linearized PDF document. 

 Value: 0

### PDF_FORM_TYPE_ACRO_FORM

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val PDF_FORM_TYPE_ACRO_FORM: Int
```

Represents a PDF with form fields specified using the AcroForm spec 

 Value: 1

### PDF_FORM_TYPE_NONE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val PDF_FORM_TYPE_NONE: Int
```

Represents a PDF without form fields 

 Value: 0

### PDF_FORM_TYPE_XFA_FOREGROUND

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val PDF_FORM_TYPE_XFA_FOREGROUND: Int
```

Represents a PDF with form fields specified using the XFAF subset of the XFA spec 

 Value: 3

### PDF_FORM_TYPE_XFA_FULL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val PDF_FORM_TYPE_XFA_FULL: Int
```

Represents a PDF with form fields specified using the entire XFA spec 

 Value: 2

## Public constructors

### PdfRendererPreV

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
PdfRendererPreV(fileDescriptor: ParcelFileDescriptor)
```

Creates a new instance of PdfRendererPreV class.

**Note:** The provided file descriptor must be**seekable**, i.e. its data being randomly accessed, e.g. pointing to a file.

**Note:**This class takes ownership of the passed in file descriptor and is responsible for closing it when the renderer is closed.

If the file is from an untrusted source it is recommended to run the renderer in a separate, isolated process with minimal permissions to limit the impact of security exploits.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileDescriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):Seekable file descriptor to read from. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If an error occurs while reading the file. |
| `java.lang.SecurityException` | If the file requires a password or the security scheme is not supported by the renderer. |
| `java.lang.IllegalArgumentException` | If the [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) is not seekable. |
| --- | --- |
| `java.lang.NullPointerException` | If the file descriptor is null. |

### PdfRendererPreV

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
PdfRendererPreV(
    fileDescriptor: ParcelFileDescriptor, 
    params: LoadParams)
```

Creates a new instance of PdfRendererPreV class.

**Note:** The provided file descriptor must be**seekable** , i.e. its data being randomly accessed, e.g. pointing to a file. If the password passed in [android.graphics.pdf.LoadParams](LoadParams.md) is incorrect, the [android.graphics.pdf.PdfRendererPreV](PdfRendererPreV.md) will throw a [SecurityException](../java.lang/SecurityException.md).

**Note:**This class takes ownership of the passed in file descriptor and is responsible for closing it when the renderer is closed.

If the file is from an untrusted source it is recommended to run the renderer in a separate, isolated process with minimal permissions to limit the impact of security exploits.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileDescriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):Seekable file descriptor to read from. This value cannot be`null`. |
| `params` | [LoadParams](LoadParams.md):Instance of [LoadParams](LoadParams.md) specifying params for loading PDF document. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If an error occurs while reading the file. |
| `java.lang.SecurityException` | If the file requires a password or the security scheme is not supported by the renderer. |
| `java.lang.IllegalArgumentException` | If the [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) is not seekable. |
| --- | --- |
| `java.lang.NullPointerException` | If the file descriptor or load params is null. |

## Public methods

### close

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Closes this renderer and destroys any cached instance of the document. You should not use this instance after this method is called.

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.lang.IllegalStateException` | If [close()](PdfRendererPreV.md))is called before invoking this. |

### getDocumentLinearizationType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getDocumentLinearizationType(): Int
```

Gets the type of the PDF document.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The PDF document type. Value is [android.graphics.pdf.PdfRendererPreV#DOCUMENT_LINEARIZED_TYPE_NON_LINEARIZED](PdfRendererPreV.md), or [android.graphics.pdf.PdfRendererPreV#DOCUMENT_LINEARIZED_TYPE_LINEARIZED](PdfRendererPreV.md) |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If [close()](PdfRendererPreV.md))is called before invoking this. |

### getPageCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getPageCount(): Int
```

Gets the number of pages in the document.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The page count. Value is 0 or greater |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If [close()](PdfRendererPreV.md))is called before invoking this. |

### getPdfFormType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getPdfFormType(): Int
```

Returns the form type of the loaded PDF

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.pdf.PdfRendererPreV#PDF_FORM_TYPE_NONE](PdfRendererPreV.md), [android.graphics.pdf.PdfRendererPreV#PDF_FORM_TYPE_ACRO_FORM](PdfRendererPreV.md), [android.graphics.pdf.PdfRendererPreV#PDF_FORM_TYPE_XFA_FULL](PdfRendererPreV.md), or [android.graphics.pdf.PdfRendererPreV#PDF_FORM_TYPE_XFA_FOREGROUND](PdfRendererPreV.md) |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalStateException` | if the renderer is closed |
| `java.lang.IllegalArgumentException` | if an unexpected PDF form type is returned |

### openPage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun openPage(index: Int): PdfRendererPreV.Page
```

Opens a [Page](../android/graphics/pdf/PdfRendererPreV.Page.md) for rendering.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The page index to open, starting from index 0. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [PdfRendererPreV.Page](../android/graphics/pdf/PdfRendererPreV.Page.md) | A page that can be rendered. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If [close()](PdfRendererPreV.md))is called before invoking this. |
| `java.lang.IllegalArgumentException` | If the page number is less than 0 or greater than or equal to the total page count. |

### write

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun write(
    destination: ParcelFileDescriptor, 
    removePasswordProtection: Boolean
): Unit
```

Saves the current state of the loaded PDF document to the given writable [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md). If the document is password-protected then setting`removePasswordProtection`removes the protection before saving. The PDF document should already be decrypted with the correct password before writing. Useful for printing or sharing.**Note:**This method closes the provided file descriptor.

| Parameters ||
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):The writable [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) This value cannot be`null`. |
| `removePasswordProtection` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, removes password protection from the PDF before saving. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If there's a write error, or if 'removePasswordSecurity' is`true`but the document remains encrypted. |
| `java.lang.IllegalStateException` | If [close()](PdfRendererPreV.md))is called before invoking this. |

## Protected methods

### finalize

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
