# UTFDataFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UTFDataFormatException

```
open class UTFDataFormatException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.UTFDataFormatException](https://developer.android.com/reference/kotlin/java/io/UTFDataFormatException#) |

Signals that a malformed string in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format has been read in a data input stream or by any class that implements the data input interface. See the [`DataInput`](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) class description for the format in which modified UTF-8 strings are read and written.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UTFDataFormatException](https://developer.android.com/reference/kotlin/java/io/UTFDataFormatException#UTFDataFormatException())`()` Constructs a`UTFDataFormatException`with`null`as its error detail message. |
| [UTFDataFormatException](https://developer.android.com/reference/kotlin/java/io/UTFDataFormatException#UTFDataFormatException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`UTFDataFormatException`with the specified detail message. |

## Public constructors

### UTFDataFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UTFDataFormatException()
```

Constructs a`UTFDataFormatException`with`null`as its error detail message. 

### UTFDataFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UTFDataFormatException(s: String!)
```

Constructs a`UTFDataFormatException`with the specified detail message. The string`s`can be retrieved later by the [java.lang.Throwable#getMessage](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method of class`java.lang.Throwable`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
