# FileSystemAlreadyExistsException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileSystemAlreadyExistsException

```
open class FileSystemAlreadyExistsException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [java.nio.file.FileSystemAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemAlreadyExistsException#) |

Runtime exception thrown when an attempt is made to create a file system that already exists.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileSystemAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemAlreadyExistsException#FileSystemAlreadyExistsException())`()` Constructs an instance of this class. |
| [FileSystemAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemAlreadyExistsException#FileSystemAlreadyExistsException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

## Public constructors

### FileSystemAlreadyExistsException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileSystemAlreadyExistsException()
```

Constructs an instance of this class. 

### FileSystemAlreadyExistsException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileSystemAlreadyExistsException(msg: String!)
```

Constructs an instance of this class.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
