# FileNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileNotFoundException

```
open class FileNotFoundException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException#) |

Signals that an attempt to open the file denoted by a specified pathname has failed.

This exception will be thrown by the [FileInputStream](https://developer.android.com/reference/kotlin/java/io/FileInputStream), [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream), and [RandomAccessFile](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile) constructors when a file with the specified pathname does not exist. It will also be thrown by these constructors if the file does exist but for some reason is inaccessible, for example when an attempt is made to open a read-only file for writing.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException#FileNotFoundException())`()` Constructs a`FileNotFoundException`with`null`as its error detail message. |
| [FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException#FileNotFoundException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`FileNotFoundException`with the specified detail message. |

## Public constructors

### FileNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileNotFoundException()
```

Constructs a`FileNotFoundException`with`null`as its error detail message. 

### FileNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileNotFoundException(s: String!)
```

Constructs a`FileNotFoundException`with the specified detail message. The string`s`can be retrieved later by the [java.lang.Throwable#getMessage](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method of class`java.lang.Throwable`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
