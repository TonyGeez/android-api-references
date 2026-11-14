# ThreadDeath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadDeath

```
open class ThreadDeath : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](Error.md) ||
| | | ↳ | [java.lang.ThreadDeath](ThreadDeath.md) |
| --- | --- | --- | --- |

An instance of `ThreadDeath` is thrown in the victim thread when the (deprecated) [Thread.stop()](Thread.md)) method is invoked.

An application should catch instances of this class only if it must clean up after being terminated asynchronously. If `ThreadDeath` is caught by a method, it is important that it be rethrown so that the thread actually dies.

The [handler](ThreadGroup.md)) does not print out a message if `ThreadDeath` is never caught.

The class `ThreadDeath` is specifically a subclass of `Error` rather than `Exception`, even though it is a "normal occurrence", because many applications catch all occurrences of `Exception` and then discard the exception.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------|---|
| [ThreadDeath](ThreadDeath.md))`()` <br /> |

## Public constructors

### ThreadDeath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ThreadDeath()
```
