# BadParcelableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BadParcelableException

Kotlin| [Java](../android/os/BadParcelableException.md) 
| --- | --- |

```
open class BadParcelableException : AndroidRuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.util.AndroidRuntimeException](../android/util/AndroidRuntimeException.md) ||
| | | | | ↳ | [android.os.BadParcelableException](../android/os/BadParcelableException.md) |

Exception thrown when a [Parcelable](../android/os/Parcelable.md) is malformed or otherwise invalid.

This is typically encountered when a custom [Parcelable](../android/os/Parcelable.md) object is passed to another process that doesn't have the same [Parcelable](../android/os/Parcelable.md) class in its [ClassLoader](../java/lang/ClassLoader.md).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BadParcelableException](../android/os/BadParcelableException.md))`(`cause:` ` [Exception](../java/lang/Exception.md)!`)` <br /> |
| [BadParcelableException](../android/os/BadParcelableException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### BadParcelableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BadParcelableException(cause: Exception!)
```  

### BadParcelableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BadParcelableException(msg: String!)
```
