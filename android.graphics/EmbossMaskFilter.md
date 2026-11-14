Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EmbossMaskFilter

Kotlin | [Java](https://developer.android.com/reference/android/graphics/EmbossMaskFilter "View this page in Java")
| --- | --- |

```
open class EmbossMaskFilter : MaskFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.MaskFilter](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter) ||
| | ↳ | [android.graphics.EmbossMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/EmbossMaskFilter#) |

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/EmbossMaskFilter#EmbossMaskFilter(kotlin.FloatArray,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!, ambient: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, specular: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, blurRadius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Create an emboss maskfilter |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/graphics/MaskFilter` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/MaskFilter#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | ||

## Public constructors

### EmbossMaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
EmbossMaskFilter(
    direction: FloatArray!, 
    ambient: Float, 
    specular: Float, 
    blurRadius: Float)
```

**Deprecated:** *This subclass is not supported and should not be instantiated.*

Create an emboss maskfilter

| Parameters ||
|---|---|
| `direction` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: array of 3 scalars \[x, y, z\] specifying the direction of the light source |
| `ambient` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): 0...1 amount of ambient light |
| `specular` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): coefficient for specular highlights (e.g. 8) |
| --- | --- |
| `blurRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): amount to blur before applying lighting (e.g. 3) |

| Return ||
|---|---|
| | the emboss maskfilter |
