# AssociationRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssociationRequest

Kotlin| [Java](https://developer.android.com/reference/android/companion/AssociationRequest "View this page in Java") 
| --- | --- |

```
class AssociationRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.companion.AssociationRequest](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#) |

A request for the user to select a companion device to associate with. You can optionally set [filters](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#addDeviceFilter(android.companion.DeviceFilter))for which devices to show to the user to select from. The exact type and fields of the filter you can set depend on the medium type. See [Builder](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder)'s static factory methods for specific protocols that are supported. You can also set [single device](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setSingleDevice(kotlin.Boolean))to request a popup with single device to be shown instead of a list to choose from

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder) A builder for [AssociationRequest](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#) |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_APP_STREAMING](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_APP_STREAMING:kotlin.String) Device profile: a virtual display capable of rendering Android applications, and sending back input events. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_AUTOMOTIVE_PROJECTION](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_AUTOMOTIVE_PROJECTION:kotlin.String) Device profile: Android Automotive Projection Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION:kotlin.String) are allowed to request to be associated with such devices. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_COMPUTER](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_COMPUTER:kotlin.String) Device profile: Allows the companion app to access notification, recent photos and media for computer cross-device features. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_GLASSES](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_GLASSES:kotlin.String) Device profile: glasses. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_NEARBY_DEVICE_STREAMING](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_NEARBY_DEVICE_STREAMING:kotlin.String) Device profile: a virtual device capable of rendering content from an Android host to a nearby device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEVICE_PROFILE_WATCH](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_WATCH:kotlin.String) Device profile: watch. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | [getDeviceIcon](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#getDeviceIcon())`()` Get the device icon of the self-managed association request. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDeviceProfile](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#getDeviceProfile())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDisplayName](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#getDisplayName())`()` The Display name of the device to be shown in the CDM confirmation UI. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isForceConfirmation](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#isForceConfirmation())`()` Indicates whether the application requires the [CompanionDeviceManager](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager) service to collect an explicit confirmation from the user before creating an association, even if such confirmation is not required from the service's perspective. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelfManaged](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#isSelfManaged())`()` Whether the association is to be managed by the companion application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSingleDevice](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#isSingleDevice())`()` Whether only a single device should match the provided filter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#toString())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AssociationRequest](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### DEVICE_PROFILE_APP_STREAMING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_APP_STREAMING: String
```

Device profile: a virtual display capable of rendering Android applications, and sending back input events.

Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_APP_STREAMING](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_APP_STREAMING:kotlin.String) are allowed to request to be associated with such devices. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_APP_STREAMING](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_APP_STREAMING:kotlin.String) 

 Value: "android.app.role.COMPANION_DEVICE_APP_STREAMING"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setDeviceProfile(kotlin.String)) 

### DEVICE_PROFILE_AUTOMOTIVE_PROJECTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_AUTOMOTIVE_PROJECTION: String
```

Device profile: Android Automotive Projection Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION:kotlin.String) are allowed to request to be associated with such devices. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_AUTOMOTIVE_PROJECTION:kotlin.String) 

 Value: "android.app.role.SYSTEM_AUTOMOTIVE_PROJECTION"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setDeviceProfile(kotlin.String)) 

### DEVICE_PROFILE_COMPUTER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_COMPUTER: String
```

Device profile: Allows the companion app to access notification, recent photos and media for computer cross-device features. Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_COMPUTER](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_COMPUTER:kotlin.String) are allowed to request to be associated with such devices. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_COMPUTER](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_COMPUTER:kotlin.String) 

 Value: "android.app.role.COMPANION_DEVICE_COMPUTER"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setDeviceProfile(kotlin.String)) 

