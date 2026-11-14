# LogPrinter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LogPrinter

Kotlin| [Java](https://developer.android.com/reference/android/util/LogPrinter "View this page in Java") 
| --- | --- |

```
open class LogPrinter : Printer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.LogPrinter](https://developer.android.com/reference/kotlin/android/util/LogPrinter#) |

Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer) that sends its output to the system log.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LogPrinter](https://developer.android.com/reference/kotlin/android/util/LogPrinter#LogPrinter(kotlin.Int,%20kotlin.String))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new Printer that sends to the log with the given priority and tag. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/android/util/LogPrinter#println(kotlin.String))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### LogPrinter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LogPrinter(
    priority: Int, 
    tag: String!)
```

Create a new Printer that sends to the log with the given priority and tag.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired log priority: [Log.VERBOSE](https://developer.android.com/reference/kotlin/android/util/Log#VERBOSE:kotlin.Int), [Log.DEBUG](https://developer.android.com/reference/kotlin/android/util/Log#DEBUG:kotlin.Int), [Log.INFO](https://developer.android.com/reference/kotlin/android/util/Log#INFO:kotlin.Int), [Log.WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int), or [Log.ERROR](https://developer.android.com/reference/kotlin/android/util/Log#ERROR:kotlin.Int). |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string tag to associate with each printed log statement. |

## Public methods

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: String!): Unit
```
