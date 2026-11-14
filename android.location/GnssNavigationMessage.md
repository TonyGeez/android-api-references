# GnssNavigationMessage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssNavigationMessage

Kotlin| [Java](../android/location/GnssNavigationMessage.md) 
| --- | --- |

```
class GnssNavigationMessage : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.GnssNavigationMessage](../android/location/GnssNavigationMessage.md) |

A class containing a GNSS satellite Navigation Message.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/location/GnssNavigationMessage.Callback.md) Used for receiving GNSS satellite Navigation Messages from the GNSS engine. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PARITY_PASSED](../android/location/GnssNavigationMessage.md) The Navigation Message was received without any parity error in its navigation words. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PARITY_REBUILT](../android/location/GnssNavigationMessage.md) The Navigation Message was received with words that failed parity check, but the receiver was able to correct those words. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_UNKNOWN](../android/location/GnssNavigationMessage.md) The Navigation Message Status is 'unknown'. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BDS_CNAV1](../android/location/GnssNavigationMessage.md) Beidou CNAV1 message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BDS_CNAV2](../android/location/GnssNavigationMessage.md) Beidou CNAV2 message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BDS_D1](../android/location/GnssNavigationMessage.md) Beidou D1 message contained in the structure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BDS_D2](../android/location/GnssNavigationMessage.md) Beidou D2 message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GAL_F](../android/location/GnssNavigationMessage.md) Galileo F/NAV message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GAL_I](../android/location/GnssNavigationMessage.md) Galileo I/NAV message contained in the structure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GLO_L1CA](../android/location/GnssNavigationMessage.md) Glonass L1 CA message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GPS_CNAV2](../android/location/GnssNavigationMessage.md) GPS CNAV-2 message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GPS_L1CA](../android/location/GnssNavigationMessage.md) GPS L1 C/A message contained in the structure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GPS_L2CNAV](../android/location/GnssNavigationMessage.md) GPS L2-CNAV message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GPS_L5CNAV](../android/location/GnssNavigationMessage.md) GPS L5-CNAV message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IRN_L1](../android/location/GnssNavigationMessage.md) NavIC L1 message contained in the structure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IRN_L5](../android/location/GnssNavigationMessage.md) NavIC L5 message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IRN_L5CA](../android/location/GnssNavigationMessage.md) NavIC L5 C/A message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_QZS_L1CA](../android/location/GnssNavigationMessage.md) QZSS L1 C/A message contained in the structure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SBS](../android/location/GnssNavigationMessage.md) SBAS message contained in the structure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNKNOWN](../android/location/GnssNavigationMessage.md) Message type unknown |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/location/GnssNavigationMessage.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getData](../android/location/GnssNavigationMessage.md))`()` Gets the data of the reported GNSS message. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMessageId](../android/location/GnssNavigationMessage.md))`()` Gets the Message identifier. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](../android/location/GnssNavigationMessage.md))`()` Gets the Status of the navigation message contained in the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubmessageId](../android/location/GnssNavigationMessage.md))`()` Gets the sub-message identifier, relevant to the [getType()](../android/location/GnssNavigationMessage.md))of the message. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSvid](../android/location/GnssNavigationMessage.md))`()` Gets the satellite ID. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/location/GnssNavigationMessage.md))`()` Gets the type of the navigation message contained in the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/location/GnssNavigationMessage.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/location/GnssNavigationMessage.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GnssNavigationMessage](../android/location/GnssNavigationMessage.md)!\> | [CREATOR](../android/location/GnssNavigationMessage.md) <br /> |

## Constants

### STATUS_PARITY_PASSED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PARITY_PASSED: Int
```

The Navigation Message was received without any parity error in its navigation words. 

 Value: 1

### STATUS_PARITY_REBUILT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PARITY_REBUILT: Int
```

The Navigation Message was received with words that failed parity check, but the receiver was able to correct those words. 

 Value: 2

### STATUS_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_UNKNOWN: Int
```

The Navigation Message Status is 'unknown'. 

 Value: 0

