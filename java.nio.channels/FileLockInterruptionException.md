# FileLockInterruptionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileLockInterruptionException

```
open class FileLockInterruptionException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.channels.FileLockInterruptionException](FileLockInterruptionException.md) |

Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock. Before this exception is thrown the interrupt status of the previously-blocked thread will have been set.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileLockInterruptionException](FileLockInterruptionException.md))`()` Constructs an instance of this class. |

## Public constructors

### FileLockInterruptionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileLockInterruptionException()
```

Constructs an instance of this class.
