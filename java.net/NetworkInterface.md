# NetworkInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkInterface

```
class NetworkInterface
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.NetworkInterface](../java/net/NetworkInterface.md) |

This class represents a Network Interface made up of a name, and a list of IP addresses assigned to this interface. It is used to identify the local interface on which a multicast group is joined. Interfaces are normally known by names such as "le0".

Note that information about [NetworkInterface](../java/net/NetworkInterface.md) s may be restricted. For example, non-system apps will only have access to information about [NetworkInterface](../java/net/NetworkInterface.md) s that are associated with an [InetAddress](../java/net/InetAddress.md).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/net/NetworkInterface.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| static [NetworkInterface](../java/net/NetworkInterface.md)! | [getByIndex](../java/net/NetworkInterface.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a network interface given its index. |
| static [NetworkInterface](../java/net/NetworkInterface.md)! | [getByInetAddress](../java/net/NetworkInterface.md))`(`addr:` ` [InetAddress](../java/net/InetAddress.md)!`)` Convenience method to search for a network interface that has the specified Internet Protocol (IP) address bound to it. |
| --- | --- |
| static [NetworkInterface](../java/net/NetworkInterface.md)! | [getByName](../java/net/NetworkInterface.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Searches for the network interface with the specified name. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../java/net/NetworkInterface.md))`()` Get the display name of this network interface. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getHardwareAddress](../java/net/NetworkInterface.md))`()` Returns the hardware address (usually MAC) of the interface if it has one and if it can be accessed given the current privileges. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../java/net/NetworkInterface.md))`()` Returns the index of this network interface. |
| [Enumeration](../java/util/Enumeration.md)\< [InetAddress](../java/net/InetAddress.md)!\>! | [getInetAddresses](../java/net/NetworkInterface.md))`()` Convenience method to return an Enumeration with all or a subset of the InetAddresses bound to this network interface. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InterfaceAddress](../java/net/InterfaceAddress.md)!\>! | [getInterfaceAddresses](../java/net/NetworkInterface.md))`()` Get a List of all or a subset of the`InterfaceAddresses`of this network interface. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMTU](../java/net/NetworkInterface.md))`()` Returns the Maximum Transmission Unit (MTU) of this interface. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/net/NetworkInterface.md))`()` Get the name of this network interface. |
| static [Enumeration](../java/util/Enumeration.md)\< [NetworkInterface](../java/net/NetworkInterface.md)!\>! | [getNetworkInterfaces](../java/net/NetworkInterface.md))`()` Returns all the interfaces on this machine. |
| --- | --- |
| [NetworkInterface](../java/net/NetworkInterface.md)! | [getParent](../java/net/NetworkInterface.md))`()` Returns the parent NetworkInterface of this interface if this is a subinterface, or`null`if it is a physical (non virtual) interface or has no parent. |
| [Enumeration](../java/util/Enumeration.md)\< [NetworkInterface](../java/net/NetworkInterface.md)!\>! | [getSubInterfaces](../java/net/NetworkInterface.md))`()` Get an Enumeration with all the subinterfaces (also known as virtual interfaces) attached to this network interface. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/net/NetworkInterface.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoopback](../java/net/NetworkInterface.md))`()` Returns whether a network interface is a loopback interface. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPointToPoint](../java/net/NetworkInterface.md))`()` Returns whether a network interface is a point to point interface. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUp](../java/net/NetworkInterface.md))`()` Returns whether a network interface is up and running. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVirtual](../java/net/NetworkInterface.md))`()` Returns whether this interface is a virtual interface (also called subinterface). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMulticast](../java/net/NetworkInterface.md))`()` Returns whether a network interface supports multicasting or not. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/net/NetworkInterface.md))`()` <br /> |
| --- | --- |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is`true`if and only if the argument is not`null`and it represents the same NetworkInterface as this object.

Two instances of`NetworkInterface`represent the same NetworkInterface if both name and addrs are the same for both.

| Parameters ||
|-------|--------------------------------|
| `obj` | the object to compare against. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are the same;`false`otherwise. |

**See Also**

- [java.net.InetAddress#getAddress()](../java/net/InetAddress.md)) 

### getByIndex

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getByIndex(index: Int): NetworkInterface!
```