### TYPE_BDS_CNAV1

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BDS_CNAV1: Int
```

Beidou CNAV1 message contained in the structure. 

 Value: 1283

### TYPE_BDS_CNAV2

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BDS_CNAV2: Int
```

Beidou CNAV2 message contained in the structure. 

 Value: 1284

### TYPE_BDS_D1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BDS_D1: Int
```

Beidou D1 message contained in the structure. 

 Value: 1281

### TYPE_BDS_D2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BDS_D2: Int
```

Beidou D2 message contained in the structure. 

 Value: 1282

### TYPE_GAL_F

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GAL_F: Int
```

Galileo F/NAV message contained in the structure. 

 Value: 1538

### TYPE_GAL_I

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GAL_I: Int
```

Galileo I/NAV message contained in the structure. 

 Value: 1537

### TYPE_GLO_L1CA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GLO_L1CA: Int
```

Glonass L1 CA message contained in the structure. 

 Value: 769

### TYPE_GPS_CNAV2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GPS_CNAV2: Int
```

GPS CNAV-2 message contained in the structure. 

 Value: 260

### TYPE_GPS_L1CA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GPS_L1CA: Int
```

GPS L1 C/A message contained in the structure. 

 Value: 257

### TYPE_GPS_L2CNAV

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GPS_L2CNAV: Int
```

GPS L2-CNAV message contained in the structure. 

 Value: 258

### TYPE_GPS_L5CNAV

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GPS_L5CNAV: Int
```

GPS L5-CNAV message contained in the structure. 

 Value: 259

### TYPE_IRN_L1

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_IRN_L1: Int
```

NavIC L1 message contained in the structure. 

 Value: 1795

### TYPE_IRN_L5

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_IRN_L5: Int
```

NavIC L5 message contained in the structure. 

 Value: 1794

### TYPE_IRN_L5CA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_IRN_L5CA: Int
```

NavIC L5 C/A message contained in the structure. 

 Value: 1793

### TYPE_QZS_L1CA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_QZS_L1CA: Int
```

QZSS L1 C/A message contained in the structure. 

 Value: 1025

### TYPE_SBS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SBS: Int
```

SBAS message contained in the structure. 

 Value: 513

### TYPE_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: Int
```

Message type unknown 

 Value: 0

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): ByteArray
```

Gets the data of the reported GNSS message.

The bytes (or words) specified using big endian format (MSB first).

- For GPS L1 C/A, NavIC L5, Beidou D1 \& Beidou D2, each subframe contains 10 30-bit words. Each word (30 bits) should be fit into the last 30 bits in a 4-byte word (skip B31 and B32), with MSB first, for a total of 40 bytes, covering a time period of 6, 6, and 0.6 seconds, respectively.
- For Glonass L1 C/A, each string contains 85 data bits, including the checksum. These bits should be fit into 11 bytes, with MSB first (skip B86-B88), covering a time period of 2 seconds.
- For Galileo F/NAV, each word consists of 238-bit (sync \& tail symbols excluded). Each word should be fit into 30-bytes, with MSB first (skip B239, B240), covering a time period of 10 seconds.
- For Galileo I/NAV, each page contains 2 page parts, even and odd, with a total of 2x114 = 228 bits, (sync \& tail excluded) that should be fit into 29 bytes, with MSB first (skip B229-B232).
- For SBAS, each block consists of 250 data bits, that should be fit into 32 bytes. MSB first (skip B251-B256).
- For Beidou CNAV1, subframe #1 consists of 14 data bits, that should be fit into 2 bytes. MSB first (skip B15-B16). subframe #2 consists of 600 bits that should be fit into 75 bytes. subframe #3 consists of 264 data bits that should be fit into 33 bytes.
- For Beidou CNAV2, each subframe consists of 288 data bits, that should be fit into 36 bytes.
- For NavIC L1, subframe #1 consists of 9 data bits that should be fit into 2 bytes (skip B10-B16). subframe #2 consists of 600 bits that should be fit into 75 bytes. subframe #3 consists of 274 data bits that should be fit into 35 bytes (skip B275-B280).

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

