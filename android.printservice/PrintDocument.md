# PrintDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintDocument

Kotlin| [Java](PrintDocument.md) 
| --- | --- |

```
class PrintDocument
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.printservice.PrintDocument](PrintDocument.md) |

This class represents a printed document from the perspective of a print service. It exposes APIs to query the document and obtain its data.

**Note:**All methods of this class must be executed on the main application thread.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | [getData](PrintDocument.md))`()` Gets the data associated with this document. |
| [PrintDocumentInfo](../android.print/PrintDocumentInfo.md) | [getInfo](PrintDocument.md))`()` Gets the [PrintDocumentInfo](../android.print/PrintDocumentInfo.md) that describes this document. |

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
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | A file descriptor for reading the data. This value may be`null`. |

### getInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInfo(): PrintDocumentInfo
```

Gets the [PrintDocumentInfo](../android.print/PrintDocumentInfo.md) that describes this document.

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [PrintDocumentInfo](../android.print/PrintDocumentInfo.md) | The document info. This value cannot be`null`. |
