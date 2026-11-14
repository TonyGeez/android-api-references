# PrintDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintDocument

Kotlin| [Java](https://developer.android.com/reference/android/printservice/PrintDocument "View this page in Java") 

```
class PrintDocument
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.printservice.PrintDocument](https://developer.android.com/reference/kotlin/android/printservice/PrintDocument#) |

This class represents a printed document from the perspective of a print service. It exposes APIs to query the document and obtain its data.

**Note:**All methods of this class must be executed on the main application thread.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [getData](https://developer.android.com/reference/kotlin/android/printservice/PrintDocument#getData())`()` Gets the data associated with this document. |
| [PrintDocumentInfo](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo.html#) | [getInfo](https://developer.android.com/reference/kotlin/android/printservice/PrintDocument#getInfo())`()` Gets the [PrintDocumentInfo](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo.html#) that describes this document. |

## Public methods

### getData

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): ParcelFileDescriptor?
```

Gets the data associated with this document.

**Note:**It is a responsibility of the client to open a stream to the returned file descriptor, fully read the data, and close the file descriptor.

| Return ||
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | A file descriptor for reading the data. This value may be`null`. |

### getInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInfo(): PrintDocumentInfo
```

Gets the [PrintDocumentInfo](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo.html#) that describes this document.

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [PrintDocumentInfo](https://developer.android.com/reference/kotlin/android/print/PrintDocumentInfo.html#) | The document info. This value cannot be`null`. |
