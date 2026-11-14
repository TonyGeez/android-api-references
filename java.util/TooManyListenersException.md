# TooManyListenersException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TooManyListenersException

```
open class TooManyListenersException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.util.TooManyListenersException](https://developer.android.com/reference/kotlin/java/util/TooManyListenersException#) |

The`TooManyListenersException `Exception is used as part of the Java Event model to annotate and implement a unicast special case of a multicast Event Source.

The presence of a "throws TooManyListenersException" clause on any given concrete implementation of the normally multicast "void addXyzEventListener" event listener registration pattern is used to annotate that interface as implementing a unicast Listener special case, that is, that one and only one Listener may be registered on the particular event listener source concurrently.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TooManyListenersException](https://developer.android.com/reference/kotlin/java/util/TooManyListenersException#TooManyListenersException())`()` Constructs a TooManyListenersException with no detail message. |
| [TooManyListenersException](https://developer.android.com/reference/kotlin/java/util/TooManyListenersException#TooManyListenersException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a TooManyListenersException with the specified detail message. |

## Public constructors

### TooManyListenersException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TooManyListenersException()
```

Constructs a TooManyListenersException with no detail message. A detail message is a String that describes this particular exception. 

### TooManyListenersException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TooManyListenersException(s: String!)
```

Constructs a TooManyListenersException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
