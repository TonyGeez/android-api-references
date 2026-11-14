Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApnSetting

```
open class ApnSetting : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.data.ApnSetting](../android/telephony/data/ApnSetting.md) |

An Access Point Name (APN) configuration for a carrier data connection.

The APN provides configuration to connect a cellular network device to an IP data network. A carrier uses the name, type and other configuration in an `APNSetting` to decide which IP address to assign, any security methods to apply, and how the device might be connected to private networks.

Use `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting.Builder` to create new instances.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting.Builder` Provides a convenient way to set the fields of a `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#` when creating a new instance. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#AUTH_TYPE_CHAP:kotlin.Int` Authentication type for CHAP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#AUTH_TYPE_NONE:kotlin.Int` Authentication is not required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#AUTH_TYPE_PAP:kotlin.Int` Authentication type for PAP. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#AUTH_TYPE_PAP_OR_CHAP:kotlin.Int` Authentication type for PAP or CHAP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#MVNO_TYPE_GID:kotlin.Int` MVNO type for group identifier level 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#MVNO_TYPE_ICCID:kotlin.Int` MVNO type for ICCID. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#MVNO_TYPE_IMSI:kotlin.Int` MVNO type for IMSI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#MVNO_TYPE_SPN:kotlin.Int` MVNO type for service provider name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IP:kotlin.Int` Internet protocol. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IPV4V6:kotlin.Int` Virtual PDP type introduced to handle dual IP stack UE capability. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IPV6:kotlin.Int` Internet protocol, version 6. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_NON_IP:kotlin.Int` Transfer of Non-IP data to external packet data network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_PPP:kotlin.Int` Point to point protocol. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_UNSTRUCTURED:kotlin.Int` Transfer of Unstructured data to the Data Network via N6. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_BIP:kotlin.Int` APN type for BIP. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_CBS:kotlin.Int` APN type for CBS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DEFAULT:kotlin.Int` APN type for default data traffic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DUN:kotlin.Int` APN type for DUN traffic. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_EMERGENCY:kotlin.Int` APN type for Emergency PDN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_ENTERPRISE:kotlin.Int` APN type for ENTERPRISE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_FOTA:kotlin.Int` APN type for accessing the carrier's FOTA portal, used for over the air updates. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_HIPRI:kotlin.Int` APN type for HiPri traffic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_IA:kotlin.Int` APN type for IA Initial Attach APN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_IMS:kotlin.Int` APN type for IMS. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MCX:kotlin.Int` APN type for MCX (Mission Critical Service) where X can be PTT/Video/Data |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MMS:kotlin.Int` APN type for MMS traffic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_OEM_PAID:kotlin.Int` APN type for OEM_PAID networks (Automotive PANS) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_OEM_PRIVATE:kotlin.Int` APN type for OEM_PRIVATE networks (Automotive PANS) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_RCS:kotlin.Int` APN type for RCS (Rich Communication Services). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_SUPL:kotlin.Int` APN type for SUPL assisted GPS. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_VSIM:kotlin.Int` APN type for VSIM. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_XCAP:kotlin.Int` APN type for XCAP. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getApnName()()` Returns the name of the APN. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getApnTypeBitmask()()` Returns the bitmask of APN types. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getAuthType()()` Returns the authentication type of the APN. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getCarrierId()()` Returns the carrier id for this APN. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getEntryName()()` Gets the human-readable name that describes the APN. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getId()()` Returns the unique database id for this entry. |
| open [InetAddress](../java/net/InetAddress.md)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getMmsProxyAddress()()` Gets the MMS proxy address configured for the APN. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getMmsProxyAddressAsString()()` Returns the MMS proxy address of the APN. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getMmsProxyPort()()` Returns the MMS proxy port of the APN. |
| open [Uri](../android/net/Uri.md)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getMmsc()()` Returns the MMSC Uri of the APN. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getMtuV4()()` Returns the default MTU (Maximum Transmission Unit) size in bytes of the IPv4 routes brought up by this APN setting. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getMtuV6()()` Returns the MTU size of the IPv6 mobile interface to which the APN connected. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getMvnoType()()` Returns the MVNO match type for this APN. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getNetworkTypeBitmask()()` Returns a bitmask describing the Radio Technologies (Network Types) which this APN may use. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getOperatorNumeric()()` Returns the numeric operator ID for the APN. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getPassword()()` Returns the APN password of the APN. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getProfileId()()` Returns the profile id to which the APN saved in modem. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getProtocol()()` Returns the protocol to use to connect to this APN. |
| open [InetAddress](../java/net/InetAddress.md)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getProxyAddress()()` Gets the HTTP proxy address configured for the APN. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getProxyAddressAsString()()` Returns the proxy address of the APN. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getProxyPort()()` Returns the proxy address of the APN. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getRoamingProtocol()()` Returns the protocol to use to connect to this APN while the device is roaming. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getUser()()` Returns the APN username of the APN. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#hashCode()()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#isAlwaysOn()()` Returns whether User Plane resources have to be activated during every transition from CM-IDLE mode to CM-CONNECTED state for this APN See 3GPP TS 23. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#isEnabled()()` Returns the current status of APN. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#isPersistent()()` Returns if the APN setting is persistent on the modem. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#toString()()` Returns the string representation of ApnSetting. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ApnSetting](../android/telephony/data/ApnSetting.md)!\> | `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### AUTH_TYPE_CHAP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_TYPE_CHAP: Int
```

Authentication type for CHAP.

 Value: 2

### AUTH_TYPE_NONE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_TYPE_NONE: Int
```

