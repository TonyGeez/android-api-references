# ReadOnlyBufferException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadOnlyBufferException

```
open class ReadOnlyBufferException : UnsupportedOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) ||
| | | | | ↳ | [java.nio.ReadOnlyBufferException](https://developer.android.com/reference/kotlin/java/nio/ReadOnlyBufferException#) |

Unchecked exception thrown when a content-mutation method such as put or compact is invoked upon a read-only buffer.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReadOnlyBufferException](https://developer.android.com/reference/kotlin/java/nio/ReadOnlyBufferException#ReadOnlyBufferException())`()` Constructs an instance of this class. |

## Public constructors

### ReadOnlyBufferException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReadOnlyBufferException()
```

Constructs an instance of this class.
