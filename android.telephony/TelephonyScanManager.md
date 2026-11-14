# TelephonyScanManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TelephonyScanManager

Kotlin| [Java](../android/telephony/TelephonyScanManager.md) 
| --- | --- |

```
class TelephonyScanManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.TelephonyScanManager](../android/telephony/TelephonyScanManager.md) |

Manages the radio access network scan requests and callbacks. 
Requires the [PackageManager#FEATURE_TELEPHONY_RADIO_ACCESS](../android/content/pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [NetworkScanCallback](../android/telephony/TelephonyScanManager.NetworkScanCallback.md) The caller of [android.telephony.TelephonyManager#requestNetworkScan(android.telephony.NetworkScanRequest,java.util.concurrent.Executor,android.telephony.TelephonyScanManager.NetworkScanCallback)](../android/telephony/TelephonyManager.md))should implement and provide this callback so that the scan results or errors can be returned. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TelephonyScanManager](../android/telephony/TelephonyScanManager.md))`()` <br /> |

## Public constructors

### TelephonyScanManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TelephonyScanManager()
```
