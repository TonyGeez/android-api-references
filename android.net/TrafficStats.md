# TrafficStats

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrafficStats

Kotlin| [Java](../android/net/TrafficStats.md) 
| --- | --- |

```
open class TrafficStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.TrafficStats](../android/net/TrafficStats.md) |

Class that provides network traffic statistics. These statistics include bytes transmitted and received and network packets transmitted and received, over all interfaces, over the mobile interface, and on a per-UID basis.

These statistics may not be available on all platforms. If the statistics are not supported by this device, [UNSUPPORTED](../android/net/TrafficStats.md) will be returned.

Note that the statistics returned by this class reset and start from zero after every reboot. To access more robust historical network statistics data, use [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md) instead.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNSUPPORTED](../android/net/TrafficStats.md) The return value to indicate that the device does not support the statistic. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [TrafficStats](../android/net/TrafficStats.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearThreadStatsTag](../android/net/TrafficStats.md))`()` Clear any active tag set to account [Socket](../java/net/Socket.md) traffic originating from the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearThreadStatsUid](../android/net/TrafficStats.md))`()` Clear any active UID set to account [Socket](../java/net/Socket.md) traffic originating from the current thread. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndSetThreadStatsTag](../android/net/TrafficStats.md))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set active tag to use when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMobileRxBytes](../android/net/TrafficStats.md))`()` Return number of bytes received across mobile networks since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMobileRxPackets](../android/net/TrafficStats.md))`()` Return number of packets received across mobile networks since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMobileTxBytes](../android/net/TrafficStats.md))`()` Return number of bytes transmitted across mobile networks since device boot. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMobileTxPackets](../android/net/TrafficStats.md))`()` Return number of packets transmitted across mobile networks since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRxBytes](../android/net/TrafficStats.md))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return the number of bytes received on the specified interface since the interface was created. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRxPackets](../android/net/TrafficStats.md))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return the number of packets received on the specified interface since the interface was created. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadStatsTag](../android/net/TrafficStats.md))`()` Get the active tag used when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadStatsUid](../android/net/TrafficStats.md))`()` Get the active UID used when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalRxBytes](../android/net/TrafficStats.md))`()` Return number of bytes received since device boot. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalRxPackets](../android/net/TrafficStats.md))`()` Return number of packets received since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalTxBytes](../android/net/TrafficStats.md))`()` Return number of bytes transmitted since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalTxPackets](../android/net/TrafficStats.md))`()` Return number of packets transmitted since device boot. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTxBytes](../android/net/TrafficStats.md))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return the number of bytes transmitted on the specified interface since the interface was created. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTxPackets](../android/net/TrafficStats.md))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return the number of packets transmitted on the specified interface since the interface was created. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidRxBytes](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return number of bytes received by the given UID since device boot. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidRxPackets](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return number of packets received by the given UID since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTcpRxBytes](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTcpRxSegments](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTcpTxBytes](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTcpTxSegments](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTxBytes](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return number of bytes transmitted by the given UID since device boot. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidTxPackets](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return number of packets transmitted by the given UID since device boot. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidUdpRxBytes](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidUdpRxPackets](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidUdpTxBytes](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUidUdpTxPackets](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [incrementOperationCount](../android/net/TrafficStats.md))`(`operationCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increment count of network operations performed under the accounting tag currently active on the calling thread. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [incrementOperationCount](../android/net/TrafficStats.md))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `operationCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increment count of network operations performed under the given accounting tag. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThreadStatsTag](../android/net/TrafficStats.md))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set active tag to use when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThreadStatsUid](../android/net/TrafficStats.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set specific UID to use when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tagDatagramSocket](../android/net/TrafficStats.md))`(`socket:` ` [DatagramSocket](../java/net/DatagramSocket.md)`)` Tag the given [DatagramSocket](../java/net/DatagramSocket.md) with any statistics parameters active for the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tagFileDescriptor](../android/net/TrafficStats.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)`)` Tag the given [FileDescriptor](../java/io/FileDescriptor.md) socket with any statistics parameters active for the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tagSocket](../android/net/TrafficStats.md))`(`socket:` ` [Socket](../java/net/Socket.md)`)` Tag the given [Socket](../java/net/Socket.md) with any statistics parameters active for the current thread. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [untagDatagramSocket](../android/net/TrafficStats.md))`(`socket:` ` [DatagramSocket](../java/net/DatagramSocket.md)`)` Remove any statistics parameters from the given [DatagramSocket](../java/net/DatagramSocket.md). |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [untagFileDescriptor](../android/net/TrafficStats.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)`)` Remove any statistics parameters from the given [FileDescriptor](../java/io/FileDescriptor.md) socket. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [untagSocket](../android/net/TrafficStats.md))`(`socket:` ` [Socket](../java/net/Socket.md)`)` Remove any statistics parameters from the given [Socket](../java/net/Socket.md). |
| --- | --- |

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

