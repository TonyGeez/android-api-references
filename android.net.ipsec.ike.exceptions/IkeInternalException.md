# IkeInternalException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeInternalException

Kotlin| [Java](IkeInternalException.md) 
| --- | --- |

```
class IkeInternalException : IkeNonProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](IkeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNonProtocolException](IkeNonProtocolException.md) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.IkeInternalException](IkeInternalException.md) |

IkeInternalException encapsulates all local implementation or resource related exceptions.

Causes may include exceptions such as [android.net.IpSecManager.SpiUnavailableException](../android/net/IpSecManager.SpiUnavailableException.md) when the requested SPI resources failed to be allocated.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IkeInternalException](IkeInternalException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Constructs a new exception with the specified cause. |
| [IkeInternalException](IkeInternalException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Constructs a new exception with the specified cause. |

## Public constructors

### IkeInternalException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeInternalException(
    message: String, 
    cause: Throwable)
```

Constructs a new exception with the specified cause.

Except for testing, IKE library users normally do not instantiate this object themselves but instead get a reference via [IkeSessionCallback](../android.net.ipsec.ike/IkeSessionCallback.md) or [ChildSessionCallback](../android.net.ipsec.ike/ChildSessionCallback.md).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the descriptive message (which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method). This value cannot be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). This value cannot be`null`. |

### IkeInternalException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeInternalException(cause: Throwable)
```

Constructs a new exception with the specified cause.

Except for testing, IKE library users normally do not instantiate this object themselves but instead get a reference via [IkeSessionCallback](../android.net.ipsec.ike/IkeSessionCallback.md) or [ChildSessionCallback](../android.net.ipsec.ike/ChildSessionCallback.md).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). This value cannot be`null`. |