### DEVICE_PROFILE_GLASSES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_GLASSES: String
```

Device profile: glasses. If specified, the current request may have a modified UI to highlight that the device being set up is a glasses device, and some extra permissions may be granted to the app as a result. Using it requires declaring uses-permission [android.Manifest.permission#REQUEST_COMPANION_PROFILE_GLASSES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_GLASSES:kotlin.String) in the manifest. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_GLASSES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_GLASSES:kotlin.String) 

 Value: "android.app.role.COMPANION_DEVICE_GLASSES"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setDeviceProfile(kotlin.String)) 

### DEVICE_PROFILE_NEARBY_DEVICE_STREAMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_NEARBY_DEVICE_STREAMING: String
```

Device profile: a virtual device capable of rendering content from an Android host to a nearby device.

Only applications that have been granted [android.Manifest.permission#REQUEST_COMPANION_PROFILE_NEARBY_DEVICE_STREAMING](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_NEARBY_DEVICE_STREAMING:kotlin.String) are allowed to request to be associated with such devices. 
Requires [android.Manifest.permission#REQUEST_COMPANION_PROFILE_NEARBY_DEVICE_STREAMING](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_NEARBY_DEVICE_STREAMING:kotlin.String) 

 Value: "android.app.role.COMPANION_DEVICE_NEARBY_DEVICE_STREAMING"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setDeviceProfile(kotlin.String)) 

### DEVICE_PROFILE_WATCH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_PROFILE_WATCH: String
```

Device profile: watch. If specified, the current request may have a modified UI to highlight that the device being set up is a specific kind of device, and some extra permissions may be granted to the app as a result. Using it requires declaring uses-permission [android.Manifest.permission#REQUEST_COMPANION_PROFILE_WATCH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_PROFILE_WATCH:kotlin.String) in the manifest. [Learn more](https://developer.android.com/about/versions/12/features#cdm-profiles) about device profiles. 

 Value: "android.app.role.COMPANION_DEVICE_WATCH"

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceProfile](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setDeviceProfile(kotlin.String))

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | the device icon, or`null`if no device icon has been set. |

**See Also**

- [android.companion.AssociationRequest.Builder#setDeviceIcon(Icon)](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setDeviceIcon(android.graphics.drawable.Icon)) 

### getDeviceProfile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceProfile(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | profile of the companion device. This value may be`null`. Value is [android.companion.AssociationRequest#DEVICE_PROFILE_WATCH](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_WATCH:kotlin.String), [android.companion.AssociationRequest#DEVICE_PROFILE_COMPUTER](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_COMPUTER:kotlin.String), [android.companion.AssociationRequest#DEVICE_PROFILE_AUTOMOTIVE_PROJECTION](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_AUTOMOTIVE_PROJECTION:kotlin.String), [android.companion.AssociationRequest#DEVICE_PROFILE_APP_STREAMING](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_APP_STREAMING:kotlin.String), [android.companion.AssociationRequest#DEVICE_PROFILE_GLASSES](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_GLASSES:kotlin.String), [android.companion.AssociationRequest#DEVICE_PROFILE_NEARBY_DEVICE_STREAMING](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest#DEVICE_PROFILE_NEARBY_DEVICE_STREAMING:kotlin.String), or android.companion.AssociationRequest.DEVICE_PROFILE_WEARABLE_SENSING |

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

Indicates whether the application requires the [CompanionDeviceManager](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager) service to collect an explicit confirmation from the user before creating an association, even if such confirmation is not required from the service's perspective. 
**See Also**

- [android.companion.AssociationRequest.Builder#setForceConfirmation(boolean)](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setForceConfirmation(kotlin.Boolean)) 

### isSelfManaged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSelfManaged(): Boolean
```

Whether the association is to be managed by the companion application. 
**See Also**

- [android.companion.AssociationRequest.Builder#setSelfManaged(boolean)](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder#setSelfManaged(kotlin.Boolean)) 

### isSingleDevice

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSingleDevice(): Boolean
```

Whether only a single device should match the provided filter. When scanning for a single device with a specific [BluetoothDeviceFilter](https://developer.android.com/reference/kotlin/android/companion/BluetoothDeviceFilter) mac address, bonded devices are also searched among. This allows to obtain the necessary app privileges even if the device is already paired. 

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AssociationRequest!>
```
