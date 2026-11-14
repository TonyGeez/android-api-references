# OutOfMemoryError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutOfMemoryError

```
open class OutOfMemoryError : VirtualMachineError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](Error.md) |||
| | | ↳ | [java.lang.VirtualMachineError](VirtualMachineError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.OutOfMemoryError](OutOfMemoryError.md) |

Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector.`OutOfMemoryError`objects may be constructed by the virtual machine as if [writable](Throwable.md)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OutOfMemoryError](OutOfMemoryError.md))`()` Constructs an`OutOfMemoryError`with no detail message. |
| [OutOfMemoryError](OutOfMemoryError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`OutOfMemoryError`with the specified detail message. |

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
