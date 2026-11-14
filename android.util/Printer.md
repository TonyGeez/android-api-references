# Printer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Printer

Kotlin| [Java](https://developer.android.com/reference/android/util/Printer "View this page in Java") 
| --- | --- |

```
interface Printer
```

| [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer#) |

| Known Direct Subclasses [LogPrinter](https://developer.android.com/reference/kotlin/android/util/LogPrinter), [PrintStreamPrinter](https://developer.android.com/reference/kotlin/android/util/PrintStreamPrinter), [PrintWriterPrinter](https://developer.android.com/reference/kotlin/android/util/PrintWriterPrinter), [StringBuilderPrinter](https://developer.android.com/reference/kotlin/android/util/StringBuilderPrinter) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [LogPrinter](https://developer.android.com/reference/kotlin/android/util/LogPrinter) | Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer#) that sends its output to the system log. | | [PrintStreamPrinter](https://developer.android.com/reference/kotlin/android/util/PrintStreamPrinter) | Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer#) that sends its output to a [java.io.PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#). | | [PrintWriterPrinter](https://developer.android.com/reference/kotlin/android/util/PrintWriterPrinter) | Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer#) that sends its output to a [java.io.PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#). | | [StringBuilderPrinter](https://developer.android.com/reference/kotlin/android/util/StringBuilderPrinter) | Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer#) that sends its output to a [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Simple interface for printing text, allowing redirection to various targets. Standard implementations are [android.util.LogPrinter](https://developer.android.com/reference/kotlin/android/util/LogPrinter), [android.util.StringBuilderPrinter](https://developer.android.com/reference/kotlin/android/util/StringBuilderPrinter), and [android.util.PrintWriterPrinter](https://developer.android.com/reference/kotlin/android/util/PrintWriterPrinter).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/android/util/Printer#println(kotlin.String))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Write a line of text to the output. |

## Public methods

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun println(x: String!): Unit
```

Write a line of text to the output. There is no need to terminate the given string with a newline.
