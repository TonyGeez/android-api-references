# PrintManager

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintManager

Kotlin| [Java](../android/print/PrintManager.md) 
| --- | --- |

```
class PrintManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.print.PrintManager](../android/print/PrintManager.md) |

System level service for accessing the printing capabilities of the platform.

### Print mechanics

<br />

The key idea behind printing on the platform is that the content to be printed should be laid out for the currently selected print options resulting in an optimized output and higher user satisfaction. To achieve this goal the platform declares a contract that the printing application has to follow which is defined by the [PrintDocumentAdapter](../android/print/PrintDocumentAdapter.md) class. At a higher level the contract is that when the user selects some options from the print UI that may affect the way content is laid out, for example page size, the application receives a callback allowing it to layout the content to better fit these new constraints. After a layout pass the system may ask the application to render one or more pages one or more times. For example, an application may produce a single column list for smaller page sizes and a multi-column table for larger page sizes.

### Print jobs

Print jobs are started by calling the [print(java.lang.String,android.print.PrintDocumentAdapter,android.print.PrintAttributes)](../android/print/PrintManager.md))from an activity which results in bringing up the system print UI. Once the print UI is up, when the user changes a selected print option that affects the way content is laid out the system starts to interact with the application following the mechanics described the section above.

Print jobs can be in [created](../android/print/PrintJobInfo.md), [queued](../android/print/PrintJobInfo.md), [started](../android/print/PrintJobInfo.md), [blocked](../android/print/PrintJobInfo.md), [completed](../android/print/PrintJobInfo.md), [failed](../android/print/PrintJobInfo.md), and [canceled](../android/print/PrintJobInfo.md) state. Print jobs are stored in dedicated system spooler until they are handled which is they are cancelled or completed. Active print jobs, ones that are not cancelled or completed, are considered failed if the device reboots as the new boot may be after a very long time. The user may choose to restart such print jobs. Once a print job is queued all relevant content is stored in the system spooler and its lifecycle becomes detached from this of the application that created it.

An applications can query the print spooler for current print jobs it created but not print jobs created by other applications.

Requires the [PackageManager#FEATURE_PRINTING](../android/content/pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrintJob](../android/print/PrintJob.md)!\> | [getPrintJobs](../android/print/PrintManager.md))`()` Gets the print jobs for this application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrintServiceEnabled](../android/print/PrintManager.md))`(`service:` ` [ComponentName](../android/content/ComponentName.md)`)` Checks whether a given print service is enabled. |
| [PrintJob](../android/print/PrintJob.md) | [print](../android/print/PrintManager.md))`(`printJobName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `documentAdapter:` ` [PrintDocumentAdapter](../android/print/PrintDocumentAdapter.md)`, `attributes:` ` [PrintAttributes](../android/print/PrintAttributes.md)?`)` Creates a print job for printing a [PrintDocumentAdapter](../android/print/PrintDocumentAdapter.md) with default print attributes. |
| --- | --- |

## Public methods

### getPrintJobs

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrintJobs(): MutableList<PrintJob!>
```

Gets the print jobs for this application.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrintJob](../android/print/PrintJob.md)!> | The print job list. This value cannot be`null`. |

**See Also**

- [android.print.PrintJob](../android/print/PrintJob.md) 

### isPrintServiceEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPrintServiceEnabled(service: ComponentName): Boolean
```

Checks whether a given print service is enabled. The provided service must share UID with the calling package, otherwise a [SecurityException](../java/lang/SecurityException.md) is thrown.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `service` | [ComponentName](../android/content/ComponentName.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given print service is enabled |

### print

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun print(
    printJobName: String, 
    documentAdapter: PrintDocumentAdapter, 
    attributes: PrintAttributes?
): PrintJob
```

Creates a print job for printing a [PrintDocumentAdapter](../android/print/PrintDocumentAdapter.md) with default print attributes.

Calling this method brings the print UI allowing the user to customize the print job and returns a [PrintJob](../android/print/PrintJob.md) object without waiting for the user to customize or confirm the print job. The returned print job instance is in a [created](../android/print/PrintJobInfo.md) state.

This method can be called only from an [Activity](../android/app/Activity.md). The rationale is that printing from a service will create an inconsistent user experience as the print UI would appear without any context.

Also the passed in [PrintDocumentAdapter](../android/print/PrintDocumentAdapter.md) will be considered invalid if your activity is finished. The rationale is that once the activity that initiated printing is finished, the provided adapter may be in an inconsistent state as it may depend on the UI presented by the activity.

The default print attributes are a hint to the system how the data is to be printed. For example, a photo editor may look at the photo aspect ratio to determine the default orientation and provide a hint whether the printing should be in portrait or landscape. The system will do a best effort to selected the hinted options in the print dialog, given the current printer supports them.

**Note:** Calling this method will bring the print dialog and the system will connect to the provided [PrintDocumentAdapter](../android/print/PrintDocumentAdapter.md). If a configuration change occurs that you application does not handle, for example a rotation change, the system will drop the connection to the adapter as the activity has to be recreated and the old adapter may be invalid in this context, hence a new adapter instance is required. As a consequence, if your activity does not handle configuration changes (default behavior), you have to save the state that you were printing and call this method again when your activity is recreated.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `printJobName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A name for the new print job which is shown to the user. This value cannot be`null`. |
| `documentAdapter` | [PrintDocumentAdapter](../android/print/PrintDocumentAdapter.md):An adapter that emits the document to print. This value cannot be`null`. |
| `attributes` | [PrintAttributes](../android/print/PrintAttributes.md)?:The default print job attributes or`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [PrintJob](../android/print/PrintJob.md) | The created print job on success or null on failure. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If not called from an [Activity](../android/app/Activity.md). |
| `java.lang.IllegalArgumentException` | If the print job name is empty or the document adapter is null. |

**See Also**

- [android.print.PrintJob](../android/print/PrintJob.md)
