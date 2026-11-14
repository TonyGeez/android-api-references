Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceControl

```
class SurfaceControl : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.SurfaceControl](SurfaceControl.md) |

Handle to an on-screen Surface managed by the system compositor. The SurfaceControl is a combination of a buffer source, and metadata about how to display the buffers. By constructing a Surface from this SurfaceControl you can submit buffers to be composited. Using `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction` you can manipulate various properties of how the buffer will be displayed on-screen. SurfaceControl's are arranged into a scene-graph like hierarchy, and as such any SurfaceControl may have a parent. Geometric properties like transform, crop, and Z-ordering will be inherited from the parent, as if the child were content in the parents buffer stream.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Builder` Builder class for SurfaceControl objects. |
| | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.JankData` Jank information to be fed back via `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener`. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener` Listener interface to be informed about SurfaceFlinger's jank classification for a specific surface. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListenerRegistration` Handle to a registered OnJankDatalistener. |
| | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction` An atomic set of changes to a set of SurfaceControl. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.TransactionCommittedListener` Interface to handle request to addTransactionCommittedListener |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.TransactionStats` Transaction stats given to the listener registered in addTransactionCompletedListener |
| | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.TrustedPresentationThresholds` Threshold values that are sent with setTrustedPresentationCallback |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_IDENTITY:kotlin.Int` Identity transform. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_HORIZONTAL:kotlin.Int` Mirror horizontally. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_HORIZONTAL_ROTATE_90:kotlin.Int` Mirror horizontally and rotate 90 degrees clock-wise. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_VERTICAL:kotlin.Int` Mirror vertically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_VERTICAL_ROTATE_90:kotlin.Int` Mirror vertically and rotate 90 degrees clock-wise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_180:kotlin.Int` Rotate 180 degrees clock-wise. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_270:kotlin.Int` Rotate 270 degrees clock-wise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_90:kotlin.Int` Rotate 90 degrees clock-wise. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isValid Check whether this instance points to a valid layer with the system-compositor. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readFromParcel <br /> |
| --- | --- |
| [SurfaceControl.OnJankDataListenerRegistration](../android/view/SurfaceControl.OnJankDataListenerRegistration.md) | registerOnJankDataListener Registers a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener` to receive jank classification data about rendered frames. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | release Release the local reference to the server-side surface. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SurfaceControl](SurfaceControl.md)!\> | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### BUFFER_TRANSFORM_IDENTITY

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_TRANSFORM_IDENTITY: Int
```

Identity transform. These transforms that can be applied to buffers as they are displayed to a window.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#`

### BUFFER_TRANSFORM_MIRROR_HORIZONTAL

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_TRANSFORM_MIRROR_HORIZONTAL: Int
```

Mirror horizontally. Can be combined with `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_VERTICAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_90:kotlin.Int`.

 Value: 1

### BUFFER_TRANSFORM_MIRROR_HORIZONTAL_ROTATE_90

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_TRANSFORM_MIRROR_HORIZONTAL_ROTATE_90: Int
```

Mirror horizontally and rotate 90 degrees clock-wise. Equivalent to (`https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_HORIZONTAL:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_90:kotlin.Int`).
| --- | --- |

 Value: 5

### BUFFER_TRANSFORM_MIRROR_VERTICAL

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_TRANSFORM_MIRROR_VERTICAL: Int
```

Mirror vertically. Can be combined with `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_HORIZONTAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_90:kotlin.Int`.

 Value: 2

### BUFFER_TRANSFORM_MIRROR_VERTICAL_ROTATE_90

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_TRANSFORM_MIRROR_VERTICAL_ROTATE_90: Int
```

Mirror vertically and rotate 90 degrees clock-wise. Equivalent to (`https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_VERTICAL:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_90:kotlin.Int`).
| --- | --- |

 Value: 6

### BUFFER_TRANSFORM_ROTATE_180

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_TRANSFORM_ROTATE_180: Int
```

Rotate 180 degrees clock-wise. Cannot be combined with other transforms. Equivalent to (`https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_HORIZONTAL:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_VERTICAL:kotlin.Int`).
| --- | --- |

 Value: 3

### BUFFER_TRANSFORM_ROTATE_270

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_TRANSFORM_ROTATE_270: Int
```

Rotate 270 degrees clock-wise. Cannot be combined with other transforms. Equivalent to (`https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_180:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_ROTATE_90:kotlin.Int`).
| --- | --- |

 Value: 7

### BUFFER_TRANSFORM_ROTATE_90

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_TRANSFORM_ROTATE_90: Int
```

Rotate 90 degrees clock-wise. Can be combined with `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_HORIZONTAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/SurfaceControl#BUFFER_TRANSFORM_MIRROR_VERTICAL:kotlin.Int`.

 Value: 4

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### isValid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isValid(): Boolean
```

Check whether this instance points to a valid layer with the system-compositor. For example this may be false if construction failed, or the layer was released (release).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this SurfaceControl is valid. |

### readFromParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readFromParcel(in: Parcel!): Unit
```

### registerOnJankDataListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerOnJankDataListener(
    executor: Executor, 
    listener: SurfaceControl.OnJankDataListener
): SurfaceControl.OnJankDataListenerRegistration
```

Registers a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener` to receive jank classification data about rendered frames.

Use removeAfter to unregister the listener.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor on which the listener will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [SurfaceControl.OnJankDataListener](../android/view/SurfaceControl.OnJankDataListener.md): The listener to add. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListenerRegistration` | The `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListenerRegistration` for the listener. This value cannot be `null`. |

### release

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun release(): Unit
```

Release the local reference to the server-side surface. The surface may continue to exist on-screen as long as its parent continues to exist. To explicitly remove a surface from the screen use reparent with a null-parent. After release, isValid will return false and other methods will throw an exception. Always call release() when you're done with a SurfaceControl.

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Protected methods

### finalize

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
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

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SurfaceControl!>
```
