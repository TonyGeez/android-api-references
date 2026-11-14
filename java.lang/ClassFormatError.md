# ClassFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClassFormatError

```
open class ClassFormatError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](Error.md) |||
| | | ↳ | [java.lang.LinkageError](LinkageError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.ClassFormatError](ClassFormatError.md) |

| Known Direct Subclasses [GenericSignatureFormatError](../java.lang.reflect/GenericSignatureFormatError.md), [UnsupportedClassVersionError](UnsupportedClassVersionError.md) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [GenericSignatureFormatError](../java.lang.reflect/GenericSignatureFormatError.md) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. | | [UnsupportedClassVersionError](UnsupportedClassVersionError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClassFormatError](ClassFormatError.md))`()` Constructs a`ClassFormatError`with no detail message. |
| [ClassFormatError](ClassFormatError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`ClassFormatError`with the specified detail message. |

## Public constructors

### ClassFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassFormatError()
```

Constructs a`ClassFormatError`with no detail message. 

### ClassFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassFormatError(s: String!)
```

Constructs a`ClassFormatError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