Clear any active tag set to account [Socket](../java/net/Socket.md) traffic originating from the current thread. 
**See Also**

- [#setThreadStatsTag(int)](../android/net/TrafficStats.md)) 

### clearThreadStatsUid

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun clearThreadStatsUid(): Unit
```

Clear any active UID set to account [Socket](../java/net/Socket.md) traffic originating from the current thread. 
**See Also**

- [#setThreadStatsUid(int)](../android/net/TrafficStats.md)) 

### getAndSetThreadStatsTag

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAndSetThreadStatsTag(tag: Int): Int
```

Set active tag to use when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. Only one active tag per thread is supported.

Changes only take effect during subsequent calls to [tagSocket(java.net.Socket)](../android/net/TrafficStats.md)).

Tags between`0xFFFFFF00`and`0xFFFFFFFF`are reserved and used internally by system services like [DownloadManager](../android/app/DownloadManager.md) when performing traffic on behalf of an application.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current tag for the calling thread, which can be used to restore any existing values after a nested operation is finished |

### getMobileRxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMobileRxBytes(): Long
```

Return number of bytes received across mobile networks since device boot. Counts packets across all mobile network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available. 

### getMobileRxPackets

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMobileRxPackets(): Long
```

Return number of packets received across mobile networks since device boot. Counts packets across all mobile network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available. 

### getMobileTxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMobileTxBytes(): Long
```

Return number of bytes transmitted across mobile networks since device boot. Counts packets across all mobile network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available. 

### getMobileTxPackets

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMobileTxPackets(): Long
```

Return number of packets transmitted across mobile networks since device boot. Counts packets across all mobile network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available. 

### getRxBytes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRxBytes(iface: String): Long
```

Return the number of bytes received on the specified interface since the interface was created. Statistics are measured at the network layer, so both TCP and UDP usage are included. Note that the returned values are partial statistics that do not count data from several sources and do not apply several adjustments that are necessary for correctness, such as adjusting for VPN apps, IPv6-in-IPv4 translation, etc. These values can be used to determine whether traffic is being transferred on the specific interface but are not a substitute for the more accurate statistics provided by the [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md) APIs.

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

Return the number of packets received on the specified interface since the interface was created. Statistics are measured at the network layer, so both TCP and UDP usage are included. Note that the returned values are partial statistics that do not count data from several sources and do not apply several adjustments that are necessary for correctness, such as adjusting for VPN apps, IPv6-in-IPv4 translation, etc. These values can be used to determine whether traffic is being transferred on the specific interface but are not a substitute for the more accurate statistics provided by the [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md) APIs.

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

Get the active tag used when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. Only one active tag per thread is supported. [tagSocket(java.net.Socket)](../android/net/TrafficStats.md)). 
**See Also**

- [#setThreadStatsTag(int)](../android/net/TrafficStats.md)) 

### getThreadStatsUid

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getThreadStatsUid(): Int
```

Get the active UID used when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. Only one active tag per thread is supported. [tagSocket(java.net.Socket)](../android/net/TrafficStats.md)). 
**See Also**

