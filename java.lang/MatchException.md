# MatchException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MatchException

```
class MatchException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.MatchException](https://developer.android.com/reference/kotlin/java/lang/MatchException#) |

Thrown to indicate an unexpected failure in pattern matching.

`MatchException`may be thrown when an exhaustive pattern matching language construct (such as a`switch`expression) encounters a value that does not match any of the specified patterns at run time, even though the construct has been deemed exhaustive. This is intentional and can arise from a number of cases:

- Separate compilation anomalies, where parts of the type hierarchy that the patterns reference have been changed, but the pattern matching construct has not been recompiled. For example, if a sealed interface has a different set of permitted subtypes at run time than it had at compile time, or if an enum class has a different set of enum constants at runtime than it had at compile time, or if the type hierarchy has been changed in some incompatible way between compile time and run time.
- `null`values and nested patterns involving sealed classes. If, for example, an interface`I`is`sealed`with two permitted subclasses`A`and`B`, and a record class`R`has a single component of type`I`, then the two record patterns`R(A a)`and`R(B b)`together are considered to be exhaustive for the type`R`, but neither of these patterns will match against the result of`new R(null)`.
- `null`values and nested record patterns. Given a record class`S`with a single component of type`T`, where`T`is another record class with a single component of type`String`, then the nested record pattern`R(S(var s))`is considered exhaustive for the type`R`but it does not match against the result of`new R(null)`(whereas it does match against the result of`new R(new S(null))`does).

`MatchException`may also be thrown by the process of pattern matching a value against a pattern. For example, pattern matching involving a record pattern may require accessor methods to be implicitly invoked in order to extract the component values. If any of these accessor methods throws an exception, pattern matching completes abruptly and throws`MatchException`. The original exception will be set as a [cause](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())of the`MatchException`. No [suppressed](https://developer.android.com/reference/kotlin/java/lang/Throwable#addSuppressed(kotlin.Throwable))exceptions will be recorded.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MatchException](https://developer.android.com/reference/kotlin/java/lang/MatchException#MatchException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`MatchException`with the specified detail message and cause. |

## Public constructors

### MatchException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MatchException(
    message: String!, 
    cause: Throwable!)
```

Constructs an`MatchException`with the specified detail message and cause.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
