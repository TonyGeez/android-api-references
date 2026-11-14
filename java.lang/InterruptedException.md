# InterruptedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InterruptedException

```
open class InterruptedException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](Exception.md) ||
| | | ↳ | [java.lang.InterruptedException](InterruptedException.md) |
| --- | --- | --- | --- |

Thrown when a thread is waiting, sleeping, or otherwise occupied, and the thread is interrupted, either before or during the activity. Occasionally a method may wish to test whether the current thread has been interrupted, and if so, to immediately throw this exception. The following code can be used to achieve this effect: 

```kotlin
if (Thread.interrupted())  // Clears interrupted status!
       throw new InterruptedException();
  
```

<br />

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InterruptedException](InterruptedException.md))`()` Constructs an `InterruptedException` with no detail message. |
| [InterruptedException](InterruptedException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an `InterruptedException` with the specified detail message. |

## Public constructors

### InterruptedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InterruptedException()
```

Constructs an `InterruptedException` with no detail message. 

### InterruptedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InterruptedException(s: String!)
```

Constructs an `InterruptedException` with the specified detail message.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
