# StackOverflowError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StackOverflowError

```
open class StackOverflowError : VirtualMachineError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) |||
| | | ↳ | [java.lang.VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.StackOverflowError](https://developer.android.com/reference/kotlin/java/lang/StackOverflowError#) |

Thrown when a stack overflow occurs because an application recurses too deeply.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StackOverflowError](https://developer.android.com/reference/kotlin/java/lang/StackOverflowError#StackOverflowError())`()` Constructs a`StackOverflowError`with no detail message. |
| [StackOverflowError](https://developer.android.com/reference/kotlin/java/lang/StackOverflowError#StackOverflowError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`StackOverflowError`with the specified detail message. |

## Public constructors

### StackOverflowError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StackOverflowError()
```

Constructs a`StackOverflowError`with no detail message. 

### StackOverflowError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StackOverflowError(s: String!)
```

Constructs a`StackOverflowError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
