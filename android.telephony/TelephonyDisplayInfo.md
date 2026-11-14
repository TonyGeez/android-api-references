# TelephonyDisplayInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TelephonyDisplayInfo

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyDisplayInfo "View this page in Java") 
| --- | --- |

```
class TelephonyDisplayInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#) |

TelephonyDisplayInfo contains telephony-related information used for display purposes only. This information is provided in accordance with carrier policy and branding preferences; it is not necessarily a precise or accurate representation of the current state and should be treated accordingly. To be notified of changes in TelephonyDisplayInfo, use android.telephony.TelephonyManager#registerTelephonyCallback with a [TelephonyCallback](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback) that implements [TelephonyCallback.DisplayInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DisplayInfoListener). Override the onDisplayInfoChanged() method to handle the broadcast.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OVERRIDE_NETWORK_TYPE_LTE_ADVANCED_PRO](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_LTE_ADVANCED_PRO:kotlin.Int) Override network type when the device is connected to advanced pro [TelephonyManager.NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int) cellular network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OVERRIDE_NETWORK_TYPE_LTE_CA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_LTE_CA:kotlin.Int) Override network type when the device is connected to [TelephonyManager.NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int) cellular network and is using carrier aggregation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OVERRIDE_NETWORK_TYPE_NONE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NONE:kotlin.Int) No override. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OVERRIDE_NETWORK_TYPE_NR_ADVANCED](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NR_ADVANCED:kotlin.Int) Override network type when the device is connected NR cellular network and the data rate is higher than the generic 5G date rate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OVERRIDE_NETWORK_TYPE_NR_NSA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NR_NSA:kotlin.Int) Override network type when the device is connected to [TelephonyManager.NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int) network and has E-UTRA-NR Dual Connectivity(EN-DC) capability or is currently connected to the secondary [TelephonyManager.NETWORK_TYPE_NR](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int) cellular network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OVERRIDE_NETWORK_TYPE_NR_NSA_MMWAVE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NR_NSA_MMWAVE:kotlin.Int) Override network type when the device is connected to [TelephonyManager.NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int) network and has E-UTRA-NR Dual Connectivity(EN-DC) capability or is currently connected to the secondary [TelephonyManager.NETWORK_TYPE_NR](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int) cellular network on millimeter wave bands. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkType](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#getNetworkType())`()` Get current packet-switching cellular network type. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOverrideNetworkType](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#getOverrideNetworkType())`()` Get the override network type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRoaming](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#isRoaming())`()` Get device is roaming or not. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### OVERRIDE_NETWORK_TYPE_LTE_ADVANCED_PRO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERRIDE_NETWORK_TYPE_LTE_ADVANCED_PRO: Int
```

Override network type when the device is connected to advanced pro [TelephonyManager.NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int) cellular network. 

 Value: 2

### OVERRIDE_NETWORK_TYPE_LTE_CA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERRIDE_NETWORK_TYPE_LTE_CA: Int
```

Override network type when the device is connected to [TelephonyManager.NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int) cellular network and is using carrier aggregation. 

 Value: 1

### OVERRIDE_NETWORK_TYPE_NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERRIDE_NETWORK_TYPE_NONE: Int
```

No override. [getNetworkType()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#getNetworkType())should be used for display network type. 

 Value: 0

### OVERRIDE_NETWORK_TYPE_NR_ADVANCED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERRIDE_NETWORK_TYPE_NR_ADVANCED: Int
```

Override network type when the device is connected NR cellular network and the data rate is higher than the generic 5G date rate. Including but not limited to

- The device is connected to the NR cellular network on millimeter wave bands.
- The device is connected to the specific network which the carrier is using proprietary means to provide a faster overall data connection than would be otherwise possible. This may include using other bands unique to the carrier, or carrier aggregation, for example.

One of the use case is that UX can show a different icon, for example, "5G+"

<br />

 Value: 5

### OVERRIDE_NETWORK_TYPE_NR_NSA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERRIDE_NETWORK_TYPE_NR_NSA: Int
```

Override network type when the device is connected to [TelephonyManager.NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int) network and has E-UTRA-NR Dual Connectivity(EN-DC) capability or is currently connected to the secondary [TelephonyManager.NETWORK_TYPE_NR](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int) cellular network. 

 Value: 3

### OVERRIDE_NETWORK_TYPE_NR_NSA_MMWAVE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERRIDE_NETWORK_TYPE_NR_NSA_MMWAVE: Int
```

**Deprecated:** *Use{@link #OVERRIDE_NETWORK_TYPE_NR_ADVANCED} instead.*

Override network type when the device is connected to [TelephonyManager.NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int) network and has E-UTRA-NR Dual Connectivity(EN-DC) capability or is currently connected to the secondary [TelephonyManager.NETWORK_TYPE_NR](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int) cellular network on millimeter wave bands. 

 Value: 4

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getNetworkType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkType(): Int
```

Get current packet-switching cellular network type. This is the actual network type the device is camped on.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The network type. Value is [android.telephony.TelephonyManager#NETWORK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_GPRS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EDGE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_UMTS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_CDMA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_0](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_A](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_1xRTT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSDPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSUPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_IDEN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_B](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EHRPD](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPAP](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_GSM](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_TD_SCDMA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int), or [android.telephony.TelephonyManager#NETWORK_TYPE_NR](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int) |

### getOverrideNetworkType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOverrideNetworkType(): Int
```

Get the override network type. Note the override network type is for market branding or visualization purposes only. It cannot be treated as the actual network type device is camped on.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The override network type. Value is [android.telephony.TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NONE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NONE:kotlin.Int), [android.telephony.TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_LTE_CA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_LTE_CA:kotlin.Int), [android.telephony.TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_LTE_ADVANCED_PRO](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_LTE_ADVANCED_PRO:kotlin.Int), [android.telephony.TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NR_NSA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NR_NSA:kotlin.Int), or [android.telephony.TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NR_ADVANCED](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#OVERRIDE_NETWORK_TYPE_NR_ADVANCED:kotlin.Int) |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isRoaming

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRoaming(): Boolean
```

Get device is roaming or not. Note the isRoaming is for market branding or visualization purposes only. It cannot be treated as the actual roaming device is camped on.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the device is registered on roaming network overridden by config. |

**See Also**

- [android.telephony.CarrierConfigManager#KEY_GSM_ROAMING_NETWORKS_STRING_ARRAY](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String)
- [android.telephony.CarrierConfigManager#KEY_GSM_NONROAMING_NETWORKS_STRING_ARRAY](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_NONROAMING_NETWORKS_STRING_ARRAY:kotlin.String)
- [android.telephony.CarrierConfigManager#KEY_CDMA_ROAMING_NETWORKS_STRING_ARRAY](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String)
- [android.telephony.CarrierConfigManager#KEY_CDMA_NONROAMING_NETWORKS_STRING_ARRAY](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_NONROAMING_NETWORKS_STRING_ARRAY:kotlin.String) 

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

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TelephonyDisplayInfo!>
```