### getMessageId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMessageId(): Int
```

Gets the Message identifier.

This provides an index to help with complete Navigation Message assembly. Similar identifiers within the data bits themselves often supplement this information, in ways even more specific to each message type; see the relevant satellite constellation ICDs for details.

- For GPS L1 C/A subframe 4 and 5, this value corresponds to the 'frame id' of the navigation message, in the range of 1-25 (Subframe 1, 2, 3 does not contain a 'frame id' and this value can be set to -1.)
- For Glonass L1 C/A, this refers to the frame ID, in the range of 1-5.
- For BeiDou D1, this refers to the frame number in the range of 1-24
- For Beidou D2, this refers to the frame number, in the range of 1-120
- For Galileo F/NAV nominal frame structure, this refers to the subframe number, in the range of 1-12
- For Galileo I/NAV nominal frame structure, this refers to the subframe number in the range of 1-24
- For SBAS and Beidou CNAV2, this is unused and can be set to -1.
- For QZSS L1 C/A subframe 4 and 5, this value corresponds to the 'frame id' of the navigation message, in the range of 1-25 (Subframe 1, 2, 3 does not contain a 'frame id' and this value can be set to -1.)
- For Beidou CNAV1 this refers to the page type number in the range of 1-63.
- For NavIC L5 subframe 3 and 4, this value corresponds to the Message Id of the navigation message, in the range of 1-63. (Subframe 1 and 2 does not contain a message type id and this value can be set to -1.)
- For NavIC L1 subframe 3, this value corresponds to the Message Id of the navigation message, in the range of 1-63. (Subframe 1 and 2 does not contain a message type id and this value can be set to -1.)

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between -1 and 120 inclusive |

### getStatus

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatus(): Int
```

Gets the Status of the navigation message contained in the object.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.GnssNavigationMessage#STATUS_UNKNOWN](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#STATUS_PARITY_PASSED](../android/location/GnssNavigationMessage.md), or [android.location.GnssNavigationMessage#STATUS_PARITY_REBUILT](../android/location/GnssNavigationMessage.md) |

### getSubmessageId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubmessageId(): Int
```

Gets the sub-message identifier, relevant to the [getType()](../android/location/GnssNavigationMessage.md))of the message.

- For GPS L1 C/A, BeiDou D1 \& BeiDou D2, the submessage id corresponds to the subframe number of the navigation message, in the range of 1-5.
- For Glonass L1 C/A, this refers to the String number, in the range from 1-15
- For Galileo F/NAV, this refers to the page type in the range 1-6
- For Galileo I/NAV, this refers to the word type in the range 1-10+
- For Galileo in particular, the type information embedded within the data bits may be even more useful in interpretation, than the nominal page and word types provided in this field.
- For SBAS, the submessage id corresponds to the message type, in the range 1-63.
- For Beidou CNAV1, the submessage id corresponds to the subframe number of the navigation message, in the range of 1-3.
- For Beidou CNAV2, the submessage id corresponds to the message type, in the range 1-63.
- For NavIC L5, the submessage id corresponds to the subframe number of the navigation message, in the range of 1-4.
- For NavIC L1, the submessage id corresponds to the subframe number of the navigation message, in the range of 1-3.

<br />

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 1 or greater |

### getSvid

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSvid(): Int
```

Gets the satellite ID.

Range varies by constellation. See definition at`GnssStatus#getSvid(int)`

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 1 and 200 inclusive |

### getType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Gets the type of the navigation message contained in the object.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.GnssNavigationMessage#TYPE_UNKNOWN](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_GPS_L1CA](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_GPS_L2CNAV](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_GPS_L5CNAV](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_GPS_CNAV2](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_SBS](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_GLO_L1CA](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_QZS_L1CA](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_BDS_D1](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_BDS_D2](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_BDS_CNAV1](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_BDS_CNAV2](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_GAL_I](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_GAL_F](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_IRN_L5CA](../android/location/GnssNavigationMessage.md), [android.location.GnssNavigationMessage#TYPE_IRN_L5](../android/location/GnssNavigationMessage.md), or [android.location.GnssNavigationMessage#TYPE_IRN_L1](../android/location/GnssNavigationMessage.md) |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GnssNavigationMessage!>
```
