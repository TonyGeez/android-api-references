# TransportDiscoveryData

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransportDiscoveryData

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/le/TransportDiscoveryData "View this page in Java") 

```
class TransportDiscoveryData : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.le.TransportDiscoveryData](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#) |

Wrapper for Transport Discovery Data AD Type. This class contains the Transport Discovery Data AD Type Code as well as a list of potential Transport Blocks.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransportDiscoveryData](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#TransportDiscoveryData(kotlin.ByteArray))`(`transportDiscoveryData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Creates a TransportDiscoveryData instance from byte arrays. |
| [TransportDiscoveryData](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#TransportDiscoveryData(kotlin.Int,%20kotlin.collections.MutableList))`(`transportDataType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `transportBlocks:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TransportBlock](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportBlock)!>`)` Creates a TransportDiscoveryData instance. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TransportBlock](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportBlock)!\> | [getTransportBlocks](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#getTransportBlocks())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransportDataType](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#getTransportDataType())`()` Gets the transport data type. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [toByteArray](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#toByteArray())`()` Converts this TransportDiscoveryData to byte array |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#toString())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [totalBytes](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#totalBytes())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TransportDiscoveryData](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportDiscoveryData#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### TransportDiscoveryData

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransportDiscoveryData(transportDiscoveryData: ByteArray)
```

Creates a TransportDiscoveryData instance from byte arrays.

Uses the transport discovery data bytes and parses them into an usable class.

| Parameters ||
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `transportDiscoveryData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the raw discovery data This value cannot be`null`. |

### TransportDiscoveryData

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransportDiscoveryData(
    transportDataType: Int, 
    transportBlocks: MutableList<TransportBlock!>)
```

Creates a TransportDiscoveryData instance.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transportDataType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Transport Discovery Data AD Type |
| `transportBlocks` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TransportBlock](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportBlock)!\>:the list of Transport Blocks This value cannot be`null`. |

## Public methods

### getTransportBlocks

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransportBlocks(): MutableList<TransportBlock!>
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TransportBlock](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportBlock)!> | the list of [TransportBlock](https://developer.android.com/reference/kotlin/android/bluetooth/le/TransportBlock) in this TransportDiscoveryData or an empty list if there are no Transport Blocks This value cannot be`null`. |

### getTransportDataType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransportDataType(): Int
```

Gets the transport data type. 

### toByteArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByteArray(): ByteArray?
```

Converts this TransportDiscoveryData to byte array

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | byte array representation of this Transport Discovery Data or null if the conversion failed |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### totalBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun totalBytes(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | total byte count of this TransportDataDiscovery |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TransportDiscoveryData!>
```
