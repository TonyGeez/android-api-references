# FileNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileNotFoundException

```
open class FileNotFoundException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.FileNotFoundException](../java/io/FileNotFoundException.md) |

Signals that an attempt to open the file denoted by a specified pathname has failed.

This exception will be thrown by the [FileInputStream](../java/io/FileInputStream.md), [FileOutputStream](../java/io/FileOutputStream.md), and [RandomAccessFile](../java/io/RandomAccessFile.md) constructors when a file with the specified pathname does not exist. It will also be thrown by these constructors if the file does exist but for some reason is inaccessible, for example when an attempt is made to open a read-only file for writing.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileNotFoundException](../java/io/FileNotFoundException.md))`()` Constructs a`FileNotFoundException`with`null`as its error detail message. |
| [FileNotFoundException](../java/io/FileNotFoundException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`FileNotFoundException`with the specified detail message. |

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

Constructs a`FileNotFoundException`with the specified detail message. The string`s`can be retrieved later by the [java.lang.Throwable#getMessage](../java/lang/Throwable.md))method of class`java.lang.Throwable`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
