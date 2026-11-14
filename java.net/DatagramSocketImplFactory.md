# DatagramSocketImplFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatagramSocketImplFactory

```
interface DatagramSocketImplFactory
```

| [java.net.DatagramSocketImplFactory](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImplFactory#) |

This interface defines a factory for datagram socket implementations. It is used by the classes `DatagramSocket` to create actual socket implementations.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DatagramSocketImpl](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl)! | [createDatagramSocketImpl](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImplFactory#createDatagramSocketImpl())`()` Creates a new `DatagramSocketImpl` instance. |

## Public methods

### createDatagramSocketImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createDatagramSocketImpl(): DatagramSocketImpl!
```

Creates a new `DatagramSocketImpl` instance.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------|
| [DatagramSocketImpl](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl)! | a new instance of `DatagramSocketImpl`. |

**See Also**

- [java.net.DatagramSocketImpl](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl)
