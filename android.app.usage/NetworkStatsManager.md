# NetworkStatsManager

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkStatsManager

Kotlin | [Java](NetworkStatsManager.md) 
| --- | --- |

```
open class NetworkStatsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.NetworkStatsManager](NetworkStatsManager.md) |

Provides access to network usage history and statistics. Usage data is collected in discrete bins of time called 'Buckets'. See [NetworkStats.Bucket](../android/app/usage/NetworkStats.Bucket.md) for details.

<br />

Queries can define a time interval in the form of start and end timestamps (Long.MIN_VALUE and Long.MAX_VALUE can be used to simulate open ended intervals). By default, apps can only obtain data about themselves. See the below note for special cases in which apps can obtain data about other applications.

### Summary queries

[querySummaryForDevice](NetworkStatsManager.md))

<br />

[querySummaryForUser](NetworkStatsManager.md))

<br />

[querySummary](NetworkStatsManager.md))

<br />

These queries aggregate network usage across the whole interval. Therefore there will be only one bucket for a particular key, state, metered and roaming combination. In case of the user-wide and device-wide summaries a single bucket containing the totalised network usage is returned.

### History queries

[queryDetailsForUid](NetworkStatsManager.md))

<br />

[queryDetails](NetworkStatsManager.md))

<br />

These queries do not aggregate over time but do aggregate over state, metered and roaming. Therefore there can be multiple buckets for a particular key. However, all Buckets will have `state` [NetworkStats.Bucket.STATE_ALL](../android/app/usage/NetworkStats.Bucket.md), `defaultNetwork` [NetworkStats.Bucket.DEFAULT_NETWORK_ALL](../android/app/usage/NetworkStats.Bucket.md), `metered ` [NetworkStats.Bucket.METERED_ALL](../android/app/usage/NetworkStats.Bucket.md), `roaming` [NetworkStats.Bucket.ROAMING_ALL](../android/app/usage/NetworkStats.Bucket.md).

<br />

**NOTE:** Calling [querySummaryForDevice](NetworkStatsManager.md)) or accessing stats for apps other than the calling app requires the permission [android.Manifest.permission#PACKAGE_USAGE_STATS](../android/Manifest.permission.md), which is a system-level permission and will not be granted to third-party apps. However, declaring the permission implies intention to use the API and the user of the device can grant permission through the Settings application.

<br />

Profile owner apps are automatically granted permission to query data on the profile they manage (that is, for any query except [querySummaryForDevice](NetworkStatsManager.md))). Device owner apps and carrier- privileged apps likewise get access to usage data for all users on the device.

<br />

In addition to tethering usage, usage by removed users and apps, and usage by the system is also included in the results for callers with one of these higher levels of access.

<br />

**NOTE:** Prior to API level {@value android.os.Build.VERSION_CODES#N}, all calls to these APIs required the above permission, even to access an app's own data usage, and carrier-privileged apps were not included.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md) Base class for usage callbacks. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [NetworkStats](NetworkStats.md)! | [queryDetails](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Query network usage statistics details. |
| open [NetworkStats](NetworkStats.md) | [queryDetailsForUid](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Query network usage statistics details for a given uid. |
| open [NetworkStats](NetworkStats.md) | [queryDetailsForUidTag](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Query network usage statistics details for a given uid and tag. |
| --- | --- |
| open [NetworkStats](NetworkStats.md) | [queryDetailsForUidTagState](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Query network usage statistics details for a given uid, tag, and state. |
| open [NetworkStats](NetworkStats.md)! | [querySummary](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Query network usage statistics summaries. |
| open [NetworkStats.Bucket](../android/app/usage/NetworkStats.Bucket.md)! | [querySummaryForDevice](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Query network usage statistics summaries. |
| --- | --- |
| open [NetworkStats.Bucket](../android/app/usage/NetworkStats.Bucket.md)! | [querySummaryForUser](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Query network usage statistics summaries. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerUsageCallback](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `thresholdBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `callback:` ` [NetworkStatsManager.UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md)`)` Registers to receive notifications about data usage on specified networks. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerUsageCallback](NetworkStatsManager.md))`(`networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriberId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `thresholdBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `callback:` ` [NetworkStatsManager.UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Registers to receive notifications about data usage on specified networks. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterUsageCallback](NetworkStatsManager.md))`(`callback:` ` [NetworkStatsManager.UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md)`)` Unregisters callbacks on data usage. |

## Public methods

### queryDetails

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryDetails(
    networkType: Int, 
    subscriberId: String?, 
    startTime: Long, 
    endTime: Long
): NetworkStats!
```

Query network usage statistics details. Result filtered to include only uids belonging to calling user. Result is aggregated over state but not aggregated over time, uid, tag, metered, nor roaming. This means buckets' start and end timestamps are going to be between 'startTime' and 'endTime' parameters. State is going to be [NetworkStats.Bucket.STATE_ALL](../android/app/usage/NetworkStats.Bucket.md), uid will vary, tag [NetworkStats.Bucket.TAG_NONE](../android/app/usage/NetworkStats.Bucket.md), default network is going to be [NetworkStats.Bucket.DEFAULT_NETWORK_ALL](../android/app/usage/NetworkStats.Bucket.md), metered is going to be [NetworkStats.Bucket.METERED_ALL](../android/app/usage/NetworkStats.Bucket.md), and roaming is going to be [NetworkStats.Bucket.ROAMING_ALL](../android/app/usage/NetworkStats.Bucket.md).

Only includes buckets that atomically occur in the inclusive time range. Doesn't interpolate across partial buckets. Since bucket length is in the order of hours, this method cannot be used to measure data usage on a fine grained time scale. This may take a long time, and apps should avoid calling this on their main thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): As defined in [ConnectivityManager](../android.net/ConnectivityManager.md), e.g. [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md), [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md) etc. |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when querying for the mobile network type to receive usage for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| --- | --- |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): End of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [NetworkStats](NetworkStats.md)! | Statistics object or null if permissions are insufficient or error happened during statistics collection. |

### queryDetailsForUid

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryDetailsForUid(
    networkType: Int, 
    subscriberId: String?, 
    startTime: Long, 
    endTime: Long, 
    uid: Int
): NetworkStats
```

Query network usage statistics details for a given uid. This may take a long time, and apps should avoid calling this on their main thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): As defined in [ConnectivityManager](../android.net/ConnectivityManager.md), e.g. [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md), [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md) etc. |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when querying for the mobile network type to receive usage for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| --- | --- |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): End of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): UID of app |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [NetworkStats](NetworkStats.md) | Statistics which is described above. This value cannot be `null`. |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------|
| `java.lang.SecurityException` | if permissions are insufficient to read network statistics. |

**See Also**

- [#queryDetailsForUidTagState(int, String, long, long, int, int, int)](NetworkStatsManager.md)) 

### queryDetailsForUidTag

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryDetailsForUidTag(
    networkType: Int, 
    subscriberId: String?, 
    startTime: Long, 
    endTime: Long, 
    uid: Int, 
    tag: Int
): NetworkStats
```

Query network usage statistics details for a given uid and tag. This may take a long time, and apps should avoid calling this on their main thread. Only usable for uids belonging to calling user. Result is not aggregated over time. This means buckets' start and end timestamps are going to be between 'startTime' and 'endTime' parameters. The uid is going to be the same as the 'uid' parameter, the tag the same as the 'tag' parameter, and the state the same as the 'state' parameter. defaultNetwork is going to be [NetworkStats.Bucket.DEFAULT_NETWORK_ALL](../android/app/usage/NetworkStats.Bucket.md), metered is going to be [NetworkStats.Bucket.METERED_ALL](../android/app/usage/NetworkStats.Bucket.md), and roaming is going to be [NetworkStats.Bucket.ROAMING_ALL](../android/app/usage/NetworkStats.Bucket.md).

Only includes buckets that atomically occur in the inclusive time range. Doesn't interpolate across partial buckets. Since bucket length is in the order of hours, this method cannot be used to measure data usage on a fine grained time scale. This may take a long time, and apps should avoid calling this on their main thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): As defined in [ConnectivityManager](../android.net/ConnectivityManager.md), e.g. [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md), [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md) etc. |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when querying for the mobile network type to receive usage for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| --- | --- |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): End of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): UID of app |
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): TAG of interest. Use [NetworkStats.Bucket.TAG_NONE](../android/app/usage/NetworkStats.Bucket.md) for aggregated data across all the tags. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [NetworkStats](NetworkStats.md) | Statistics which is described above. This value cannot be `null`. |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------|
| `java.lang.SecurityException` | if permissions are insufficient to read network statistics. |

