# AndroidRuntimeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidRuntimeException

Kotlin| [Java](../android/util/AndroidRuntimeException.md) 
| --- | --- |

```
open class AndroidRuntimeException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.util.AndroidRuntimeException](../android/util/AndroidRuntimeException.md) |

| Known Direct Subclasses [BadParcelableException](../android/os/BadParcelableException.md), [Fragment.InstantiationException](../android/app/Fragment.InstantiationException.md), [KeyCharacterMap.UnavailableException](../android/view/KeyCharacterMap.UnavailableException.md), [ReceiverCallNotAllowedException](../android/content/ReceiverCallNotAllowedException.md) |------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BadParcelableException](../android/os/BadParcelableException.md) | Exception thrown when a [Parcelable](../android/os/Parcelable.md) is malformed or otherwise invalid. | | [Fragment.InstantiationException](../android/app/Fragment.InstantiationException.md) | Thrown by [Fragment.instantiate(Context, String, Bundle)](../android/app/Fragment.md))when there is an instantiation failure. | | [KeyCharacterMap.UnavailableException](../android/view/KeyCharacterMap.UnavailableException.md) | Thrown by [KeyCharacterMap.load](../android/view/KeyCharacterMap.md))when a key character map could not be loaded. | | [ReceiverCallNotAllowedException](../android/content/ReceiverCallNotAllowedException.md) | This exception is thrown from android. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for all unchecked exceptions thrown by the Android frameworks.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidRuntimeException](../android/util/AndroidRuntimeException.md))`()` <br /> |
| [AndroidRuntimeException](../android/util/AndroidRuntimeException.md))`(`cause:` ` [Exception](../java/lang/Exception.md)!`)` <br /> |
| [AndroidRuntimeException](../android/util/AndroidRuntimeException.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [AndroidRuntimeException](../android/util/AndroidRuntimeException.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

## Public constructors

### AndroidRuntimeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AndroidRuntimeException()
```  

### AndroidRuntimeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AndroidRuntimeException(cause: Exception!)
```  

### AndroidRuntimeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AndroidRuntimeException(name: String!)
```  

### AndroidRuntimeException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AndroidRuntimeException(
    name: String!, 
    cause: Throwable!)
```
