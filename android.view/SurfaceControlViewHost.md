Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceControlViewHost

```
open class SurfaceControlViewHost
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.SurfaceControlViewHost](../android/view/SurfaceControlViewHost.md) |

Utility class for adding a View hierarchy to a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl`. The View hierarchy will render in to a root SurfaceControl, and receive input based on the SurfaceControl's placement on-screen. The primary usage of this class is to embed a View hierarchy from one process in to another. After the SurfaceControlViewHost has been set up in the embedded content provider, we can send the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage` to the host process. The host process can then attach the hierarchy to a SurfaceView within its own by calling `https://developer.android.com/reference/kotlin/android/view/SurfaceView#setChildSurfacePackage(android.view.SurfaceControlViewHost.SurfacePackage)`.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams` Specifies the layout parameters for a `https://developer.android.com/reference/kotlin/android/view/View` hosted by a `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#`. |
| | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage` Package encapsulating a Surface hierarchy which contains interactive view elements. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#SurfaceControlViewHost(android.content.Context,%20android.view.Display,%20android.os.IBinder)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, display: https://developer.android.com/reference/kotlin/android/view/Display, hostToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#?)` Construct a new SurfaceControlViewHost. |
| `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#SurfaceControlViewHost(android.content.Context,%20android.view.Display,%20android.window.InputTransferToken)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, display: https://developer.android.com/reference/kotlin/android/view/Display, hostInputTransferToken: https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#?)` Construct a new SurfaceControlViewHost. |

| Public methods ||
|---|---|
| open [SurfaceControlViewHost.LayoutParams](../android/view/SurfaceControlViewHost.LayoutParams.md) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#getLayoutParams()()` Returns the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams` of the root view. |
| open [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md)? | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#getSurfacePackage()()` Return a SurfacePackage for the root SurfaceControl of the embedded hierarchy. |
| open [View](../android/view/View.md)? | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#getView()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#relayout(android.view.SurfaceControlViewHost.LayoutParams)(attrs: https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams)` Modifies the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams` of the root view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#relayout(kotlin.Int,%20kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Modify the size of the root view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#release()()` Trigger the tear down of the embedded view hierarchy and release the SurfaceControl. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#setView(android.view.View,%20android.view.SurfaceControlViewHost.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View, attrs: https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams)` Sets the root view of the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#setView(android.view.View,%20kotlin.Int,%20kotlin.Int)(view: https://developer.android.com/reference/kotlin/android/view/View, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the root view of the SurfaceControlViewHost. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#transferTouchGestureToHost()()` Transfer the currently in progress touch gesture to the parent (if any) of this SurfaceControlViewHost. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public constructors

### SurfaceControlViewHost

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SurfaceControlViewHost(
    context: Context, 
    display: Display, 
    hostToken: IBinder?)
```

Construct a new SurfaceControlViewHost. The root Surface will be allocated internally and is accessible via getSurfacePackage(). The `hostToken` parameter, primarily used for ANR reporting, must be obtained from whomever will be hosting the embedded hierarchy. It's accessible from `https://developer.android.com/reference/kotlin/android/view/SurfaceView#getHostToken()`.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): The Context object for your activity or application. This value cannot be `null`. |
| `display` | [Display](../android/view/Display.md): The Display the hierarchy will be placed on. This value cannot be `null`. |
| `hostToken` | [IBinder](../android/os/IBinder.md)?: The host token, as discussed above. This value may be `null`. |
| --- | --- |

### SurfaceControlViewHost

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SurfaceControlViewHost(
    context: Context, 
    display: Display, 
    hostInputTransferToken: InputTransferToken?)
```

Construct a new SurfaceControlViewHost. The root Surface will be allocated internally and is accessible via getSurfacePackage().

The hostInputTransferToken parameter allows the host and embedded to be associated with each other to allow transferring touch gesture and focus. This is also used for ANR reporting. It's accessible from `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#getInputTransferToken()`.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): The Context object for your activity or application. This value cannot be `null`. |
| `display` | [Display](../android/view/Display.md): The Display the hierarchy will be placed on. This value cannot be `null`. |
| `hostInputTransferToken` | [InputTransferToken](../android/window/InputTransferToken.md)?: The host input transfer token, as discussed above. This value may be `null`. |
| --- | --- |

## Public methods

### getLayoutParams

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutParams(): SurfaceControlViewHost.LayoutParams
```

Returns the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams` of the root view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams` | This value cannot be `null`. |

### getSurfacePackage

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSurfacePackage(): SurfaceControlViewHost.SurfacePackage?
```

Return a SurfacePackage for the root SurfaceControl of the embedded hierarchy. Rather than be directly reparented using `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction` this SurfacePackage should be passed to `https://developer.android.com/reference/kotlin/android/view/SurfaceView#setChildSurfacePackage(android.view.SurfaceControlViewHost.SurfacePackage)` which will not only reparent the Surface, but ensure the accessibility hierarchies are linked.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage?` | This value may be `null`. |

### getView

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getView(): View?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View?` | The view passed to setView, or null if none has been passed. |

### relayout

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun relayout(attrs: SurfaceControlViewHost.LayoutParams): Unit
```

Modifies the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams` of the root view.

| Parameters ||
|---|---|
| `attrs` | [SurfaceControlViewHost.LayoutParams](../android/view/SurfaceControlViewHost.LayoutParams.md): This value cannot be `null`. |

### relayout

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun relayout(
    width: Int, 
    height: Int
): Unit
```

Modify the size of the root view.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width in pixels |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height in pixels |

### release

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun release(): Unit
```

Trigger the tear down of the embedded view hierarchy and release the SurfaceControl. This will result in onDispatchedFromWindow being dispatched to the embedded view hierarchy and render the object unusable.

### setView

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setView(
    view: View, 
    attrs: SurfaceControlViewHost.LayoutParams
): Unit
```

Sets the root view of the `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#`. This view will render in to the SurfaceControl, and receive input based on the SurfaceControl's positioning on screen. It will be laid out as if it were in a window of the passed in width and height.

| Parameters ||
|---|---|
| `view` | [View](../android/view/View.md): The `https://developer.android.com/reference/kotlin/android/view/View` to add. This value cannot be `null`. |
| `attrs` | [SurfaceControlViewHost.LayoutParams](../android/view/SurfaceControlViewHost.LayoutParams.md): The `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.LayoutParams` parameters for the `https://developer.android.com/reference/kotlin/android/view/View`. This value cannot be `null`. |

### setView

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setView(
    view: View, 
    width: Int, 
    height: Int
): Unit
```

Set the root view of the SurfaceControlViewHost. This view will render in to the SurfaceControl, and receive input based on the SurfaceControls positioning on screen. It will be laid as if it were in a window of the passed in width and height.

| Parameters ||
|---|---|
| `view` | [View](../android/view/View.md): The View to add. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width to layout the View within, in pixels. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height to layout the View within, in pixels. |
| --- | --- |

### transferTouchGestureToHost

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun transferTouchGestureToHost(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/WindowManager#transferTouchGesture(android.window.InputTransferToken,%20android.window.InputTransferToken)` instead.*

Transfer the currently in progress touch gesture to the parent (if any) of this SurfaceControlViewHost. This requires that the SurfaceControlViewHost was created with an associated host `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the touch stream was transferred. |

## Protected methods

### finalize

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
