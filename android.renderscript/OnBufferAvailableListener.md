# Allocation.OnBufferAvailableListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBufferAvailableListener

Kotlin| [Java](../android/renderscript/Allocation.OnBufferAvailableListener.md) 
| --- | --- |

```
interface OnBufferAvailableListener
```

| [android.renderscript.Allocation.OnBufferAvailableListener](../android/renderscript/Allocation.OnBufferAvailableListener.md) |

| **This interface was deprecated in API level 31.**
|
| Deprecated in Java.

Interface to handle notification when new buffers are available via [USAGE_IO_INPUT](../android/renderscript/Allocation.md). An application will receive one notification when a buffer is available. Additional buffers will not trigger new notifications until a buffer is processed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBufferAvailable](../android/renderscript/Allocation.OnBufferAvailableListener.md))`(`a:` ` [Allocation](../android/renderscript/Allocation.md)!`)` <br /> |

## Public methods

### onBufferAvailable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBufferAvailable(a: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*
