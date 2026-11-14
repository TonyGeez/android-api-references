# IllegalBlockSizeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalBlockSizeException

```
open class IllegalBlockSizeException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.crypto.IllegalBlockSizeException](../javax/crypto/IllegalBlockSizeException.md) |

This exception is thrown when the length of data provided to a block cipher is incorrect, i.e., does not match the block size of the cipher.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalBlockSizeException](../javax/crypto/IllegalBlockSizeException.md))`()` Constructs an IllegalBlockSizeException with no detail message. |
| [IllegalBlockSizeException](../javax/crypto/IllegalBlockSizeException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an IllegalBlockSizeException with the specified detail message. |

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
