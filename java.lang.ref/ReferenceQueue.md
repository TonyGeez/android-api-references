# ReferenceQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReferenceQueue

```
open class ReferenceQueue<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ref.ReferenceQueue](../java/lang/ref/ReferenceQueue.md) |

Reference queues, to which registered reference objects are appended by the garbage collector after the appropriate reachability changes are detected.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReferenceQueue](../java/lang/ref/ReferenceQueue.md))`()` Constructs a new reference-object queue. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Reference](../java/lang/ref/Reference.md)\<outT\>! | [poll](../java/lang/ref/ReferenceQueue.md))`()` Polls this queue to see if a reference object is available. |
| open [Reference](../java/lang/ref/Reference.md)\<outT\>! | [remove](../java/lang/ref/ReferenceQueue.md))`()` Removes the next reference object in this queue, blocking until one becomes available. |
| open [Reference](../java/lang/ref/Reference.md)\<outT\>! | [remove](../java/lang/ref/ReferenceQueue.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Removes the next reference object in this queue, blocking until either one becomes available or the given timeout period expires. |
| --- | --- |

## Public constructors

### ReferenceQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReferenceQueue()
```

Constructs a new reference-object queue.

## Public methods

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(): Reference<out T>!
```

Polls this queue to see if a reference object is available. If one is available without further delay then it is removed from the queue and returned. Otherwise this method immediately returns null.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Reference](../java/lang/ref/Reference.md)<out` `T>! | A reference object, if one was immediately available, otherwise`null` |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(): Reference<out T>!
```

Removes the next reference object in this queue, blocking until one becomes available.

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Reference](../java/lang/ref/Reference.md)<out` `T>! | A reference object, blocking until one becomes available |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.InterruptedException` | If the wait is interrupted |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(timeout: Long): Reference<out T>!
```

Removes the next reference object in this queue, blocking until either one becomes available or the given timeout period expires.

This method does not offer real-time guarantees: It schedules the timeout as if by invoking the [Object.wait(long)](../java/lang/Object.md))method.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):If positive, block for up to`timeout`milliseconds while waiting for a reference to be added to this queue. If zero, block indefinitely. |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Reference](../java/lang/ref/Reference.md)<out` `T>! | A reference object, if one was available within the specified timeout period, otherwise`null` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the value of the timeout argument is negative |
| `java.lang.InterruptedException` | If the timeout wait is interrupted |
