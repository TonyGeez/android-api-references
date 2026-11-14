# PrintedPdfDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintedPdfDocument

Kotlin| [Java](PrintedPdfDocument.md) 
| --- | --- |

```
open class PrintedPdfDocument : PdfDocument
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.PdfDocument](../android.graphics.pdf/PdfDocument.md) ||
| | ↳ | [android.print.pdf.PrintedPdfDocument](PrintedPdfDocument.md) |

This class is a helper for creating a PDF file for given print attributes. It is useful for implementing printing via the native Android graphics APIs.

This class computes the page width, page height, and content rectangle from the provided print attributes and these precomputed values can be accessed via [getPageWidth()](PrintedPdfDocument.md)), [getPageHeight()](PrintedPdfDocument.md)), and [getPageContentRect()](PrintedPdfDocument.md)), respectively. The [startPage(int)](PrintedPdfDocument.md))methods creates pages whose [PageInfo](../android/graphics/pdf/PdfDocument.PageInfo.md) is initialized with the precomputed values for width, height, and content rectangle.

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
| [PrintedPdfDocument](PrintedPdfDocument.md))`(`context:` ` [Context](../android.content/Context.md)`, `attributes:` ` [PrintAttributes](../android.print/PrintAttributes.md)`)` Creates a new document. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Rect](../android.graphics/Rect.md) | [getPageContentRect](PrintedPdfDocument.md))`()` Gets the content rectangle. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageHeight](PrintedPdfDocument.md))`()` Gets the page height. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPageWidth](PrintedPdfDocument.md))`()` Gets the page width. |
| --- | --- |
| open [PdfDocument.Page](../android/graphics/pdf/PdfDocument.Page.md) | [startPage](PrintedPdfDocument.md))`(`pageNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Starts a new page. |

| Inherited functions ||
|---|---|
| From class [PdfDocument](../android.graphics.pdf/PdfDocument.md) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android.graphics.pdf/PdfDocument.md))`()` <br /> Closes this document. This method should be called after you are done working with the document. After this call the document is considered closed and none of its methods should be called. **Note:** Do not call this method if the page returned by [startPage(android.graphics.pdf.PdfDocument.PageInfo)](../android.graphics.pdf/PdfDocument.md))is not finished by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](../android.graphics.pdf/PdfDocument.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android.graphics.pdf/PdfDocument.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finishPage](../android.graphics.pdf/PdfDocument.md))`(`page:` ` [PdfDocument.Page](../android/graphics/pdf/PdfDocument.Page.md)!`)` <br /> Finishes a started page. You should always finish the last started page. **Note:** Do not call this method after [close()](../android.graphics.pdf/PdfDocument.md)). You should not finish the same page more than once. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PdfDocument.PageInfo](../android/graphics/pdf/PdfDocument.PageInfo.md)!>! | [getPages](../android.graphics.pdf/PdfDocument.md))`()` <br /> Gets the pages of the document. <br /> | | [PdfDocument.Page](../android/graphics/pdf/PdfDocument.Page.md)! | [startPage](../android.graphics.pdf/PdfDocument.md))`(`pageInfo:` ` [PdfDocument.PageInfo](../android/graphics/pdf/PdfDocument.PageInfo.md)!`)` <br /> Starts a page using the provided [PageInfo](../android/graphics/pdf/PdfDocument.PageInfo.md). After the page is created you can draw arbitrary content on the page's canvas which you can get by calling [Page.getCanvas()](../android/graphics/pdf/PdfDocument.Page.md)). After you are done drawing the content you should finish the page by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](../android.graphics.pdf/PdfDocument.md)). After the page is finished you should no longer access the page or its canvas. **Note:** Do not call this method after [close()](../android.graphics.pdf/PdfDocument.md)). Also do not call this method if the last page returned by this method is not finished by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](../android.graphics.pdf/PdfDocument.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeTo](../android.graphics.pdf/PdfDocument.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`)` <br /> Writes the document to an output stream. You can call this method multiple times. **Note:** Do not call this method after [close()](../android.graphics.pdf/PdfDocument.md)). Also do not call this method if a page returned by [startPage(android.graphics.pdf.PdfDocument.PageInfo)](../android.graphics.pdf/PdfDocument.md))is not finished by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](../android.graphics.pdf/PdfDocument.md)). <br /> | ||

## Public constructors

### PrintedPdfDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintedPdfDocument(
    context: Context, 
    attributes: PrintAttributes)
```

Creates a new document.

**Note:** You must close the document after you are done by calling [close()](../android.graphics.pdf/PdfDocument.md)).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):Context instance for accessing resources. This value cannot be`null`. |
| `attributes` | [PrintAttributes](../android.print/PrintAttributes.md):The print attributes. This value cannot be`null`. |

## Public methods

### getPageContentRect

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPageContentRect(): Rect
```

Gets the content rectangle. This is the area of the page that contains printed data and is relative to the page top left.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Rect](../android.graphics/Rect.md) | The content rectangle. This value cannot be`null`. |

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

Starts a new page. The page is created using width, height and content rectangle computed from the print attributes passed in the constructor and the given page number to create an appropriate [PageInfo](../android/graphics/pdf/PdfDocument.PageInfo.md).

After the page is created you can draw arbitrary content on the page's canvas which you can get by calling [Page.getCanvas()](../android/graphics/pdf/PdfDocument.Page.md)). After you are done drawing the content you should finish the page by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](../android.graphics.pdf/PdfDocument.md)). After the page is finished you should no longer access the page or its canvas.

**Note:** Do not call this method after [close()](../android.graphics.pdf/PdfDocument.md)). Also do not call this method if the last page returned by this method is not finished by calling [finishPage(android.graphics.pdf.PdfDocument.Page)](../android.graphics.pdf/PdfDocument.md)).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `pageNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The page number. Must be a non negative. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [PdfDocument.Page](../android/graphics/pdf/PdfDocument.Page.md) | A blank page. This value cannot be`null`. |

**See Also**

- [#finishPage(Page)](../android.graphics.pdf/PdfDocument.md))
