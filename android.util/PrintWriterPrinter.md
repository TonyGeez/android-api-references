# PrintWriterPrinter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintWriterPrinter

Kotlin| [Java](../android/util/PrintWriterPrinter.md) 
| --- | --- |

```
open class PrintWriterPrinter : Printer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.PrintWriterPrinter](../android/util/PrintWriterPrinter.md) |

Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to a [java.io.PrintWriter](../java/io/PrintWriter.md).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrintWriterPrinter](../android/util/PrintWriterPrinter.md))`(`pw:` ` [PrintWriter](../java/io/PrintWriter.md)!`)` Create a new Printer that sends to a PrintWriter object. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](../android/util/PrintWriterPrinter.md))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### PrintWriterPrinter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintWriterPrinter(pw: PrintWriter!)
```

Create a new Printer that sends to a PrintWriter object.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `pw` | [PrintWriter](../java/io/PrintWriter.md)!:The PrintWriter where you would like output to go. |

## Public methods

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: String!): Unit
```
