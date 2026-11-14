# Printer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Printer

Kotlin| [Java](../android/util/Printer.md) 
| --- | --- |

```
interface Printer
```

| [android.util.Printer](../android/util/Printer.md) |

| Known Direct Subclasses [LogPrinter](../android/util/LogPrinter.md), [PrintStreamPrinter](../android/util/PrintStreamPrinter.md), [PrintWriterPrinter](../android/util/PrintWriterPrinter.md), [StringBuilderPrinter](../android/util/StringBuilderPrinter.md) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [LogPrinter](../android/util/LogPrinter.md) | Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to the system log. | | [PrintStreamPrinter](../android/util/PrintStreamPrinter.md) | Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to a [java.io.PrintStream](../java/io/PrintStream.md). | | [PrintWriterPrinter](../android/util/PrintWriterPrinter.md) | Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to a [java.io.PrintWriter](../java/io/PrintWriter.md). | | [StringBuilderPrinter](../android/util/StringBuilderPrinter.md) | Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to a [StringBuilder](../java/lang/StringBuilder.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Simple interface for printing text, allowing redirection to various targets. Standard implementations are [android.util.LogPrinter](../android/util/LogPrinter.md), [android.util.StringBuilderPrinter](../android/util/StringBuilderPrinter.md), and [android.util.PrintWriterPrinter](../android/util/PrintWriterPrinter.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](../android/util/Printer.md))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Write a line of text to the output. |

## Public methods

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun println(x: String!): Unit
```

Write a line of text to the output. There is no need to terminate the given string with a newline.
