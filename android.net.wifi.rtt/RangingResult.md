Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingResult

```
class RangingResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.rtt.RangingResult](RangingResult.md) |

Ranging result for a request started by `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/WifiRttManager#startRanging(android.net.wifi.rtt.RangingRequest,%20java.util.concurrent.Executor,%20android.net.wifi.rtt.RangingResultCallback)`. Results are returned in `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResultCallback#onRangingResults(kotlin.collections.MutableList)`.

A ranging result is the distance measurement result for a single device specified in the `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingRequest`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult.Builder` Builder class used to construct `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#` objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_BUSY_TRY_LATER:kotlin.Int` Individual range request status, `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_FAIL:kotlin.Int` Individual range request status, `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_RESPONDER_DOES_NOT_SUPPORT_IEEE80211MC:kotlin.Int` Individual range request status, `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int` Individual range request status, `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#UNSPECIFIED:kotlin.Int` The unspecified value. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#get80211azInitiatorTxLtfRepetitionsCount()()` Gets LTF repetitions that the initiator station (ISTA) used in the preamble of the initiator to responder (I2R) null data PPDU (NDP) for this result. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#get80211azNumberOfRxSpatialStreams()()` Gets number of receive spatial streams that the initiator station (ISTA) used for the initiator to responder (I2R) null data PPDU (NDP) for this result. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#get80211azNumberOfTxSpatialStreams()()` Gets number of transmit spatial streams that the initiator station (ISTA) used for the initiator to responder (I2R) null data PPDU (NDP) for this result. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#get80211azResponderTxLtfRepetitionsCount()()` Gets LTF repetitions that the responder station (RSTA) used in the preamble of the responder to initiator (I2R) null data PPDU (NDP) for this result. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getAvailabilityWindowDurationMillis()()` Gets availability window between measurements in milliseconds for proximity detection measurements. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getDistanceMm()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getDistanceStdDevMm()()` <br /> |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getLci()()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getLcr()()` <br /> |
| [MacAddress](../android.net/MacAddress.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getMacAddress()()` <br /> |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getMaxTimeBetweenNtbMeasurementsMicros()()` Gets maximum time between measurements in microseconds for IEEE 802. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getMeasurementBandwidth()()` The bandwidth used to transmit the RTT measurement frame. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getMeasurementChannelFrequencyMHz()()` The center frequency of the primary 20 MHz frequency (in MHz) of the channel over which the measurement frames are sent. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getMinTimeBetweenNtbMeasurementsMicros()()` Gets minimum time between measurements in microseconds for IEEE 802. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getNominalTimeMillis()()` Get the nominal duration between adjacent availability window in milliseconds for proximity detection measurements. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getNumAttemptedMeasurements()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getNumNtbRepetitionsPerMeasurement()()` Get the number of range repetitions carried out for distance calculation in Non Trigger Based (NTB) ranging. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getNumSuccessfulMeasurements()()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getPasnComebackAfterMillis()()` Get Comeback after time in milliseconds. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getPasnComebackCookie()()` Get PASN comeback cookie. |
| [PeerHandle](../android.net.wifi.aware/PeerHandle.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getPeerHandle()()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getRangingTimestampMillis()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getRetryAfterDurationMillis()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getRssi()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getSecureHeLtfProtocolVersion()()` Get Secure HE-LTF protocol version used. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()()` <br /> |
| [ResponderLocation](ResponderLocation.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getUnverifiedResponderLocation()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getUsdPeerId()()` Returns the USD peer identifier of the device whose range measurement was requested. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#is80211azNtbMeasurement()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#is80211mcMeasurement()()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#isLmrDelayed()()` Returns whether the Location Measurement Report (LMR) feedback is delayed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#isRangingAuthenticated()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#isRangingFrameProtected()()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#isSecureHeLtfEnabled()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RangingResult](RangingResult.md)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### STATUS_BUSY_TRY_LATER

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_BUSY_TRY_LATER: Int
```

Individual range request status, `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()`. Indicates that the ranging operation failed because the peer is busy and unable to handle the request at this time. The requester should try again after a suggested delay, which can be retrieved with `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getRetryAfterDurationMillis()`.

 Value: 12

### STATUS_FAIL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_FAIL: Int
```

Individual range request status, `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()`. Indicates ranging operation failed and the distance value is invalid.

 Value: 1

### STATUS_RESPONDER_DOES_NOT_SUPPORT_IEEE80211MC

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_RESPONDER_DOES_NOT_SUPPORT_IEEE80211MC: Int
```

Individual range request status, `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()`. Indicates that the ranging operation failed because the specified peer does not support IEEE 802.11mc RTT operations. Support by an Access Point can be confirmed using `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#is80211mcResponder()`.

On such a failure, the individual result fields of `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#` such as `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getDistanceMm()` are invalid.

 Value: 2

### STATUS_SUCCESS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUCCESS: Int
```

Individual range request status, `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()`. Indicates ranging operation was successful and distance value is valid.

 Value: 0

### UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNSPECIFIED: Int
```

The unspecified value.

 Value: -1

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
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

### get80211azInitiatorTxLtfRepetitionsCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get80211azInitiatorTxLtfRepetitionsCount(): Int
```

Gets LTF repetitions that the initiator station (ISTA) used in the preamble of the initiator to responder (I2R) null data PPDU (NDP) for this result. LTF repetitions is the multiple transmissions of HE-LTF symbols in an HE ranging NDP. An HE-LTF repetition value of 1 indicates no repetitions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | LTF repetitions count |

### get80211azNumberOfRxSpatialStreams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get80211azNumberOfRxSpatialStreams(): Int
```

Gets number of receive spatial streams that the initiator station (ISTA) used for the initiator to responder (I2R) null data PPDU (NDP) for this result.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Number of spatial streams |

### get80211azNumberOfTxSpatialStreams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get80211azNumberOfTxSpatialStreams(): Int
```

Gets number of transmit spatial streams that the initiator station (ISTA) used for the initiator to responder (I2R) null data PPDU (NDP) for this result.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Number of spatial streams |

### get80211azResponderTxLtfRepetitionsCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get80211azResponderTxLtfRepetitionsCount(): Int
```

Gets LTF repetitions that the responder station (RSTA) used in the preamble of the responder to initiator (I2R) null data PPDU (NDP) for this result. LTF repetitions is the multiple transmissions of HE-LTF symbols in an HE ranging NDP. An HE-LTF repetition value of 1 indicates no repetitions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | LTF repetitions count |

### getAvailabilityWindowDurationMillis

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailabilityWindowDurationMillis(): Long
```

Gets availability window between measurements in milliseconds for proximity detection measurements. P2P Proximity Ranging uses two additional time parameters to coordinate availability duration called Availability Windows (AW). These are the Nominal Time and AW Duration that coordinate the time window period, and the start time of the time window period respectively. During AWs the ISTA and RSTA devices shall be available to exchange N successful FTM measurements instances where N equal the negotiated Meas Per AW. The ISTA indicates its preference for an AW duration and nominal time interval in the P2P Proximity Ranging Availability subelement, and the RSTA assigns the values used during the FTM session. The start of an AW duration is Nominal Time from the 1st successful measurement instance of the previous AW. The 1st AW occurs Nominal Time from the beginning of the 1st measurement instance following the initial FTM negotiation.

### getDistanceMm

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDistanceMm(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The distance (in mm) to the device specified by `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getMacAddress()` or `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getPeerHandle()`. Note: the measured distance may be negative for very close devices. Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. |

### getDistanceStdDevMm

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDistanceStdDevMm(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The standard deviation of the measured distance (in mm) to the device specified by `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getMacAddress()` or `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getPeerHandle()`. The standard deviation is calculated over the measurements executed in a single RTT burst. The number of measurements is returned by `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getNumSuccessfulMeasurements()` - 0 successful measurements indicate that the standard deviation is not valid (a valid standard deviation requires at least 2 data points). Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. |

### getLci

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLci(): ByteArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | The Location Configuration Information (LCI) as self-reported by the peer. The format is specified in the IEEE 802.11-2016 specifications, section 9.4.2.22.10. Note: the information is NOT validated - use with caution. Consider validating it with other sources of information before using it. This value cannot be `null`. |

### getLcr

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLcr(): ByteArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | The Location Civic report (LCR) as self-reported by the peer. The format is specified in the IEEE 802.11-2016 specifications, section 9.4.2.22.13. Note: the information is NOT validated - use with caution. Consider validating it with other sources of information before using it. This value cannot be `null`. |

### getMacAddress

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMacAddress(): MacAddress?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/MacAddress.html#?` | The MAC address of the device whose range measurement was requested. Will correspond to the MAC address of the device in the `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingRequest`. Will return a `null` for results corresponding to requests issued using a `PeerHandle`, i.e. using the `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingRequest.Builder#addWifiAwarePeer(android.net.wifi.aware.PeerHandle)` API. |

### getMaxTimeBetweenNtbMeasurementsMicros

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxTimeBetweenNtbMeasurementsMicros(): Long
```

Gets maximum time between measurements in microseconds for IEEE 802.11az non-trigger based ranging. The next 11az ranging request needs to be invoked before the maximum time from the last measurement time `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getRangingTimestampMillis()`. Otherwise, the non-trigger based ranging session will be terminated and a new ranging negotiation will happen with the responding station.

### getMeasurementBandwidth

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMeasurementBandwidth(): Int
```

The bandwidth used to transmit the RTT measurement frame.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_20MHZ:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_40MHZ:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_160MHZ:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#` or `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#` if available, otherwise `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#UNSPECIFIED:kotlin.Int` is returned. . Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_20MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_40MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_160MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ_PLUS_MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_320MHZ:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` does not return `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`. |

### getMeasurementChannelFrequencyMHz

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMeasurementChannelFrequencyMHz(): Int
```

The center frequency of the primary 20 MHz frequency (in MHz) of the channel over which the measurement frames are sent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | center frequency in Mhz of the channel if available, otherwise `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#UNSPECIFIED:kotlin.Int` is returned. <br /> |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` does not return `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`. |

### getMinTimeBetweenNtbMeasurementsMicros

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinTimeBetweenNtbMeasurementsMicros(): Long
```

Gets minimum time between measurements in microseconds for IEEE 802.11az non-trigger based ranging. The next 11az ranging measurement request must be invoked after the minimum time from the last measurement time `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getRangingTimestampMillis()` for the peer. Otherwise, cached ranging result will be returned for the peer.

### getNominalTimeMillis

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNominalTimeMillis(): Long
```

Get the nominal duration between adjacent availability window in milliseconds for proximity detection measurements.

### getNumAttemptedMeasurements

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumAttemptedMeasurements(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of attempted measurements used in the RTT exchange resulting in this set of results. The number of successful measurements is returned by `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getNumSuccessfulMeasurements()` which at most, if there are no errors, will be 1 less than the number of attempted measurements. Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. If the value is 0, it should be interpreted as no information available, which may occur for one-sided RTT measurements. Instead `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingRequest#getRttBurstSize()` should be used instead. |

### getNumNtbRepetitionsPerMeasurement

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumNtbRepetitionsPerMeasurement(): Int
```

Get the number of range repetitions carried out for distance calculation in Non Trigger Based (NTB) ranging. Note: Only applicable for IEEE 802.11az result.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of repetitions. |

### getNumSuccessfulMeasurements

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumSuccessfulMeasurements(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of successful measurements used to calculate the distance and standard deviation. If the number of successful measurements if 1 then then standard deviation, returned by `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getDistanceStdDevMm()`, is not valid (a 0 is returned for the standard deviation). The total number of measurement attempts is returned by `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getNumAttemptedMeasurements()`. The number of successful measurements will be at most 1 less then the number of attempted measurements. Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. |

### getPasnComebackAfterMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPasnComebackAfterMillis(): Long
```

Get Comeback after time in milliseconds. See `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getPasnComebackCookie()`. A value 0 indicates the ranging request operation can be tried immediately with the cookie.

### getPasnComebackCookie

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPasnComebackCookie(): ByteArray?
```

Get PASN comeback cookie. PASN authentication allows an AP to indicate the deferral time and optionally a Cookie. See `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getPasnComebackAfterMillis()`

When an AP receives a large volume of initial PASN Authentication frames, it can use the comeback after field in the PASN Parameters element to indicate a deferral time and optionally provide a comeback cookie which is an opaque sequence of octets. Upon receiving this response, the ranging initiator (STA) must wait for the specified time before retrying secure authentication, presenting the received cookie to the AP.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | This value may be `null`. |

### getPeerHandle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPeerHandle(): PeerHandle?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle.html#?` | The PeerHandle of the device whose range measurement was requested. Will correspond to the PeerHandle of the devices requested using `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingRequest.Builder#addWifiAwarePeer(android.net.wifi.aware.PeerHandle)`. Will return a `null` for results corresponding to requests issued using a MAC address. |

### getRangingTimestampMillis

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRangingTimestampMillis(): Long
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The timestamp at which the ranging operation was performed. The timestamp is in milliseconds since boot, including time spent in sleep, corresponding to values provided by `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()`. Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. |

### getRetryAfterDurationMillis

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRetryAfterDurationMillis(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The duration in milliseconds after which the ranging operation may be retried. A value of 0 means an immediate retry, otherwise retry after that much time in millisec. The time offset is from the measurement time `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getRangingTimestampMillis()`. . Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` does not return `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_BUSY_TRY_LATER:kotlin.Int`. |

### getRssi

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRssi(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The average RSSI, in units of dBm, observed during the RTT measurement. Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. |

### getSecureHeLtfProtocolVersion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSecureHeLtfProtocolVersion(): Int
```

Get Secure HE-LTF protocol version used. The secure HE-LTF negotiation supports negotiation of the secure HE-LTF protocol version which allows a responder and an initiator to negotiate the highest mutually supported secure HE-LTF protocol version. Refer IEEE 802.11az-2022 spec, section 9.4.2.298 Ranging Parameters element.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 0 and 7 inclusive |

### getStatus

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStatus(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The status of ranging measurement: `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int` in case of success, and `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_FAIL:kotlin.Int` in case of failure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_FAIL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_RESPONDER_DOES_NOT_SUPPORT_IEEE80211MC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_BUSY_TRY_LATER:kotlin.Int` |

### getUnverifiedResponderLocation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUnverifiedResponderLocation(): ResponderLocation?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation?` | The unverified responder location represented as `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation` which captures location information the responder is programmed to broadcast. The responder location is referred to as unverified, because we are relying on the device/site administrator to correctly configure its location data. Will return a `null` when the location information cannot be parsed. Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. |

### getUsdPeerId

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUsdPeerId(): Int
```

Returns the USD peer identifier of the device whose range measurement was requested.

This value is non-negative if the responder is a USD peer and the range request was placed using android.net.wifi.rtt.RangingRequest.Builder#addWifiUsdPeer(DiscoveryResult,android.net.wifi.rtt.ProximityDetectionConfig,android.net.wifi.rtt.SecureRangingConfig). The peer ID is an opaque identifier for a specific USD peer discovered during USD discovery operations and obtained from the DiscoveryResult#getPeerId()

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Will return a positive peer ID for results corresponding to requests issued using a USD peer ID, otherwise `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#UNSPECIFIED:kotlin.Int` is returned. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### is80211azNtbMeasurement

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun is80211azNtbMeasurement(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The result is true if the IEEE 802.11az non-trigger based protocol was used. If the result is false, and `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#is80211mcMeasurement()` is also false a one-side RTT result is provided which does not subtract the turnaround time at the responder. . Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. |

### is80211mcMeasurement

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun is80211mcMeasurement(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The result is true if the IEEE 802.11mc protocol was used. If the result is false, and `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#is80211azNtbMeasurement()` is also false a one-side RTT result is provided which does not subtract the turnaround time at the responder. Only valid if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#getStatus()` returns `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResult#STATUS_SUCCESS:kotlin.Int`, otherwise will throw an exception. |

### isLmrDelayed

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLmrDelayed(): Boolean
```

Returns whether the Location Measurement Report (LMR) feedback is delayed. Note: Only applicable for IEEE 802.11az result.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if LMR is delayed, `false` otherwise. |

### isRangingAuthenticated

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRangingAuthenticated(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the ranging is authenticated or not. Refer IEEE 802.11az-2022 spec, section 12 Security. |

### isRangingFrameProtected

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRangingFrameProtected(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the ranging frames are protected or not. Refer IEEE 802.11az-2022 spec, section 12 Security. |

### isSecureHeLtfEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSecureHeLtfEnabled(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the secure HE-LTF is enabled or not. Refer IEEE 802.11az-2022 spec, section 9.4.2.298 Ranging Parameters element. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<RangingResult!>
```