Authentication is not required.

 Value: 0

### AUTH_TYPE_PAP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_TYPE_PAP: Int
```

Authentication type for PAP.

 Value: 1

### AUTH_TYPE_PAP_OR_CHAP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_TYPE_PAP_OR_CHAP: Int
```

Authentication type for PAP or CHAP.

 Value: 3

### MVNO_TYPE_GID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MVNO_TYPE_GID: Int
```

MVNO type for group identifier level 1.

 Value: 2

### MVNO_TYPE_ICCID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MVNO_TYPE_ICCID: Int
```

MVNO type for ICCID.

 Value: 3

### MVNO_TYPE_IMSI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MVNO_TYPE_IMSI: Int
```

MVNO type for IMSI.

 Value: 1

### MVNO_TYPE_SPN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MVNO_TYPE_SPN: Int
```

MVNO type for service provider name.

 Value: 0

### PROTOCOL_IP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_IP: Int
```

Internet protocol.

 Value: 0

### PROTOCOL_IPV4V6

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_IPV4V6: Int
```

Virtual PDP type introduced to handle dual IP stack UE capability.

 Value: 2

### PROTOCOL_IPV6

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_IPV6: Int
```

Internet protocol, version 6.

 Value: 1

### PROTOCOL_NON_IP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_NON_IP: Int
```

Transfer of Non-IP data to external packet data network.

 Value: 4

### PROTOCOL_PPP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_PPP: Int
```

Point to point protocol.

 Value: 3

### PROTOCOL_UNSTRUCTURED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_UNSTRUCTURED: Int
```

Transfer of Unstructured data to the Data Network via N6.

 Value: 5

### TYPE_BIP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BIP: Int
```

APN type for BIP.

 Value: 8192

### TYPE_CBS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CBS: Int
```

APN type for CBS.

 Value: 128

### TYPE_DEFAULT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DEFAULT: Int
```

APN type for default data traffic.

 Value: 17

### TYPE_DUN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DUN: Int
```

APN type for DUN traffic.

 Value: 8

### TYPE_EMERGENCY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_EMERGENCY: Int
```

APN type for Emergency PDN. This is not an IA apn, but is used for access to carrier services in an emergency call situation.

 Value: 512

### TYPE_ENTERPRISE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ENTERPRISE: Int
```

