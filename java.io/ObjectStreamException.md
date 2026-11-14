# ObjectStreamException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectStreamException

```
abstract class ObjectStreamException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.ObjectStreamException](ObjectStreamException.md) |

| Known Direct Subclasses [InvalidClassException](InvalidClassException.md), [InvalidObjectException](InvalidObjectException.md), [NotActiveException](NotActiveException.md), [NotSerializableException](NotSerializableException.md), [OptionalDataException](OptionalDataException.md), [StreamCorruptedException](StreamCorruptedException.md), [WriteAbortedException](WriteAbortedException.md) |-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InvalidClassException](InvalidClassException.md) | Thrown when the Serialization runtime detects one of the following problems with a Class. | | [InvalidObjectException](InvalidObjectException.md) | Indicates that one or more deserialized objects failed validation tests. | | [NotActiveException](NotActiveException.md) | Thrown when serialization or deserialization is not active. | | [NotSerializableException](NotSerializableException.md) | Thrown when an instance is required to have a Serializable interface. | | [OptionalDataException](OptionalDataException.md) | Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream. | | [StreamCorruptedException](StreamCorruptedException.md) | Thrown when control information that was read from an object stream violates internal consistency checks. | | [WriteAbortedException](WriteAbortedException.md) | Signals that one of the ObjectStreamExceptions was thrown during a write operation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Superclass of all exceptions specific to Object Stream classes.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ObjectStreamException](ObjectStreamException.md))`()` Create an ObjectStreamException. |
| [ObjectStreamException](ObjectStreamException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create an ObjectStreamException with the specified argument. |

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
