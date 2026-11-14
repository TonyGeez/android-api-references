# DirectoryIteratorException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DirectoryIteratorException

```
class DirectoryIteratorException : ConcurrentModificationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.ConcurrentModificationException](../java/util/ConcurrentModificationException.md) ||
| | | | | ↳ | [java.nio.file.DirectoryIteratorException](../java/nio/file/DirectoryIteratorException.md) |

Runtime exception thrown if an I/O error is encountered when iterating over the entries in a directory. The I/O error is retrieved as an [IOException](../java/io/IOException.md) using the [getCause()](../java/nio/file/DirectoryIteratorException.md) method.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DirectoryIteratorException](../java/nio/file/DirectoryIteratorException.md))`(`cause:` ` [IOException](../java/io/IOException.md)!`)` Constructs an instance of this class. |

| Properties ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IOException](../java/io/IOException.md)? | [cause](../java/nio/file/DirectoryIteratorException.md) Returns the cause of this exception. |

## Public constructors

### DirectoryIteratorException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DirectoryIteratorException(cause: IOException!)
```

Constructs an instance of this class.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [IOException](../java/io/IOException.md)!:the`IOException`that caused the directory iteration to fail |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if the cause is`null` |

## Properties

### cause

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val cause: IOException?
```

Returns the cause of this exception.

| Return ||
|------------------------------------------------------------------------------------------|-----------|
| [IOException](../java/io/IOException.md)? | the cause |