### queryDetailsForUidTagState

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryDetailsForUidTagState(
    networkType: Int, 
    subscriberId: String?, 
    startTime: Long, 
    endTime: Long, 
    uid: Int, 
    tag: Int, 
    state: Int
): NetworkStats
```

Query network usage statistics details for a given uid, tag, and state. Only usable for uids belonging to calling user. Result is not aggregated over time. This means buckets' start and end timestamps are going to be between 'startTime' and 'endTime' parameters. The uid is going to be the same as the 'uid' parameter, the tag the same as the 'tag' parameter, and the state the same as the 'state' parameter. defaultNetwork is going to be [NetworkStats.Bucket.DEFAULT_NETWORK_ALL](../android/app/usage/NetworkStats.Bucket.md), metered is going to be [NetworkStats.Bucket.METERED_ALL](../android/app/usage/NetworkStats.Bucket.md), and roaming is going to be [NetworkStats.Bucket.ROAMING_ALL](../android/app/usage/NetworkStats.Bucket.md).

Only includes buckets that atomically occur in the inclusive time range. Doesn't interpolate across partial buckets. Since bucket length is in the order of hours, this method cannot be used to measure data usage on a fine grained time scale. This may take a long time, and apps should avoid calling this on their main thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): As defined in [ConnectivityManager](../android.net/ConnectivityManager.md), e.g. [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md), [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md) etc. |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when querying for the mobile network type to receive usage for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| --- | --- |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): End of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): UID of app |
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): TAG of interest. Use [NetworkStats.Bucket.TAG_NONE](../android/app/usage/NetworkStats.Bucket.md) for aggregated data across all the tags. |
| --- | --- |
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): state of interest. Use [NetworkStats.Bucket.STATE_ALL](../android/app/usage/NetworkStats.Bucket.md) to aggregate traffic from all states. |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [NetworkStats](NetworkStats.md) | Statistics which is described above. This value cannot be `null`. |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------|
| `java.lang.SecurityException` | if permissions are insufficient to read network statistics. |

### querySummary

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun querySummary(
    networkType: Int, 
    subscriberId: String?, 
    startTime: Long, 
    endTime: Long
): NetworkStats!
```

