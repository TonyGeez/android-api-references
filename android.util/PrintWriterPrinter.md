# PrintWriterPrinter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintWriterPrinter

Kotlin| [Java](https://developer.android.com/reference/android/util/PrintWriterPrinter "View this page in Java") 
| --- | --- |

```
open class PrintWriterPrinter : Printer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.PrintWriterPrinter](https://developer.android.com/reference/kotlin/android/util/PrintWriterPrinter#) |

Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer) that sends its output to a [java.io.PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrintWriterPrinter](https://developer.android.com/reference/kotlin/android/util/PrintWriterPrinter#PrintWriterPrinter(java.io.PrintWriter))`(`pw:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`)` Create a new Printer that sends to a PrintWriter object. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/android/util/PrintWriterPrinter#println(kotlin.String))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### PrintWriterPrinter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintWriterPrinter(pw: PrintWriter!)
```

Create a new Printer that sends to a PrintWriter object.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `pw` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:The PrintWriter where you would like output to go. |

## Public methods

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: String!): Unit
```