APN type for ENTERPRISE.

 Value: 16384

### TYPE_FOTA

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FOTA: Int
```

APN type for accessing the carrier's FOTA portal, used for over the air updates.

 Value: 32

### TYPE_HIPRI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HIPRI: Int
```

APN type for HiPri traffic.

 Value: 16

### TYPE_IA

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_IA: Int
```

APN type for IA Initial Attach APN.

 Value: 256

### TYPE_IMS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_IMS: Int
```

APN type for IMS.

 Value: 64

### TYPE_MCX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MCX: Int
```

APN type for MCX (Mission Critical Service) where X can be PTT/Video/Data

 Value: 1024

### TYPE_MMS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MMS: Int
```

APN type for MMS traffic.

 Value: 2

### TYPE_OEM_PAID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_OEM_PAID: Int
```

APN type for OEM_PAID networks (Automotive PANS)

 Value: 65536

### TYPE_OEM_PRIVATE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_OEM_PRIVATE: Int
```

APN type for OEM_PRIVATE networks (Automotive PANS)

 Value: 131072

### TYPE_RCS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_RCS: Int
```

APN type for RCS (Rich Communication Services).

 Value: 32768

### TYPE_SUPL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SUPL: Int
```

APN type for SUPL assisted GPS.

 Value: 4

### TYPE_VSIM

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VSIM: Int
```

APN type for VSIM.

 Value: 4096

### TYPE_XCAP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_XCAP: Int
```

APN type for XCAP.

 Value: 2048

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getApnName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApnName(): String!
```

Returns the name of the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | APN name |

### getApnTypeBitmask

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApnTypeBitmask(): Int
```

Returns the bitmask of APN types.

Apn types are usage categories for an APN entry. One APN entry may support multiple APN types, eg, a single APN may service regular internet traffic ("default") as well as MMS-specific connections.

The bitmask of APN types is calculated from APN types defined in `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask describing the types of the APN. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_SUPL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_DUN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_HIPRI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_FOTA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_IMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_CBS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_IA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_EMERGENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_MCX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_XCAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_BIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_VSIM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_ENTERPRISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_RCS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_OEM_PAID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#TYPE_OEM_PRIVATE:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting.Builder#setApnTypeBitmask(kotlin.Int)`

### getAuthType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthType(): Int
```

Returns the authentication type of the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | authentication type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#AUTH_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#AUTH_TYPE_PAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#AUTH_TYPE_CHAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#AUTH_TYPE_PAP_OR_CHAP:kotlin.Int` |

### getCarrierId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCarrierId(): Int
```

Returns the carrier id for this APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the carrier id |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting.Builder#setCarrierId(kotlin.Int)`

### getEntryName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEntryName(): String!
```

Gets the human-readable name that describes the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the entry name for the APN |

### getId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): Int
```

Returns the unique database id for this entry.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the unique database id |

### getMmsProxyAddress

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMmsProxyAddress(): InetAddress!
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getMmsProxyAddressAsString()` instead.*

Gets the MMS proxy address configured for the APN. The MMS proxy address might be an IP address or hostname. This method returns `null` if system networking (typically DNS) isn't available to resolve a hostname value---values set as IP addresses don't have this restriction. This is a known problem and will be addressed in a future release.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!` | the MMS proxy address or `null` if DNS isn't available to resolve a hostname |

### getMmsProxyAddressAsString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMmsProxyAddressAsString(): String!
```

Returns the MMS proxy address of the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | MMS proxy address. |

### getMmsProxyPort

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMmsProxyPort(): Int
```

Returns the MMS proxy port of the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | MMS proxy port |

### getMmsc

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMmsc(): Uri!
```

Returns the MMSC Uri of the APN.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | MMSC Uri. |

### getMtuV4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMtuV4(): Int
```

