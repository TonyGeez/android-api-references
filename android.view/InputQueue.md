# InputQueue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputQueue

Kotlin| [Java](https://developer.android.com/reference/android/view/InputQueue "View this page in Java") 
| --- | --- |

```
class InputQueue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.InputQueue](https://developer.android.com/reference/kotlin/android/view/InputQueue#) |

An input queue provides a mechanism for an application to receive incoming input events. Currently only usable from native code.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/view/InputQueue.Callback) Interface to receive notification of when an InputQueue is associated and dissociated with a thread. |

| Protected methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/view/InputQueue#finalize())`()` <br /> |

## Protected methods

### finalize

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
