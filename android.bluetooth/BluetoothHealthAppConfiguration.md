Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHealthAppConfiguration

Kotlin | [Java](../android/bluetooth/BluetoothHealthAppConfiguration.md)
| --- | --- |

```
class BluetoothHealthAppConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md) |

| **This class was deprecated in API level 29.**
|
| Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()`, or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)`

The Bluetooth Health Application Configuration that is used in conjunction with the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth` class. This class represents an application configuration that the Bluetooth Health third party application will register to communicate with the remote Bluetooth health device.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration#getDataType()()` Return the data type associated with this application configuration. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration#getName()()` Return the name of the application configuration. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration#getRole()()` Return the role associated with this application configuration. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getDataType

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataType(): Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()`, or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)`*

Return the data type associated with this application configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | dataType |

### getName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String!
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()`, or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)`*

Return the name of the application configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | String name |

### getRole

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRole(): Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()`, or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)`*

Return the role associated with this application configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#SOURCE_ROLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#SINK_ROLE:kotlin.Int` |

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<BluetoothHealthAppConfiguration!>
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()`, or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)`*
