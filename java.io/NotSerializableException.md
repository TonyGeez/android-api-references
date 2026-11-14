# NotSerializableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NotSerializableException

```
open class NotSerializableException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException) ||
| | | | | ↳ | [java.io.NotSerializableException](https://developer.android.com/reference/kotlin/java/io/NotSerializableException#) |

Thrown when an instance is required to have a Serializable interface. The serialization runtime or the class of the instance can throw this exception. The argument should be the name of the class.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NotSerializableException](https://developer.android.com/reference/kotlin/java/io/NotSerializableException#NotSerializableException())`()` Constructs a NotSerializableException object. |
| [NotSerializableException](https://developer.android.com/reference/kotlin/java/io/NotSerializableException#NotSerializableException(kotlin.String))`(`classname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a NotSerializableException object with message string. |

## Public constructors

### NotSerializableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NotSerializableException()
```

Constructs a NotSerializableException object. 

### NotSerializableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NotSerializableException(classname: String!)
```

Constructs a NotSerializableException object with message string.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `classname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Class of the instance being serialized/deserialized. |
