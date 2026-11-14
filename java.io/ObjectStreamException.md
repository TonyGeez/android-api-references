# ObjectStreamException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectStreamException

```
abstract class ObjectStreamException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.ObjectStreamException](../java/io/ObjectStreamException.md) |

| Known Direct Subclasses [InvalidClassException](../java/io/InvalidClassException.md), [InvalidObjectException](../java/io/InvalidObjectException.md), [NotActiveException](../java/io/NotActiveException.md), [NotSerializableException](../java/io/NotSerializableException.md), [OptionalDataException](../java/io/OptionalDataException.md), [StreamCorruptedException](../java/io/StreamCorruptedException.md), [WriteAbortedException](../java/io/WriteAbortedException.md) |-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InvalidClassException](../java/io/InvalidClassException.md) | Thrown when the Serialization runtime detects one of the following problems with a Class. | | [InvalidObjectException](../java/io/InvalidObjectException.md) | Indicates that one or more deserialized objects failed validation tests. | | [NotActiveException](../java/io/NotActiveException.md) | Thrown when serialization or deserialization is not active. | | [NotSerializableException](../java/io/NotSerializableException.md) | Thrown when an instance is required to have a Serializable interface. | | [OptionalDataException](../java/io/OptionalDataException.md) | Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream. | | [StreamCorruptedException](../java/io/StreamCorruptedException.md) | Thrown when control information that was read from an object stream violates internal consistency checks. | | [WriteAbortedException](../java/io/WriteAbortedException.md) | Signals that one of the ObjectStreamExceptions was thrown during a write operation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Superclass of all exceptions specific to Object Stream classes.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ObjectStreamException](../java/io/ObjectStreamException.md))`()` Create an ObjectStreamException. |
| [ObjectStreamException](../java/io/ObjectStreamException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create an ObjectStreamException with the specified argument. |

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
