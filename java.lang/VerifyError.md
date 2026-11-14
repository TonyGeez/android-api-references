# VerifyError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VerifyError

```
open class VerifyError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) |||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.VerifyError](../java/lang/VerifyError.md) |

Thrown when the "verifier" detects that a class file, though well formed, contains some sort of internal inconsistency or security problem.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VerifyError](../java/lang/VerifyError.md))`()` Constructs an`VerifyError`with no detail message. |
| [VerifyError](../java/lang/VerifyError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`VerifyError`with the specified detail message. |

## Public constructors

### VerifyError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VerifyError()
```

Constructs an`VerifyError`with no detail message. 

### VerifyError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VerifyError(s: String!)
```

Constructs an`VerifyError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
