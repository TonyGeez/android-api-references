# DirectoryIteratorException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DirectoryIteratorException

```
class DirectoryIteratorException : ConcurrentModificationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException.html#) ||
| | | | | ↳ | [java.nio.file.DirectoryIteratorException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryIteratorException#) |

Runtime exception thrown if an I/O error is encountered when iterating over the entries in a directory. The I/O error is retrieved as an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) using the [getCause()](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryIteratorException#cause:java.io.IOException) method.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DirectoryIteratorException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryIteratorException#DirectoryIteratorException(java.io.IOException))`(`cause:` ` [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!`)` Constructs an instance of this class. |

| Properties ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)? | [cause](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryIteratorException#cause:java.io.IOException) Returns the cause of this exception. |

## Public constructors

### DirectoryIteratorException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DirectoryIteratorException(cause: IOException!)
```

Constructs an instance of this class.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!:the`IOException`that caused the directory iteration to fail |

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
| [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)? | the cause |
