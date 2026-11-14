Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# Device

```
class Device
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.Device](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#) |

A physical device (such as phone, watch, scale, or chest strap) which captured associated health data point.

Device needs to be populated by users of the API. Metadata fields not provided by clients will remain absent.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device.Builder` <br /> |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_CHEST_STRAP:kotlin.Int` Wearable straps worn around the chest, primarily used for highly accurate heart rate monitoring during exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_CONSUMER_MEDICAL_DEVICE:kotlin.Int` Over-the-counter Medical devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_FITNESS_BAND:kotlin.Int` Wearable devices, typically worn on the wrist or arm, primarily focused on tracking physical activity and basic health metrics. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_FITNESS_EQUIPMENT:kotlin.Int` Tools and accessories designed for use during physical exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_FITNESS_MACHINE:kotlin.Int` Stationary or mobile equipment designed for physical exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_GLASSES:kotlin.Int` Wearable glasses with integrated technology and computing capabilities. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_HEAD_MOUNTED:kotlin.Int` Devices worn on the head, beyond glasses, designed for specific health or fitness applications, often involving sensing or stimulation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_HEARABLE:kotlin.Int` Electronic devices worn in or around the ears, often with audio capabilities. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_METER:kotlin.Int` Equipment attachments that measure a specific metric. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_PHONE:kotlin.Int` A handheld mobile computing and communication device, equipped with various sensors (e.g., accelerometer, GPS) that can collect health and fitness data, or serve as a primary interface for manual data entry or managing data from connected peripherals. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_PORTABLE_COMPUTER:kotlin.Int` A portable computer usually with GPS and performance tracking capabilities that is either handheld or attached to a device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_RING:kotlin.Int` Wearable devices worn on a finger, typically designed for discreet tracking of sleep, activity, and potentially other physiological data. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_SCALE:kotlin.Int` Devices designed to measure body weight and often other body composition metrics. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_SMART_DISPLAY:kotlin.Int` Stationary devices with a screen and connectivity, often used in homes or gyms to provide guided workouts, track progress, and offer health-related information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_UNKNOWN:kotlin.Int` A device whose specific type is not identified, not yet supported in the Health Connect list, or where the originating device type could not be determined by the data writer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_WATCH:kotlin.Int` A wearable computing device designed to be worn on the wrist, typically featuring an interactive display and offering a broad range of functionalities including, but not limited to, health and fitness tracking, app integration, and communication. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#getDisplayName()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#getManufacturer()()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#getModel()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#getType()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#getUdi()()` Returns the UDI (Unique Device Identifier), a unique numeric or alphanumeric code assigned to a medical device, of this `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#` instance. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#hashCode()()` Returns a hash code value for the object. |

## Constants

### DEVICE_TYPE_CHEST_STRAP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_CHEST_STRAP: Int
```

Wearable straps worn around the chest, primarily used for highly accurate heart rate monitoring during exercise.

 Value: 7

### DEVICE_TYPE_CONSUMER_MEDICAL_DEVICE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_CONSUMER_MEDICAL_DEVICE: Int
```

Over-the-counter Medical devices.

For example: CGM / Glucometers, Blood Pressure Cuff

 Value: 9

### DEVICE_TYPE_FITNESS_BAND

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_FITNESS_BAND: Int
```

Wearable devices, typically worn on the wrist or arm, primarily focused on tracking physical activity and basic health metrics.

 Value: 6

### DEVICE_TYPE_FITNESS_EQUIPMENT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_FITNESS_EQUIPMENT: Int
```

Tools and accessories designed for use during physical exercise.

For example: Dumbbells, Jump Ropes

 Value: 13

### DEVICE_TYPE_FITNESS_MACHINE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_FITNESS_MACHINE: Int
```

Stationary or mobile equipment designed for physical exercise.

For example: Treadmill, Indoor Cycles, Rowing Machines, Outdoor Bicycle. Outdoor Scooter

 Value: 12

### DEVICE_TYPE_GLASSES

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_GLASSES: Int
```

