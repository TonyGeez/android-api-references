# AccessDeniedException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessDeniedException

```
open class AccessDeniedException : FileSystemException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.file.FileSystemException](FileSystemException.md) ||
| | | | | ↳ | [java.nio.file.AccessDeniedException](AccessDeniedException.md) |

Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check.

This exception is not related to the or [SecurityException](../java.lang/SecurityException.md) thrown by access controllers or security managers when access to a file is denied.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessDeniedException](AccessDeniedException.md))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |
| [AccessDeniedException](AccessDeniedException.md))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Inherited functions ||
|---|---|
| From class [FileSystemException](FileSystemException.md) |-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFile](FileSystemException.md))`()` <br /> Returns the file used to create this exception. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOtherFile](FileSystemException.md))`()` <br /> Returns the other file used to create this exception. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](FileSystemException.md))`()` <br /> Returns the string explaining why the file system operation failed. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FileSystemException](FileSystemException.md) |-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](FileSystemException.md) <br /> Returns the detail message string. <br /> | ||

## Public constructors

### AccessDeniedException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessDeniedException(file: String!)
```

Constructs an instance of this class.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the file or`null`if not known |

### AccessDeniedException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessDeniedException(
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
