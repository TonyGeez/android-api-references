# PrintStreamPrinter

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintStreamPrinter

Kotlin| [Java](https://developer.android.com/reference/android/util/PrintStreamPrinter "View this page in Java") 
| --- | --- |

```
open class PrintStreamPrinter : Printer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.PrintStreamPrinter](https://developer.android.com/reference/kotlin/android/util/PrintStreamPrinter#) |

Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer) that sends its output to a [java.io.PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrintStreamPrinter](https://developer.android.com/reference/kotlin/android/util/PrintStreamPrinter#PrintStreamPrinter(java.io.PrintStream))`(`pw:` ` [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)!`)` Create a new Printer that sends to a PrintWriter object. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/android/util/PrintStreamPrinter#println(kotlin.String))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### PrintStreamPrinter

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStreamPrinter(pw: PrintStream!)
```

Create a new Printer that sends to a PrintWriter object.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `pw` | [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)!:The PrintWriter where you would like output to go. |

## Public methods

### println

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: String!): Unit
```
