# ActivityNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityNotFoundException

Kotlin| [Java](https://developer.android.com/reference/android/content/ActivityNotFoundException "View this page in Java") 
| --- | --- |

```
open class ActivityNotFoundException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.content.ActivityNotFoundException](https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException#) |

This exception is thrown when a call to android.content.Context#startActivity or one of its variants fails because an Activity can not be found to execute the given Intent.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ActivityNotFoundException](https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException#ActivityNotFoundException())`()` <br /> |
| [ActivityNotFoundException](https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException#ActivityNotFoundException(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### ActivityNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityNotFoundException()
```  

### ActivityNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityNotFoundException(name: String!)
```
