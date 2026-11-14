# WifiP2pDevice

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pDevice

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pDevice "View this page in Java") 

```
open class WifiP2pDevice : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.p2p.WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#) |

A class representing a Wi-Fi p2p device Note that the operations are not thread safe {@see WifiP2pManager}

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABLE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#AVAILABLE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#CONNECTED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FAILED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#FAILED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVITED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#INVITED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#UNAVAILABLE:kotlin.Int) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#WifiP2pDevice())`()` <br /> |
| [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#WifiP2pDevice(android.net.wifi.p2p.WifiP2pDevice))`(`source:` ` [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#)!`)` copy constructor |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#describeContents())`()` Implement the Parcelable interface |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)? | [getIpAddress](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#getIpAddress())`()` Get the IP address of the connected client device. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult.InformationElement](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.InformationElement.html#)!\> | [getVendorElements](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#getVendorElements())`()` Get the vendor-specific information elements received as part of the discovery of the peer device. |
| open [WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo)? | [getWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#getWfdInfo())`()` The Wifi Display information for this device, or null if unavailable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#hashCode())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGroupOwner](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#isGroupOwner())`()` Returns true if the device is a group owner |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpportunisticBootstrappingMethodSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#isOpportunisticBootstrappingMethodSupported())`()` Returns true if opportunistic bootstrapping method is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassphraseDisplayBootstrappingMethodSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#isPassphraseDisplayBootstrappingMethodSupported())`()` Returns true if passphrase display bootstrapping method is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassphraseKeypadBootstrappingMethodSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#isPassphraseKeypadBootstrappingMethodSupported())`()` Returns true if passphrase keypad bootstrapping method is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPinCodeDisplayBootstrappingMethodSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#isPinCodeDisplayBootstrappingMethodSupported())`()` Returns true if pin-code display bootstrapping method is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPinCodeKeypadBootstrappingMethodSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#isPinCodeKeypadBootstrappingMethodSupported())`()` Returns true if pin-code keypad bootstrapping method is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isServiceDiscoveryCapable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#isServiceDiscoveryCapable())`()` Returns true if the device is capable of service discovery |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#update(android.net.wifi.p2p.WifiP2pDevice))`(`device:` ` [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#)`)` Update this device's details using another [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#) instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wpsDisplaySupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#wpsDisplaySupported())`()` Returns true if WPS display configuration is supported |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wpsKeypadSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#wpsKeypadSupported())`()` Returns true if WPS keypad configuration is supported |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wpsPbcSupported](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#wpsPbcSupported())`()` Returns true if WPS push button configuration is supported |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [deviceAddress](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#deviceAddress:kotlin.String) The device MAC address uniquely identifies a Wi-Fi p2p device |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [deviceName](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#deviceName:kotlin.String) The device name is a user friendly string to identify a Wi-Fi p2p device |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [primaryDeviceType](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#primaryDeviceType:kotlin.String) Primary device type identifies the type of device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [secondaryDeviceType](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#secondaryDeviceType:kotlin.String) Secondary device type is an optional attribute that can be provided by a device in addition to the primary device type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [status](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#status:kotlin.Int) Device connection status |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Get the IP address of the connected client device. The application should listen to [WifiP2pManager.WIFI_P2P_CONNECTION_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_CONNECTION_CHANGED_ACTION:kotlin.String) broadcast to obtain the IP address of the connected client. When system assigns the IP address, the connected P2P device information ([WifiP2pGroup.getClientList()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getClientList())) in the group is updated with the IP address and broadcast the group information using [WifiP2pManager.EXTRA_WIFI_P2P_GROUP](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_GROUP:kotlin.String) extra of the [WifiP2pManager.WIFI_P2P_CONNECTION_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_CONNECTION_CHANGED_ACTION:kotlin.String) broadcast intent. Alternatively, the application can request for the group details with [WifiP2pManager.requestGroupInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestGroupInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.GroupInfoListener))and use ([WifiP2pGroup.getClientList()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getClientList())) to obtain the connected client details.

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)? | the IP address if the device is a part of the group; otherwise null. |

### getVendorElements

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVendorElements(): MutableList<ScanResult.InformationElement!>
```

Get the vendor-specific information elements received as part of the discovery of the peer device.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ScanResult.InformationElement](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.InformationElement.html#)!> | the list of vendor-specific information elements The information element format is defined in the IEEE 802.11-2016 spec Table 9-77. This value cannot be`null`. |

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

Update this device's details using another [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#) instance. This will throw an exception if the device address does not match.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#):another instance of [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#) used to update this instance. This value cannot be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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
