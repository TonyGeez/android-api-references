# DeviceFilter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceFilter

Kotlin | [Java](../android/companion/DeviceFilter.md) 
| --- | --- |

```
interface DeviceFilter<D : Parcelable!> : Parcelable
```

| [android.companion.DeviceFilter](../android/companion/DeviceFilter.md) |

| Known Direct Subclasses [BluetoothDeviceFilter](../android/companion/BluetoothDeviceFilter.md), [BluetoothLeDeviceFilter](../android/companion/BluetoothLeDeviceFilter.md), [WifiDeviceFilter](../android/companion/WifiDeviceFilter.md) |---------------------------------------------------------------------------------------------------------------------|----------------------------------------| | [BluetoothDeviceFilter](../android/companion/BluetoothDeviceFilter.md) | A filter for Bluetooth(non-LE) devices | | [BluetoothLeDeviceFilter](../android/companion/BluetoothLeDeviceFilter.md) | A filter for Bluetooth LE devices | | [WifiDeviceFilter](../android/companion/WifiDeviceFilter.md) | A filter for Wifi devices | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A filter for companion devices of type `D`

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Inherited functions ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/os/Parcelable.md))`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/os/Parcelable.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. <br /> | ||
