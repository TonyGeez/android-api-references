# DeadSystemException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeadSystemException

Kotlin| [Java](https://developer.android.com/reference/android/os/DeadSystemException "View this page in Java") 
| --- | --- |

```
open class DeadSystemException : DeadObjectException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [android.util.AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.RemoteException](https://developer.android.com/reference/kotlin/android/os/RemoteException) |||
| | | | | ↳ | [android.os.DeadObjectException](https://developer.android.com/reference/kotlin/android/os/DeadObjectException) ||
| | | | | | ↳ | [android.os.DeadSystemException](https://developer.android.com/reference/kotlin/android/os/DeadSystemException#) |
| --- | --- | --- | --- | --- | --- | --- |

The core Android system has died and is going through a runtime restart. All running apps will be promptly killed.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------|---|
| [DeadSystemException](https://developer.android.com/reference/kotlin/android/os/DeadSystemException#DeadSystemException())`()` <br /> |

## Public constructors

### DeadSystemException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeadSystemException()
```