Query network usage statistics summaries. Result filtered to include only uids belonging to calling user. Result is aggregated over time, hence all buckets will have the same start and end timestamps. Not aggregated over state, uid, default network, metered, or roaming. This means buckets' start and end timestamps are going to be the same as the 'startTime' and 'endTime' parameters. State, uid, metered, and roaming are going to vary, and tag is going to be the same. This may take a long time, and apps should avoid calling this on their main thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): As defined in [ConnectivityManager](../android.net/ConnectivityManager.md), e.g. [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md), [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md) etc. |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when querying for the mobile network type to receive usage for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| --- | --- |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): End of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [NetworkStats](NetworkStats.md)! | Statistics object or null if permissions are insufficient or error happened during statistics collection. |

### querySummaryForDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun querySummaryForDevice(
    networkType: Int, 
    subscriberId: String?, 
    startTime: Long, 
    endTime: Long
): NetworkStats.Bucket!
```

Query network usage statistics summaries. Result is summarised data usage for the whole device. Result is a single Bucket aggregated over time, state, uid, tag, metered, and roaming. This means the bucket's start and end timestamp are going to be the same as the 'startTime' and 'endTime' parameters. State is going to be [NetworkStats.Bucket.STATE_ALL](../android/app/usage/NetworkStats.Bucket.md), uid [NetworkStats.Bucket.UID_ALL](../android/app/usage/NetworkStats.Bucket.md), tag [NetworkStats.Bucket.TAG_NONE](../android/app/usage/NetworkStats.Bucket.md), default network [NetworkStats.Bucket.DEFAULT_NETWORK_ALL](../android/app/usage/NetworkStats.Bucket.md), metered [NetworkStats.Bucket.METERED_ALL](../android/app/usage/NetworkStats.Bucket.md), and roaming [NetworkStats.Bucket.ROAMING_ALL](../android/app/usage/NetworkStats.Bucket.md). This may take a long time, and apps should avoid calling this on their main thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): As defined in [ConnectivityManager](../android.net/ConnectivityManager.md), e.g. [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md), [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md) etc. |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when querying for the mobile network type to receive usage for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| --- | --- |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): End of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [NetworkStats.Bucket](../android/app/usage/NetworkStats.Bucket.md)! | Bucket object or null if permissions are insufficient or error happened during statistics collection. |

### querySummaryForUser

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun querySummaryForUser(
    networkType: Int, 
    subscriberId: String?, 
    startTime: Long, 
    endTime: Long
): NetworkStats.Bucket!
```

