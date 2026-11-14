Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PdfDocument

Kotlin | [Java](PdfDocument.md)
| --- | --- |

```
open class PdfDocument
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.PdfDocument](PdfDocument.md) |

| Known Direct Subclasses [PrintedPdfDocument](../android.print.pdf/PrintedPdfDocument.md) |---|---| | [PrintedPdfDocument](../android.print.pdf/PrintedPdfDocument.md) | This class is a helper for creating a PDF file for given print attributes. | |
| --- | --- | --- | --- | --- | --- | --- |

This class enables generating a PDF document from native Android content. You create a new document and then for every page you want to add you start a page, write content to the page, and finish the page. After you are done with all pages, you write the document to an output stream and close the document. After a document is closed you should not use it anymore. Note that pages are created one by one, i.e. you can have only a single page to which you are writing at any given time. This class is not thread safe.

A typical use of the APIs looks like this:

```kotlin
// create a new document
  PdfDocument document = new PdfDocument();
 
  // create a page description
  PageInfo pageInfo = new PageInfo.Builder(100, 100, 1).create();
 
  // start a page
  Page page = document.startPage(pageInfo);
 
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
 
  // close the document
  document.close();
  
```

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page` This class represents a PDF document page. |
| | `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo` This class represents meta-data that describes a PDF `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page`. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#PdfDocument()()` Creates a new instance. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#close()()` Closes this document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#finishPage(android.graphics.pdf.PdfDocument.Page)(page: https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page!)` Finishes a started page. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PdfDocument.PageInfo](../android/graphics/pdf/PdfDocument.PageInfo.md)!\>! | `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#getPages()()` Gets the pages of the document. |
| --- | --- |
| open [PdfDocument.Page](../android/graphics/pdf/PdfDocument.Page.md)! | `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#startPage(android.graphics.pdf.PdfDocument.PageInfo)(pageInfo: https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo!)` Starts a page using the provided `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#writeTo(java.io.OutputStream)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!)` Writes the document to an output stream. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public constructors

### PdfDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PdfDocument()
```

Creates a new instance.

## Public methods

### close

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes this document. This method should be called after you are done working with the document. After this call the document is considered closed and none of its methods should be called.

**Note:** Do not call this method if the page returned by `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#startPage(android.graphics.pdf.PdfDocument.PageInfo)` is not finished by calling `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#finishPage(android.graphics.pdf.PdfDocument.Page)`.

### finishPage

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishPage(page: PdfDocument.Page!): Unit
```

Finishes a started page. You should always finish the last started page.

**Note:** Do not call this method after `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#close()`. You should not finish the same page more than once.

| Parameters ||
|---|---|
| `page` | [PdfDocument.Page](../android/graphics/pdf/PdfDocument.Page.md)!: The page. Cannot be null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#startPage(android.graphics.pdf.PdfDocument.PageInfo)`

### getPages

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPages(): MutableList<PdfDocument.PageInfo!>!
```

Gets the pages of the document.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo!>!` | The pages or an empty list. |

### startPage

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startPage(pageInfo: PdfDocument.PageInfo!): PdfDocument.Page!
```

Starts a page using the provided `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.PageInfo`. After the page is created you can draw arbitrary content on the page's canvas which you can get by calling `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page#getCanvas()`. After you are done drawing the content you should finish the page by calling `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#finishPage(android.graphics.pdf.PdfDocument.Page)`. After the page is finished you should no longer access the page or its canvas.

**Note:** Do not call this method after `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#close()`. Also do not call this method if the last page returned by this method is not finished by calling `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#finishPage(android.graphics.pdf.PdfDocument.Page)`.

| Parameters ||
|---|---|
| `pageInfo` | [PdfDocument.PageInfo](../android/graphics/pdf/PdfDocument.PageInfo.md)!: The page info. Cannot be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument.Page!` | A blank page. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#finishPage(android.graphics.pdf.PdfDocument.Page)`

### writeTo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeTo(out: OutputStream!): Unit
```

Writes the document to an output stream. You can call this method multiple times.

**Note:** Do not call this method after `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#close()`. Also do not call this method if a page returned by `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#startPage(android.graphics.pdf.PdfDocument.PageInfo)` is not finished by calling `https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfDocument#finishPage(android.graphics.pdf.PdfDocument.Page)`.

| Parameters ||
|---|---|
| `out` | [OutputStream](../java.io/OutputStream.md)!: The output stream. Cannot be null. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an error occurs while writing. |

## Protected methods

### finalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
