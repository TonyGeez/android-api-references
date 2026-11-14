# IkeInternalException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeInternalException

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/exceptions/IkeInternalException "View this page in Java") 

```
class IkeInternalException : IkeNonProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException) |||
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNonProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNonProtocolException) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException#) |

IkeInternalException encapsulates all local implementation or resource related exceptions.

Causes may include exceptions such as [android.net.IpSecManager.SpiUnavailableException](https://developer.android.com/reference/kotlin/android/net/IpSecManager.SpiUnavailableException.html#) when the requested SPI resources failed to be allocated.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException#IkeInternalException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Constructs a new exception with the specified cause. |
| [IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException#IkeInternalException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Constructs a new exception with the specified cause. |

## Public constructors

### IkeInternalException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeInternalException(
    message: String, 
    cause: Throwable)
```

Constructs a new exception with the specified cause.

Except for testing, IKE library users normally do not instantiate this object themselves but instead get a reference via [IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#) or [ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback.html#).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the descriptive message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method). This value cannot be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). This value cannot be`null`. |

### IkeInternalException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeInternalException(cause: Throwable)
```

Constructs a new exception with the specified cause.

Except for testing, IKE library users normally do not instantiate this object themselves but instead get a reference via [IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#) or [ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback.html#).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). This value cannot be`null`. |
