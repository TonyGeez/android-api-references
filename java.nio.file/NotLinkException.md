# NotLinkException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NotLinkException

```
open class NotLinkException : FileSystemException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.file.FileSystemException](FileSystemException.md) ||
| | | | | ↳ | [java.nio.file.NotLinkException](NotLinkException.md) |

Checked exception thrown when a file system operation fails because a file is not a symbolic link.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NotLinkException](NotLinkException.md))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |
| [NotLinkException](NotLinkException.md))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Inherited functions ||
|---|---|
| From class [FileSystemException](FileSystemException.md) |-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFile](FileSystemException.md))`()` <br /> Returns the file used to create this exception. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOtherFile](FileSystemException.md))`()` <br /> Returns the other file used to create this exception. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](FileSystemException.md))`()` <br /> Returns the string explaining why the file system operation failed. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FileSystemException](FileSystemException.md) |-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](FileSystemException.md) <br /> Returns the detail message string. <br /> | ||

## Public constructors

### NotLinkException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NotLinkException(file: String!)
```

Constructs an instance of this class.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the file or`null`if not known |

### NotLinkException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NotLinkException(
    file: String!, 
    other: String!, 
    reason: String!)
```

Constructs an instance of this class.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the file or`null`if not known |
| `other` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the other file or`null`if not known |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a reason message with additional information or`null` |
| --- | --- |
