# BluetoothHidDeviceAppQosSettings

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHidDeviceAppQosSettings

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothHidDeviceAppQosSettings "View this page in Java") 

```
class BluetoothHidDeviceAppQosSettings : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#) |

Represents the Quality of Service (QoS) settings for a Bluetooth HID Device application.

The BluetoothHidDevice framework will update the L2CAP QoS settings for the app during registration.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#MAX:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_BEST_EFFORT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#SERVICE_BEST_EFFORT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_GUARANTEED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#SERVICE_GUARANTEED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_NO_TRAFFIC](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#SERVICE_NO_TRAFFIC:kotlin.Int) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#BluetoothHidDeviceAppQosSettings(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`serviceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tokenRate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tokenBucketSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `peakBandwidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `latency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delayVariation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a BluetoothHidDeviceAppQosSettings object for the Bluetooth L2CAP channel. |

| Public methods ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDelayVariation](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#getDelayVariation())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLatency](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#getLatency())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPeakBandwidth](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#getPeakBandwidth())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getServiceType](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#getServiceType())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTokenBucketSize](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#getTokenBucketSize())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTokenRate](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#getTokenRate())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### MAX

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX: Int
```  

 Value: -1

### SERVICE_BEST_EFFORT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_BEST_EFFORT: Int
```  

 Value: 1

### SERVICE_GUARANTEED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_GUARANTEED: Int
```  

 Value: 2

### SERVICE_NO_TRAFFIC

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_NO_TRAFFIC: Int
```  

 Value: 0

## Public constructors

### BluetoothHidDeviceAppQosSettings

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BluetoothHidDeviceAppQosSettings(
    serviceType: Int, 
    tokenRate: Int, 
    tokenBucketSize: Int, 
    peakBandwidth: Int, 
    latency: Int, 
    delayVariation: Int)
```

Create a BluetoothHidDeviceAppQosSettings object for the Bluetooth L2CAP channel. The QoS Settings is optional. Please refer to Bluetooth HID Specification v1.1.1 Section 5.2 and Appendix D for parameters.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| `serviceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP service type, default = SERVICE_BEST_EFFORT |
| `tokenRate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP token rate, default = 0 |
| `tokenBucketSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP token bucket size, default = 0 |
| `peakBandwidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP peak bandwidth, default = 0 |
| `latency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP latency, default = MAX |
| `delayVariation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP delay variation, default = MAX |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDelayVariation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDelayVariation(): Int
```  

### getLatency

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLatency(): Int
```  

### getPeakBandwidth

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPeakBandwidth(): Int
```  

### getServiceType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceType(): Int
```  

### getTokenBucketSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTokenBucketSize(): Int
```  

### getTokenRate

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTokenRate(): Int
```  

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BluetoothHidDeviceAppQosSettings!>
```
