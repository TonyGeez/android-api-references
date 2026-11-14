Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttachedSurfaceControl

```
interface AttachedSurfaceControl
```

| [android.view.AttachedSurfaceControl](https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#) |

Provides an interface to the root-Surface of a View Hierarchy or Window. This is used in combination with the `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` API to enable attaching app created SurfaceControl to the SurfaceControl hierarchy used by the app, and enable SurfaceTransactions to be performed in sync with the View hierarchy drawing. This object is obtained from `https://developer.android.com/reference/kotlin/android/view/View#getRootSurfaceControl()` and `https://developer.android.com/reference/kotlin/android/view/Window#getRootSurfaceControl()`. It must be used from the UI thread of the object it was obtained from.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener` Buffer transform hint change listener. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#addOnBufferTransformHintChangedListener(android.view.AttachedSurfaceControl.OnBufferTransformHintChangedListener)(listener: https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener)` Registers a `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener` to receive notifications about when the transform hint changes. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#applyTransactionOnDraw(android.view.SurfaceControl.Transaction)(t: https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction)` Consume the passed in transaction, and request the View hierarchy to apply it atomically with the next draw. |
| abstract [SurfaceControl.Transaction](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction)? | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#buildReparentTransaction(android.view.SurfaceControl)(child: https://developer.android.com/reference/kotlin/android/view/SurfaceControl)` Create a transaction which will reparent `child` to the View hierarchy root SurfaceControl. |
| --- | --- |
| open [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#createMirror()()` Creates a mirrored `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` of the root `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` hierarchy. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#getBufferTransformHint()()` The transform hint can be used by a buffer producer to pre-rotate the rendering such that the final transformation in the system composer is identity. |
| open [InputTransferToken](https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#getInputTransferToken()()` Gets the token used for associating this `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#` with an embedded `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost` or `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` |
| --- | --- |
| open [SurfaceControl.OnJankDataListenerRegistration](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListenerRegistration) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#registerOnJankDataListener(java.util.concurrent.Executor,%20android.view.SurfaceControl.OnJankDataListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener)` Registers a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener` to receive jank classification data about rendered frames. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#removeOnBufferTransformHintChangedListener(android.view.AttachedSurfaceControl.OnBufferTransformHintChangedListener)(listener: https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener)` Unregisters a `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#setChildBoundingInsets(android.graphics.Rect)(insets: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Set a crop region on all children parented to the layer represented by this AttachedSurfaceControl. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#setTouchableRegion(android.graphics.Region)(r: https://developer.android.com/reference/kotlin/android/graphics/Region.html#?)` Sets the touchable region for this SurfaceControl, expressed in surface local coordinates. |

## Public methods

### addOnBufferTransformHintChangedListener

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnBufferTransformHintChangedListener(listener: AttachedSurfaceControl.OnBufferTransformHintChangedListener): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener` to receive notifications about when the transform hint changes.

| Parameters ||
|---|---|
| `listener` | [AttachedSurfaceControl.OnBufferTransformHintChangedListener](https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#getBufferTransformHint()`
- `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#removeOnBufferTransformHintChangedListener(android.view.AttachedSurfaceControl.OnBufferTransformHintChangedListener)`

### applyTransactionOnDraw

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun applyTransactionOnDraw(t: SurfaceControl.Transaction): Boolean
```

Consume the passed in transaction, and request the View hierarchy to apply it atomically with the next draw. This transaction will be merged with the buffer transaction from the ViewRoot and they will show up on-screen atomically synced. This will not cause a draw to be scheduled, and if there are no other changes to the View hierarchy you may need to call android.view.View#invalidate

| Parameters ||
|---|---|
| `t` | [SurfaceControl.Transaction](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction): This value cannot be `null`. |

### buildReparentTransaction

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun buildReparentTransaction(child: SurfaceControl): SurfaceControl.Transaction?
```

Create a transaction which will reparent `child` to the View hierarchy root SurfaceControl. See `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction#reparent(android.view.SurfaceControl,%20android.view.SurfaceControl)`. This transacton must be applied or merged in to another transaction by the caller, otherwise it will have no effect.

| Parameters ||
|---|---|
| `child` | [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl): The SurfaceControl to reparent. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction?` | A new transaction which performs the reparent operation when applied. This value may be `null`. |

### createMirror

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createMirror(): SurfaceControl
```

Creates a mirrored `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` of the root `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` hierarchy.

The returned `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` acts as a new root for the mirrored content, and its properties can be manipulated independently from the original surface. Transformations applied to this returned `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` will affect the mirrored content, but will not affect the original.

The returned `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` will be invalid if the mirror creation failed. Caller is responsible to call `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#release()` for the mirror after usage.

The relationship can be visualized as:

```kotlin
Real Hierarchy    Mirror
                      SC (value that's returned)
                       |
       A               A'
       |               |
       B               B'
  
```

In the diagram above, A is the root `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` of this `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#`. A' is a mirror of A. B is a child of A and B' is a mirror of B. The returned value, SC, is a new `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` that is the parent of the mirrored hierarchy.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` | a mirrored `https://developer.android.com/reference/kotlin/android/view/SurfaceControl` of the root `https://developer.android.com/reference/kotlin/android/view/SurfaceControl`. This value cannot be `null`. |

### getBufferTransformHint

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBufferTransformHint(): Int
```

The transform hint can be used by a buffer producer to pre-rotate the rendering such that the final transformation in the system composer is identity. This can be very useful when used in conjunction with the h/w composer HAL in situations where it cannot handle rotations or handle them with an additional power cost. The transform hint should be used with ASurfaceControl APIs when submitting buffers. Example usage: 1. After a configuration change, before dequeuing a buffer, the buffer producer queries the function for the transform hint. 2. The desired buffer width and height is rotated by the transform hint. 3. The producer dequeues a buffer of the new pre-rotated size. 4. The producer renders to the buffer such that the image is already transformed, that is applying the transform hint to the rendering. 5. The producer applies the inverse transform hint to the buffer it just rendered. 6. The producer queues the pre-transformed buffer with the buffer transform. 7. The composer combines the buffer transform with the display transform. If the buffer transform happens to cancel out the display transform then no rotation is needed and there will be no performance penalties. Note, when using ANativeWindow APIs in conjunction with a NativeActivity Surface or SurfaceView Surface, the buffer producer will already have access to the transform hint and no additional work is needed. If the root surface is not available, the API will return `BUFFER_TRANSFORM_IDENTITY`. The caller should register a listener to listen for any changes. @see `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#addOnBufferTransformHintChangedListener(android.view.AttachedSurfaceControl.OnBufferTransformHintChangedListener)`. Warning: Calling this API in Android 14 (API Level 34) or earlier will crash if the root surface is not available.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_IDENTITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_HORIZONTAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_VERTICAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_90:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_180:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_270:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_HORIZONTAL_ROTATE_90:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_VERTICAL_ROTATE_90:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#`

### getInputTransferToken

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInputTransferToken(): InputTransferToken
```

Gets the token used for associating this `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#` with an embedded `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost` or `https://developer.android.com/reference/kotlin/android/view/SurfaceControl`

This token should be passed to `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost#SurfaceControlViewHost(android.content.Context,%20android.view.Display,%20android.window.InputTransferToken)` or android.view.WindowManager#registerBatchedSurfaceControlInputReceiver(int,android.window.InputTransferToken,android.view.SurfaceControl,android.view.Choreographer,android.view.SurfaceControlInputReceiver) or android.view.WindowManager#registerUnbatchedSurfaceControlInputReceiver(int,android.window.InputTransferToken,android.view.SurfaceControl,android.os.Looper,android.view.SurfaceControlInputReceiver)

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#` | The `https://developer.android.com/reference/kotlin/android/window/InputTransferToken.html#` for the `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#` This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#` was created with no registered input |

### registerOnJankDataListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerOnJankDataListener(
    executor: Executor, 
    listener: SurfaceControl.OnJankDataListener
): SurfaceControl.OnJankDataListenerRegistration
```

Registers a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener` to receive jank classification data about rendered frames.

Use `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListenerRegistration#removeAfter(kotlin.Long)` to unregister the listener.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which the listener will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [SurfaceControl.OnJankDataListener](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener): The listener to add. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListenerRegistration` | The `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListenerRegistration` for the listener. This value cannot be `null`. |

### removeOnBufferTransformHintChangedListener

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnBufferTransformHintChangedListener(listener: AttachedSurfaceControl.OnBufferTransformHintChangedListener): Unit
```

Unregisters a `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener`.

| Parameters ||
|---|---|
| `listener` | [AttachedSurfaceControl.OnBufferTransformHintChangedListener](https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.OnBufferTransformHintChangedListener): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl#addOnBufferTransformHintChangedListener(android.view.AttachedSurfaceControl.OnBufferTransformHintChangedListener)`

### setChildBoundingInsets

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChildBoundingInsets(insets: Rect): Unit
```

Set a crop region on all children parented to the layer represented by this AttachedSurfaceControl. This includes SurfaceView, and an example usage may be to ensure that SurfaceView with `https://developer.android.com/reference/kotlin/android/view/SurfaceView#setZOrderOnTop(kotlin.Boolean)` are cropped to a region not including the app bar.

This cropped is expressed in terms of insets in window-space. Negative insets are considered invalid and will produce an exception. Insets of zero will produce the same result as if this function had never been called.

| Parameters ||
|---|---|
| `insets` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): The insets in each direction by which to bound the children expressed in window-space. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If negative insets are provided. |

### setTouchableRegion

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTouchableRegion(r: Region?): Unit
```

Sets the touchable region for this SurfaceControl, expressed in surface local coordinates. By default the touchable region is the entire Layer, indicating that if the layer is otherwise eligible to receive touch it receives touch on the entire surface. Setting the touchable region allows the SurfaceControl to receive touch in some regions, while allowing for pass-through in others.

| Parameters ||
|---|---|
| `r` | [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)?: The region to use or null to use the entire Layer bounds |
