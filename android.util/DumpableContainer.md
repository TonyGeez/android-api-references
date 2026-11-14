# DumpableContainer

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DumpableContainer

Kotlin| [Java](DumpableContainer.md) 
| --- | --- |

```
interface DumpableContainer
```

| [android.util.DumpableContainer](DumpableContainer.md) |

Represents a container that manages [dumpables](Dumpable.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addDumpable](DumpableContainer.md))`(`dumpable:` ` [Dumpable](Dumpable.md)`)` Adds the given [dumpable](Dumpable.md) to the container. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeDumpable](DumpableContainer.md))`(`dumpable:` ` [Dumpable](Dumpable.md)`)` Removes the given [dumpable](Dumpable.md) from the container. |

## Public methods

### addDumpable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addDumpable(dumpable: Dumpable): Boolean
```

Adds the given [dumpable](Dumpable.md) to the container.

If a dumpable with the same [name](Dumpable.md))was added before, this call is ignored.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `dumpable` | [Dumpable](Dumpable.md):dumpable to be added. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the dumpable was added,`false`if the call was ignored. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the [dumpable name](Dumpable.md))is`null`. |

### removeDumpable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeDumpable(dumpable: Dumpable): Boolean
```

Removes the given [dumpable](Dumpable.md) from the container.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `dumpable` | [Dumpable](Dumpable.md):dumpable to be removed. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the dumpable was removed,`false`if it was not previously [added](DumpableContainer.md))with the same identify (object reference) and [name](Dumpable.md)). |
