# ReadOnlyBufferException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadOnlyBufferException

```
open class ReadOnlyBufferException : UnsupportedOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.UnsupportedOperationException](../java/lang/UnsupportedOperationException.md) ||
| | | | | ↳ | [java.nio.ReadOnlyBufferException](../java/nio/ReadOnlyBufferException.md) |

Unchecked exception thrown when a content-mutation method such as put or compact is invoked upon a read-only buffer.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReadOnlyBufferException](../java/nio/ReadOnlyBufferException.md))`()` Constructs an instance of this class. |

## Public constructors

### ReadOnlyBufferException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReadOnlyBufferException()
```

Constructs an instance of this class.
