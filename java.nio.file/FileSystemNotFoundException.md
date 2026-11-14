# FileSystemNotFoundException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileSystemNotFoundException

```
open class FileSystemNotFoundException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.file.FileSystemNotFoundException](FileSystemNotFoundException.md) |

Runtime exception thrown when a file system cannot be found.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileSystemNotFoundException](FileSystemNotFoundException.md))`()` Constructs an instance of this class. |
| [FileSystemNotFoundException](FileSystemNotFoundException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

## Public constructors

### FileSystemNotFoundException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileSystemNotFoundException()
```

Constructs an instance of this class. 

### FileSystemNotFoundException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileSystemNotFoundException(msg: String!)
```

Constructs an instance of this class.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