Get a network interface given its index.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer, the index of the interface |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NetworkInterface](../java/net/NetworkInterface.md)! | the NetworkInterface obtained from its index, or`null`if an interface with the specified index does not exist or [can't be accessed](../java/net/NetworkInterface.md). |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.net.SocketException` | if an I/O error occurs. |
| `java.lang.IllegalArgumentException` | if index has a negative value |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/NetworkInterface#getIndex()> 

### getByInetAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getByInetAddress(addr: InetAddress!): NetworkInterface!
```

Convenience method to search for a network interface that has the specified Internet Protocol (IP) address bound to it.

If the specified IP address is bound to multiple network interfaces it is not defined which network interface is returned.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `addr` | [InetAddress](../java/net/InetAddress.md)!:The`InetAddress`to search with. |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [NetworkInterface](../java/net/NetworkInterface.md)! | A`NetworkInterface`or`null`if there is no network interface with the specified IP address. |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.net.SocketException` | If an I/O error occurs. |
| `java.lang.NullPointerException` | If the specified address is`null`. |

### getByName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getByName(name: String!): NetworkInterface!
```

Searches for the network interface with the specified name.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the network interface. |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NetworkInterface](../java/net/NetworkInterface.md)! | A`NetworkInterface`with the specified name, or`null`if the network interface with the specified name does not exist or [can't be accessed](../java/net/NetworkInterface.md). |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.net.SocketException` | If an I/O error occurs. |
| `java.lang.NullPointerException` | If the specified name is`null`. |

### getDisplayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(): String!
```

Get the display name of this network interface. A display name is a human readable String describing the network device.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a non-empty string representing the display name of this network interface, or null if no display name is available. |

### getHardwareAddress

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHardwareAddress(): ByteArray!
```

Returns the hardware address (usually MAC) of the interface if it has one and if it can be accessed given the current privileges. If a security manager is set, then the caller must have the permission [NetPermission](../java/net/NetPermission.md)("getNetworkInformation").

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing the address, or`null`if the address doesn't exist, is not accessible or a security manager is set and the caller does not have the permission NetPermission("getNetworkInformation"). For example, this method will generally return`null`when called by non-system apps (or 02:00:00:00:00:00 for apps having`targetSdkVersion < android.os.Build.VERSION_CODES.R`). |

| Exceptions ||
|----------------------------|-------------------------|
| `java.net.SocketException` | if an I/O error occurs. |

### getIndex

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIndex(): Int
```

Returns the index of this network interface. The index is an integer greater or equal to zero, or`-1`for unknown. This is a system specific value and interfaces with the same name can have different indexes on different machines.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of this network interface or`-1`if the index is unknown |

**See Also**

- [#getByIndex(int)](../java/net/NetworkInterface.md)) 

### getInetAddresses

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInetAddresses(): Enumeration<InetAddress!>!
```

Convenience method to return an Enumeration with all or a subset of the InetAddresses bound to this network interface.

If there is a security manager, its`checkConnect`method is called for each InetAddress. Only InetAddresses where the`checkConnect`doesn't throw a SecurityException will be returned in the Enumeration. However, if the caller has the [NetPermission](../java/net/NetPermission.md)("getNetworkInformation") permission, then all InetAddresses are returned.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [InetAddress](../java/net/InetAddress.md)!>! | an Enumeration object with all or a subset of the InetAddresses bound to this network interface |

### getInterfaceAddresses

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInterfaceAddresses(): MutableList<InterfaceAddress!>!
```

Get a List of all or a subset of the`InterfaceAddresses`of this network interface.

If there is a security manager, its`checkConnect`method is called with the InetAddress for each InterfaceAddress. Only InterfaceAddresses where the`checkConnect`doesn't throw a SecurityException will be returned in the List.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InterfaceAddress](../java/net/InterfaceAddress.md)!>! | a`List`object with all or a subset of the InterfaceAddresss of this network interface |

### getMTU

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMTU(): Int
```

Returns the Maximum Transmission Unit (MTU) of this interface.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of the MTU for that interface. |

| Exceptions ||
|----------------------------|-------------------------|
| `java.net.SocketException` | if an I/O error occurs. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

Get the name of this network interface.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of this network interface |

### getNetworkInterfaces

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNetworkInterfaces(): Enumeration<NetworkInterface!>!
```

Returns all the interfaces on this machine. The`Enumeration`contains at least one element, possibly representing a loopback interface that only supports communication between entities on this machine. NOTE: can use getNetworkInterfaces()+getInetAddresses() to obtain all IP addresses for this node

For non-system apps, this method will only return information for [NetworkInterface](../java/net/NetworkInterface.md) s associated with an [InetAddress](../java/net/InetAddress.md).

ANDROID NOTE: On Android versions before S (API level 31), this method may throw a NullPointerException if called in an environment where there is a virtual interface without a parent interface present.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [NetworkInterface](../java/net/NetworkInterface.md)!>! | an Enumeration of NetworkInterfaces found on this machine that [are accessible](../java/net/NetworkInterface.md). |

| Exceptions ||
|----------------------------|-------------------------|
| `java.net.SocketException` | if an I/O error occurs. |

### getParent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParent(): NetworkInterface!
```

Returns the parent NetworkInterface of this interface if this is a subinterface, or`null`if it is a physical (non virtual) interface or has no parent.

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [NetworkInterface](../java/net/NetworkInterface.md)! | The`NetworkInterface`this interface is attached to. |

### getSubInterfaces

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubInterfaces(): Enumeration<NetworkInterface!>!
```

Get an Enumeration with all the subinterfaces (also known as virtual interfaces) attached to this network interface.

For instance eth0:1 will be a subinterface to eth0.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [NetworkInterface](../java/net/NetworkInterface.md)!>! | an Enumeration object with all of the subinterfaces of this network interface |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isLoopback

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLoopback(): Boolean
```

Returns whether a network interface is a loopback interface.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the interface is a loopback interface. |

| Exceptions ||
|----------------------------|-------------------------|
| `java.net.SocketException` | if an I/O error occurs. |

### isPointToPoint

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPointToPoint(): Boolean
```

Returns whether a network interface is a point to point interface. A typical point to point interface would be a PPP connection through a modem.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the interface is a point to point interface. |

| Exceptions ||
|----------------------------|-------------------------|
| `java.net.SocketException` | if an I/O error occurs. |

### isUp

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUp(): Boolean
```

Returns whether a network interface is up and running.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the interface is up and running. |

| Exceptions ||
|----------------------------|-------------------------|
| `java.net.SocketException` | if an I/O error occurs. |

### isVirtual

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVirtual(): Boolean
```

Returns whether this interface is a virtual interface (also called subinterface). Virtual interfaces are, on some systems, interfaces created as a child of a physical interface and given different settings (like address or MTU). Usually the name of the interface will the name of the parent followed by a colon (:) and a number identifying the child since there can be several virtual interfaces attached to a single physical interface.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this interface is a virtual interface. |

### supportsMulticast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun supportsMulticast(): Boolean
```

Returns whether a network interface supports multicasting or not.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the interface supports Multicasting. |

| Exceptions ||
|----------------------------|-------------------------|
| `java.net.SocketException` | if an I/O error occurs. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
