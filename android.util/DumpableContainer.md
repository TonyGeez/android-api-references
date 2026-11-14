# DumpableContainer

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DumpableContainer

Kotlin| [Java](../android/util/DumpableContainer.md) 
| --- | --- |

```
interface DumpableContainer
```

| [android.util.DumpableContainer](../android/util/DumpableContainer.md) |

Represents a container that manages [dumpables](../android/util/Dumpable.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addDumpable](../android/util/DumpableContainer.md))`(`dumpable:` ` [Dumpable](../android/util/Dumpable.md)`)` Adds the given [dumpable](../android/util/Dumpable.md) to the container. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeDumpable](../android/util/DumpableContainer.md))`(`dumpable:` ` [Dumpable](../android/util/Dumpable.md)`)` Removes the given [dumpable](../android/util/Dumpable.md) from the container. |

## Public methods

### addDumpable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addDumpable(dumpable: Dumpable): Boolean
```

Adds the given [dumpable](../android/util/Dumpable.md) to the container.

If a dumpable with the same [name](../android/util/Dumpable.md))was added before, this call is ignored.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `dumpable` | [Dumpable](../android/util/Dumpable.md):dumpable to be added. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the dumpable was added,`false`if the call was ignored. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the [dumpable name](../android/util/Dumpable.md))is`null`. |

### removeDumpable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeDumpable(dumpable: Dumpable): Boolean
```

Removes the given [dumpable](../android/util/Dumpable.md) from the container.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `dumpable` | [Dumpable](../android/util/Dumpable.md):dumpable to be removed. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the dumpable was removed,`false`if it was not previously [added](../android/util/DumpableContainer.md))with the same identify (object reference) and [name](../android/util/Dumpable.md)). |
