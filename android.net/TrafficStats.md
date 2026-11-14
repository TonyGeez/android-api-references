# TrafficStats

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrafficStats

Kotlin| [Java](https://developer.android.com/reference/android/net/TrafficStats "View this page in Java") 

```
open class TrafficStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.TrafficStats](https://developer.android.com/reference/kotlin/android/net/TrafficStats#) |

Class that provides network traffic statistics. These statistics include bytes transmitted and received and network packets transmitted and received, over all interfaces, over the mobile interface, and on a per-UID basis.

These statistics may not be available on all platforms. If the statistics are not supported by this device, [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) will be returned.

Note that the statistics returned by this class reset and start from zero after every reboot. To access more robust historical network statistics data, use [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#) instead.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) The return value to indicate that the device does not support the statistic. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [TrafficStats](https://developer.android.com/reference/kotlin/android/net/TrafficStats#TrafficStats())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearThreadStatsTag](https://developer.android.com/reference/kotlin/android/net/TrafficStats#clearThreadStatsTag())`()` Clear any active tag set to account [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearThreadStatsUid](https://developer.android.com/reference/kotlin/android/net/TrafficStats#clearThreadStatsUid())`()` Clear any active UID set to account [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndSetThreadStatsTag](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getAndSetThreadStatsTag(kotlin.Int))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set active tag to use when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMobileRxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getMobileRxBytes())`()` Return number of bytes received across mobile networks since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMobileRxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getMobileRxPackets())`()` Return number of packets received across mobile networks since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMobileTxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getMobileTxBytes())`()` Return number of bytes transmitted across mobile networks since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMobileTxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getMobileTxPackets())`()` Return number of packets transmitted across mobile networks since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getRxBytes(kotlin.String))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return the number of bytes received on the specified interface since the interface was created. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getRxPackets(kotlin.String))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return the number of packets received on the specified interface since the interface was created. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadStatsTag](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getThreadStatsTag())`()` Get the active tag used when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadStatsUid](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getThreadStatsUid())`()` Get the active UID used when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalRxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getTotalRxBytes())`()` Return number of bytes received since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalRxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getTotalRxPackets())`()` Return number of packets received since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalTxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getTotalTxBytes())`()` Return number of bytes transmitted since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalTxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getTotalTxPackets())`()` Return number of packets transmitted since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getTxBytes(kotlin.String))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return the number of bytes transmitted on the specified interface since the interface was created. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getTxPackets(kotlin.String))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return the number of packets transmitted on the specified interface since the interface was created. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidRxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidRxBytes(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return number of bytes received by the given UID since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidRxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidRxPackets(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return number of packets received by the given UID since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTcpRxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTcpRxBytes(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTcpRxSegments](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTcpRxSegments(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTcpTxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTcpTxBytes(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTcpTxSegments](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTcpTxSegments(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTxBytes(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return number of bytes transmitted by the given UID since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTxPackets(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return number of packets transmitted by the given UID since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidUdpRxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidUdpRxBytes(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidUdpRxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidUdpRxPackets(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidUdpTxBytes](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidUdpTxBytes(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidUdpTxPackets](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidUdpTxPackets(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [incrementOperationCount](https://developer.android.com/reference/kotlin/android/net/TrafficStats#incrementOperationCount(kotlin.Int))`(`operationCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increment count of network operations performed under the accounting tag currently active on the calling thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [incrementOperationCount](https://developer.android.com/reference/kotlin/android/net/TrafficStats#incrementOperationCount(kotlin.Int,%20kotlin.Int))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `operationCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increment count of network operations performed under the given accounting tag. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThreadStatsTag](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsTag(kotlin.Int))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set active tag to use when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThreadStatsUid](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsUid(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set specific UID to use when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tagDatagramSocket](https://developer.android.com/reference/kotlin/android/net/TrafficStats#tagDatagramSocket(java.net.DatagramSocket))`(`socket:` ` [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#)`)` Tag the given [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#) with any statistics parameters active for the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tagFileDescriptor](https://developer.android.com/reference/kotlin/android/net/TrafficStats#tagFileDescriptor(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`)` Tag the given [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#) socket with any statistics parameters active for the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tagSocket](https://developer.android.com/reference/kotlin/android/net/TrafficStats#tagSocket(java.net.Socket))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)`)` Tag the given [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) with any statistics parameters active for the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [untagDatagramSocket](https://developer.android.com/reference/kotlin/android/net/TrafficStats#untagDatagramSocket(java.net.DatagramSocket))`(`socket:` ` [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#)`)` Remove any statistics parameters from the given [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#). |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [untagFileDescriptor](https://developer.android.com/reference/kotlin/android/net/TrafficStats#untagFileDescriptor(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`)` Remove any statistics parameters from the given [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#) socket. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [untagSocket](https://developer.android.com/reference/kotlin/android/net/TrafficStats#untagSocket(java.net.Socket))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)`)` Remove any statistics parameters from the given [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#). |

## Constants

### UNSUPPORTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNSUPPORTED: Int
```

The return value to indicate that the device does not support the statistic. 

 Value: -1

## Public constructors

### TrafficStats

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TrafficStats()
```

## Public methods

### clearThreadStatsTag

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun clearThreadStatsTag(): Unit
```

Clear any active tag set to account [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. 
**See Also**

- [#setThreadStatsTag(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsTag(kotlin.Int)) 

### clearThreadStatsUid

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun clearThreadStatsUid(): Unit
```

Clear any active UID set to account [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. 
**See Also**

- [#setThreadStatsUid(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsUid(kotlin.Int)) 

### getAndSetThreadStatsTag

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAndSetThreadStatsTag(tag: Int): Int
```

Set active tag to use when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. Only one active tag per thread is supported.

Changes only take effect during subsequent calls to [tagSocket(java.net.Socket)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#tagSocket(java.net.Socket)).

Tags between`0xFFFFFF00`and`0xFFFFFFFF`are reserved and used internally by system services like [DownloadManager](https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#) when performing traffic on behalf of an application.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current tag for the calling thread, which can be used to restore any existing values after a nested operation is finished |

### getMobileRxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMobileRxBytes(): Long
```

Return number of bytes received across mobile networks since device boot. Counts packets across all mobile network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available. 

### getMobileRxPackets

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMobileRxPackets(): Long
```

Return number of packets received across mobile networks since device boot. Counts packets across all mobile network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available. 

### getMobileTxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMobileTxBytes(): Long
```

Return number of bytes transmitted across mobile networks since device boot. Counts packets across all mobile network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available. 

### getMobileTxPackets

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMobileTxPackets(): Long
```

Return number of packets transmitted across mobile networks since device boot. Counts packets across all mobile network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available. 

### getRxBytes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRxBytes(iface: String): Long
```

Return the number of bytes received on the specified interface since the interface was created. Statistics are measured at the network layer, so both TCP and UDP usage are included. Note that the returned values are partial statistics that do not count data from several sources and do not apply several adjustments that are necessary for correctness, such as adjusting for VPN apps, IPv6-in-IPv4 translation, etc. These values can be used to determine whether traffic is being transferred on the specific interface but are not a substitute for the more accurate statistics provided by the [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#) APIs.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `iface` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the interface. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of received bytes. |

### getRxPackets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRxPackets(iface: String): Long
```

Return the number of packets received on the specified interface since the interface was created. Statistics are measured at the network layer, so both TCP and UDP usage are included. Note that the returned values are partial statistics that do not count data from several sources and do not apply several adjustments that are necessary for correctness, such as adjusting for VPN apps, IPv6-in-IPv4 translation, etc. These values can be used to determine whether traffic is being transferred on the specific interface but are not a substitute for the more accurate statistics provided by the [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#) APIs.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `iface` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the interface. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of received packets. |

### getThreadStatsTag

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getThreadStatsTag(): Int
```

Get the active tag used when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. Only one active tag per thread is supported. [tagSocket(java.net.Socket)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#tagSocket(java.net.Socket)). 
**See Also**

- [#setThreadStatsTag(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsTag(kotlin.Int)) 

### getThreadStatsUid

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getThreadStatsUid(): Int
```

Get the active UID used when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. Only one active tag per thread is supported. [tagSocket(java.net.Socket)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#tagSocket(java.net.Socket)). 
**See Also**

- [#setThreadStatsUid(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsUid(kotlin.Int)) 

### getTotalRxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTotalRxBytes(): Long
```

Return number of bytes received since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available. 

### getTotalRxPackets

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTotalRxPackets(): Long
```

Return number of packets received since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available. 

### getTotalTxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTotalTxBytes(): Long
```

Return number of bytes transmitted since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available. 

### getTotalTxPackets

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTotalTxPackets(): Long
```

Return number of packets transmitted since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available. 

### getTxBytes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTxBytes(iface: String): Long
```

Return the number of bytes transmitted on the specified interface since the interface was created. Statistics are measured at the network layer, so both TCP and UDP usage are included. Note that the returned values are partial statistics that do not count data from several sources and do not apply several adjustments that are necessary for correctness, such as adjusting for VPN apps, IPv6-in-IPv4 translation, etc. These values can be used to determine whether traffic is being transferred on the specific interface but are not a substitute for the more accurate statistics provided by the [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#) APIs.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `iface` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the interface. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of transmitted bytes. |

### getTxPackets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTxPackets(iface: String): Long
```

Return the number of packets transmitted on the specified interface since the interface was created. Statistics are measured at the network layer, so both TCP and UDP usage are included. Note that the returned values are partial statistics that do not count data from several sources and do not apply several adjustments that are necessary for correctness, such as adjusting for VPN apps, IPv6-in-IPv4 translation, etc. These values can be used to determine whether traffic is being transferred on the specific interface but are not a substitute for the more accurate statistics provided by the [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#) APIs.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `iface` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the interface. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of transmitted packets. |

### getUidRxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidRxBytes(uid: Int): Long
```

Return number of bytes received by the given UID since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available.

Starting in [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) this will only report traffic statistics for the calling UID. It will return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) for all other UIDs for privacy reasons. To access historical network statistics belonging to other UIDs, use [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#). 
**See Also**

- [android.os.Process#myUid()](https://developer.android.com/reference/kotlin/android/os/Process.html#myUid())
- [android.content.pm.ApplicationInfo#uid](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#uid:kotlin.Int) 

### getUidRxPackets

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidRxPackets(uid: Int): Long
```

Return number of packets received by the given UID since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available.

Starting in [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) this will only report traffic statistics for the calling UID. It will return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) for all other UIDs for privacy reasons. To access historical network statistics belonging to other UIDs, use [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#). 
**See Also**

- [android.os.Process#myUid()](https://developer.android.com/reference/kotlin/android/os/Process.html#myUid())
- [android.content.pm.ApplicationInfo#uid](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#uid:kotlin.Int) 

### getUidTcpRxBytes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTcpRxBytes(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), transport layer statistics are no longer available, and will always return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int).* 
**See Also**

- [#getUidRxBytes(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidRxBytes(kotlin.Int)) 

### getUidTcpRxSegments

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTcpRxSegments(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), transport layer statistics are no longer available, and will always return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int).* 
**See Also**

- [#getUidRxPackets(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidRxPackets(kotlin.Int)) 

### getUidTcpTxBytes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTcpTxBytes(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), transport layer statistics are no longer available, and will always return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int).* 
**See Also**

- [#getUidTxBytes(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTxBytes(kotlin.Int)) 

### getUidTcpTxSegments

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTcpTxSegments(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), transport layer statistics are no longer available, and will always return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int).* 
**See Also**

- [#getUidTxPackets(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTxPackets(kotlin.Int)) 

### getUidTxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTxBytes(uid: Int): Long
```

Return number of bytes transmitted by the given UID since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available.

Starting in [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) this will only report traffic statistics for the calling UID. It will return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) for all other UIDs for privacy reasons. To access historical network statistics belonging to other UIDs, use [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#). 
**See Also**

- [android.os.Process#myUid()](https://developer.android.com/reference/kotlin/android/os/Process.html#myUid())
- [android.content.pm.ApplicationInfo#uid](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#uid:kotlin.Int) 

### getUidTxPackets

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTxPackets(uid: Int): Long
```

Return number of packets transmitted by the given UID since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), this may return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) on devices where statistics aren't available.

Starting in [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) this will only report traffic statistics for the calling UID. It will return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int) for all other UIDs for privacy reasons. To access historical network statistics belonging to other UIDs, use [NetworkStatsManager](https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#). 
**See Also**

- [android.os.Process#myUid()](https://developer.android.com/reference/kotlin/android/os/Process.html#myUid())
- [android.content.pm.ApplicationInfo#uid](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#uid:kotlin.Int) 

### getUidUdpRxBytes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidUdpRxBytes(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), transport layer statistics are no longer available, and will always return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int).* 
**See Also**

- [#getUidRxBytes(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidRxBytes(kotlin.Int)) 

### getUidUdpRxPackets

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidUdpRxPackets(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), transport layer statistics are no longer available, and will always return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int).* 
**See Also**

- [#getUidRxPackets(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidRxPackets(kotlin.Int)) 

### getUidUdpTxBytes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidUdpTxBytes(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), transport layer statistics are no longer available, and will always return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int).* 
**See Also**

- [#getUidTxBytes(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTxBytes(kotlin.Int)) 

### getUidUdpTxPackets

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidUdpTxPackets(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), transport layer statistics are no longer available, and will always return [UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TrafficStats#UNSUPPORTED:kotlin.Int).* 
**See Also**

- [#getUidTxPackets(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#getUidTxPackets(kotlin.Int)) 

### incrementOperationCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun incrementOperationCount(operationCount: Int): Unit
```

Increment count of network operations performed under the accounting tag currently active on the calling thread. This can be used to derive bytes-per-operation.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------|
| `operationCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of operations to increment count by. |

### incrementOperationCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun incrementOperationCount(
    tag: Int, 
    operationCount: Int
): Unit
```

Increment count of network operations performed under the given accounting tag. This can be used to derive bytes-per-operation.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Accounting tag used in [setThreadStatsTag(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsTag(kotlin.Int)). |
| `operationCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of operations to increment count by. |

### setThreadStatsTag

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setThreadStatsTag(tag: Int): Unit
```

Set active tag to use when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. Only one active tag per thread is supported.

Changes only take effect during subsequent calls to [tagSocket(java.net.Socket)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#tagSocket(java.net.Socket)).

Tags between`0xFFFFFF00`and`0xFFFFFFFF`are reserved and used internally by system services like [DownloadManager](https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#) when performing traffic on behalf of an application. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/net/TrafficStats#clearThreadStatsTag()> 

### setThreadStatsUid

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setThreadStatsUid(uid: Int): Unit
```

Set specific UID to use when accounting [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) traffic originating from the current thread. Designed for use when performing an operation on behalf of another application, or when another application is performing operations on your behalf.

Any app can*accept* blame for traffic performed on a socket originally created by another app by calling this method with the [android.system.Os#getuid()](https://developer.android.com/reference/kotlin/android/system/Os.html#getuid())value. However, only apps holding the`android.Manifest.permission#UPDATE_DEVICE_STATS`permission may*assign*blame to another UIDs.

Changes only take effect during subsequent calls to [tagSocket(java.net.Socket)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#tagSocket(java.net.Socket)). 

### tagDatagramSocket

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tagDatagramSocket(socket: DatagramSocket): Unit
```

Tag the given [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#) with any statistics parameters active for the current thread. Subsequent calls always replace any existing parameters. When finished, call [untagDatagramSocket(java.net.DatagramSocket)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#untagDatagramSocket(java.net.DatagramSocket))to remove statistics parameters.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `socket` | [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#):This value cannot be`null`. |

**See Also**

- [#setThreadStatsTag(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsTag(kotlin.Int)) 

### tagFileDescriptor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tagFileDescriptor(fd: FileDescriptor): Unit
```

Tag the given [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#) socket with any statistics parameters active for the current thread. Subsequent calls always replace any existing parameters. When finished, call [untagFileDescriptor(java.io.FileDescriptor)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#untagFileDescriptor(java.io.FileDescriptor))to remove statistics parameters.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):This value cannot be`null`. |

**See Also**

- [#setThreadStatsTag(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsTag(kotlin.Int)) 

### tagSocket

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tagSocket(socket: Socket): Unit
```

Tag the given [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) with any statistics parameters active for the current thread. Subsequent calls always replace any existing parameters. When finished, call [untagSocket(java.net.Socket)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#untagSocket(java.net.Socket))to remove statistics parameters.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#):This value cannot be`null`. |

**See Also**

- [#setThreadStatsTag(int)](https://developer.android.com/reference/kotlin/android/net/TrafficStats#setThreadStatsTag(kotlin.Int)) 

### untagDatagramSocket

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun untagDatagramSocket(socket: DatagramSocket): Unit
```

Remove any statistics parameters from the given [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `socket` | [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#):This value cannot be`null`. |

### untagFileDescriptor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun untagFileDescriptor(fd: FileDescriptor): Unit
```

Remove any statistics parameters from the given [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#) socket.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):This value cannot be`null`. |

### untagSocket

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun untagSocket(socket: Socket): Unit
```

Remove any statistics parameters from the given [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#).

In Android 8.1 (API level 27) and lower, a socket is automatically untagged when it's sent to another process using binder IPC with a`ParcelFileDescriptor`container. In Android 9.0 (API level 28) and higher, the socket tag is kept when the socket is sent to another process using binder IPC. You can mimic the previous behavior by calling`untagSocket()`before sending the socket to another process.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#):This value cannot be`null`. |
