# IpSecTransform

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IpSecTransform

Kotlin| [Java](IpSecTransform.md) 
| --- | --- |

```
class IpSecTransform : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.IpSecTransform](IpSecTransform.md) |

This class represents a transform, which roughly corresponds to an IPsec Security Association.

Transforms are created using [IpSecTransform.Builder](../android/net/IpSecTransform.Builder.md). Each`IpSecTransform`object encapsulates the properties and state of an IPsec security association. That includes, but is not limited to, algorithm choice, key material, and allocated system resources.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/IpSecTransform.Builder.md) This class is used to build [IpSecTransform](IpSecTransform.md) objects. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](IpSecTransform.md))`()` Deactivate this`IpSecTransform`and free allocated resources. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](IpSecTransform.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Standard equals. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestIpSecTransformState](IpSecTransform.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [IpSecTransformState](IpSecTransformState.md)!,` ` [RuntimeException](../java.lang/RuntimeException.md)!>`)` Retrieve the current state of this IpSecTransform. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](IpSecTransform.md))`()` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](IpSecTransform.md))`()` Check that the transform was closed properly. |

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
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) on which to call the supplied callback. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [IpSecTransformState](IpSecTransformState.md)!, [RuntimeException](../java.lang/RuntimeException.md)!\>:Callback that's called after the transform state is ready or when an error occurs. This value cannot be`null`. |

**See Also**

- [android.net.IpSecTransformState](IpSecTransformState.md) 

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
