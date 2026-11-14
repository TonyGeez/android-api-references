# SyncFailedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncFailedException

```
open class SyncFailedException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.SyncFailedException](SyncFailedException.md) |

Signals that a sync operation has failed.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SyncFailedException](SyncFailedException.md))`(`desc:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an SyncFailedException with a detail message. |

## Public constructors

### SyncFailedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SyncFailedException(desc: String!)
```

Constructs an SyncFailedException with a detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `desc` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String describing the exception. |
