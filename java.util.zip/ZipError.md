# ZipError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipError

```
open class ZipError : InternalError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](../java.lang/Error.md) ||||
| | | ↳ | [java.lang.VirtualMachineError](../java.lang/VirtualMachineError.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.InternalError](../java.lang/InternalError.md) ||
| | | | | ↳ | [java.util.zip.ZipError](ZipError.md) |

Signals that an unrecoverable error has occurred.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZipError](ZipError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a ZipError with the given detail message. |

## Public constructors

### ZipError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipError(s: String!)
```

Constructs a ZipError with the given detail message.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`containing a detail message |
