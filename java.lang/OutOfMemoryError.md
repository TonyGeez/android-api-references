# OutOfMemoryError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutOfMemoryError

```
open class OutOfMemoryError : VirtualMachineError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) |||
| | | ↳ | [java.lang.VirtualMachineError](../java/lang/VirtualMachineError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.OutOfMemoryError](../java/lang/OutOfMemoryError.md) |

Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector.`OutOfMemoryError`objects may be constructed by the virtual machine as if [writable](../java/lang/Throwable.md)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OutOfMemoryError](../java/lang/OutOfMemoryError.md))`()` Constructs an`OutOfMemoryError`with no detail message. |
| [OutOfMemoryError](../java/lang/OutOfMemoryError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`OutOfMemoryError`with the specified detail message. |

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
