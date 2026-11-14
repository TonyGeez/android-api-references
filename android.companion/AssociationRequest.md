# AssociationRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssociationRequest

Kotlin| [Java](../android/companion/AssociationRequest.md) 
| --- | --- |

```
class AssociationRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.companion.AssociationRequest](../android/companion/AssociationRequest.md) |

A request for the user to select a companion device to associate with. You can optionally set [filters](../android/companion/AssociationRequest.Builder.md))for which devices to show to the user to select from. The exact type and fields of the filter you can set depend on the medium type. See [Builder](../android/companion/AssociationRequest.Builder.md)'s static factory methods for specific protocols that are supported. You can also set [single device](../android/companion/AssociationRequest.Builder.md))to request a popup with single device to be shown instead of a list to choose from

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/companion/AssociationRequest.Builder.md) A builder for [AssociationRequest](../android/companion/AssociationRequest.md) |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_APP_STREAMING](../android/companion/AssociationRequest.md) Device profile: a virtual display capable of rendering Android applications, and sending back input events. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_AUTOMOTIVE_PROJECTION](../android/companion/AssociationRequest.md) Device profile: Android Automotive Projection Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION](../android/Manifest.permission.md) are allowed to request to be associated with such devices. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_COMPUTER](../android/companion/AssociationRequest.md) Device profile: Allows the companion app to access notification, recent photos and media for computer cross-device features. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_GLASSES](../android/companion/AssociationRequest.md) Device profile: glasses. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_NEARBY_DEVICE_STREAMING](../android/companion/AssociationRequest.md) Device profile: a virtual device capable of rendering content from an Android host to a nearby device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_WATCH](../android/companion/AssociationRequest.md) Device profile: watch. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/companion/AssociationRequest.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/companion/AssociationRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Icon](../android/graphics/drawable/Icon.md)? | [getDeviceIcon](../android/companion/AssociationRequest.md))`()` Get the device icon of the self-managed association request. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDeviceProfile](../android/companion/AssociationRequest.md))`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDisplayName](../android/companion/AssociationRequest.md))`()` The Display name of the device to be shown in the CDM confirmation UI. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isForceConfirmation](../android/companion/AssociationRequest.md))`()` Indicates whether the application requires the [CompanionDeviceManager](../android/companion/CompanionDeviceManager.md) service to collect an explicit confirmation from the user before creating an association, even if such confirmation is not required from the service's perspective. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelfManaged](../android/companion/AssociationRequest.md))`()` Whether the association is to be managed by the companion application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSingleDevice](../android/companion/AssociationRequest.md))`()` Whether only a single device should match the provided filter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/companion/AssociationRequest.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/companion/AssociationRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AssociationRequest](../android/companion/AssociationRequest.md)!\> | [CREATOR](../android/companion/AssociationRequest.md) <br /> |

## Constants

### DEVICE_PROFILE_APP_STREAMING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_APP_STREAMING: String
```

Device profile: a virtual display capable of rendering Android applications, and sending back input events.

Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_APP_STREAMING](../android/Manifest.permission.md) are allowed to request to be associated with such devices. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_APP_STREAMING](../android/Manifest.permission.md) 

 Value: "android.app.role.COMPANION_DEVICE_APP_STREAMING"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](../android/companion/AssociationRequest.Builder.md)) 

### DEVICE_PROFILE_AUTOMOTIVE_PROJECTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_AUTOMOTIVE_PROJECTION: String
```

Device profile: Android Automotive Projection Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION](../android/Manifest.permission.md) are allowed to request to be associated with such devices. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION](../android/Manifest.permission.md) 

 Value: "android.app.role.SYSTEM_AUTOMOTIVE_PROJECTION"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](../android/companion/AssociationRequest.Builder.md)) 

### DEVICE_PROFILE_COMPUTER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_COMPUTER: String
```

Device profile: Allows the companion app to access notification, recent photos and media for computer cross-device features. Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_COMPUTER](../android/Manifest.permission.md) are allowed to request to be associated with such devices. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_COMPUTER](../android/Manifest.permission.md) 

 Value: "android.app.role.COMPANION_DEVICE_COMPUTER"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](../android/companion/AssociationRequest.Builder.md)) 

### DEVICE_PROFILE_GLASSES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_GLASSES: String
```

