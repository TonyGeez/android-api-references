# UnsupportedClassVersionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedClassVersionError

```
open class UnsupportedClassVersionError : ClassFormatError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.ClassFormatError](../java/lang/ClassFormatError.md) ||
| | | | | ↳ | [java.lang.UnsupportedClassVersionError](../java/lang/UnsupportedClassVersionError.md) |

Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedClassVersionError](../java/lang/UnsupportedClassVersionError.md))`()` Constructs a`UnsupportedClassVersionError`with no detail message. |
| [UnsupportedClassVersionError](../java/lang/UnsupportedClassVersionError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`UnsupportedClassVersionError`with the specified detail message. |

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
