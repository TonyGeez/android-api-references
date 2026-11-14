# AndroidRuntimeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidRuntimeException

Kotlin| [Java](https://developer.android.com/reference/android/util/AndroidRuntimeException "View this page in Java") 
| --- | --- |

```
open class AndroidRuntimeException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.util.AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException#) |

| Known Direct Subclasses [BadParcelableException](https://developer.android.com/reference/kotlin/android/os/BadParcelableException.html#), [Fragment.InstantiationException](https://developer.android.com/reference/kotlin/android/app/Fragment.InstantiationException.html#), [KeyCharacterMap.UnavailableException](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.UnavailableException.html#), [ReceiverCallNotAllowedException](https://developer.android.com/reference/kotlin/android/content/ReceiverCallNotAllowedException.html#) |------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BadParcelableException](https://developer.android.com/reference/kotlin/android/os/BadParcelableException.html#) | Exception thrown when a [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) is malformed or otherwise invalid. | | [Fragment.InstantiationException](https://developer.android.com/reference/kotlin/android/app/Fragment.InstantiationException.html#) | Thrown by [Fragment.instantiate(Context, String, Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment.html#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle))when there is an instantiation failure. | | [KeyCharacterMap.UnavailableException](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.UnavailableException.html#) | Thrown by [KeyCharacterMap.load](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.html#load(kotlin.Int))when a key character map could not be loaded. | | [ReceiverCallNotAllowedException](https://developer.android.com/reference/kotlin/android/content/ReceiverCallNotAllowedException.html#) | This exception is thrown from android. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for all unchecked exceptions thrown by the Android frameworks.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException#AndroidRuntimeException())`()` <br /> |
| [AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException#AndroidRuntimeException(java.lang.Exception))`(`cause:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` <br /> |
| [AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException#AndroidRuntimeException(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException#AndroidRuntimeException(kotlin.String,%20kotlin.Throwable))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

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
