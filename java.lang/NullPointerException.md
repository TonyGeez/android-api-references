# NullPointerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NullPointerException

```
open class NullPointerException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException#) |

Thrown when an application attempts to use`null`in a case where an object is required. These include:

- Calling the instance method of a`null`object.
- Accessing or modifying the field of a`null`object.
- Taking the length of`null`as if it were an array.
- Accessing or modifying the slots of`null`as if it were an array.
- Throwing`null`as if it were a`Throwable`value.

<br />

Applications should throw instances of this class to indicate other illegal uses of the`null`object.`NullPointerException`objects may be constructed by the virtual machine as if [stack trace was not writable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean)).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException#NullPointerException())`()` Constructs a`NullPointerException`with no detail message. |
| [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException#NullPointerException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`NullPointerException`with the specified detail message. |

## Public constructors

### NullPointerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NullPointerException()
```

Constructs a`NullPointerException`with no detail message. 

### NullPointerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NullPointerException(s: String!)
```

Constructs a`NullPointerException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
