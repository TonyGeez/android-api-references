# DumpableContainer

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DumpableContainer

Kotlin| [Java](https://developer.android.com/reference/android/util/DumpableContainer "View this page in Java") 
| --- | --- |

```
interface DumpableContainer
```

| [android.util.DumpableContainer](https://developer.android.com/reference/kotlin/android/util/DumpableContainer#) |

Represents a container that manages [dumpables](https://developer.android.com/reference/kotlin/android/util/Dumpable).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addDumpable](https://developer.android.com/reference/kotlin/android/util/DumpableContainer#addDumpable(android.util.Dumpable))`(`dumpable:` ` [Dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable)`)` Adds the given [dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable) to the container. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeDumpable](https://developer.android.com/reference/kotlin/android/util/DumpableContainer#removeDumpable(android.util.Dumpable))`(`dumpable:` ` [Dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable)`)` Removes the given [dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable) from the container. |

## Public methods

### addDumpable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addDumpable(dumpable: Dumpable): Boolean
```

Adds the given [dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable) to the container.

If a dumpable with the same [name](https://developer.android.com/reference/kotlin/android/util/Dumpable#getDumpableName())was added before, this call is ignored.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `dumpable` | [Dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable):dumpable to be added. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the dumpable was added,`false`if the call was ignored. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the [dumpable name](https://developer.android.com/reference/kotlin/android/util/Dumpable#getDumpableName())is`null`. |

### removeDumpable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeDumpable(dumpable: Dumpable): Boolean
```

Removes the given [dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable) from the container.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `dumpable` | [Dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable):dumpable to be removed. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the dumpable was removed,`false`if it was not previously [added](https://developer.android.com/reference/kotlin/android/util/DumpableContainer#addDumpable(android.util.Dumpable))with the same identify (object reference) and [name](https://developer.android.com/reference/kotlin/android/util/Dumpable#getDumpableName()). |
