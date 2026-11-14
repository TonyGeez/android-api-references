# FileLockInterruptionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileLockInterruptionException

```
open class FileLockInterruptionException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [java.nio.channels.FileLockInterruptionException](https://developer.android.com/reference/kotlin/java/nio/channels/FileLockInterruptionException#) |

Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock. Before this exception is thrown the interrupt status of the previously-blocked thread will have been set.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileLockInterruptionException](https://developer.android.com/reference/kotlin/java/nio/channels/FileLockInterruptionException#FileLockInterruptionException())`()` Constructs an instance of this class. |

## Public constructors

### FileLockInterruptionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileLockInterruptionException()
```

Constructs an instance of this class.
