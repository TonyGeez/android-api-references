# WifiP2pWfdInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pWfdInfo

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pWfdInfo "View this page in Java") 

```
class WifiP2pWfdInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.p2p.WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#) |

A class representing Wifi Display information for a device. See Wifi Display technical specification v1.0.0, section 5.1.2. See Wifi Display technical specification v2.0.0, section 5.1.12 for Wifi Display R2.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate audo is only supported at source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate audio is not supported at primary sink. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_CONTENT_PROTECTION_SUPPORT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_CONTENT_PROTECTION_SUPPORT:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate the support of Content Protection using the HDCP system 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicates that coupled sink is supporeted at sink. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicates that coupled sink is supported at source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_DEVICE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK:kotlin.Int) [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo())\& [DEVICE_INFO_DEVICE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK:kotlin.Int) is one of [DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int), [DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int), [DEVICE_TYPE_SECONDARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK:kotlin.Int) or [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate the preferred connectifity for Wifi Display. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_SESSION_AVAILABLE_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_SESSION_AVAILABLE_MASK:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicates that Wifi Display session is available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_TDLS_PERSISTENT_GROUP](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_TDLS_PERSISTENT_GROUP:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate that TDLS persistent group is intended. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate that the request is for re-invocation of TDLS persistent group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate time synchronization using 802. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT:kotlin.Int) Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicates that Wifi Display discovery is supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int) The device is a primary sink. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TYPE_SECONDARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK:kotlin.Int) The device is a secondary sink. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int) The device is dual-role capable i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int) The device is a Wifi Display Source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREFERRED_CONNECTIVITY_P2P](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#PREFERRED_CONNECTIVITY_P2P:kotlin.Int) Wifi Display (WFD) preferred connectivity is Wifi Direct (P2P). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREFERRED_CONNECTIVITY_TDLS](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#PREFERRED_CONNECTIVITY_TDLS:kotlin.Int) Wifi Display (WFD) preferred connectivity is TDLS. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#WifiP2pWfdInfo())`()` Default constructor. |
| [WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#WifiP2pWfdInfo(android.net.wifi.p2p.WifiP2pWfdInfo))`(`source:` ` [WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#)?`)` Copy constructor. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#describeContents())`()` Implement the Parcelable interface |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getControlPort](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getControlPort())`()` Returns the TCP port at which the WFD Device listens for RTSP messages. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo())`()` Return R1 raw device info, See Wifi Display technical specification v1. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceType](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceType())`()` Get the type of the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxThroughput](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getMaxThroughput())`()` Returns the maximum average throughput capability of the WFD Device, in megabits/second. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getR2DeviceInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getR2DeviceInfo())`()` Return R2 raw device info, See Wifi Display technical specification v2. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getR2DeviceType](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getR2DeviceType())`()` Get the type of the R2 device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isContentProtectionSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#isContentProtectionSupported())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCoupledSinkSupportedAtSink](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#isCoupledSinkSupportedAtSink())`()` Returns true if Coupled Sink is supported by WFD Sink. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCoupledSinkSupportedAtSource](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#isCoupledSinkSupportedAtSource())`()` Returns true if Coupled Sink is supported by WFD Source. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#isEnabled())`()` Returns true is Wifi Display is enabled, false otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isR2Supported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#isR2Supported())`()` Returns true is Wifi Display R2 is enabled, false otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSessionAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#isSessionAvailable())`()` Returns true if a session is available, false otherwise. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentProtectionSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setContentProtectionSupported(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Content Protection using the HDCP system 2. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlPort](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setControlPort(kotlin.Int))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the TCP port at which the WFD Device listens for RTSP messages. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCoupledSinkSupportAtSink](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setCoupledSinkSupportAtSink(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Coupled Sink feature is supported by WFD Sink. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCoupledSinkSupportAtSource](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setCoupledSinkSupportAtSource(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Coupled Sink feature is supported by WFD Source. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setDeviceType](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setDeviceType(kotlin.Int))`(`deviceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of the device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Wifi Display should be enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxThroughput](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setMaxThroughput(kotlin.Int))`(`maxThroughput:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum average throughput capability of the WFD Device, in megabits/second. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setR2DeviceType](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setR2DeviceType(kotlin.Int))`(`deviceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of the Wifi Display R2 device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSessionAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#setSessionAvailable(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether a session is available. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

## Constants

### DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate audo is only supported at source. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 2048

### DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate audio is not supported at primary sink. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 1024

### DEVICE_INFO_CONTENT_PROTECTION_SUPPORT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_CONTENT_PROTECTION_SUPPORT: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate the support of Content Protection using the HDCP system 2.0/2.1. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 256

### DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicates that coupled sink is supporeted at sink. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 8

### DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicates that coupled sink is supported at source. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 4

### DEVICE_INFO_DEVICE_TYPE_MASK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_DEVICE_TYPE_MASK: Int
```

[getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo())\& [DEVICE_INFO_DEVICE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK:kotlin.Int) is one of [DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int), [DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int), [DEVICE_TYPE_SECONDARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK:kotlin.Int) or [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int). The bit definition is listed in 5.1.2 WFD Device Information Subelement and 5.1.12 WFD R2 Device Information Subelement in Wifi Display Technical Specification. 

 Value: 3

### DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate the preferred connectifity for Wifi Display. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. The value is one of [PREFERRED_CONNECTIVITY_P2P](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#PREFERRED_CONNECTIVITY_P2P:kotlin.Int) or [PREFERRED_CONNECTIVITY_TDLS](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#PREFERRED_CONNECTIVITY_TDLS:kotlin.Int). 

 Value: 128

### DEVICE_INFO_SESSION_AVAILABLE_MASK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_SESSION_AVAILABLE_MASK: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicates that Wifi Display session is available. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 48

### DEVICE_INFO_TDLS_PERSISTENT_GROUP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_TDLS_PERSISTENT_GROUP: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate that TDLS persistent group is intended. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 4096

### DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate that the request is for re-invocation of TDLS persistent group. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 8192

### DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicate time synchronization using 802.1AS is supported. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 512

### DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT: Int
```

Bit field for [getDeviceInfo()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#getDeviceInfo()), indicates that Wifi Display discovery is supported. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 64

### DEVICE_TYPE_PRIMARY_SINK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_TYPE_PRIMARY_SINK: Int
```

The device is a primary sink. 

 Value: 1

### DEVICE_TYPE_SECONDARY_SINK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_TYPE_SECONDARY_SINK: Int
```

The device is a secondary sink. This type is only supported by R1. 

 Value: 2

### DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK: Int
```

The device is dual-role capable i.e. either a WFD source or a primary sink. 

 Value: 3

### DEVICE_TYPE_WFD_SOURCE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_TYPE_WFD_SOURCE: Int
```

The device is a Wifi Display Source. 

 Value: 0

### PREFERRED_CONNECTIVITY_P2P

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREFERRED_CONNECTIVITY_P2P: Int
```

Wifi Display (WFD) preferred connectivity is Wifi Direct (P2P). 

 Value: 0

### PREFERRED_CONNECTIVITY_TDLS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREFERRED_CONNECTIVITY_TDLS: Int
```

Wifi Display (WFD) preferred connectivity is TDLS. 

 Value: 1

## Public constructors

### WifiP2pWfdInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiP2pWfdInfo()
```

Default constructor. 

### WifiP2pWfdInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiP2pWfdInfo(source: WifiP2pWfdInfo?)
```

Copy constructor.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `source` | [WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#)?:This value may be`null`. |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getControlPort

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getControlPort(): Int
```

Returns the TCP port at which the WFD Device listens for RTSP messages. 

### getDeviceInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceInfo(): Int
```

Return R1 raw device info, See Wifi Display technical specification v1.0.0, section 5.1.2. Access bit fields by DEVICE_INFO_\* constants.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_SESSION_AVAILABLE_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_SESSION_AVAILABLE_MASK:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_CONTENT_PROTECTION_SUPPORT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_CONTENT_PROTECTION_SUPPORT:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_TDLS_PERSISTENT_GROUP](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_TDLS_PERSISTENT_GROUP:kotlin.Int), and [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE:kotlin.Int) |

### getDeviceType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceType(): Int
```

Get the type of the device. One of [DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int), [DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int), [DEVICE_TYPE_SECONDARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK:kotlin.Int), [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int)

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK:kotlin.Int), or [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int) |

### getMaxThroughput

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxThroughput(): Int
```

Returns the maximum average throughput capability of the WFD Device, in megabits/second. 

### getR2DeviceInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getR2DeviceInfo(): Int
```

Return R2 raw device info, See Wifi Display technical specification v2.0.0, section 5.1.12. Access bit fields by [DEVICE_INFO_DEVICE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK:kotlin.Int) |

### getR2DeviceType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getR2DeviceType(): Int
```

Get the type of the R2 device. One of [DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int), [DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int), or [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int)

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK:kotlin.Int), or [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int) |

### isContentProtectionSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isContentProtectionSupported(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if Content Protection using the HDCP system 2.0/2.1 is supported. |

### isCoupledSinkSupportedAtSink

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCoupledSinkSupportedAtSink(): Boolean
```

Returns true if Coupled Sink is supported by WFD Sink. See Wifi Display technical specification v1.0.0, section 4.9. 

### isCoupledSinkSupportedAtSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCoupledSinkSupportedAtSource(): Boolean
```

Returns true if Coupled Sink is supported by WFD Source. See Wifi Display technical specification v1.0.0, section 4.9. 

### isEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnabled(): Boolean
```

Returns true is Wifi Display is enabled, false otherwise. 

### isR2Supported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isR2Supported(): Boolean
```

Returns true is Wifi Display R2 is enabled, false otherwise. 

### isSessionAvailable

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSessionAvailable(): Boolean
```

Returns true if a session is available, false otherwise. 

### setContentProtectionSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setContentProtectionSupported(enabled: Boolean): Unit
```

Sets whether Content Protection using the HDCP system 2.0/2.1 is supported.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to indicate that Content Protection is supported, false otherwise. |

### setControlPort

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setControlPort(port: Int): Unit
```

Sets the TCP port at which the WFD Device listens for RTSP messages.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

### setCoupledSinkSupportAtSink

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCoupledSinkSupportAtSink(enabled: Boolean): Unit
```

Sets whether Coupled Sink feature is supported by WFD Sink. See Wifi Display technical specification v1.0.0, section 4.9.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to indicate support for coupled sink, false otherwise. |

### setCoupledSinkSupportAtSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCoupledSinkSupportAtSource(enabled: Boolean): Unit
```

Sets whether Coupled Sink feature is supported by WFD Source. See Wifi Display technical specification v1.0.0, section 4.9.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to indicate support for coupled sink, false otherwise. |

### setDeviceType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDeviceType(deviceType: Int): Boolean
```

Sets the type of the device.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int), [DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int), [DEVICE_TYPE_SECONDARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK:kotlin.Int), [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int) Value is [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK:kotlin.Int), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK:kotlin.Int), or [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device type was successfully set, false otherwise |

### setEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEnabled(enabled: Boolean): Unit
```

Sets whether Wifi Display should be enabled.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to enable Wifi Display, false to disable |

### setMaxThroughput

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMaxThroughput(maxThroughput: Int): Unit
```

Sets the maximum average throughput capability of the WFD Device, in megabits/second.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------|
| `maxThroughput` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

### setR2DeviceType

```
fun setR2DeviceType(deviceType: Int): Boolean
```

Sets the type of the Wifi Display R2 device. See Wifi Display technical specification v2.0.0, section 5.1.12 for Wifi Display R2. Before calling this API, call WifiManager#isWifiDisplayR2Supported() 

### setSessionAvailable

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSessionAvailable(enabled: Boolean): Unit
```

Sets whether a session is available.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to indicate that a session is available, false otherwise. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiP2pWfdInfo!>
```

Implement the Parcelable interface
