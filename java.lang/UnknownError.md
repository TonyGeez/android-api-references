# UnknownError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnknownError

```
open class UnknownError : VirtualMachineError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](Error.md) |||
| | | ↳ | [java.lang.VirtualMachineError](VirtualMachineError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.UnknownError](UnknownError.md) |

Thrown when an unknown but serious exception has occurred in the Java Virtual Machine.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnknownError](UnknownError.md))`()` Constructs an`UnknownError`with no detail message. |
| [UnknownError](UnknownError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`UnknownError`with the specified detail message. |

## Public constructors

### UnknownError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnknownError()
```

Constructs an`UnknownError`with no detail message. 

### UnknownError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnknownError(s: String!)
```

Constructs an`UnknownError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
