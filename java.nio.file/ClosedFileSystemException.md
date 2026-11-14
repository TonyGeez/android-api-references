# ClosedFileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClosedFileSystemException

```
open class ClosedFileSystemException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) ||
| | | | | ↳ | [java.nio.file.ClosedFileSystemException](ClosedFileSystemException.md) |

Unchecked exception thrown when an attempt is made to invoke an operation on a file and the file system is closed.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClosedFileSystemException](ClosedFileSystemException.md))`()` Constructs an instance of this class. |

## Public constructors

### ClosedFileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClosedFileSystemException()
```

Constructs an instance of this class.
