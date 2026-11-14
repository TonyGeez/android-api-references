Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RouteListingPreference

```
class RouteListingPreference : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.RouteListingPreference](https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#) |

Allows applications to customize the list of routes used for media routing (for example, in the System UI Output Switcher).

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Builder` Builder for `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#`. |
| | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item` Holds preference information for a specific route in a `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#`. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#ACTION_RESOLVE_MISSING_PERMISSIONS:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action for apps to handle issues with missing permissions. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#ACTION_TRANSFER_MEDIA:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action that the system uses to take the user the app when the user selects an `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item` whose `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#getSelectionBehavior()` is `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#SELECTION_BEHAVIOR_GO_TO_APP:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#EXTRA_MISSING_PERMISSIONS:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` string extra key that contains missing permissions. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#EXTRA_ROUTE_ID:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` string extra key that contains the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#getRouteId()` of the route to transfer to, as part of an `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#ACTION_TRANSFER_MEDIA:kotlin.String` intent. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RouteListingPreference.Item](https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item)!\> | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getItems()()` Returns an unmodifiable list containing the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item` that the app wants to be listed for media routing. |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getLinkedItemComponentName()()` Returns a `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for navigating to the application. |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getMissingPermissionsComponentName()()` Returns a `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for navigating to the application to fix missing permissions. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getUseSystemOrdering()()` Returns true if the application would like media route listing to use the system's ordering strategy, or false if the application would like route listing to respect the ordering obtained from `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getItems()`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#hashCode()()` Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RouteListingPreference](https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#)!\> | `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ACTION_RESOLVE_MISSING_PERMISSIONS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_RESOLVE_MISSING_PERMISSIONS: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` action for apps to handle issues with missing permissions.

The system uses this action to take the user to the app when a `https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference` set by the app cannot be satisfied due to missing permissions, and the user has triggered a UI flow to fix the issue.

The launched intent will identify the missing permissions using the extra identified by `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#EXTRA_MISSING_PERMISSIONS:kotlin.String`.

 Value: "android.media.action.RESOLVE_MISSING_PERMISSIONS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getMissingPermissionsComponentName()`

### ACTION_TRANSFER_MEDIA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_TRANSFER_MEDIA: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` action that the system uses to take the user the app when the user selects an `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item` whose `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#getSelectionBehavior()` is `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#SELECTION_BEHAVIOR_GO_TO_APP:kotlin.Int`.

The launched intent will identify the selected item using the extra identified by `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#EXTRA_ROUTE_ID:kotlin.String`.

 Value: "android.media.action.TRANSFER_MEDIA"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getLinkedItemComponentName()`
- `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#SELECTION_BEHAVIOR_GO_TO_APP:kotlin.Int`

### EXTRA_MISSING_PERMISSIONS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MISSING_PERMISSIONS: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` string extra key that contains missing permissions.

This is part of an `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#ACTION_RESOLVE_MISSING_PERMISSIONS:kotlin.String` intent. The value can be obtained through `https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringArrayListExtra(kotlin.String)`. It is the list of permissions which the app has requested in its AndroidManifest.xml but were not granted, and are part of the required permissions for some routes.

 Value: "android.media.extra.MISSING_PERMISSIONS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getMissingPermissionsComponentName()`

### EXTRA_ROUTE_ID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ROUTE_ID: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` string extra key that contains the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#getRouteId()` of the route to transfer to, as part of an `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#ACTION_TRANSFER_MEDIA:kotlin.String` intent.

 Value: "android.media.extra.ROUTE_ID"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getLinkedItemComponentName()`
- `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#SELECTION_BEHAVIOR_GO_TO_APP:kotlin.Int`

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

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getItems

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getItems(): MutableList<RouteListingPreference.Item!>
```

Returns an unmodifiable list containing the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item` that the app wants to be listed for media routing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item!>` | This value cannot be `null`. |

### getLinkedItemComponentName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLinkedItemComponentName(): ComponentName?
```

Returns a `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for navigating to the application.

Must not be null if any of the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getItems()` of this route listing preference has `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#getSelectionBehavior()` `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#SELECTION_BEHAVIOR_GO_TO_APP:kotlin.Int`.

The system navigates to the application when the user selects `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item` with `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.Item#SELECTION_BEHAVIOR_GO_TO_APP:kotlin.Int` by launching an intent to the returned `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#`, using action `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#ACTION_TRANSFER_MEDIA:kotlin.String`, with the extra `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#EXTRA_ROUTE_ID:kotlin.String`.

### getMissingPermissionsComponentName

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMissingPermissionsComponentName(): ComponentName?
```

Returns a `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for navigating to the application to fix missing permissions.

The system navigates to the application when a route discovery preference set by the app cannot be satisfied due to missing permissions, and the user has triggered a UI flow to fix the issue.

The system launches an intent to the returned `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#`, using action `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#ACTION_RESOLVE_MISSING_PERMISSIONS:kotlin.String`, with the extra `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#EXTRA_MISSING_PERMISSIONS:kotlin.String`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` | This value may be `null`. |

### getUseSystemOrdering

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUseSystemOrdering(): Boolean
```

Returns true if the application would like media route listing to use the system's ordering strategy, or false if the application would like route listing to respect the ordering obtained from `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference#getItems()`.

The system's ordering strategy is implementation-dependent, but may take into account each route's recency or frequency of use in order to rank them.

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<RouteListingPreference!>
```
