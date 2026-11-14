# UnsupportedClassVersionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedClassVersionError

```
open class UnsupportedClassVersionError : ClassFormatError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) ||||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) |||
| | | | ↳ | [java.lang.ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError) ||
| | | | | ↳ | [java.lang.UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError#) |

Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError#UnsupportedClassVersionError())`()` Constructs a`UnsupportedClassVersionError`with no detail message. |
| [UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError#UnsupportedClassVersionError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`UnsupportedClassVersionError`with the specified detail message. |

## Public constructors

### UnsupportedClassVersionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedClassVersionError()
```

Constructs a`UnsupportedClassVersionError`with no detail message. 

### UnsupportedClassVersionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedClassVersionError(s: String!)
```

Constructs a`UnsupportedClassVersionError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
