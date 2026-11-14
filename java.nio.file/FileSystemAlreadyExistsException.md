# FileSystemAlreadyExistsException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileSystemAlreadyExistsException

```
open class FileSystemAlreadyExistsException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.file.FileSystemAlreadyExistsException](FileSystemAlreadyExistsException.md) |

Runtime exception thrown when an attempt is made to create a file system that already exists.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileSystemAlreadyExistsException](FileSystemAlreadyExistsException.md))`()` Constructs an instance of this class. |
| [FileSystemAlreadyExistsException](FileSystemAlreadyExistsException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

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
