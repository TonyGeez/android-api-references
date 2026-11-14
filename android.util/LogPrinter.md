# LogPrinter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LogPrinter

Kotlin| [Java](LogPrinter.md) 
| --- | --- |

```
open class LogPrinter : Printer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.LogPrinter](LogPrinter.md) |

Implementation of a [android.util.Printer](Printer.md) that sends its output to the system log.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LogPrinter](LogPrinter.md))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new Printer that sends to the log with the given priority and tag. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](LogPrinter.md))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired log priority: [Log.VERBOSE](Log.md), [Log.DEBUG](Log.md), [Log.INFO](Log.md), [Log.WARN](Log.md), or [Log.ERROR](Log.md). |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string tag to associate with each printed log statement. |

## Public methods

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: String!): Unit
```
