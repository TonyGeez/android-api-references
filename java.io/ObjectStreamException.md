# ObjectStreamException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectStreamException

```
abstract class ObjectStreamException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException#) |

| Known Direct Subclasses [InvalidClassException](https://developer.android.com/reference/kotlin/java/io/InvalidClassException), [InvalidObjectException](https://developer.android.com/reference/kotlin/java/io/InvalidObjectException), [NotActiveException](https://developer.android.com/reference/kotlin/java/io/NotActiveException), [NotSerializableException](https://developer.android.com/reference/kotlin/java/io/NotSerializableException), [OptionalDataException](https://developer.android.com/reference/kotlin/java/io/OptionalDataException), [StreamCorruptedException](https://developer.android.com/reference/kotlin/java/io/StreamCorruptedException), [WriteAbortedException](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException) |-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InvalidClassException](https://developer.android.com/reference/kotlin/java/io/InvalidClassException) | Thrown when the Serialization runtime detects one of the following problems with a Class. | | [InvalidObjectException](https://developer.android.com/reference/kotlin/java/io/InvalidObjectException) | Indicates that one or more deserialized objects failed validation tests. | | [NotActiveException](https://developer.android.com/reference/kotlin/java/io/NotActiveException) | Thrown when serialization or deserialization is not active. | | [NotSerializableException](https://developer.android.com/reference/kotlin/java/io/NotSerializableException) | Thrown when an instance is required to have a Serializable interface. | | [OptionalDataException](https://developer.android.com/reference/kotlin/java/io/OptionalDataException) | Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream. | | [StreamCorruptedException](https://developer.android.com/reference/kotlin/java/io/StreamCorruptedException) | Thrown when control information that was read from an object stream violates internal consistency checks. | | [WriteAbortedException](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException) | Signals that one of the ObjectStreamExceptions was thrown during a write operation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Superclass of all exceptions specific to Object Stream classes.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException#ObjectStreamException())`()` Create an ObjectStreamException. |
| [ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException#ObjectStreamException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create an ObjectStreamException with the specified argument. |

## Protected constructors

### ObjectStreamException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ObjectStreamException()
```

Create an ObjectStreamException. 

### ObjectStreamException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ObjectStreamException(message: String!)
```

Create an ObjectStreamException with the specified argument.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detailed message for the exception |
