# RoutingSessionInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RoutingSessionInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/RoutingSessionInfo "View this page in Java") 

```
class RoutingSessionInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.RoutingSessionInfo](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#) |

Describes a routing session which is created when a media route is selected.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo.Builder) Builder class for [RoutingSessionInfo](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#). |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSFER_REASON_APP](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#TRANSFER_REASON_APP:kotlin.Int) Indicates that the transfer happened from a non-privileged app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSFER_REASON_FALLBACK](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#TRANSFER_REASON_FALLBACK:kotlin.Int) Indicates that the transfer happened by the default logic without explicit system's or user's request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSFER_REASON_SYSTEM_REQUEST](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#TRANSFER_REASON_SYSTEM_REQUEST:kotlin.Int) Indicates that the transfer happened from within a privileged application. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getClientPackageName](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getClientPackageName())`()` Gets the client package name of the session |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getControlHints](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getControlHints())`()` Gets the control hints |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDeselectableRoutes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getDeselectableRoutes())`()` Gets the list of IDs of deselectable routes for the session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getId())`()` Gets the id of the session. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getName](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getName())`()` Gets the user-visible name of the session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSelectableRoutes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getSelectableRoutes())`()` Gets the list of IDs of selectable routes for the session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSelectedRoutes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getSelectedRoutes())`()` Gets the list of IDs of selected routes for the session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransferReason](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getTransferReason())`()` Returns the transfer reason for this routing session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getTransferableRoutes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getTransferableRoutes())`()` Gets the list of IDs of transferable routes for the session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolume](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getVolume())`()` Gets the current volume of the session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeHandling](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getVolumeHandling())`()` Gets the information about how volume is handled on the session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeMax](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getVolumeMax())`()` Gets the maximum volume of the session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RoutingSessionInfo](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TRANSFER_REASON_APP

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSFER_REASON_APP: Int
```

Indicates that the transfer happened from a non-privileged app. 

 Value: 2

### TRANSFER_REASON_FALLBACK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSFER_REASON_FALLBACK: Int
```

Indicates that the transfer happened by the default logic without explicit system's or user's request.

For example, an automatically connected Bluetooth device will have this transfer reason. 

 Value: 0

### TRANSFER_REASON_SYSTEM_REQUEST

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSFER_REASON_SYSTEM_REQUEST: Int
```

Indicates that the transfer happened from within a privileged application. 

 Value: 1

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getClientPackageName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientPackageName(): String
```

Gets the client package name of the session

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getControlHints

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getControlHints(): Bundle?
```

Gets the control hints

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

### getDeselectableRoutes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeselectableRoutes(): MutableList<String!>
```

Gets the list of IDs of deselectable routes for the session.

Deselectable routes can be removed from the [selected routes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getSelectedRoutes()), so that the routing session stops routing to the newly deselected route, but continues on any remaining selected routes.

Deselectable routes should be a subset of the [selected](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getSelectedRoutes()), meaning not all of the selected routes might be deselectable. For example, one of the selected routes may be a leader device coordinating group playback, which must always remain selected while the session is active.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | A possibly empty list of deselectable route ids. This value cannot be`null`. |

### getId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

Gets the id of the session. The sessions which are given by [MediaRouter2](https://developer.android.com/reference/kotlin/android/media/MediaRouter2) will have unique IDs.

In order to ensure uniqueness in [MediaRouter2](https://developer.android.com/reference/kotlin/android/media/MediaRouter2) side, the value of this method can be different from what was set in [MediaRoute2ProviderService](https://developer.android.com/reference/kotlin/android/media/MediaRoute2ProviderService).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

**See Also**

- [android.media.RoutingSessionInfo.Builder#Builder(String, String)](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo.Builder#Builder(kotlin.String,%20kotlin.String)) 

### getName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): CharSequence?
```

Gets the user-visible name of the session. It may be`null`. 

### getSelectableRoutes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectableRoutes(): MutableList<String!>
```

Gets the list of IDs of selectable routes for the session.

Selectable routes can be added to a routing session (via [android.media.MediaRouter2.RoutingController#selectRoute](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController#selectRoute(android.media.MediaRoute2Info))) in order to add them to the [selected routes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getSelectedRoutes()), so that media plays on the newly selected route along with the other selected routes.

Not to be confused with [transferable routes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getTransferableRoutes()). Transferring to a route makes it the sole selected route.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | A possibly empty list of selectable route ids. This value cannot be`null`. |

### getSelectedRoutes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectedRoutes(): MutableList<String!>
```

Gets the list of IDs of selected routes for the session.

Selected routes are the routes that this session is actively routing media to.

The behavior of a routing session with multiple selected routes is ultimately defined by the [MediaRoute2ProviderService](https://developer.android.com/reference/kotlin/android/media/MediaRoute2ProviderService) implementation. However, typically, it's expected that all the selected routes of a routing session are playing the same media in sync.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | A non-empty list of selected route ids. This value cannot be`null`. |

### getTransferReason

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransferReason(): Int
```

Returns the transfer reason for this routing session.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.RoutingSessionInfo#TRANSFER_REASON_FALLBACK](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#TRANSFER_REASON_FALLBACK:kotlin.Int), [android.media.RoutingSessionInfo#TRANSFER_REASON_SYSTEM_REQUEST](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#TRANSFER_REASON_SYSTEM_REQUEST:kotlin.Int), or [android.media.RoutingSessionInfo#TRANSFER_REASON_APP](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#TRANSFER_REASON_APP:kotlin.Int) |

### getTransferableRoutes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransferableRoutes(): MutableList<String!>
```

Gets the list of IDs of transferable routes for the session.

Transferring to a route (for example, using [MediaRouter2.transferTo](https://developer.android.com/reference/kotlin/android/media/MediaRouter2#transferTo(android.media.MediaRoute2Info))) replaces the list of [selected routes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getSelectedRoutes())with the target route, causing playback to move from one route to another.

Note that this is different from [selectable routes](https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo#getSelectableRoutes()), because selecting a route makes it part of the selected routes, while transferring to a route makes it the selected route. A route can be both transferable and selectable.

Note that playback may transfer across routes without the target route being in the list of transferable routes. This can happen by creating a new routing session to the target route, and releasing the routing session being transferred from. The difference is that a transfer to a route in the transferable list can happen with no intervention from the app, with the route provider taking care of the entire operation. A transfer to a route that is not in the list of transferable routes (by creating a new session) requires the app to move the playback state from one device to the other.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | A possibly empty list of transferable route ids. This value cannot be`null`. |

### getVolume

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolume(): Int
```

Gets the current volume of the session.

When it's available, it represents the volume of routing session, which is a group of selected routes. To get the volume of each route, use [MediaRoute2Info.getVolume()](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getVolume()). 
**See Also**

- [android.media.MediaRoute2Info#getVolume()](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getVolume()) 

### getVolumeHandling

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeHandling(): Int
```

Gets the information about how volume is handled on the session.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MediaRoute2Info.PLAYBACK_VOLUME_FIXED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_FIXED:kotlin.Int) or [MediaRoute2Info.PLAYBACK_VOLUME_VARIABLE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_VARIABLE:kotlin.Int). Value is [android.media.MediaRoute2Info#PLAYBACK_VOLUME_FIXED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_FIXED:kotlin.Int), or [android.media.MediaRoute2Info#PLAYBACK_VOLUME_VARIABLE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_VARIABLE:kotlin.Int) |

### getVolumeMax

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeMax(): Int
```

Gets the maximum volume of the session. 

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RoutingSessionInfo!>
```
