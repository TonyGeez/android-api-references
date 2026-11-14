# IpSecTransform

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IpSecTransform

Kotlin| [Java](https://developer.android.com/reference/android/net/IpSecTransform "View this page in Java") 
| --- | --- |

```
class IpSecTransform : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform#) |

This class represents a transform, which roughly corresponds to an IPsec Security Association.

Transforms are created using [IpSecTransform.Builder](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.Builder). Each`IpSecTransform`object encapsulates the properties and state of an IPsec security association. That includes, but is not limited to, algorithm choice, key material, and allocated system resources.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.Builder) This class is used to build [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform#) objects. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close())`()` Deactivate this`IpSecTransform`and free allocated resources. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/IpSecTransform#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Standard equals. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestIpSecTransformState](https://developer.android.com/reference/kotlin/android/net/IpSecTransform#requestIpSecTransformState(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [IpSecTransformState](https://developer.android.com/reference/kotlin/android/net/IpSecTransformState)!,` ` [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#)!>`)` Retrieve the current state of this IpSecTransform. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/IpSecTransform#toString())`()` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/net/IpSecTransform#finalize())`()` Check that the transform was closed properly. |

## Public methods

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Deactivate this`IpSecTransform`and free allocated resources.

Deactivating a transform while it is still applied to a socket will result in errors on that socket. Make sure to remove transforms by calling android.net.IpSecManager#removeTransportModeTransforms. Note, removing an`IpSecTransform`from a socket will not deactivate it (because one transform may be applied to multiple sockets).

It is safe to call this method on a transform that has already been deactivated.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Standard equals.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### requestIpSecTransformState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestIpSecTransformState(
    executor: Executor, 
    callback: OutcomeReceiver<IpSecTransformState!, RuntimeException!>
): Unit
```

Retrieve the current state of this IpSecTransform.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to call the supplied callback. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [IpSecTransformState](https://developer.android.com/reference/kotlin/android/net/IpSecTransformState)!, [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#)!\>:Callback that's called after the transform state is ready or when an error occurs. This value cannot be`null`. |

**See Also**

- [android.net.IpSecTransformState](https://developer.android.com/reference/kotlin/android/net/IpSecTransformState) 

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Protected methods

### finalize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

Check that the transform was closed properly.

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
