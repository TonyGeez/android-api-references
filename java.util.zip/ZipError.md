# ZipError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipError

```
open class ZipError : InternalError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||||
| | | ↳ | [java.lang.VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError.html#) ||
| | | | | ↳ | [java.util.zip.ZipError](https://developer.android.com/reference/kotlin/java/util/zip/ZipError#) |

Signals that an unrecoverable error has occurred.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZipError](https://developer.android.com/reference/kotlin/java/util/zip/ZipError#ZipError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a ZipError with the given detail message. |

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
