# MembershipKey

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MembershipKey

```
abstract class MembershipKey
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#) |

A token representing the membership of an Internet Protocol (IP) multicast group.

A membership key may represent a membership to receive all datagrams sent to the group, or it may be*source-specific* , meaning that it represents a membership that receives only datagrams from a specific source address. Whether or not a membership key is source-specific may be determined by invoking its [sourceAddress](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#sourceAddress())method.

A membership key is valid upon creation and remains valid until the membership is dropped by invoking the [drop](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#drop())method, or the channel is closed. The validity of the membership key may be tested by invoking its [isValid](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#isValid())method.

Where a membership key is not source-specific and the underlying operation system supports source filtering, then the [block](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#block(java.net.InetAddress))and [unblock](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#unblock(java.net.InetAddress))methods can be used to block or unblock multicast datagrams from particular source addresses.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#MembershipKey())`()` Initializes a new instance of this class. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#)! | [block](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#block(java.net.InetAddress))`(`source:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` Block multicast datagrams from the given source address. |
| abstract [MulticastChannel](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel)! | [channel](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#channel())`()` Returns the channel for which this membership key was created. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drop](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#drop())`()` Drop membership. |
| --- | --- |
| abstract [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [group](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#group())`()` Returns the multicast group for which this membership key was created. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#isValid())`()` Tells whether or not this membership is valid. |
| abstract [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#)! | [networkInterface](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#networkInterface())`()` Returns the network interface for which this membership key was created. |
| --- | --- |
| abstract [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [sourceAddress](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#sourceAddress())`()` Returns the source address if this membership key is source-specific, or`null`if this membership is not source-specific. |
| abstract [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#)! | [unblock](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#unblock(java.net.InetAddress))`(`source:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` Unblock multicast datagrams from the given source address that was previously blocked using the [block](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#block(java.net.InetAddress))method. |

## Protected constructors

### MembershipKey

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected MembershipKey()
```

Initializes a new instance of this class.

## Public methods

### block

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun block(source: InetAddress!): MembershipKey!
```

Block multicast datagrams from the given source address.

If this membership key is not source-specific, and the underlying operating system supports source filtering, then this method blocks multicast datagrams from the given source address. If the given source address is already blocked then this method has no effect. After a source address is blocked it may still be possible to receive datagrams from that source. This can arise when datagrams are waiting to be received in the socket's receive buffer.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `source` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:The source address to block |

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------|
| [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#)! | This membership key |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the`source`parameter is not a unicast address or is not the same address type as the multicast group |
| `java.lang.IllegalStateException` | If this membership key is source-specific or is no longer valid |
| `java.lang.UnsupportedOperationException` | If the underlying operating system does not support source filtering |
| --- | --- |
| `java.io.IOException` | If an I/O error occurs |

### channel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun channel(): MulticastChannel!
```

Returns the channel for which this membership key was created. This method will continue to return the channel even after the membership becomes [invalid](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#isValid()).

| Return ||
|--------------------------------------------------------------------------------------------------------|-------------|
| [MulticastChannel](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel)! | the channel |

### drop

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun drop(): Unit
```

Drop membership.

If the membership key represents a membership to receive all datagrams then the membership is dropped and the channel will no longer receive any datagrams sent to the group. If the membership key is source-specific then the channel will no longer receive datagrams sent to the group from that source address.

After membership is dropped it may still be possible to receive datagrams sent to the group. This can arise when datagrams are waiting to be received in the socket's receive buffer. After membership is dropped then the channel may java.nio.channels.MulticastChannel#join the group again in which case a new membership key is returned.

Upon return, this membership object will be [invalid](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#isValid()). If the multicast group membership is already invalid then invoking this method has no effect. Once a multicast group membership is invalid, it remains invalid forever. 

### group

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun group(): InetAddress!
```

Returns the multicast group for which this membership key was created. This method will continue to return the group even after the membership becomes [invalid](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#isValid()).

| Return ||
|-------------------------------------------------------------------------------------------|---------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | the multicast group |

### isValid

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isValid(): Boolean
```

Tells whether or not this membership is valid.

A multicast group membership is valid upon creation and remains valid until the membership is dropped by invoking the [drop](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#drop())method, or the channel is closed.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this membership key is valid,`false`otherwise |

### networkInterface

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun networkInterface(): NetworkInterface!
```

Returns the network interface for which this membership key was created. This method will continue to return the network interface even after the membership becomes [invalid](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#isValid()).

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------|
| [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#)! | the network interface |

### sourceAddress

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sourceAddress(): InetAddress!
```

Returns the source address if this membership key is source-specific, or`null`if this membership is not source-specific.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | The source address if this membership key is source-specific, otherwise`null` |

### unblock

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unblock(source: InetAddress!): MembershipKey!
```

Unblock multicast datagrams from the given source address that was previously blocked using the [block](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#block(java.net.InetAddress))method.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------|
| `source` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:The source address to unblock |

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------|
| [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#)! | This membership key |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the given source address is not currently blocked or the membership key is no longer valid |
