# WifiP2pDevice

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pDevice

Kotlin| [Java](WifiP2pDevice.md) 
| --- | --- |

```
open class WifiP2pDevice : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.WifiP2pDevice](WifiP2pDevice.md) |

A class representing a Wi-Fi p2p device Note that the operations are not thread safe {@see WifiP2pManager}

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABLE](WifiP2pDevice.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTED](WifiP2pDevice.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FAILED](WifiP2pDevice.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVITED](WifiP2pDevice.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNAVAILABLE](WifiP2pDevice.md) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiP2pDevice](WifiP2pDevice.md))`()` <br /> |
| [WifiP2pDevice](WifiP2pDevice.md))`(`source:` ` [WifiP2pDevice](WifiP2pDevice.md)!`)` copy constructor |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](WifiP2pDevice.md))`()` Implement the Parcelable interface |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](WifiP2pDevice.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [InetAddress](../java.net/InetAddress.md)? | [getIpAddress](WifiP2pDevice.md))`()` Get the IP address of the connected client device. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult.InformationElement](../android/net/wifi/ScanResult.InformationElement.md)!\> | [getVendorElements](WifiP2pDevice.md))`()` Get the vendor-specific information elements received as part of the discovery of the peer device. |
| open [WifiP2pWfdInfo](WifiP2pWfdInfo.md)? | [getWfdInfo](WifiP2pDevice.md))`()` The Wifi Display information for this device, or null if unavailable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](WifiP2pDevice.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGroupOwner](WifiP2pDevice.md))`()` Returns true if the device is a group owner |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpportunisticBootstrappingMethodSupported](WifiP2pDevice.md))`()` Returns true if opportunistic bootstrapping method is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassphraseDisplayBootstrappingMethodSupported](WifiP2pDevice.md))`()` Returns true if passphrase display bootstrapping method is supported. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassphraseKeypadBootstrappingMethodSupported](WifiP2pDevice.md))`()` Returns true if passphrase keypad bootstrapping method is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPinCodeDisplayBootstrappingMethodSupported](WifiP2pDevice.md))`()` Returns true if pin-code display bootstrapping method is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPinCodeKeypadBootstrappingMethodSupported](WifiP2pDevice.md))`()` Returns true if pin-code keypad bootstrapping method is supported. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isServiceDiscoveryCapable](WifiP2pDevice.md))`()` Returns true if the device is capable of service discovery |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](WifiP2pDevice.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](WifiP2pDevice.md))`(`device:` ` [WifiP2pDevice](WifiP2pDevice.md)`)` Update this device's details using another [WifiP2pDevice](WifiP2pDevice.md) instance. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wpsDisplaySupported](WifiP2pDevice.md))`()` Returns true if WPS display configuration is supported |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wpsKeypadSupported](WifiP2pDevice.md))`()` Returns true if WPS keypad configuration is supported |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wpsPbcSupported](WifiP2pDevice.md))`()` Returns true if WPS push button configuration is supported |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](WifiP2pDevice.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiP2pDevice](WifiP2pDevice.md)!\> | [CREATOR](WifiP2pDevice.md) Implement the Parcelable interface |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [deviceAddress](WifiP2pDevice.md) The device MAC address uniquely identifies a Wi-Fi p2p device |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [deviceName](WifiP2pDevice.md) The device name is a user friendly string to identify a Wi-Fi p2p device |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [primaryDeviceType](WifiP2pDevice.md) Primary device type identifies the type of device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [secondaryDeviceType](WifiP2pDevice.md) Secondary device type is an optional attribute that can be provided by a device in addition to the primary device type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [status](WifiP2pDevice.md) Device connection status |
| --- | --- |

## Constants

### AVAILABLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABLE: Int
```  

 Value: 3

### CONNECTED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTED: Int
```  

 Value: 0

### FAILED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FAILED: Int
```  

 Value: 2

### INVITED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVITED: Int
```  

 Value: 1

### UNAVAILABLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNAVAILABLE: Int
```  

 Value: 4

## Public constructors

### WifiP2pDevice

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiP2pDevice()
```  

### WifiP2pDevice

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiP2pDevice(source: WifiP2pDevice!)
```