Wearable glasses with integrated technology and computing capabilities.

 Value: 10

### DEVICE_TYPE_HEAD_MOUNTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_HEAD_MOUNTED: Int
```

Devices worn on the head, beyond glasses, designed for specific health or fitness applications, often involving sensing or stimulation.

For example: VR/MR Headsets, ECG Head Bands

 Value: 5

### DEVICE_TYPE_HEARABLE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_HEARABLE: Int
```

Electronic devices worn in or around the ears, often with audio capabilities.

 Value: 11

### DEVICE_TYPE_METER

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_METER: Int
```

Equipment attachments that measure a specific metric.

For example: Pedal Meters, Insole Meters

 Value: 15

### DEVICE_TYPE_PHONE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_PHONE: Int
```

A handheld mobile computing and communication device, equipped with various sensors (e.g., accelerometer, GPS) that can collect health and fitness data, or serve as a primary interface for manual data entry or managing data from connected peripherals.

 Value: 2

### DEVICE_TYPE_PORTABLE_COMPUTER

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_PORTABLE_COMPUTER: Int
```

A portable computer usually with GPS and performance tracking capabilities that is either handheld or attached to a device.

For example: Handheld GPS, Cycling Computer, Rowing Computer

 Value: 14

### DEVICE_TYPE_RING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_RING: Int
```

Wearable devices worn on a finger, typically designed for discreet tracking of sleep, activity, and potentially other physiological data.

 Value: 4

### DEVICE_TYPE_SCALE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_SCALE: Int
```

Devices designed to measure body weight and often other body composition metrics.

 Value: 3

### DEVICE_TYPE_SMART_DISPLAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_SMART_DISPLAY: Int
```

Stationary devices with a screen and connectivity, often used in homes or gyms to provide guided workouts, track progress, and offer health-related information.

For example: Home Smart Displays, Interactive Fitness Mirrors

 Value: 8

### DEVICE_TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_UNKNOWN: Int
```

A device whose specific type is not identified, not yet supported in the Health Connect list, or where the originating device type could not be determined by the data writer.

 Value: 0

### DEVICE_TYPE_WATCH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DEVICE_TYPE_WATCH: Int
```

A wearable computing device designed to be worn on the wrist, typically featuring an interactive display and offering a broad range of functionalities including, but not limited to, health and fitness tracking, app integration, and communication.

 Value: 1

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getDisplayName

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
fun getDisplayName(): String?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The display name if set, null otherwise |

### getManufacturer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getManufacturer(): String?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The device manufacturer if set, null otherwise |

### getModel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getModel(): String?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The device model if set, null otherwise |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getType(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The device type if set `DEVICE_TYPE_UNKNOWN` otherwise. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_WATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_PHONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_SCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_RING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_HEAD_MOUNTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_FITNESS_BAND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_CHEST_STRAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_SMART_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_CONSUMER_MEDICAL_DEVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_GLASSES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_HEARABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_FITNESS_MACHINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_FITNESS_EQUIPMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_PORTABLE_COMPUTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#DEVICE_TYPE_METER:kotlin.Int` |

### getUdi

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getUdi(): String?
```

Returns the UDI (Unique Device Identifier), a unique numeric or alphanumeric code assigned to a medical device, of this `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Device#` instance.

The identifier is entirely "self-declared" by the device or app writing the data. Health Connect acts as a passive data store; it does not cross-reference this ID against the FDA's GUDID database or any other regulatory registry to ensure the device is legitimate. The presence of a UDI indicates that the data source is a Registered Medical Device. However, it does not guarantee specific FDA Clearance or Approval. Data Readers should use the UDI to query the GUDID database if they need to filter by Regulatory Class (I, II, or III) or intended use.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The device Unique Device Identifier (UDI) if set, null otherwise. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
