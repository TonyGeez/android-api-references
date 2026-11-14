# PrintStreamPrinter

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintStreamPrinter

Kotlin| [Java](PrintStreamPrinter.md) 
| --- | --- |

```
open class PrintStreamPrinter : Printer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.PrintStreamPrinter](PrintStreamPrinter.md) |

Implementation of a [android.util.Printer](Printer.md) that sends its output to a [java.io.PrintStream](../java.io/PrintStream.md).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrintStreamPrinter](PrintStreamPrinter.md))`(`pw:` ` [PrintStream](../java.io/PrintStream.md)!`)` Create a new Printer that sends to a PrintWriter object. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](PrintStreamPrinter.md))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### PrintStreamPrinter

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStreamPrinter(pw: PrintStream!)
```

Create a new Printer that sends to a PrintWriter object.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `pw` | [PrintStream](../java.io/PrintStream.md)!:The PrintWriter where you would like output to go. |

## Public methods

### println

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: String!): Unit
```
