# SystemCleaner

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemCleaner

Kotlin| [Java](../android/system/SystemCleaner.md) 
| --- | --- |

```
class SystemCleaner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.system.SystemCleaner](../android/system/SystemCleaner.md) |

Java.lang.ref.Cleaner encourages each library to create a Cleaner, with an associated thread, to process Cleaner Runnables for that library's registered cleaning actions. This approach isolates cleaning actions from different libraries from each other; a slow cleaning action in one library will only minimally affect cleaning actions in another. However, this comes at the cost of introducing one Cleaner thread per library that uses Cleaners. This could introduce dozens of additional threads per process, which is often not an acceptable cost, especially on memory-limited devices. SystemCleaner instead provides access to a shared Cleaner, shared across the entire process. It is greatly preferred when all cleaning actions registered by a client are known to complete quickly, without explicit I/O, interprocess communication, or network access. Registering a non-terminating or excessively slow cleaning action with the shared cleaner may cause the process to perform very badly, hang, or be killed.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Cleaner](../java/lang/ref/Cleaner.md) | [cleaner](../android/system/SystemCleaner.md))`()` Return a single Cleaner that's shared across the entire process. |

## Public methods

### cleaner

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun cleaner(): Cleaner
```

Return a single Cleaner that's shared across the entire process. Thread-safe. Unlike normal Cleaners, uncaught exceptions during cleaning will throw an uncaught exception from the daemon running the cleaning action. This will normally cause the process to crash, and thus cause the problem to be reported.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [Cleaner](../java/lang/ref/Cleaner.md) | This value cannot be`null`. |
