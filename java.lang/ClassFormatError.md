# ClassFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClassFormatError

```
open class ClassFormatError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) |||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) ||
| | | | ↳ | [java.lang.ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError#) |

| Known Direct Subclasses [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError), [UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. | | [UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. | |

Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError#ClassFormatError())`()` Constructs a`ClassFormatError`with no detail message. |
| [ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError#ClassFormatError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`ClassFormatError`with the specified detail message. |

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
