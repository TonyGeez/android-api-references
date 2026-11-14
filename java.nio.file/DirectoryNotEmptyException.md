# DirectoryNotEmptyException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DirectoryNotEmptyException

```
open class DirectoryNotEmptyException : FileSystemException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| | | | ↳ | [java.nio.file.FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException) ||
| | | | | ↳ | [java.nio.file.DirectoryNotEmptyException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryNotEmptyException#) |

Checked exception thrown when a file system operation fails because a directory is not empty.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DirectoryNotEmptyException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryNotEmptyException#DirectoryNotEmptyException(kotlin.String))`(`dir:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Inherited functions ||
|---|---|
| From class [FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException) |-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFile](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getFile())`()` <br /> Returns the file used to create this exception. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOtherFile](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getOtherFile())`()` <br /> Returns the other file used to create this exception. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getReason())`()` <br /> Returns the string explaining why the file system operation failed. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException) |-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#message:kotlin.String) <br /> Returns the detail message string. <br /> | ||

## Public constructors

### DirectoryNotEmptyException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DirectoryNotEmptyException(dir: String!)
```

Constructs an instance of this class.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the directory or`null`if not known |
