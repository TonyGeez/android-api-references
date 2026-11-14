Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IpSecTransformState

Kotlin | [Java](IpSecTransformState.md)
| --- | --- |

```
class IpSecTransformState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.IpSecTransformState](IpSecTransformState.md) |

This class represents a snapshot of the state of an IpSecTransform

This class provides the current state of an IpSecTransform, enabling link metric analysis by the caller. Use cases include understanding transform usage, such as packet and byte counts, as well as observing out-of-order delivery by checking the bitmap. Additionally, callers can query IpSecTransformStates at two timestamps. By comparing the changes in packet counts and sequence numbers, callers can estimate IPsec data loss in the inbound direction.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/IpSecTransformState.Builder` Builder class for testing purposes |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getByteCount Retrieve the number of bytes processed so far as an unsigned long |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getPacketCount Retrieve the number of packets processed so far as an unsigned long. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | getReplayBitmap Retrieve the replay bitmap |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getRxHighestSequenceNumber Retrieve the highest sequence number received so far as an unsigned long |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getTimestampMillis Retrieve the timestamp (milliseconds) when this state was created, as per elapsedRealtime |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getTxHighestSequenceNumber Retrieve the highest sequence number sent so far as an unsigned long |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [IpSecTransformState](IpSecTransformState.md)!\> | `https://developer.android.com/reference/kotlin/android/net/IpSecTransformState#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getByteCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByteCount(): Long
```

Retrieve the number of bytes processed so far as an unsigned long

The byte count direction (inbound or outbound) aligns with the direction in which the IpSecTransform is applied to.
**See Also**

- setByteCount

### getPacketCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPacketCount(): Long
```

Retrieve the number of packets processed so far as an unsigned long.

The packet count direction (inbound or outbound) aligns with the direction in which the IpSecTransform is applied to.
**See Also**

- setPacketCount

### getReplayBitmap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReplayBitmap(): ByteArray
```

Retrieve the replay bitmap

This bitmap represents a replay window, allowing the caller to observe out-of-order delivery. The last bit represents the highest sequence number received so far and bits for the received packets will be marked as true.

The size of a replay bitmap will never change over the lifetime of an IpSecTransform

The replay bitmap is solely useful for inbound IpSecTransforms. For outbound IpSecTransforms, all bits will be unchecked.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | This value cannot be `null`. |

**See Also**

- setReplayBitmap

### getRxHighestSequenceNumber

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRxHighestSequenceNumber(): Long
```

Retrieve the highest sequence number received so far as an unsigned long
**See Also**

- setRxHighestSequenceNumber

### getTimestampMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimestampMillis(): Long
```

Retrieve the timestamp (milliseconds) when this state was created, as per elapsedRealtime
**See Also**

- setTimestampMillis

### getTxHighestSequenceNumber

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTxHighestSequenceNumber(): Long
```

Retrieve the highest sequence number sent so far as an unsigned long
**See Also**

- setTxHighestSequenceNumber

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `out` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<IpSecTransformState!>
```
