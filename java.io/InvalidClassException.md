# InvalidClassException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidClassException

```
open class InvalidClassException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.ObjectStreamException](../java/io/ObjectStreamException.md) ||
| | | | | ↳ | [java.io.InvalidClassException](../java/io/InvalidClassException.md) |

Thrown when the Serialization runtime detects one of the following problems with a Class.

- The serial version of the class does not match that of the class descriptor read from the stream
- The class contains unknown datatypes
- The class does not have an accessible no-arg constructor
- The ObjectStreamClass of an enum constant does not represent an enum type
- Other conditions given in the Java Object Serialization Specification

<br />

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidClassException](../java/io/InvalidClassException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report an InvalidClassException for the reason specified. |
| [InvalidClassException](../java/io/InvalidClassException.md))`(`cname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an InvalidClassException object. |

| Properties ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [classname](../java/io/InvalidClassException.md) Name of the invalid class. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../java/io/InvalidClassException.md) Produce the message and include the classname, if present. |

## Public constructors

### InvalidClassException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidClassException(reason: String!)
```

Report an InvalidClassException for the reason specified.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String describing the reason for the exception. |

### InvalidClassException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidClassException(
    cname: String!, 
    reason: String!)
```

Constructs an InvalidClassException object.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `cname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String naming the invalid class. |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String describing the reason for the exception. |

## Properties

### classname

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var classname: String!
```

Name of the invalid class. 

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Produce the message and include the classname, if present.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
