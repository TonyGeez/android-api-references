Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualDevice

```
class VirtualDevice : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.companion.virtual.VirtualDevice](../android/companion/virtual/VirtualDevice.md) |

Details of a particular virtual device.

Read-only device representation exposing the properties of an existing virtual device.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#DEVICE_PROFILE_APP_STREAMING:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#DEVICE_PROFILE_AUTOMOTIVE_PROJECTION:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#DEVICE_PROFILE_NEARBY_DEVICE_STREAMING:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#DEVICE_PROFILE_UNKNOWN:kotlin.Int` An unknown virtual device profile, indicating an error. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#getDeviceId()()` Returns the unique ID of the virtual device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#getDeviceProfile()()` Returns the device profile of the virtual device. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#getDisplayIds()()` Returns the IDs of all virtual displays that belong to this device, if any. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#getDisplayName()()` Returns the human-readable name of the virtual device, if defined, which is suitable to be shown in UI. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#getName()()` Returns the name of the virtual device (optionally) provided during its creation. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#getPersistentDeviceId()()` Returns the persistent identifier of this virtual device, if any. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#hasCustomSensorSupport()()` Returns whether this device may have custom sensors. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [VirtualDevice](../android/companion/virtual/VirtualDevice.md)!\> | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### DEVICE_PROFILE_APP_STREAMING

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_PROFILE_APP_STREAMING: Int
```

 Value: 102

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.html#DEVICE_PROFILE_APP_STREAMING:kotlin.String`

### DEVICE_PROFILE_AUTOMOTIVE_PROJECTION

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_PROFILE_AUTOMOTIVE_PROJECTION: Int
```

 Value: 101

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.html#DEVICE_PROFILE_AUTOMOTIVE_PROJECTION:kotlin.String`

### DEVICE_PROFILE_NEARBY_DEVICE_STREAMING

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_PROFILE_NEARBY_DEVICE_STREAMING: Int
```

 Value: 103

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.html#DEVICE_PROFILE_NEARBY_DEVICE_STREAMING:kotlin.String`

### DEVICE_PROFILE_UNKNOWN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_PROFILE_UNKNOWN: Int
```

An unknown virtual device profile, indicating an error.

 Value: -1

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getDeviceId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeviceId(): Int
```

Returns the unique ID of the virtual device.

This identifier corresponds to `https://developer.android.com/reference/kotlin/android/content/Context.html#getDeviceId()` and can be used to access device-specific system capabilities.

This identifier is ephemeral and should not be used for persisting any data per device.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceContext(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice#getPersistentDeviceId()`

### getDeviceProfile

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeviceProfile(): Int
```

Returns the device profile of the virtual device.

The device profile indicates the intended use and capabilities of the device.

### getDisplayIds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayIds(): IntArray
```

Returns the IDs of all virtual displays that belong to this device, if any.

The actual `https://developer.android.com/reference/kotlin/android/view/Display.html#` objects can be obtained by passing the returned IDs to `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | This value cannot be `null`. |

### getDisplayName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(): CharSequence?
```

Returns the human-readable name of the virtual device, if defined, which is suitable to be shown in UI.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | This value may be `null`. |

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String?
```

Returns the name of the virtual device (optionally) provided during its creation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getPersistentDeviceId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPersistentDeviceId(): String?
```

Returns the persistent identifier of this virtual device, if any.

If there is no stable identifier for this virtual device, then this returns `null`.

This identifier may correspond to a physical device. In that case it remains valid for as long as that physical device is associated with the host device and may be used to persist data per device.

This identifier may not be unique across virtual devices, in case there are more than one virtual devices corresponding to the same physical device.

### hasCustomSensorSupport

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCustomSensorSupport(): Boolean
```

Returns whether this device may have custom sensors.

Returning `true` does not necessarily mean that this device has sensors, it only means that a `https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#` instance created from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` associated with this device will return this device's sensors, if any.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Context.html#getDeviceId()`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceContext(kotlin.Int)`

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<VirtualDevice!>
```
