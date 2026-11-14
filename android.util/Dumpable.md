# Dumpable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Dumpable

Kotlin| [Java](https://developer.android.com/reference/android/util/Dumpable "View this page in Java") 
| --- | --- |

```
interface Dumpable
```

| [android.util.Dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable#) |

Represents an object whose state can be dumped into a [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/util/Dumpable#dump(java.io.PrintWriter,%20kotlin.Array))`(`writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Dumps the internal state into the given`writer`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDumpableName](https://developer.android.com/reference/kotlin/android/util/Dumpable#getDumpableName())`()` Gets the name of the [Dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable#). |

## Public methods

### dump

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dump(
    writer: PrintWriter, 
    args: Array<String!>?
): Unit
```

Dumps the internal state into the given`writer`.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#):writer to be written to This value cannot be`null`. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:optional list of arguments This value may be`null`. |

### getDumpableName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDumpableName(): String
```

Gets the name of the [Dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable#).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | class name, by default. This value cannot be`null`. |