- [#setThreadStatsUid(int)](../android/net/TrafficStats.md)) 

### getTotalRxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTotalRxBytes(): Long
```

Return number of bytes received since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available. 

### getTotalRxPackets

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTotalRxPackets(): Long
```

Return number of packets received since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available. 

### getTotalTxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTotalTxBytes(): Long
```

Return number of bytes transmitted since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available. 

### getTotalTxPackets

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTotalTxPackets(): Long
```

Return number of packets transmitted since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available. 

### getTxBytes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTxBytes(iface: String): Long
```

Return the number of bytes transmitted on the specified interface since the interface was created. Statistics are measured at the network layer, so both TCP and UDP usage are included. Note that the returned values are partial statistics that do not count data from several sources and do not apply several adjustments that are necessary for correctness, such as adjusting for VPN apps, IPv6-in-IPv4 translation, etc. These values can be used to determine whether traffic is being transferred on the specific interface but are not a substitute for the more accurate statistics provided by the [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md) APIs.

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

Return the number of packets transmitted on the specified interface since the interface was created. Statistics are measured at the network layer, so both TCP and UDP usage are included. Note that the returned values are partial statistics that do not count data from several sources and do not apply several adjustments that are necessary for correctness, such as adjusting for VPN apps, IPv6-in-IPv4 translation, etc. These values can be used to determine whether traffic is being transferred on the specific interface but are not a substitute for the more accurate statistics provided by the [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md) APIs.

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

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available.

Starting in [android.os.Build.VERSION_CODES#N](../android/os/Build.VERSION_CODES.md) this will only report traffic statistics for the calling UID. It will return [UNSUPPORTED](../android/net/TrafficStats.md) for all other UIDs for privacy reasons. To access historical network statistics belonging to other UIDs, use [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md). 
**See Also**

- [android.os.Process#myUid()](../android/os/Process.md))
- [android.content.pm.ApplicationInfo#uid](../android/content/pm/ApplicationInfo.md) 

### getUidRxPackets

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidRxPackets(uid: Int): Long
```

Return number of packets received by the given UID since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available.

Starting in [android.os.Build.VERSION_CODES#N](../android/os/Build.VERSION_CODES.md) this will only report traffic statistics for the calling UID. It will return [UNSUPPORTED](../android/net/TrafficStats.md) for all other UIDs for privacy reasons. To access historical network statistics belonging to other UIDs, use [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md). 
**See Also**

- [android.os.Process#myUid()](../android/os/Process.md))
- [android.content.pm.ApplicationInfo#uid](../android/content/pm/ApplicationInfo.md) 

### getUidTcpRxBytes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTcpRxBytes(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), transport layer statistics are no longer available, and will always return [UNSUPPORTED](../android/net/TrafficStats.md).* 
**See Also**

- [#getUidRxBytes(int)](../android/net/TrafficStats.md)) 

### getUidTcpRxSegments

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTcpRxSegments(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), transport layer statistics are no longer available, and will always return [UNSUPPORTED](../android/net/TrafficStats.md).* 
**See Also**

- [#getUidRxPackets(int)](../android/net/TrafficStats.md)) 

### getUidTcpTxBytes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTcpTxBytes(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), transport layer statistics are no longer available, and will always return [UNSUPPORTED](../android/net/TrafficStats.md).* 
**See Also**

- [#getUidTxBytes(int)](../android/net/TrafficStats.md)) 

### getUidTcpTxSegments

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTcpTxSegments(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), transport layer statistics are no longer available, and will always return [UNSUPPORTED](../android/net/TrafficStats.md).* 
**See Also**

- [#getUidTxPackets(int)](../android/net/TrafficStats.md)) 

### getUidTxBytes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTxBytes(uid: Int): Long
```

Return number of bytes transmitted by the given UID since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available.

Starting in [android.os.Build.VERSION_CODES#N](../android/os/Build.VERSION_CODES.md) this will only report traffic statistics for the calling UID. It will return [UNSUPPORTED](../android/net/TrafficStats.md) for all other UIDs for privacy reasons. To access historical network statistics belonging to other UIDs, use [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md). 
**See Also**

- [android.os.Process#myUid()](../android/os/Process.md))
- [android.content.pm.ApplicationInfo#uid](../android/content/pm/ApplicationInfo.md) 

### getUidTxPackets

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidTxPackets(uid: Int): Long
```

Return number of packets transmitted by the given UID since device boot. Counts packets across all network interfaces, and always increases monotonically since device boot. Statistics are measured at the network layer, so they include both TCP and UDP usage.

Before [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this may return [UNSUPPORTED](../android/net/TrafficStats.md) on devices where statistics aren't available.

Starting in [android.os.Build.VERSION_CODES#N](../android/os/Build.VERSION_CODES.md) this will only report traffic statistics for the calling UID. It will return [UNSUPPORTED](../android/net/TrafficStats.md) for all other UIDs for privacy reasons. To access historical network statistics belonging to other UIDs, use [NetworkStatsManager](../android/app/usage/NetworkStatsManager.md). 
**See Also**

- [android.os.Process#myUid()](../android/os/Process.md))
- [android.content.pm.ApplicationInfo#uid](../android/content/pm/ApplicationInfo.md) 

### getUidUdpRxBytes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidUdpRxBytes(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), transport layer statistics are no longer available, and will always return [UNSUPPORTED](../android/net/TrafficStats.md).* 
**See Also**

- [#getUidRxBytes(int)](../android/net/TrafficStats.md)) 

### getUidUdpRxPackets

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidUdpRxPackets(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), transport layer statistics are no longer available, and will always return [UNSUPPORTED](../android/net/TrafficStats.md).* 
**See Also**

- [#getUidRxPackets(int)](../android/net/TrafficStats.md)) 

### getUidUdpTxBytes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidUdpTxBytes(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), transport layer statistics are no longer available, and will always return [UNSUPPORTED](../android/net/TrafficStats.md).* 
**See Also**

- [#getUidTxBytes(int)](../android/net/TrafficStats.md)) 

### getUidUdpTxPackets

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUidUdpTxPackets(uid: Int): Long
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), transport layer statistics are no longer available, and will always return [UNSUPPORTED](../android/net/TrafficStats.md).* 
**See Also**

- [#getUidTxPackets(int)](../android/net/TrafficStats.md)) 

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
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Accounting tag used in [setThreadStatsTag(int)](../android/net/TrafficStats.md)). |
| `operationCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of operations to increment count by. |

### setThreadStatsTag

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setThreadStatsTag(tag: Int): Unit
```

Set active tag to use when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. Only one active tag per thread is supported.

Changes only take effect during subsequent calls to [tagSocket(java.net.Socket)](../android/net/TrafficStats.md)).

Tags between`0xFFFFFF00`and`0xFFFFFFFF`are reserved and used internally by system services like [DownloadManager](../android/app/DownloadManager.md) when performing traffic on behalf of an application. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/net/TrafficStats#clearThreadStatsTag()> 

### setThreadStatsUid

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setThreadStatsUid(uid: Int): Unit
```

Set specific UID to use when accounting [Socket](../java/net/Socket.md) traffic originating from the current thread. Designed for use when performing an operation on behalf of another application, or when another application is performing operations on your behalf.

Any app can*accept* blame for traffic performed on a socket originally created by another app by calling this method with the [android.system.Os#getuid()](../android/system/Os.md))value. However, only apps holding the`android.Manifest.permission#UPDATE_DEVICE_STATS`permission may*assign*blame to another UIDs.

Changes only take effect during subsequent calls to [tagSocket(java.net.Socket)](../android/net/TrafficStats.md)). 

### tagDatagramSocket

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tagDatagramSocket(socket: DatagramSocket): Unit
```

Tag the given [DatagramSocket](../java/net/DatagramSocket.md) with any statistics parameters active for the current thread. Subsequent calls always replace any existing parameters. When finished, call [untagDatagramSocket(java.net.DatagramSocket)](../android/net/TrafficStats.md))to remove statistics parameters.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `socket` | [DatagramSocket](../java/net/DatagramSocket.md):This value cannot be`null`. |

**See Also**

- [#setThreadStatsTag(int)](../android/net/TrafficStats.md)) 

### tagFileDescriptor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tagFileDescriptor(fd: FileDescriptor): Unit
```

Tag the given [FileDescriptor](../java/io/FileDescriptor.md) socket with any statistics parameters active for the current thread. Subsequent calls always replace any existing parameters. When finished, call [untagFileDescriptor(java.io.FileDescriptor)](../android/net/TrafficStats.md))to remove statistics parameters.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md):This value cannot be`null`. |

**See Also**

- [#setThreadStatsTag(int)](../android/net/TrafficStats.md)) 

### tagSocket

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tagSocket(socket: Socket): Unit
```

Tag the given [Socket](../java/net/Socket.md) with any statistics parameters active for the current thread. Subsequent calls always replace any existing parameters. When finished, call [untagSocket(java.net.Socket)](../android/net/TrafficStats.md))to remove statistics parameters.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](../java/net/Socket.md):This value cannot be`null`. |

**See Also**

- [#setThreadStatsTag(int)](../android/net/TrafficStats.md)) 

### untagDatagramSocket

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun untagDatagramSocket(socket: DatagramSocket): Unit
```

Remove any statistics parameters from the given [DatagramSocket](../java/net/DatagramSocket.md).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `socket` | [DatagramSocket](../java/net/DatagramSocket.md):This value cannot be`null`. |

### untagFileDescriptor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun untagFileDescriptor(fd: FileDescriptor): Unit
```

Remove any statistics parameters from the given [FileDescriptor](../java/io/FileDescriptor.md) socket.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md):This value cannot be`null`. |

### untagSocket

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun untagSocket(socket: Socket): Unit
```

Remove any statistics parameters from the given [Socket](../java/net/Socket.md).

In Android 8.1 (API level 27) and lower, a socket is automatically untagged when it's sent to another process using binder IPC with a`ParcelFileDescriptor`container. In Android 9.0 (API level 28) and higher, the socket tag is kept when the socket is sent to another process using binder IPC. You can mimic the previous behavior by calling`untagSocket()`before sending the socket to another process.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](../java/net/Socket.md):This value cannot be`null`. |
