Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringBuilderPrinter

Kotlin | [Java](https://developer.android.com/reference/android/util/StringBuilderPrinter "View this page in Java")
| --- | --- |

```
open class StringBuilderPrinter : Printer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.StringBuilderPrinter](https://developer.android.com/reference/kotlin/android/util/StringBuilderPrinter#) |

Implementation of a `https://developer.android.com/reference/kotlin/android/util/Printer` that sends its output to a `https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/StringBuilderPrinter#StringBuilderPrinter(java.lang.StringBuilder)(builder: https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#!)` Create a new Printer that sends to a StringBuilder object. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/StringBuilderPrinter#println(kotlin.String)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Write a line of text to the output. |

## Public constructors

### StringBuilderPrinter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuilderPrinter(builder: StringBuilder!)
```

Create a new Printer that sends to a StringBuilder object.

| Parameters ||
|---|---|
| `builder` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!: The StringBuilder where you would like output to go. |

## Public methods

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: String!): Unit
```

Write a line of text to the output. There is no need to terminate the given string with a newline.
