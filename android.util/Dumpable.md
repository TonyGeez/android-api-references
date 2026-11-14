# Dumpable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Dumpable

Kotlin| [Java](../android/util/Dumpable.md) 
| --- | --- |

```
interface Dumpable
```

| [android.util.Dumpable](../android/util/Dumpable.md) |

Represents an object whose state can be dumped into a [PrintWriter](../java/io/PrintWriter.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](../android/util/Dumpable.md))`(`writer:` ` [PrintWriter](../java/io/PrintWriter.md)`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Dumps the internal state into the given`writer`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDumpableName](../android/util/Dumpable.md))`()` Gets the name of the [Dumpable](../android/util/Dumpable.md). |

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
| `writer` | [PrintWriter](../java/io/PrintWriter.md):writer to be written to This value cannot be`null`. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:optional list of arguments This value may be`null`. |

### getDumpableName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDumpableName(): String
```

Gets the name of the [Dumpable](../android/util/Dumpable.md).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | class name, by default. This value cannot be`null`. |
