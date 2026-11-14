# DatagramSocketImplFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatagramSocketImplFactory

```
interface DatagramSocketImplFactory
```

| [java.net.DatagramSocketImplFactory](DatagramSocketImplFactory.md) |

This interface defines a factory for datagram socket implementations. It is used by the classes `DatagramSocket` to create actual socket implementations.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DatagramSocketImpl](DatagramSocketImpl.md)! | [createDatagramSocketImpl](DatagramSocketImplFactory.md))`()` Creates a new `DatagramSocketImpl` instance. |

## Public methods

### createDatagramSocketImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createDatagramSocketImpl(): DatagramSocketImpl!
```

Creates a new `DatagramSocketImpl` instance.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------|
| [DatagramSocketImpl](DatagramSocketImpl.md)! | a new instance of `DatagramSocketImpl`. |

**See Also**

- [java.net.DatagramSocketImpl](DatagramSocketImpl.md)
