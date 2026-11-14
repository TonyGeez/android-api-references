# TelephonyScanManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TelephonyScanManager

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyScanManager "View this page in Java") 
| --- | --- |

```
class TelephonyScanManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.TelephonyScanManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyScanManager#) |

Manages the radio access network scan requests and callbacks. 
Requires the [PackageManager#FEATURE_TELEPHONY_RADIO_ACCESS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [NetworkScanCallback](https://developer.android.com/reference/kotlin/android/telephony/TelephonyScanManager.NetworkScanCallback) The caller of [android.telephony.TelephonyManager#requestNetworkScan(android.telephony.NetworkScanRequest,java.util.concurrent.Executor,android.telephony.TelephonyScanManager.NetworkScanCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#requestNetworkScan(android.telephony.NetworkScanRequest,%20java.util.concurrent.Executor,%20android.telephony.TelephonyScanManager.NetworkScanCallback))should implement and provide this callback so that the scan results or errors can be returned. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TelephonyScanManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyScanManager#TelephonyScanManager())`()` <br /> |

## Public constructors

### TelephonyScanManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TelephonyScanManager()
```
