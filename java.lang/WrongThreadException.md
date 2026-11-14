Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WrongThreadException

```
class WrongThreadException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.WrongThreadException](WrongThreadException.md) |

Thrown to indicate that a method has been called on the wrong thread.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/WrongThreadException#WrongThreadException()()` Constructs a WrongThreadException with no detail message. |
| `https://developer.android.com/reference/kotlin/java/lang/WrongThreadException#WrongThreadException(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs a WrongThreadException with the given detail message. |
| `https://developer.android.com/reference/kotlin/java/lang/WrongThreadException#WrongThreadException(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a WrongThreadException with the given detail message and cause. |
| `https://developer.android.com/reference/kotlin/java/lang/WrongThreadException#WrongThreadException(kotlin.Throwable)(cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a WrongThreadException with the given cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). |

## Public constructors

### WrongThreadException

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WrongThreadException()
```

Constructs a WrongThreadException with no detail message.

### WrongThreadException

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WrongThreadException(s: String!)
```

Constructs a WrongThreadException with the given detail message.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the String that contains a detailed message, can be null |

### WrongThreadException

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WrongThreadException(
    message: String!, 
    cause: Throwable!)
```

Constructs a WrongThreadException with the given detail message and cause.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message, can be null |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause, can be null |

### WrongThreadException

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WrongThreadException(cause: Throwable!)
```

Constructs a WrongThreadException with the given cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`).

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause, can be null |
