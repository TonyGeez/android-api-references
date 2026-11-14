# DatagramSocketImplFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatagramSocketImplFactory

```
interface DatagramSocketImplFactory
```

| [java.net.DatagramSocketImplFactory](../java/net/DatagramSocketImplFactory.md) |

This interface defines a factory for datagram socket implementations. It is used by the classes `DatagramSocket` to create actual socket implementations.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DatagramSocketImpl](../java/net/DatagramSocketImpl.md)! | [createDatagramSocketImpl](../java/net/DatagramSocketImplFactory.md))`()` Creates a new `DatagramSocketImpl` instance. |

## Public methods

### createDatagramSocketImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createDatagramSocketImpl(): DatagramSocketImpl!
```

Creates a new `DatagramSocketImpl` instance.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------|
| [DatagramSocketImpl](../java/net/DatagramSocketImpl.md)! | a new instance of `DatagramSocketImpl`. |

**See Also**

- [java.net.DatagramSocketImpl](../java/net/DatagramSocketImpl.md)
