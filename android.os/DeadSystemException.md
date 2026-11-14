# DeadSystemException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeadSystemException

Kotlin| [Java](../android/os/DeadSystemException.md) 
| --- | --- |

```
open class DeadSystemException : DeadObjectException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [android.util.AndroidException](../android/util/AndroidException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.RemoteException](../android/os/RemoteException.md) |||
| | | | | ↳ | [android.os.DeadObjectException](../android/os/DeadObjectException.md) ||
| | | | | | ↳ | [android.os.DeadSystemException](../android/os/DeadSystemException.md) |
| --- | --- | --- | --- | --- | --- | --- |

The core Android system has died and is going through a runtime restart. All running apps will be promptly killed.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------|---|
| [DeadSystemException](../android/os/DeadSystemException.md))`()` <br /> |

## Public constructors

### DeadSystemException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeadSystemException()
```
