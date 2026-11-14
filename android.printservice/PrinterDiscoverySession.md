# PrinterDiscoverySession

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrinterDiscoverySession

Kotlin| [Java](https://developer.android.com/reference/android/printservice/PrinterDiscoverySession "View this page in Java") 

```
abstract class PrinterDiscoverySession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.printservice.PrinterDiscoverySession](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#) |

This class encapsulates the interaction between a print service and the system during printer discovery. During printer discovery you are responsible for adding discovered printers, removing previously added printers that disappeared, and updating already added printers.

During the lifetime of this session you may be asked to start and stop performing printer discovery multiple times. You will receive a call to [android.printservice.PrinterDiscoverySession#onStartPrinterDiscovery(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterDiscovery(kotlin.collections.MutableList))to start printer discovery and a call to [PrinterDiscoverySession.onStopPrinterDiscovery()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterDiscovery())to stop printer discovery. When the system is no longer interested in printers discovered by this session you will receive a call to [onDestroy()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onDestroy())at which point the system will no longer call into the session and all the session methods will do nothing.

Discovered printers are added by invoking [android.printservice.PrinterDiscoverySession#addPrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList)). Added printers that disappeared are removed by invoking [PrinterDiscoverySession.removePrinters(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#removePrinters(kotlin.collections.MutableList)). Added printers whose properties or capabilities changed are updated through a call to [PrinterDiscoverySession.addPrinters(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList)). The printers added in this session can be acquired via [getPrinters()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#getPrinters())where the returned printers will be an up-to-date snapshot of the printers that you reported during the session. Printers are**not**persisted across sessions.

The system will make a call to [onValidatePrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onValidatePrinters(kotlin.collections.MutableList))if you need to update some printers. It is possible that you add a printer without specifying its capabilities. This enables you to avoid querying all discovered printers for their capabilities, rather querying the capabilities of a printer only if necessary. For example, the system will request that you update a printer if it gets selected by the user. When validating printers you do not need to provide the printers' capabilities but may do so.

If the system is interested in being constantly updated for the state of a printer you will receive a call to [onStartPrinterStateTracking(android.print.PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterStateTracking(android.print.PrinterId))after which you will have to do a best effort to keep the system updated for changes in the printer state and capabilities. You also**must** update the printer capabilities if you did not provide them when adding it, or the printer will be ignored. When the system is no longer interested in getting updates for a printer you will receive a call to [onStopPrinterStateTracking(android.print.PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterStateTracking(android.print.PrinterId)).

**Note:**All callbacks in this class are executed on the main application thread. You also have to invoke any method of this class on the main application thread.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrinterDiscoverySession](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#PrinterDiscoverySession())`()` Constructor. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPrinters](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList))`(`printers:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrinterInfo](https://developer.android.com/reference/kotlin/android/print/PrinterInfo.html#)!>`)` Adds discovered printers. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrinterInfo](https://developer.android.com/reference/kotlin/android/print/PrinterInfo.html#)!\> | [getPrinters](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#getPrinters())`()` Gets the printers reported in this session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)!\> | [getTrackedPrinters](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#getTrackedPrinters())`()` Gets the printers that should be tracked. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isDestroyed())`()` Gets whether the session is destroyed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrinterDiscoveryStarted](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isPrinterDiscoveryStarted())`()` Gets whether printer discovery is started. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroy](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onDestroy())`()` Notifies you that the session is destroyed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRequestCustomPrinterIcon](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onRequestCustomPrinterIcon(android.print.PrinterId,%20android.os.CancellationSignal,%20android.printservice.CustomPrinterIconCallback))`(`printerId:` ` [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)`, `callback:` ` [CustomPrinterIconCallback](https://developer.android.com/reference/kotlin/android/printservice/CustomPrinterIconCallback)`)` Called by the system to request the custom icon for a printer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartPrinterDiscovery](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterDiscovery(kotlin.collections.MutableList))`(`priorityList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)!>`)` Callback asking you to start printer discovery. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartPrinterStateTracking](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterStateTracking(android.print.PrinterId))`(`printerId:` ` [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)`)` Callback asking you to start tracking the state of a printer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopPrinterDiscovery](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterDiscovery())`()` Callback notifying you that you should stop printer discovery. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopPrinterStateTracking](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterStateTracking(android.print.PrinterId))`(`printerId:` ` [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)`)` Callback asking you to stop tracking the state of a printer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onValidatePrinters](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onValidatePrinters(kotlin.collections.MutableList))`(`printerIds:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)!>`)` Callback asking you to validate that the given printers are valid, that is they exist. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePrinters](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#removePrinters(kotlin.collections.MutableList))`(`printerIds:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)!>`)` Removes added printers. |

## Public constructors

### PrinterDiscoverySession

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrinterDiscoverySession()
```

Constructor.

## Public methods

### addPrinters

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addPrinters(printers: MutableList<PrinterInfo!>): Unit
```

Adds discovered printers. Adding an already added printer updates it. Removed printers can be added again. You can call this method multiple times during the life of this session. Duplicates will be ignored.

**Note:** Calls to this method after the session is destroyed, that is after the [onDestroy()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onDestroy())callback, will be ignored.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `printers` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrinterInfo](https://developer.android.com/reference/kotlin/android/print/PrinterInfo.html#)!\>:The printers to add. This value cannot be`null`. |

**See Also**

- [#removePrinters(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#removePrinters(kotlin.collections.MutableList))
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#getPrinters()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isDestroyed()> 

### getPrinters

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrinters(): MutableList<PrinterInfo!>
```

Gets the printers reported in this session. For example, if you add two printers and remove one of them, the returned list will contain only the printer that was added but not removed.

**Note:** Calls to this method after the session is destroyed, that is after the [onDestroy()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onDestroy())callback, will be ignored.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrinterInfo](https://developer.android.com/reference/kotlin/android/print/PrinterInfo.html#)!> | The printers. This value cannot be`null`. |

**See Also**

- [#addPrinters(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList))
- [#removePrinters(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#removePrinters(kotlin.collections.MutableList))
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isDestroyed()> 

### getTrackedPrinters

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrackedPrinters(): MutableList<PrinterId!>
```

Gets the printers that should be tracked. These are printers that are important to the user and for which you received a call to [onStartPrinterStateTracking(android.print.PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterStateTracking(android.print.PrinterId))asking you to observer their state and reporting it to the system via [addPrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList)). You will receive a call to [onStopPrinterStateTracking(android.print.PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterStateTracking(android.print.PrinterId))if you should stop tracking a printer.

**Note:** Calls to this method after the session is destroyed, that is after the [onDestroy()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onDestroy())callback, will be ignored.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)!> | The printers. This value cannot be`null`. |

**See Also**

- [#onStartPrinterStateTracking(PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterStateTracking(android.print.PrinterId))
- [#onStopPrinterStateTracking(PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterStateTracking(android.print.PrinterId))
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isDestroyed()> 

### isDestroyed

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDestroyed(): Boolean
```

Gets whether the session is destroyed.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the session is destroyed. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onDestroy()> 

### isPrinterDiscoveryStarted

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPrinterDiscoveryStarted(): Boolean
```

Gets whether printer discovery is started.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether printer discovery is destroyed. |

**See Also**

- [#onStartPrinterDiscovery(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterDiscovery(kotlin.collections.MutableList))
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterDiscovery()> 

### onDestroy

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDestroy(): Unit
```

Notifies you that the session is destroyed. After this callback is invoked any calls to the methods of this class will be ignored, [isDestroyed()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isDestroyed())will return true and you will also no longer receive callbacks. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isDestroyed()> 

### onRequestCustomPrinterIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRequestCustomPrinterIcon(
    printerId: PrinterId, 
    cancellationSignal: CancellationSignal, 
    callback: CustomPrinterIconCallback
): Unit
```

Called by the system to request the custom icon for a printer. Once the icon is available the print services uses [CustomPrinterIconCallback.onCustomPrinterIconLoaded](https://developer.android.com/reference/kotlin/android/printservice/CustomPrinterIconCallback#onCustomPrinterIconLoaded(android.graphics.drawable.Icon))to send the icon to the system.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `printerId` | [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#):The printer to icon belongs to. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#):Signal used to cancel the request. This value cannot be`null`. |
| `callback` | [CustomPrinterIconCallback](https://developer.android.com/reference/kotlin/android/printservice/CustomPrinterIconCallback):Callback for returning the icon to the system. This value cannot be`null`. |

**See Also**

- [android.print.PrinterInfo.Builder#setHasCustomPrinterIcon(boolean)](https://developer.android.com/reference/kotlin/android/print/PrinterInfo.Builder.html#setHasCustomPrinterIcon(kotlin.Boolean)) 

### onStartPrinterDiscovery

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStartPrinterDiscovery(priorityList: MutableList<PrinterId!>): Unit
```

Callback asking you to start printer discovery. Discovered printers should be added via calling [addPrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList)). Added printers that disappeared should be removed via calling [removePrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#removePrinters(kotlin.collections.MutableList)). Added printers whose properties or capabilities changed should be updated via calling [addPrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList)). You will receive a call to [onStopPrinterDiscovery()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterDiscovery())when you should stop printer discovery.

During the lifetime of this session all printers that are known to your print service have to be added. The system does not retain any printers across sessions. However, if you were asked to start and then stop performing printer discovery in this session, then a subsequent discovering should not re-discover already discovered printers. You can get the printers reported during this session by calling [getPrinters()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#getPrinters()).

**Note:** You are also given a list of printers whose availability has to be checked first. For example, these printers could be the user's favorite ones, therefore they have to be verified first. You do**not need** to provide the capabilities of the printers, rather verify whether they exist similarly to [onValidatePrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onValidatePrinters(kotlin.collections.MutableList)).

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priorityList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)!\>:The list of printers to validate first. Never null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterDiscovery()>
- [#addPrinters(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList))
- [#removePrinters(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#removePrinters(kotlin.collections.MutableList))
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isPrinterDiscoveryStarted()> 

### onStartPrinterStateTracking

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStartPrinterStateTracking(printerId: PrinterId): Unit
```

Callback asking you to start tracking the state of a printer. Tracking the state means that you should do a best effort to observe the state of this printer and notify the system if that state changes via calling [addPrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList)).

**Note:** A printer can be initially added without its capabilities to avoid polling printers that the user will not select. However, after this method is called you are expected to update the printer**including**its capabilities. Otherwise, the printer will be ignored.

<br />

A scenario when you may be requested to track a printer's state is if the user selects that printer and the system has to present print options UI based on the printer's capabilities. In this case the user should be promptly informed if, for example, the printer becomes unavailable.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `printerId` | [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#):The printer to start tracking. This value cannot be`null`. |

**See Also**

- [#onStopPrinterStateTracking(PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStopPrinterStateTracking(android.print.PrinterId))
- [android.print.PrinterInfo.Builder#setCapabilities(PrinterCapabilitiesInfo)](https://developer.android.com/reference/kotlin/android/print/PrinterInfo.Builder.html#setCapabilities(android.print.PrinterCapabilitiesInfo)) 

### onStopPrinterDiscovery

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopPrinterDiscovery(): Unit
```

Callback notifying you that you should stop printer discovery. 
**See Also**

- [#onStartPrinterDiscovery(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterDiscovery(kotlin.collections.MutableList))
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isPrinterDiscoveryStarted()> 

### onStopPrinterStateTracking

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopPrinterStateTracking(printerId: PrinterId): Unit
```

Callback asking you to stop tracking the state of a printer. The passed in printer id is the one for which you received a call to [onStartPrinterStateTracking(android.print.PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterStateTracking(android.print.PrinterId)).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `printerId` | [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#):The printer to stop tracking. This value cannot be`null`. |

**See Also**

- [#onStartPrinterStateTracking(PrinterId)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onStartPrinterStateTracking(android.print.PrinterId)) 

### onValidatePrinters

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onValidatePrinters(printerIds: MutableList<PrinterId!>): Unit
```

Callback asking you to validate that the given printers are valid, that is they exist. You are responsible for checking whether these printers exist and for the ones that do exist notify the system via calling [addPrinters(java.util.List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList)).

**Note:** You are**not required**to provide the printer capabilities when updating the printers that do exist.

<br />

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `printerIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)!\>:The printers to validate. This value cannot be`null`. |

**See Also**

- [android.print.PrinterInfo.Builder#setCapabilities(PrinterCapabilitiesInfo)](https://developer.android.com/reference/kotlin/android/print/PrinterInfo.Builder.html#setCapabilities(android.print.PrinterCapabilitiesInfo)) 

### removePrinters

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removePrinters(printerIds: MutableList<PrinterId!>): Unit
```

Removes added printers. Removing an already removed or never added printer has no effect. Removed printers can be added again. You can call this method multiple times during the lifetime of this session.

**Note:** Calls to this method after the session is destroyed, that is after the [onDestroy()](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onDestroy())callback, will be ignored.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `printerIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId.html#)!\>:The ids of the removed printers. This value cannot be`null`. |

**See Also**

- [#addPrinters(List)](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#addPrinters(kotlin.collections.MutableList))
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#getPrinters()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#isDestroyed()>