copy constructor

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getIpAddress

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIpAddress(): InetAddress?
```

Get the IP address of the connected client device. The application should listen to [WifiP2pManager.WIFI_P2P_CONNECTION_CHANGED_ACTION](WifiP2pManager.md) broadcast to obtain the IP address of the connected client. When system assigns the IP address, the connected P2P device information ([WifiP2pGroup.getClientList()](WifiP2pGroup.md))) in the group is updated with the IP address and broadcast the group information using [WifiP2pManager.EXTRA_WIFI_P2P_GROUP](WifiP2pManager.md) extra of the [WifiP2pManager.WIFI_P2P_CONNECTION_CHANGED_ACTION](WifiP2pManager.md) broadcast intent. Alternatively, the application can request for the group details with [WifiP2pManager.requestGroupInfo](WifiP2pManager.md))and use ([WifiP2pGroup.getClientList()](WifiP2pGroup.md))) to obtain the connected client details.

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [InetAddress](../java.net/InetAddress.md)? | the IP address if the device is a part of the group; otherwise null. |

### getVendorElements

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVendorElements(): MutableList<ScanResult.InformationElement!>
```

Get the vendor-specific information elements received as part of the discovery of the peer device.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ScanResult.InformationElement](../android/net/wifi/ScanResult.InformationElement.md)!> | the list of vendor-specific information elements The information element format is defined in the IEEE 802.11-2016 spec Table 9-77. This value cannot be`null`. |

### getWfdInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWfdInfo(): WifiP2pWfdInfo?
```

The Wifi Display information for this device, or null if unavailable. 

### hashCode

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isGroupOwner

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isGroupOwner(): Boolean
```

Returns true if the device is a group owner 

### isOpportunisticBootstrappingMethodSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpportunisticBootstrappingMethodSupported(): Boolean
```

Returns true if opportunistic bootstrapping method is supported. Defined in Wi-Fi Alliance Wi-Fi Direct R2 Specification Table 10 - Bootstrapping Methods. 

### isPassphraseDisplayBootstrappingMethodSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPassphraseDisplayBootstrappingMethodSupported(): Boolean
```

Returns true if passphrase display bootstrapping method is supported. Defined in Wi-Fi Alliance Wi-Fi Direct R2 Specification Table 10 - Bootstrapping Methods. 

### isPassphraseKeypadBootstrappingMethodSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPassphraseKeypadBootstrappingMethodSupported(): Boolean
```

Returns true if passphrase keypad bootstrapping method is supported. Defined in Wi-Fi Alliance Wi-Fi Direct R2 Specification Table 10 - Bootstrapping Methods. 

### isPinCodeDisplayBootstrappingMethodSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPinCodeDisplayBootstrappingMethodSupported(): Boolean
```

Returns true if pin-code display bootstrapping method is supported. Defined in Wi-Fi Alliance Wi-Fi Direct R2 Specification Table 10 - Bootstrapping Methods. 

### isPinCodeKeypadBootstrappingMethodSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPinCodeKeypadBootstrappingMethodSupported(): Boolean
```

Returns true if pin-code keypad bootstrapping method is supported. Defined in Wi-Fi Alliance Wi-Fi Direct R2 Specification Table 10 - Bootstrapping Methods. 

### isServiceDiscoveryCapable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isServiceDiscoveryCapable(): Boolean
```

Returns true if the device is capable of service discovery 

### toString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### update

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(device: WifiP2pDevice): Unit
```

Update this device's details using another [WifiP2pDevice](WifiP2pDevice.md) instance. This will throw an exception if the device address does not match.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [WifiP2pDevice](WifiP2pDevice.md):another instance of [WifiP2pDevice](WifiP2pDevice.md) used to update this instance. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the device is null or the device address does not match |

### wpsDisplaySupported

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun wpsDisplaySupported(): Boolean
```

Returns true if WPS display configuration is supported 

### wpsKeypadSupported

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun wpsKeypadSupported(): Boolean
```

Returns true if WPS keypad configuration is supported 

### wpsPbcSupported

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun wpsPbcSupported(): Boolean
```

Returns true if WPS push button configuration is supported 

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiP2pDevice!>
```

Implement the Parcelable interface 

### deviceAddress

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var deviceAddress: String!
```

The device MAC address uniquely identifies a Wi-Fi p2p device 

### deviceName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var deviceName: String!
```

The device name is a user friendly string to identify a Wi-Fi p2p device 

### primaryDeviceType

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var primaryDeviceType: String!
```

Primary device type identifies the type of device. For example, an application could filter the devices discovered to only display printers if the purpose is to enable a printing action from the user. See the Wi-Fi Direct technical specification for the full list of standard device types supported. 

### secondaryDeviceType

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var secondaryDeviceType: String!
```

Secondary device type is an optional attribute that can be provided by a device in addition to the primary device type. 

### status

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var status: Int
```

Device connection status