Returns the default MTU (Maximum Transmission Unit) size in bytes of the IPv4 routes brought up by this APN setting. Note this value will only be used when MTU size is not provided in `DataCallResponse#getMtuV4()` during network bring up.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the MTU size in bytes of the route. |

### getMtuV6

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMtuV6(): Int
```

Returns the MTU size of the IPv6 mobile interface to which the APN connected. Note this value will only be used when MTU size is not provided in `DataCallResponse#getMtuV6()` during network bring up.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the MTU size in bytes of the route. |

### getMvnoType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMvnoType(): Int
```

Returns the MVNO match type for this APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the MVNO match type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#MVNO_TYPE_SPN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#MVNO_TYPE_IMSI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#MVNO_TYPE_GID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#MVNO_TYPE_ICCID:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting.Builder#setMvnoType(kotlin.Int)`

### getNetworkTypeBitmask

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkTypeBitmask(): Int
```

Returns a bitmask describing the Radio Technologies (Network Types) which this APN may use. NetworkType bitmask is calculated from NETWORK_TYPE defined in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#`. Examples of Network Types include `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_GPRS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#NETWORK_TYPE_EDGE:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask describing the Radio Technologies (Network Types) or 0 if it is undefined. |

### getOperatorNumeric

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOperatorNumeric(): String!
```

Returns the numeric operator ID for the APN. Numeric operator ID is defined as `https://developer.android.com/reference/kotlin/android/provider/Telephony.Carriers.html#MCC:kotlin.String` + `https://developer.android.com/reference/kotlin/android/provider/Telephony.Carriers.html#MNC:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the numeric operator ID |

### getPassword

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPassword(): String!
```

Returns the APN password of the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | APN password |

### getProfileId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProfileId(): Int
```

Returns the profile id to which the APN saved in modem.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the profile id of the APN |

### getProtocol

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProtocol(): Int
```

Returns the protocol to use to connect to this APN.

Protocol is one of the `PDP_type` values in TS 27.007 section 10.1.1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the protocol. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IPV6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IPV4V6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_PPP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_NON_IP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_UNSTRUCTURED:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting.Builder#setProtocol(kotlin.Int)`

### getProxyAddress

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProxyAddress(): InetAddress!
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#getProxyAddressAsString()` instead.*

Gets the HTTP proxy address configured for the APN. The proxy address might be an IP address or hostname. This method returns `null` if system networking (typically DNS) isn't available to resolve a hostname value---values set as IP addresses don't have this restriction. This is a known problem and will be addressed in a future release.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!` | the HTTP proxy address or `null` if DNS isn't available to resolve a hostname |

### getProxyAddressAsString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProxyAddressAsString(): String!
```

Returns the proxy address of the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | proxy address. |

### getProxyPort

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProxyPort(): Int
```

Returns the proxy address of the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | proxy address. |

### getRoamingProtocol

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRoamingProtocol(): Int
```

Returns the protocol to use to connect to this APN while the device is roaming.

Roaming protocol is one of the `PDP_type` values in TS 27.007 section 10.1.1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the roaming protocol. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IPV6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_IPV4V6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_PPP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_NON_IP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting#PROTOCOL_UNSTRUCTURED:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/data/ApnSetting.Builder#setRoamingProtocol(kotlin.Int)`

### getUser

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUser(): String!
```

Returns the APN username of the APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | APN username |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isAlwaysOn

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAlwaysOn(): Boolean
```

Returns whether User Plane resources have to be activated during every transition from CM-IDLE mode to CM-CONNECTED state for this APN See 3GPP TS 23.501 section 5.6.13

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the PDU session for this APN should always be on and false otherwise |

### isEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEnabled(): Boolean
```

Returns the current status of APN. `true` : enabled APN. `false` : disabled APN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the current status |

### isPersistent

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPersistent(): Boolean
```

Returns if the APN setting is persistent on the modem.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the APN setting is persistent on the modem. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns the string representation of ApnSetting. This method prints null for unset elements. The output doesn't contain password or user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ApnSetting!>
```
