# OutOfMemoryError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutOfMemoryError

```
open class OutOfMemoryError : VirtualMachineError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) |||
| | | ↳ | [java.lang.VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError) ||
| | | | ↳ | [java.lang.OutOfMemoryError](https://developer.android.com/reference/kotlin/java/lang/OutOfMemoryError#) |

Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector.`OutOfMemoryError`objects may be constructed by the virtual machine as if [writable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OutOfMemoryError](https://developer.android.com/reference/kotlin/java/lang/OutOfMemoryError#OutOfMemoryError())`()` Constructs an`OutOfMemoryError`with no detail message. |
| [OutOfMemoryError](https://developer.android.com/reference/kotlin/java/lang/OutOfMemoryError#OutOfMemoryError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`OutOfMemoryError`with the specified detail message. |

## Public constructors

### OutOfMemoryError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OutOfMemoryError()
```

Constructs an`OutOfMemoryError`with no detail message. 

### OutOfMemoryError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OutOfMemoryError(s: String!)
```

Constructs an`OutOfMemoryError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
