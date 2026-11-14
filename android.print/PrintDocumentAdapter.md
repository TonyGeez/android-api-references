Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintDocumentAdapter

Kotlin | [Java](PrintDocumentAdapter.md)
| --- | --- |

```
abstract class PrintDocumentAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.print.PrintDocumentAdapter](PrintDocumentAdapter.md) |

Base class that provides the content of a document to be printed.

### Lifecycle

<br />

- Initially, you will receive a call to `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onStart()`. This callback can be used to allocate resources.
- Next, you will get one or more calls to `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)` to inform you that the print attributes (page size, density, etc) changed giving you an opportunity to layout the content to match the new constraints.
- After every call to `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)`, you **may** get a call to `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onWrite(kotlin.Array,%20android.os.ParcelFileDescriptor,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.WriteResultCallback)` asking you to write a PDF file with the content for specific pages.
- Finally, you will receive a call to `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onFinish()`. You can use this callback to release resources allocated in `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onStart()`.

The `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onStart()` callback is always the first call you will receive and is useful for doing one time setup or resource allocation before printing. You will not receive a subsequent call here.

The `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)` callback requires that you layout the content based on the current `https://developer.android.com/reference/kotlin/android/print/PrintAttributes`. The execution of this method is not considered completed until you invoke one of the methods on the passed in callback instance. Hence, you will not receive a subsequent call to any other method of this class until the execution of this method is complete by invoking one of the callback methods.

The `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onWrite(kotlin.Array,%20android.os.ParcelFileDescriptor,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.WriteResultCallback)` requires that you render and write the content of some pages to the provided destination. The execution of this method is not considered complete until you invoke one of the methods on the passed in callback instance. Hence, you will not receive a subsequent call to any other method of this class until the execution of this method is complete by invoking one of the callback methods. You will never receive a sequence of one or more calls to this method without a previous call to `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)`.

The `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onFinish()` callback is always the last call you will receive and is useful for doing one time cleanup or resource deallocation after printing. You will not receive a subsequent call here.

<br />

### Implementation

The APIs defined in this class are designed to enable doing part or all of the work on an arbitrary thread. For example, if the printed content does not depend on the UI state, i.e. on what is shown on the screen, then you can offload the entire work on a dedicated thread, thus making your application interactive while the print work is being performed. Note that while your activity is covered by the system print UI and a user cannot interact with it, doing the printing work on the main application thread may affect the performance of your other application components as they are also executed on that thread.

You can also do work on different threads, for example if you print UI content, you can handle `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onStart()` and `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)` on the UI thread (assuming onStart initializes resources needed for layout). This will ensure that the UI does not change while you are laying out the printed content. Then you can handle `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onWrite(kotlin.Array,%20android.os.ParcelFileDescriptor,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.WriteResultCallback)` and `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onFinish()` on another thread. This will ensure that the main thread is busy for a minimal amount of time. Also this assumes that you will generate the printed content in `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)` which is not mandatory. If you use multiple threads, you are responsible for proper synchronization.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.LayoutResultCallback` Base class for implementing a callback for the result of `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)`. |
| abstract | `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.WriteResultCallback` Base class for implementing a callback for the result of `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onWrite(kotlin.Array,%20android.os.ParcelFileDescriptor,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.WriteResultCallback)`. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#EXTRA_PRINT_PREVIEW:kotlin.String` Extra: mapped to a boolean value that is `true` if the current layout is for a print preview, `false` otherwise. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#PrintDocumentAdapter()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onFinish()()` Called when printing finishes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)(oldAttributes: https://developer.android.com/reference/kotlin/android/print/PrintAttributes!, newAttributes: https://developer.android.com/reference/kotlin/android/print/PrintAttributes!, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#!, callback: https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.LayoutResultCallback!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Called when the print attributes (page size, density, etc) changed giving you a chance to layout the content such that it matches the new constraints. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onStart()()` Called when printing starts. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onWrite(kotlin.Array,%20android.os.ParcelFileDescriptor,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.WriteResultCallback)(pages: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/print/PageRange!>!, destination: https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#!, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#!, callback: https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.WriteResultCallback!)` Called when specific pages of the content should be written in the form of a PDF file to the given file descriptor. |

## Constants

### EXTRA_PRINT_PREVIEW

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PRINT_PREVIEW: String
```

Extra: mapped to a boolean value that is `true` if the current layout is for a print preview, `false` otherwise. This extra is provided in the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` argument of the `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)` callback.

 Value: "EXTRA_PRINT_PREVIEW"

**See Also**

- `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onLayout(android.print.PrintAttributes,%20android.print.PrintAttributes,%20android.os.CancellationSignal,%20android.print.PrintDocumentAdapter.LayoutResultCallback,%20android.os.Bundle)`

## Public constructors

### PrintDocumentAdapter

```
PrintDocumentAdapter()
```

## Public methods

### onFinish

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFinish(): Unit
```

Called when printing finishes. You can use this callback to release resources acquired in `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#onStart()`. This method is invoked on the main thread.

