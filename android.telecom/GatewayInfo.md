Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GatewayInfo

Kotlin | [Java](GatewayInfo.md)
| --- | --- |

```
open class GatewayInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.GatewayInfo](GatewayInfo.md) |

Encapsulated gateway address information for outgoing call. When calls are made, the system provides a facility to specify two addresses for the call: one to display as the address being dialed and a separate (gateway) address to actually dial. Telecom provides this information to ConnectionServices when placing the call as an instance of `GatewayInfo`.

The data consists of an address to call, an address to display and the package name of the service. This data is used in two ways:

1. Call the appropriate gateway address.
2. Display information about how the call is being routed to the user.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| GatewayInfo <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Uri](../android.net/Uri.md)! | getGatewayAddress Returns the gateway address to dial when placing the call. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getGatewayProviderPackageName Package name of the gateway provider service that provided the gateway information. |
| --- | --- |
| open [Uri](../android.net/Uri.md)! | getOriginalAddress Returns the address that the user is trying to connect to via the gateway. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEmpty Indicates whether this `GatewayInfo` instance contains any data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GatewayInfo](GatewayInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/telecom/GatewayInfo#CREATOR:android.os.Parcelable.Creator` The Parcelable interface. |

## Public constructors

### GatewayInfo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
GatewayInfo(
    packageName: String!, 
    gatewayUri: Uri!, 
    originalAddress: Uri!)
```

## Public methods

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getGatewayAddress

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGatewayAddress(): Uri!
```

Returns the gateway address to dial when placing the call.

### getGatewayProviderPackageName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGatewayProviderPackageName(): String!
```

Package name of the gateway provider service that provided the gateway information. This can be used to identify the gateway address source and to load an appropriate icon when displaying gateway information in the in-call UI.

### getOriginalAddress

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOriginalAddress(): Uri!
```

Returns the address that the user is trying to connect to via the gateway.

### isEmpty

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Indicates whether this `GatewayInfo` instance contains any data. A returned value of false indicates that no gateway number is being used for the call.

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    destination: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<GatewayInfo!>
```

The Parcelable interface.
