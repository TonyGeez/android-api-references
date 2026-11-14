# InputQueue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputQueue

Kotlin| [Java](../android/view/InputQueue.md) 
| --- | --- |

```
class InputQueue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.InputQueue](../android/view/InputQueue.md) |

An input queue provides a mechanism for an application to receive incoming input events. Currently only usable from native code.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/view/InputQueue.Callback.md) Interface to receive notification of when an InputQueue is associated and dissociated with a thread. |

| Protected methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/view/InputQueue.md))`()` <br /> |

## Protected methods

### finalize

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
