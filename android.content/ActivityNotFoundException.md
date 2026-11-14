# ActivityNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityNotFoundException

Kotlin| [Java](ActivityNotFoundException.md) 
| --- | --- |

```
open class ActivityNotFoundException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.content.ActivityNotFoundException](ActivityNotFoundException.md) |

This exception is thrown when a call to android.content.Context#startActivity or one of its variants fails because an Activity can not be found to execute the given Intent.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ActivityNotFoundException](ActivityNotFoundException.md))`()` <br /> |
| [ActivityNotFoundException](ActivityNotFoundException.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
