# BluetoothHidDeviceAppQosSettings

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHidDeviceAppQosSettings

Kotlin| [Java](BluetoothHidDeviceAppQosSettings.md) 
| --- | --- |

```
class BluetoothHidDeviceAppQosSettings : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHidDeviceAppQosSettings](BluetoothHidDeviceAppQosSettings.md) |

Represents the Quality of Service (QoS) settings for a Bluetooth HID Device application.

The BluetoothHidDevice framework will update the L2CAP QoS settings for the app during registration.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX](BluetoothHidDeviceAppQosSettings.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_BEST_EFFORT](BluetoothHidDeviceAppQosSettings.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_GUARANTEED](BluetoothHidDeviceAppQosSettings.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_NO_TRAFFIC](BluetoothHidDeviceAppQosSettings.md) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothHidDeviceAppQosSettings](BluetoothHidDeviceAppQosSettings.md))`(`serviceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tokenRate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tokenBucketSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `peakBandwidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `latency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delayVariation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a BluetoothHidDeviceAppQosSettings object for the Bluetooth L2CAP channel. |

| Public methods ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](BluetoothHidDeviceAppQosSettings.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDelayVariation](BluetoothHidDeviceAppQosSettings.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLatency](BluetoothHidDeviceAppQosSettings.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPeakBandwidth](BluetoothHidDeviceAppQosSettings.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getServiceType](BluetoothHidDeviceAppQosSettings.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTokenBucketSize](BluetoothHidDeviceAppQosSettings.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTokenRate](BluetoothHidDeviceAppQosSettings.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](BluetoothHidDeviceAppQosSettings.md))`(`out:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BluetoothHidDeviceAppQosSettings](BluetoothHidDeviceAppQosSettings.md)!\> | [CREATOR](BluetoothHidDeviceAppQosSettings.md) <br /> |

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
| --- | --- |
| `peakBandwidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP peak bandwidth, default = 0 |
| `latency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP latency, default = MAX |
| `delayVariation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):L2CAP delay variation, default = MAX |
| --- | --- |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BluetoothHidDeviceAppQosSettings!>
```
