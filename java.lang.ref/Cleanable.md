# Cleaner.Cleanable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Cleanable

```
interface Cleanable
```

| [java.lang.ref.Cleaner.Cleanable](../java/lang/ref/Cleaner.Cleanable.md) |

`Cleanable`represents an object and a cleaning action registered in a`Cleaner`.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clean](../java/lang/ref/Cleaner.Cleanable.md))`()` Unregisters the cleanable and invokes the cleaning action. |

## Public methods

### clean

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clean(): Unit
```

Unregisters the cleanable and invokes the cleaning action. The cleanable's cleaning action is invoked at most once regardless of the number of calls to`clean`.