Device profile: glasses. If specified, the current request may have a modified UI to highlight that the device being set up is a glasses device, and some extra permissions may be granted to the app as a result. Using it requires declaring uses-permission [android.Manifest.permission#REQUEST_COMPANION_PROFILE_GLASSES](../android/Manifest.permission.md) in the manifest. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_GLASSES](../android/Manifest.permission.md) 

 Value: "android.app.role.COMPANION_DEVICE_GLASSES"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](../android/companion/AssociationRequest.Builder.md)) 

### DEVICE_PROFILE_NEARBY_DEVICE_STREAMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_NEARBY_DEVICE_STREAMING: String
```

Device profile: a virtual device capable of rendering content from an Android host to a nearby device.

Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_NEARBY_DEVICE_STREAMING](../android/Manifest.permission.md) are allowed to request to be associated with such devices. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_NEARBY_DEVICE_STREAMING](../android/Manifest.permission.md) 

 Value: "android.app.role.COMPANION_DEVICE_NEARBY_DEVICE_STREAMING"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](../android/companion/AssociationRequest.Builder.md)) 

### DEVICE_PROFILE_WATCH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_WATCH: String
```

Device profile: watch. If specified, the current request may have a modified UI to highlight that the device being set up is a specific kind of device, and some extra permissions may be granted to the app as a result. Using it requires declaring uses-permission [android.Manifest.permission#REQUEST_COMPANION_PROFILE_WATCH](../android/Manifest.permission.md) in the manifest. [Learn more](https://developer.android.com/about/versions/12/features#cdm-profiles) about device profiles. 

 Value: "android.app.role.COMPANION_DEVICE_WATCH"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](../android/companion/AssociationRequest.Builder.md))

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDeviceIcon

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceIcon(): Icon?
```

Get the device icon of the self-managed association request.

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Icon](../android/graphics/drawable/Icon.md)? | the device icon, or`null`if no device icon has been set. |

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceIcon(Icon)](../android/companion/AssociationRequest.Builder.md)) 

### getDeviceProfile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceProfile(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | profile of the companion device. This value may be`null`. Value is [android.companion.AssociationRequest#DEVICE_PROFILE_WATCH](../android/companion/AssociationRequest.md), [android.companion.AssociationRequest#DEVICE_PROFILE_COMPUTER](../android/companion/AssociationRequest.md), [android.companion.AssociationRequest#DEVICE_PROFILE_AUTOMOTIVE_PROJECTION](../android/companion/AssociationRequest.md), [android.companion.AssociationRequest#DEVICE_PROFILE_APP_STREAMING](../android/companion/AssociationRequest.md), [android.companion.AssociationRequest#DEVICE_PROFILE_GLASSES](../android/companion/AssociationRequest.md), [android.companion.AssociationRequest#DEVICE_PROFILE_NEARBY_DEVICE_STREAMING](../android/companion/AssociationRequest.md), or android.companion.AssociationRequest.DEVICE_PROFILE_WEARABLE_SENSING |

### getDisplayName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(): CharSequence?
```

The Display name of the device to be shown in the CDM confirmation UI. Must be non-null for "self-managed" association. 

### isForceConfirmation

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isForceConfirmation(): Boolean
```

Indicates whether the application requires the [CompanionDeviceManager](../android/companion/CompanionDeviceManager.md) service to collect an explicit confirmation from the user before creating an association, even if such confirmation is not required from the service's perspective. 
**See Also**

- [android.companion.AssociationRequest.Builder#setForceConfirmation(boolean)](../android/companion/AssociationRequest.Builder.md)) 

### isSelfManaged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSelfManaged(): Boolean
```

Whether the association is to be managed by the companion application. 
**See Also**

- [android.companion.AssociationRequest.Builder#setSelfManaged(boolean)](../android/companion/AssociationRequest.Builder.md)) 

### isSingleDevice

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSingleDevice(): Boolean
```

Whether only a single device should match the provided filter. When scanning for a single device with a specific [BluetoothDeviceFilter](../android/companion/BluetoothDeviceFilter.md) mac address, bonded devices are also searched among. This allows to obtain the necessary app privileges even if the device is already paired. 

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AssociationRequest!>
```
