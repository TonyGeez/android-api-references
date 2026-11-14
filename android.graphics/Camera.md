Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Camera

Kotlin | [Java](Camera.md)
| --- | --- |

```
open class Camera
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Camera](Camera.md) |

A camera instance can be used to compute 3D transformations and generate a matrix that can be applied, for instance, on a `https://developer.android.com/reference/kotlin/android/graphics/Canvas`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Camera#Camera()()` Creates a new camera, with empty transformations. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#applyToCanvas(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas!)` Computes the matrix corresponding to the current transformation and applies it to the specified Canvas. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#dotWithNormal(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dz: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#getLocationX()()` Gets the x location of the camera. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#getLocationY()()` Gets the y location of the camera. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#getLocationZ()()` Gets the z location of the camera. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#getMatrix(android.graphics.Matrix)(matrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix!)` Computes the matrix corresponding to the current transformation and copies it to the supplied matrix object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#restore()()` Restores the saved state, if any. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotate(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, z: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Applies a rotation transform around all three axis. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateX(kotlin.Float)(deg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Applies a rotation transform around the X axis. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateY(kotlin.Float)(deg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Applies a rotation transform around the Y axis. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateZ(kotlin.Float)(deg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Applies a rotation transform around the Z axis. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#save()()` Saves the camera state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#setLocation(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, z: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the location of the camera. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#translate(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, z: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Applies a translation transform on all three axis. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Camera#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public constructors

### Camera

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Camera()
```

Creates a new camera, with empty transformations.

## Public methods

### applyToCanvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyToCanvas(canvas: Canvas!): Unit
```

Computes the matrix corresponding to the current transformation and applies it to the specified Canvas.

| Parameters ||
|---|---|
| `canvas` | [Canvas](Canvas.md)!: The Canvas to set the transform matrix onto |

### dotWithNormal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dotWithNormal(
    dx: Float, 
    dy: Float, 
    dz: Float
): Float
```

### getLocationX

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocationX(): Float
```

Gets the x location of the camera.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#setLocation(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### getLocationY

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocationY(): Float
```

Gets the y location of the camera.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#setLocation(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### getLocationZ

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocationZ(): Float
```

Gets the z location of the camera.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#setLocation(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### getMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatrix(matrix: Matrix!): Unit
```

Computes the matrix corresponding to the current transformation and copies it to the supplied matrix object.

| Parameters ||
|---|---|
| `matrix` | [Matrix](Matrix.md)!: The matrix to copy the current transforms into |

### restore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun restore(): Unit
```

Restores the saved state, if any.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#restore()`

### rotate

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rotate(
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Applies a rotation transform around all three axis.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The angle of rotation around the X axis, in degrees |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The angle of rotation around the Y axis, in degrees |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The angle of rotation around the Z axis, in degrees |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateX(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateY(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateZ(kotlin.Float)`

### rotateX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rotateX(deg: Float): Unit
```

Applies a rotation transform around the X axis.

| Parameters ||
|---|---|
| `deg` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The angle of rotation around the X axis, in degrees |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateY(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateZ(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotate(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### rotateY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rotateY(deg: Float): Unit
```

Applies a rotation transform around the Y axis.

| Parameters ||
|---|---|
| `deg` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The angle of rotation around the Y axis, in degrees |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateX(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateZ(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotate(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### rotateZ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rotateZ(deg: Float): Unit
```

Applies a rotation transform around the Z axis.

| Parameters ||
|---|---|
| `deg` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The angle of rotation around the Z axis, in degrees |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateX(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotateY(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/Camera#rotate(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### save

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun save(): Unit
```

Saves the camera state. Each save should be balanced with a call to `https://developer.android.com/reference/kotlin/android/graphics/Camera#restore()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Camera#save()`

### setLocation

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLocation(
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Sets the location of the camera. The default location is set at 0, 0, -8.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x location of the camera |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y location of the camera |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The z location of the camera |
| --- | --- |

### translate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun translate(
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Applies a translation transform on all three axis.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance to translate by on the X axis |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance to translate by on the Y axis |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance to translate by on the Z axis |
| --- | --- |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
