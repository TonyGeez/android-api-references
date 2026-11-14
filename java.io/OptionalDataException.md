# OptionalDataException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OptionalDataException

```
open class OptionalDataException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) |||
| | | | ↳ | [java.io.ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException) ||
| | | | | ↳ | [java.io.OptionalDataException](https://developer.android.com/reference/kotlin/java/io/OptionalDataException#) |

Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream. This exception may be thrown in two cases:

- An attempt was made to read an object when the next element in the stream is primitive data. In this case, the OptionalDataException's length field is set to the number of bytes of primitive data immediately readable from the stream, and the eof field is set to false.
- An attempt was made to read past the end of data consumable by a class-defined readObject or readExternal method. In this case, the OptionalDataException's eof field is set to true, and the length field is set to 0.

<br />

## Summary

| Properties ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [eof](https://developer.android.com/reference/kotlin/java/io/OptionalDataException#eof:kotlin.Boolean) True if there is no more data in the buffered part of the stream. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/java/io/OptionalDataException#length:kotlin.Int) The number of bytes of primitive data available to be read in the current buffer. |

## Properties

### eof

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var eof: Boolean
```

True if there is no more data in the buffered part of the stream. 

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var length: Int
```

The number of bytes of primitive data available to be read in the current buffer.
