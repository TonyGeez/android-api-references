# ArrayStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrayStoreException

```
open class ArrayStoreException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| | | | ↳ | [java.lang.ArrayStoreException](https://developer.android.com/reference/kotlin/java/lang/ArrayStoreException#) |

Thrown to indicate that an attempt has been made to store the wrong type of object into an array of objects. For example, the following code generates an`ArrayStoreException`: 

```kotlin
Object x[] = new String[3];
      x[0] = new Integer(0);
  
```

<br />

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArrayStoreException](https://developer.android.com/reference/kotlin/java/lang/ArrayStoreException#ArrayStoreException())`()` Constructs an`ArrayStoreException`with no detail message. |
| [ArrayStoreException](https://developer.android.com/reference/kotlin/java/lang/ArrayStoreException#ArrayStoreException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`ArrayStoreException`with the specified detail message. |

## Public constructors

### ArrayStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayStoreException()
```

Constructs an`ArrayStoreException`with no detail message. 

### ArrayStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayStoreException(s: String!)
```

Constructs an`ArrayStoreException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
