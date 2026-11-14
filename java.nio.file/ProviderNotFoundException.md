# ProviderNotFoundException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProviderNotFoundException

```
open class ProviderNotFoundException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.file.ProviderNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderNotFoundException#) |

Runtime exception thrown when a provider of the required type cannot be found.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProviderNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderNotFoundException#ProviderNotFoundException())`()` Constructs an instance of this class. |
| [ProviderNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderNotFoundException#ProviderNotFoundException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

## Public constructors

### ProviderNotFoundException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProviderNotFoundException()
```

Constructs an instance of this class. 

### ProviderNotFoundException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProviderNotFoundException(msg: String!)
```

Constructs an instance of this class.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
