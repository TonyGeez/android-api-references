# PrintedPdfDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintedPdfDocument

Kotlin| [Java](https://developer.android.com/reference/android/print/pdf/PrintedPdfDocument "View this page in Java") 
| --- | --- |

```
open class PrintedPdfDocument : PdfDocument
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.PdfDocument](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#) ||
| | ↳ | [android.print.pdf.PrintedPdfDocument](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#) |

This class is a helper for creating a PDF file for given print attributes. It is useful for implementing printing via the native Android graphics APIs.

This class computes the page width, page height, and content rectangle from the provided print attributes and these precomputed values can be accessed via [getPageWidth()](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#getPageWidth()), [getPageHeight()](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#getPageHeight()), and [getPageContentRect()](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#getPageContentRect()), respectively. The [startPage(int)](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#startPage(kotlin.Int))methods creates pages whose [PageInfo](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo.html#) is initialized with the precomputed values for width, height, and content rectangle.

A typical use of the APIs looks like this: 

```kotlin
// open a new document
  PrintedPdfDocument document = new PrintedPdfDocument(context,
          printAttributes);
 
  // start a page
  Page page = document.startPage(0);
 
  // draw something on the page
  View content = getContentView();
  content.draw(page.getCanvas());
 
  // finish the page
  document.finishPage(page);
  . . .
  // add more pages
  . . .
  // write the document content
  document.writeTo(getOutputStream());
 
  //close the document
  document.close();
  
```

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrintedPdfDocument](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#PrintedPdfDocument(android.content.Context,%20android.print.PrintAttributes))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `attributes:` ` [PrintAttributes](https://developer.android.com/reference/kotlin/android/print/PrintAttributes.html#)`)` Creates a new document. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getPageContentRect](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#getPageContentRect())`()` Gets the content rectangle. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageHeight](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#getPageHeight())`()` Gets the page height. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageWidth](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#getPageWidth())`()` Gets the page width. |
| --- | --- |
| open [PdfDocument.Page](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page.html#) | [startPage](https://developer.android.com/reference/kotlin/android/print/pdf/PrintedPdfDocument#startPage(kotlin.Int))`(`pageNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Starts a new page. |

| Inherited functions ||
|---|---|
| From class [PdfDocument](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#close())`()` <br /> Closes this document. This method should be called after you are done working with the document. After this call the document is considered closed and none of its methods should be called. **Note:** Do not call this method if the page returned by [startPage(android.graphics.pdf.PdfDocument.PageInfo)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#startPage(android.graphics.pdf.PdfDocument.PageInfo))is not finished by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finishPage(android.graphics.pdf.PdfDocument.Page)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finalize())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finishPage](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finishPage(android.graphics.pdf.PdfDocument.Page))`(`page:` ` [PdfDocument.Page](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page.html#)!`)` <br /> Finishes a started page. You should always finish the last started page. **Note:** Do not call this method after [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#close()). You should not finish the same page more than once. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PdfDocument.PageInfo](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo.html#)!>! | [getPages](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#getPages())`()` <br /> Gets the pages of the document. <br /> | | [PdfDocument.Page](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page.html#)! | [startPage](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#startPage(android.graphics.pdf.PdfDocument.PageInfo))`(`pageInfo:` ` [PdfDocument.PageInfo](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo.html#)!`)` <br /> Starts a page using the provided [PageInfo](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo.html#). After the page is created you can draw arbitrary content on the page's canvas which you can get by calling [Page.getCanvas()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page.html#getCanvas()). After you are done drawing the content you should finish the page by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finishPage(android.graphics.pdf.PdfDocument.Page)). After the page is finished you should no longer access the page or its canvas. **Note:** Do not call this method after [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#close()). Also do not call this method if the last page returned by this method is not finished by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finishPage(android.graphics.pdf.PdfDocument.Page)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeTo](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#writeTo(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` <br /> Writes the document to an output stream. You can call this method multiple times. **Note:** Do not call this method after [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#close()). Also do not call this method if a page returned by [startPage(android.graphics.pdf.PdfDocument.PageInfo)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#startPage(android.graphics.pdf.PdfDocument.PageInfo))is not finished by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finishPage(android.graphics.pdf.PdfDocument.Page)). <br /> | ||

## Public constructors

### PrintedPdfDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintedPdfDocument(
    context: Context, 
    attributes: PrintAttributes)
```

Creates a new document.

**Note:** You must close the document after you are done by calling [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#close()).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):Context instance for accessing resources. This value cannot be`null`. |
| `attributes` | [PrintAttributes](https://developer.android.com/reference/kotlin/android/print/PrintAttributes.html#):The print attributes. This value cannot be`null`. |

## Public methods

### getPageContentRect

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPageContentRect(): Rect
```

Gets the content rectangle. This is the area of the page that contains printed data and is relative to the page top left.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | The content rectangle. This value cannot be`null`. |

### getPageHeight

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPageHeight(): Int
```

Gets the page height.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The page height in PostScript points (1/72th of an inch). Value is 0 or greater |

### getPageWidth

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPageWidth(): Int
```

Gets the page width.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The page width in PostScript points (1/72th of an inch). Value is 0 or greater |

### startPage

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startPage(pageNumber: Int): PdfDocument.Page
```

Starts a new page. The page is created using width, height and content rectangle computed from the print attributes passed in the constructor and the given page number to create an appropriate [PageInfo](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo.html#).

After the page is created you can draw arbitrary content on the page's canvas which you can get by calling [Page.getCanvas()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page.html#getCanvas()). After you are done drawing the content you should finish the page by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finishPage(android.graphics.pdf.PdfDocument.Page)). After the page is finished you should no longer access the page or its canvas.

**Note:** Do not call this method after [close()](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#close()). Also do not call this method if the last page returned by this method is not finished by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finishPage(android.graphics.pdf.PdfDocument.Page)).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `pageNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The page number. Must be a non negative. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [PdfDocument.Page](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page.html#) | A blank page. This value cannot be`null`. |

**See Also**

- [#finishPage(Page)](https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.html#finishPage(android.graphics.pdf.PdfDocument.Page))
