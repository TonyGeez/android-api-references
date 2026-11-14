# DestroyFailedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DestroyFailedException

```
open class DestroyFailedException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [javax.security.auth.DestroyFailedException](https://developer.android.com/reference/kotlin/javax/security/auth/DestroyFailedException#) |
| --- | --- | --- | --- |

Signals that a `destroy` operation failed.

This exception is thrown by credentials implementing the `Destroyable` interface when the `destroy` method fails.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DestroyFailedException](https://developer.android.com/reference/kotlin/javax/security/auth/DestroyFailedException#DestroyFailedException())`()` Constructs a DestroyFailedException with no detail message. |
| [DestroyFailedException](https://developer.android.com/reference/kotlin/javax/security/auth/DestroyFailedException#DestroyFailedException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a DestroyFailedException with the specified detail message. |

## Public constructors

### DestroyFailedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DestroyFailedException()
```

Constructs a DestroyFailedException with no detail message. A detail message is a String that describes this particular exception. 

### DestroyFailedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DestroyFailedException(msg: String!)
```

Constructs a DestroyFailedException with the specified detail message. A detail message is a String that describes this particular exception.

<br />

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
