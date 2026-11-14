# WifiP2pWfdInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pWfdInfo

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pWfdInfo.md) 
| --- | --- |

```
class WifiP2pWfdInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.WifiP2pWfdInfo](../android/net/wifi/p2p/WifiP2pWfdInfo.md) |

A class representing Wifi Display information for a device. See Wifi Display technical specification v1.0.0, section 5.1.2. See Wifi Display technical specification v2.0.0, section 5.1.12 for Wifi Display R2.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate audo is only supported at source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate audio is not supported at primary sink. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_CONTENT_PROTECTION_SUPPORT](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate the support of Content Protection using the HDCP system 2. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicates that coupled sink is supporeted at sink. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicates that coupled sink is supported at source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_DEVICE_TYPE_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md))\& [DEVICE_INFO_DEVICE_TYPE_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) is one of [DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_SECONDARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) or [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate the preferred connectifity for Wifi Display. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_SESSION_AVAILABLE_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicates that Wifi Display session is available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_TDLS_PERSISTENT_GROUP](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate that TDLS persistent group is intended. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate that the request is for re-invocation of TDLS persistent group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate time synchronization using 802. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicates that Wifi Display discovery is supported. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) The device is a primary sink. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TYPE_SECONDARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) The device is a secondary sink. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) The device is dual-role capable i. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md) The device is a Wifi Display Source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREFERRED_CONNECTIVITY_P2P](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Wifi Display (WFD) preferred connectivity is Wifi Direct (P2P). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREFERRED_CONNECTIVITY_TDLS](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Wifi Display (WFD) preferred connectivity is TDLS. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiP2pWfdInfo](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Default constructor. |
| [WifiP2pWfdInfo](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`source:` ` [WifiP2pWfdInfo](../android/net/wifi/p2p/WifiP2pWfdInfo.md)?`)` Copy constructor. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Implement the Parcelable interface |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getControlPort](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Returns the TCP port at which the WFD Device listens for RTSP messages. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceInfo](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Return R1 raw device info, See Wifi Display technical specification v1. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceType](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Get the type of the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxThroughput](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Returns the maximum average throughput capability of the WFD Device, in megabits/second. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getR2DeviceInfo](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Return R2 raw device info, See Wifi Display technical specification v2. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getR2DeviceType](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Get the type of the R2 device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isContentProtectionSupported](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCoupledSinkSupportedAtSink](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Returns true if Coupled Sink is supported by WFD Sink. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCoupledSinkSupportedAtSource](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Returns true if Coupled Sink is supported by WFD Source. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Returns true is Wifi Display is enabled, false otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isR2Supported](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Returns true is Wifi Display R2 is enabled, false otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSessionAvailable](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` Returns true if a session is available, false otherwise. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentProtectionSupported](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Content Protection using the HDCP system 2. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlPort](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the TCP port at which the WFD Device listens for RTSP messages. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCoupledSinkSupportAtSink](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Coupled Sink feature is supported by WFD Sink. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCoupledSinkSupportAtSource](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Coupled Sink feature is supported by WFD Source. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setDeviceType](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`deviceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of the device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Wifi Display should be enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxThroughput](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`maxThroughput:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum average throughput capability of the WFD Device, in megabits/second. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setR2DeviceType](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`deviceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of the Wifi Display R2 device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSessionAvailable](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether a session is available. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/wifi/p2p/WifiP2pWfdInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiP2pWfdInfo](../android/net/wifi/p2p/WifiP2pWfdInfo.md)!\> | [CREATOR](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Implement the Parcelable interface |

## Constants

### DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate audo is only supported at source. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 2048

### DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate audio is not supported at primary sink. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 1024

### DEVICE_INFO_CONTENT_PROTECTION_SUPPORT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_CONTENT_PROTECTION_SUPPORT: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate the support of Content Protection using the HDCP system 2.0/2.1. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 256

### DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicates that coupled sink is supporeted at sink. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 8

### DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicates that coupled sink is supported at source. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 4

### DEVICE_INFO_DEVICE_TYPE_MASK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_DEVICE_TYPE_MASK: Int
```

[getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md))\& [DEVICE_INFO_DEVICE_TYPE_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) is one of [DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_SECONDARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) or [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md). The bit definition is listed in 5.1.2 WFD Device Information Subelement and 5.1.12 WFD R2 Device Information Subelement in Wifi Display Technical Specification. 

 Value: 3

### DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate the preferred connectifity for Wifi Display. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. The value is one of [PREFERRED_CONNECTIVITY_P2P](../android/net/wifi/p2p/WifiP2pWfdInfo.md) or [PREFERRED_CONNECTIVITY_TDLS](../android/net/wifi/p2p/WifiP2pWfdInfo.md). 

 Value: 128

### DEVICE_INFO_SESSION_AVAILABLE_MASK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_SESSION_AVAILABLE_MASK: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicates that Wifi Display session is available. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 48

### DEVICE_INFO_TDLS_PERSISTENT_GROUP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_TDLS_PERSISTENT_GROUP: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate that TDLS persistent group is intended. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 4096

### DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate that the request is for re-invocation of TDLS persistent group. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 8192

### DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicate time synchronization using 802.1AS is supported. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

 Value: 512

### DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT: Int
```

Bit field for [getDeviceInfo()](../android/net/wifi/p2p/WifiP2pWfdInfo.md)), indicates that Wifi Display discovery is supported. The bit definition is listed in 5.1.2 WFD Device Information Subelement in Wifi Display Technical Specification. 

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
| `source` | [WifiP2pWfdInfo](../android/net/wifi/p2p/WifiP2pWfdInfo.md)?:This value may be`null`. |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_COUPLED_SINK_SUPPORT_AT_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_SESSION_AVAILABLE_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_WFD_SERVICE_DISCOVERY_SUPPORT](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_PREFERRED_CONNECTIVITY_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_CONTENT_PROTECTION_SUPPORT](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_TIME_SYNCHRONIZATION_SUPPORT](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_AUDIO_UNSUPPORTED_AT_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_AUDIO_ONLY_SUPPORT_AT_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_TDLS_PERSISTENT_GROUP](../android/net/wifi/p2p/WifiP2pWfdInfo.md), and [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_TDLS_PERSISTENT_GROUP_REINVOKE](../android/net/wifi/p2p/WifiP2pWfdInfo.md) |

### getDeviceType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceType(): Int
```

Get the type of the device. One of [DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_SECONDARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md)

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), or [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) |

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

Return R2 raw device info, See Wifi Display technical specification v2.0.0, section 5.1.12. Access bit fields by [DEVICE_INFO_DEVICE_TYPE_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_INFO_DEVICE_TYPE_MASK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) |

### getR2DeviceType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getR2DeviceType(): Int
```

Get the type of the R2 device. One of [DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), or [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md)

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), or [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) |

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
| `deviceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_SECONDARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) Value is [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_WFD_SOURCE](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SECONDARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md), or [android.net.wifi.p2p.WifiP2pWfdInfo#DEVICE_TYPE_SOURCE_OR_PRIMARY_SINK](../android/net/wifi/p2p/WifiP2pWfdInfo.md) |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiP2pWfdInfo!>
```

Implement the Parcelable interface