### onLayout

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onLayout(
    oldAttributes: PrintAttributes!, 
    newAttributes: PrintAttributes!, 
    cancellationSignal: CancellationSignal!, 
    callback: PrintDocumentAdapter.LayoutResultCallback!, 
    extras: Bundle!
): Unit
```

Called when the print attributes (page size, density, etc) changed giving you a chance to layout the content such that it matches the new constraints. This method is invoked on the main thread.

After you are done laying out, you **must** invoke: `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.LayoutResultCallback#onLayoutFinished(android.print.PrintDocumentInfo,%20kotlin.Boolean)` with the last argument `true` or `false` depending on whether the layout changed the content or not, respectively; or `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.LayoutResultCallback#onLayoutFailed(kotlin.CharSequence)`, if an error occurred; or `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.LayoutResultCallback#onLayoutCancelled()` if layout was cancelled in a response to a cancellation request via the passed in `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#`. Note that you **must** call one of the methods of the given callback for this method to be considered complete which is you will not receive any calls to this adapter until the current layout operation is complete by invoking a method on the callback instance. The callback methods can be invoked from an arbitrary thread.

One of the arguments passed to this method is a `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` which is used to propagate requests from the system to your application for canceling the current layout operation. For example, a cancellation may be requested if the user changes a print option that may affect layout while you are performing a layout operation. In such a case the system will make an attempt to cancel the current layout as another one will have to be performed. Typically, you should register a cancellation callback in the cancellation signal. The cancellation callback **will not** be made on the main thread and can be registered as follows:

```kotlin
cancellationSignal.setOnCancelListener(new OnCancelListener() {
      @Override
      public void onCancel() {
          // Cancel layout
      }
  });
  
```

**Note:** If the content is large and a layout will be performed, it is a good practice to schedule the work on a dedicated thread and register an observer in the provided `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` upon invocation of which you should stop the layout.

| Parameters ||
|---|---|
| `oldAttributes` | [PrintAttributes](PrintAttributes.md)!: The old print attributes. |
| `newAttributes` | [PrintAttributes](PrintAttributes.md)!: The new print attributes. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)!: Signal for observing cancel layout requests. |
| --- | --- |
| `callback` | [PrintDocumentAdapter.LayoutResultCallback](../android/print/PrintDocumentAdapter.LayoutResultCallback.md)!: Callback to inform the system for the layout result. |
| `extras` | [Bundle](../android.os/Bundle.md)!: Additional information about how to layout the content. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.LayoutResultCallback`
- `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#`
- `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter#EXTRA_PRINT_PREVIEW:kotlin.String`

### onStart

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStart(): Unit
```

Called when printing starts. You can use this callback to allocate resources. This method is invoked on the main thread.

### onWrite

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onWrite(
    pages: Array<PageRange!>!, 
    destination: ParcelFileDescriptor!, 
    cancellationSignal: CancellationSignal!, 
    callback: PrintDocumentAdapter.WriteResultCallback!
): Unit
```

Called when specific pages of the content should be written in the form of a PDF file to the given file descriptor. This method is invoked on the main thread.

After you are done writing, you should close the file descriptor and invoke `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.WriteResultCallback#onWriteFinished(kotlin.Array)`, if writing completed successfully; or `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.WriteResultCallback#onWriteFailed(kotlin.CharSequence)`, if an error occurred; or `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.WriteResultCallback#onWriteCancelled()`, if writing was cancelled in a response to a cancellation request via the passed in `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#`. Note that you **must** call one of the methods of the given callback for this method to be considered complete which is you will not receive any calls to this adapter until the current write operation is complete by invoking a method on the callback instance. The callback methods can be invoked from an arbitrary thread.

One of the arguments passed to this method is a `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` which is used to propagate requests from the system to your application for canceling the current write operation. For example, a cancellation may be requested if the user changes a print option that may affect layout while you are performing a write operation. In such a case the system will make an attempt to cancel the current write as a layout will have to be performed which then may be followed by a write. Typically, you should register a cancellation callback in the cancellation signal. The cancellation callback **will not** be made on the main thread and can be registered as follows:

```kotlin
cancellationSignal.setOnCancelListener(new OnCancelListener() {
      @Override
      public void onCancel() {
          // Cancel write
      }
  });
  
```

**Note:** If the printed content is large, it is a good practice to schedule writing it on a dedicated thread and register an observer in the provided `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` upon invocation of which you should stop writing.

| Parameters ||
|---|---|
| `pages` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PageRange](PageRange.md)!\>!: The pages whose content to print - non-overlapping in ascending order. |
| `destination` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!: The destination file descriptor to which to write. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)!: Signal for observing cancel writing requests. |
| --- | --- |
| `callback` | [PrintDocumentAdapter.WriteResultCallback](../android/print/PrintDocumentAdapter.WriteResultCallback.md)!: Callback to inform the system for the write result. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/print/PrintDocumentAdapter.WriteResultCallback`
- `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#`
