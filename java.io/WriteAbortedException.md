# WriteAbortedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WriteAbortedException

```
open class WriteAbortedException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.ObjectStreamException](ObjectStreamException.md) ||
| | | | | ↳ | [java.io.WriteAbortedException](WriteAbortedException.md) |

Signals that one of the ObjectStreamExceptions was thrown during a write operation. Thrown during a read operation when one of the ObjectStreamExceptions was thrown during a write operation. The exception that terminated the write can be found in the detail field. The stream is reset to it's initial state and all references to objects already deserialized are discarded.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WriteAbortedException](WriteAbortedException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Exception](../java.lang/Exception.md)!`)` Constructs a WriteAbortedException with a string describing the exception and the exception causing the abort. |

| Properties ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](WriteAbortedException.md) Returns the exception that terminated the operation (the*cause*). |
| [Exception](../java.lang/Exception.md)! | [detail](WriteAbortedException.md) Exception that was caught while writing the ObjectStream. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](WriteAbortedException.md) Produce the message and include the message from the nested exception, if there is one. |
| --- | --- |

## Public constructors

### WriteAbortedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WriteAbortedException(
    s: String!, 
    ex: Exception!)
```

Constructs a WriteAbortedException with a string describing the exception and the exception causing the abort.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String describing the exception. |
| `ex` | [Exception](../java.lang/Exception.md)!:Exception causing the abort. |

## Properties

### cause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val cause: Throwable?
```

Returns the exception that terminated the operation (the*cause*).

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | the exception that terminated the operation (the*cause*), which may be null. |

### detail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var detail: Exception!
```

**Deprecated:** *This field predates the general-purpose exception chaining facility. The [Throwable.getCause()](../java.lang/Throwable.md))method is now the preferred means of obtaining this information.*

Exception that was caught while writing the ObjectStream. 

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Produce the message and include the message from the nested exception, if there is one.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
