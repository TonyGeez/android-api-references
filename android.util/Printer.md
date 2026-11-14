# Printer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Printer

Kotlin| [Java](Printer.md) 
| --- | --- |

```
interface Printer
```

| [android.util.Printer](Printer.md) |

| Known Direct Subclasses [LogPrinter](LogPrinter.md), [PrintStreamPrinter](PrintStreamPrinter.md), [PrintWriterPrinter](PrintWriterPrinter.md), [StringBuilderPrinter](StringBuilderPrinter.md) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [LogPrinter](LogPrinter.md) | Implementation of a [android.util.Printer](Printer.md) that sends its output to the system log. | | [PrintStreamPrinter](PrintStreamPrinter.md) | Implementation of a [android.util.Printer](Printer.md) that sends its output to a [java.io.PrintStream](../java.io/PrintStream.md). | | [PrintWriterPrinter](PrintWriterPrinter.md) | Implementation of a [android.util.Printer](Printer.md) that sends its output to a [java.io.PrintWriter](../java.io/PrintWriter.md). | | [StringBuilderPrinter](StringBuilderPrinter.md) | Implementation of a [android.util.Printer](Printer.md) that sends its output to a [StringBuilder](../java.lang/StringBuilder.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Simple interface for printing text, allowing redirection to various targets. Standard implementations are [android.util.LogPrinter](LogPrinter.md), [android.util.StringBuilderPrinter](StringBuilderPrinter.md), and [android.util.PrintWriterPrinter](PrintWriterPrinter.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](Printer.md))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Write a line of text to the output. |

## Public methods

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun println(x: String!): Unit
```

Write a line of text to the output. There is no need to terminate the given string with a newline.
