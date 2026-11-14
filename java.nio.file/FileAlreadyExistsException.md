# FileAlreadyExistsException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileAlreadyExistsException

```
open class FileAlreadyExistsException : FileSystemException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.file.FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException) ||
| | | | | ↳ | [java.nio.file.FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException#) |

Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException#FileAlreadyExistsException(kotlin.String))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |
| [FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException#FileAlreadyExistsException(kotlin.String,%20kotlin.String,%20kotlin.String))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Inherited functions ||
|---|---|
| From class [FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException) |-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFile](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getFile())`()` <br /> Returns the file used to create this exception. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOtherFile](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getOtherFile())`()` <br /> Returns the other file used to create this exception. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getReason())`()` <br /> Returns the string explaining why the file system operation failed. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException) |-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#message:kotlin.String) <br /> Returns the detail message string. <br /> | ||

## Public constructors

### FileAlreadyExistsException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileAlreadyExistsException(file: String!)
```

Constructs an instance of this class.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the file or`null`if not known |

### FileAlreadyExistsException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileAlreadyExistsException(
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
