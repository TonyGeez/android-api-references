Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResolveInfo

```
open class ResolveInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#) |

Information that is returned from resolving an intent against an IntentFilter. This partially corresponds to information collected from the AndroidManifest.xml's \<intent\> tags.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.DisplayNameComparator` <br /> |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#ResolveInfo()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#ResolveInfo(android.content.pm.ResolveInfo)(orig: https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#!)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#dump(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#getIconResource()()` Return the icon resource identifier to use for this match. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#isCrossProfileIntentForwarderActivity()()` Returns whether this resolution represents the intent forwarder activity. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#loadIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)` Retrieve the current graphical icon associated with this resolution. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#loadLabel(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager)` Retrieve the current textual label associated with this resolution. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo)! | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#activityInfo:android.content.pm.ActivityInfo` The activity or broadcast receiver that corresponds to this resolution match, if this resolution is for an activity or broadcast receiver. |
| [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#)! | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#filter:android.content.IntentFilter` The IntentFilter that was matched for this ResolveInfo. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#icon:kotlin.Int` A drawable resource identifier (in the package's resources) of this match's icon. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#isDefault:kotlin.Boolean` This filter has specified the Intent. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#isInstantAppAvailable:kotlin.Boolean` Whether or not an instant app is available for the resolved intent. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#labelRes:kotlin.Int` A string resource identifier (in the package's resources) of this match's label. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#match:kotlin.Int` The system's evaluation of how well the activity matches the IntentFilter. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#nonLocalizedLabel:kotlin.CharSequence` The actual string retrieve from labelRes or null if none was provided. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#preferredOrder:kotlin.Int` Order of result according to the user's preference. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#priority:kotlin.Int` The declared priority of this match. |
| [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo)! | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#providerInfo:android.content.pm.ProviderInfo` The provider that corresponds to this resolution match, if this resolution is for a provider. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#resolvePackageName:kotlin.String` Optional -- if non-null, the `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#labelRes:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#icon:kotlin.Int` resources will be loaded from this package, rather than the one containing the resolved component. |
| [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo)! | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#serviceInfo:android.content.pm.ServiceInfo` The service that corresponds to this resolution match, if this resolution is for a service. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#specificIndex:kotlin.Int` Only set when returned by android. |

## Public constructors

### ResolveInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ResolveInfo()
```

### ResolveInfo

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ResolveInfo(orig: ResolveInfo!)
```

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```

### getIconResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIconResource(): Int
```

Return the icon resource identifier to use for this match. If the match defines an icon, that is used; else if the activity defines an icon, that is used; else, the application icon is used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The icon associated with this match. |

### isCrossProfileIntentForwarderActivity

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCrossProfileIntentForwarderActivity(): Boolean
```

Returns whether this resolution represents the intent forwarder activity.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this resolution represents the intent forwarder activity |

### loadIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadIcon(pm: PackageManager!): Drawable!
```

Retrieve the current graphical icon associated with this resolution. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager)!: A PackageManager from which the icon can be loaded; usually the PackageManager from which you originally retrieved this item. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | Returns a Drawable containing the resolution's icon. If the item does not have an icon, the default activity icon is returned. |

### loadLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadLabel(pm: PackageManager): CharSequence
```

Retrieve the current textual label associated with this resolution. This will call back on the given PackageManager to load the label from the application.

| Parameters ||
|---|---|
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager): A PackageManager from which the label can be loaded; usually the PackageManager from which you originally retrieved this item. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | Returns a CharSequence containing the resolutions's label. If the item does not have a label, its name is returned. This value cannot be `null`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ResolveInfo!>
```

### activityInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var activityInfo: ActivityInfo!
```

The activity or broadcast receiver that corresponds to this resolution match, if this resolution is for an activity or broadcast receiver. Exactly one of `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#activityInfo:android.content.pm.ActivityInfo`, `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#serviceInfo:android.content.pm.ServiceInfo`, or `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#providerInfo:android.content.pm.ProviderInfo` will be non-null.

### filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var filter: IntentFilter!
```

The IntentFilter that was matched for this ResolveInfo.

### icon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var icon: Int
```

A drawable resource identifier (in the package's resources) of this match's icon. From the "icon" attribute or, if not set, 0. It is set only if the icon can be obtained by resource id alone.

### isDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var isDefault: Boolean
```

This filter has specified the Intent.CATEGORY_DEFAULT, meaning it would like to be considered a default action that the user can perform on this data.

### isInstantAppAvailable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var isInstantAppAvailable: Boolean
```

Whether or not an instant app is available for the resolved intent.

### labelRes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var labelRes: Int
```

A string resource identifier (in the package's resources) of this match's label. From the "label" attribute or, if not set, 0.

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var match: Int
```

The system's evaluation of how well the activity matches the IntentFilter. This is a match constant, a combination of `https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#MATCH_CATEGORY_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#MATCH_ADJUSTMENT_MASK:kotlin.Int`.

### nonLocalizedLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var nonLocalizedLabel: CharSequence!
```

The actual string retrieve from labelRes or null if none was provided.

### preferredOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var preferredOrder: Int
```

Order of result according to the user's preference. If the user has not set a preference for this result, the value is 0; higher values are a higher priority.

### priority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var priority: Int
```

The declared priority of this match. Comes from the "priority" attribute or, if not set, defaults to 0. Higher values are a higher priority.

### providerInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var providerInfo: ProviderInfo!
```

The provider that corresponds to this resolution match, if this resolution is for a provider. Exactly one of `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#activityInfo:android.content.pm.ActivityInfo`, `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#serviceInfo:android.content.pm.ServiceInfo`, or `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#providerInfo:android.content.pm.ProviderInfo` will be non-null.

### resolvePackageName

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var resolvePackageName: String!
```

Optional -- if non-null, the `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#labelRes:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#icon:kotlin.Int` resources will be loaded from this package, rather than the one containing the resolved component.

### serviceInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var serviceInfo: ServiceInfo!
```

The service that corresponds to this resolution match, if this resolution is for a service. Exactly one of `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#activityInfo:android.content.pm.ActivityInfo`, `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#serviceInfo:android.content.pm.ServiceInfo`, or `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#providerInfo:android.content.pm.ProviderInfo` will be non-null.

### specificIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var specificIndex: Int
```

Only set when returned by android.content.pm.PackageManager#queryIntentActivityOptions, this tells you which of the given specific intents this result came from. 0 is the first in the list, \< 0 means it came from the generic Intent query.