Query network usage statistics summaries. Result is summarised data usage for all uids belonging to calling user. Result is a single Bucket aggregated over time, state and uid. This means the bucket's start and end timestamp are going to be the same as the 'startTime' and 'endTime' parameters. State is going to be [NetworkStats.Bucket.STATE_ALL](../android/app/usage/NetworkStats.Bucket.md), uid [NetworkStats.Bucket.UID_ALL](../android/app/usage/NetworkStats.Bucket.md), tag [NetworkStats.Bucket.TAG_NONE](../android/app/usage/NetworkStats.Bucket.md), metered [NetworkStats.Bucket.METERED_ALL](../android/app/usage/NetworkStats.Bucket.md), and roaming [NetworkStats.Bucket.ROAMING_ALL](../android/app/usage/NetworkStats.Bucket.md). This may take a long time, and apps should avoid calling this on their main thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): As defined in [ConnectivityManager](../android.net/ConnectivityManager.md), e.g. [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md), [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md) etc. |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when querying for the mobile network type to receive usage for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |
| --- | --- |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): End of period. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](../java.lang/System.md)). |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [NetworkStats.Bucket](../android/app/usage/NetworkStats.Bucket.md)! | Bucket object or null if permissions are insufficient or error happened during statistics collection. |

### registerUsageCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerUsageCallback(
    networkType: Int, 
    subscriberId: String?, 
    thresholdBytes: Long, 
    callback: NetworkStatsManager.UsageCallback
): Unit
```

Registers to receive notifications about data usage on specified networks.

The callbacks will continue to be called as long as the process is live or [unregisterUsageCallback](NetworkStatsManager.md)) is called.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Type of network to monitor. Either [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md) or [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md). |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when registering for the mobile network type to receive notifications for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `thresholdBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Threshold in bytes to be notified on. |
| --- | --- |
| `callback` | [NetworkStatsManager.UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md): The [UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md) that the system will call when data usage has exceeded the specified threshold. This value cannot be `null`. |

### registerUsageCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerUsageCallback(
    networkType: Int, 
    subscriberId: String?, 
    thresholdBytes: Long, 
    callback: NetworkStatsManager.UsageCallback, 
    handler: Handler?
): Unit
```

Registers to receive notifications about data usage on specified networks.

The callbacks will continue to be called as long as the process is live or [unregisterUsageCallback](NetworkStatsManager.md)) is called.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Type of network to monitor. Either [ConnectivityManager.TYPE_MOBILE](../android.net/ConnectivityManager.md) or [ConnectivityManager.TYPE_WIFI](../android.net/ConnectivityManager.md). |
| `subscriberId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If applicable, the subscriber id of the network interface. Starting with API level 29, the `subscriberId` is guarded by additional restrictions. Calling apps that do not meet the new requirements to access the `subscriberId` can provide a `null` value when registering for the mobile network type to receive notifications for all mobile networks. For additional details see [android.telephony.TelephonyManager#getSubscriberId()](../android.telephony/TelephonyManager.md)). Starting with API level 31, calling apps can provide a `subscriberId` with wifi network type to receive usage for wifi networks which is under the given subscription if applicable. Otherwise, pass `null` when querying all wifi networks. |
| `thresholdBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Threshold in bytes to be notified on. |
| --- | --- |
| `callback` | [NetworkStatsManager.UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md): The [UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md) that the system will call when data usage has exceeded the specified threshold. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: to dispatch callback events through, otherwise if `null` it uses the calling thread. |

### unregisterUsageCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterUsageCallback(callback: NetworkStatsManager.UsageCallback): Unit
```

Unregisters callbacks on data usage.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [NetworkStatsManager.UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md): The [UsageCallback](../android/app/usage/NetworkStatsManager.UsageCallback.md) used when registering. This value cannot be `null`. |
