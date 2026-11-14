# SocketImplFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketImplFactory

```
interface SocketImplFactory
```

| [java.net.SocketImplFactory](https://developer.android.com/reference/kotlin/java/net/SocketImplFactory#) |

This interface defines a factory for socket implementations. It is used by the classes`Socket`and`ServerSocket`to create actual socket implementations.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SocketImpl](https://developer.android.com/reference/kotlin/java/net/SocketImpl)! | [createSocketImpl](https://developer.android.com/reference/kotlin/java/net/SocketImplFactory#createSocketImpl())`()` Creates a new`SocketImpl`instance. |

## Public methods

### createSocketImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSocketImpl(): SocketImpl!
```

Creates a new`SocketImpl`instance.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [SocketImpl](https://developer.android.com/reference/kotlin/java/net/SocketImpl)! | a new instance of`SocketImpl`. |

**See Also**

- [java.net.SocketImpl](https://developer.android.com/reference/kotlin/java/net/SocketImpl)
