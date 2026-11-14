# OverlappingFileLockException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OverlappingFileLockException

```
open class OverlappingFileLockException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java/lang/IllegalStateException.md) ||
| | | | | ↳ | [java.nio.channels.OverlappingFileLockException](../java/nio/channels/OverlappingFileLockException.md) |

Unchecked exception thrown when an attempt is made to acquire a lock on a region of a file that overlaps a region already locked by the same Java virtual machine, or when another thread is already waiting to lock an overlapping region of the same file.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OverlappingFileLockException](../java/nio/channels/OverlappingFileLockException.md))`()` Constructs an instance of this class. |

## Public constructors

### OverlappingFileLockException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OverlappingFileLockException()
```

Constructs an instance of this class.
