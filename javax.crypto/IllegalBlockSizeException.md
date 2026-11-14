# IllegalBlockSizeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalBlockSizeException

```
open class IllegalBlockSizeException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| | | | ↳ | [javax.crypto.IllegalBlockSizeException](https://developer.android.com/reference/kotlin/javax/crypto/IllegalBlockSizeException#) |

This exception is thrown when the length of data provided to a block cipher is incorrect, i.e., does not match the block size of the cipher.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalBlockSizeException](https://developer.android.com/reference/kotlin/javax/crypto/IllegalBlockSizeException#IllegalBlockSizeException())`()` Constructs an IllegalBlockSizeException with no detail message. |
| [IllegalBlockSizeException](https://developer.android.com/reference/kotlin/javax/crypto/IllegalBlockSizeException#IllegalBlockSizeException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an IllegalBlockSizeException with the specified detail message. |

## Public constructors

### IllegalBlockSizeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalBlockSizeException()
```

Constructs an IllegalBlockSizeException with no detail message. A detail message is a String that describes this particular exception. 

### IllegalBlockSizeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalBlockSizeException(msg: String!)
```

Constructs an IllegalBlockSizeException with the specified detail message.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
