# Allocation.OnBufferAvailableListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBufferAvailableListener

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/Allocation.OnBufferAvailableListener "View this page in Java") 

```
interface OnBufferAvailableListener
```

| [android.renderscript.Allocation.OnBufferAvailableListener](https://developer.android.com/reference/kotlin/android/renderscript/Allocation.OnBufferAvailableListener#) |

| **This interface was deprecated in API level 31.**
|
| Deprecated in Java.

Interface to handle notification when new buffers are available via [USAGE_IO_INPUT](https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_INPUT:kotlin.Int). An application will receive one notification when a buffer is available. Additional buffers will not trigger new notifications until a buffer is processed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBufferAvailable](https://developer.android.com/reference/kotlin/android/renderscript/Allocation.OnBufferAvailableListener#onBufferAvailable(android.renderscript.Allocation))`(`a:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` <br /> |

## Public methods

### onBufferAvailable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBufferAvailable(a: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*
