Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComponentInfo

```
open class ComponentInfo : PackageItemInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.content.pm.PackageItemInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo) ||
| | ↳ | [android.content.pm.ComponentInfo](https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#) |

Known Direct Subclasses [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo), [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo), [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo) [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo) Information you can retrieve about a particular application activity or receiver.
[ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo) Holds information about a specific `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`.
[ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo) Information you can retrieve about a particular application service.

Base class containing information common to all application components (`https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo`, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo`). This class is not intended to be used by itself; it is simply here to share common definitions between all application components. As such, it does not itself implement Parcelable, but does provide convenience methods to assist in the implementation of Parcelable in subclasses.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#ComponentInfo()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#ComponentInfo(android.content.pm.ComponentInfo)(orig: https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#!)` <br /> |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#ComponentInfo(android.os.Parcel)(source: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getBannerResource()()` Return the banner resource identifier to use for this component. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getIconResource()()` Return the icon resource identifier to use for this component. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getLogoResource()()` Return the logo resource identifier to use for this component. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#isEnabled()()` Return whether this component and its enclosing application are enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#dumpBack(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#dumpFront(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadBanner(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical banner associated with this item. This will call back on the given PackageManager to load the banner from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical icon associated with this item. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadLabel(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager)`

Retrieve the current textual label associated with this item. This will call back on the given PackageManager to load the label from the application.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadLogo(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical logo associated with this item. This will call back on the given PackageManager to load the logo from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadUnbadgedIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical icon associated with this item without the addition of a work badge if applicable. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadXmlMetaData(android.content.pm.PackageManager,%20kotlin.String)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Load an XML resource attached to the meta-data of this item. This will retrieved the name meta-data entry, and if defined call back on the given PackageManager to load its XML file from the application.

<br />

| Properties ||
|---|---|
| [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo)! | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#applicationInfo:android.content.pm.ApplicationInfo` Global information about the application/package this component is a part of. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#attributionTags:kotlin.Array` Set of attribution tags that should be automatically applied to this component. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#descriptionRes:kotlin.Int` A string resource identifier (in the package's resources) containing a user-readable description of the component. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#directBootAware:kotlin.Boolean` Indicates if this component is aware of direct boot lifecycle, and can be safely run before the user has entered their credentials (such as a lock pattern or PIN). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#enabled:kotlin.Boolean` Indicates whether or not this component may be instantiated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#exported:kotlin.Boolean` Set to true if this component is available for use by other applications. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#processName:kotlin.String` The name of the process this component should run in. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#splitName:kotlin.String` The name of the split in which this component is declared. |

Inherited properties From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#banner:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's banner. From the "banner" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#icon:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's icon. From the "icon" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#isArchived:kotlin.Boolean`

Whether the package is currently in an archived state.

Packages can be archived through `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestArchive(kotlin.String,%20android.content.IntentSender)` and do not have any APKs stored on the device, but do keep the data directory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#labelRes:kotlin.Int`

A string resource identifier (in the package's resources) of this component's label. From the "label" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#logo:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's logo. Logos may be larger/wider than icons and are displayed by certain UI elements in place of a name or name/icon combination. From the "logo" attribute or, if not set, 0.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#metaData:android.os.Bundle`

Additional meta-data associated with this component. This field will only be filled in if you set the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` flag when requesting the info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#name:kotlin.String`

Public name of this item. From the "android:name" attribute.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#nonLocalizedLabel:kotlin.CharSequence`

The string provided in the AndroidManifest file, if any. You probably don't want to use this. You probably want `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationLabel(android.content.pm.ApplicationInfo)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#packageName:kotlin.String`

Name of the package that this item is in.

<br />

## Public constructors

### ComponentInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ComponentInfo()
```

### ComponentInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ComponentInfo(orig: ComponentInfo!)
```

## Protected constructors

### ComponentInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected ComponentInfo(source: Parcel!)
```

## Public methods

### getBannerResource

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBannerResource(): Int
```

Return the banner resource identifier to use for this component. If the component defines a banner, that is used; else, the application banner is used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The banner associated with this component. |

### getIconResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIconResource(): Int
```

Return the icon resource identifier to use for this component. If the component defines an icon, that is used; else, the application icon is used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The icon associated with this component. |

### getLogoResource

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLogoResource(): Int
```

Return the logo resource identifier to use for this component. If the component defines a logo, that is used; else, the application logo is used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The logo associated with this component. |

### isEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEnabled(): Boolean
```

Return whether this component and its enclosing application are enabled.

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel!, 
    parcelableFlags: Int
): Unit
```

## Protected methods

### dumpBack

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dumpBack(
    pw: Printer!, 
    prefix: String!
): Unit
```

### dumpFront

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun dumpFront(
    pw: Printer!, 
    prefix: String!
): Unit
```

## Properties

### applicationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var applicationInfo: ApplicationInfo!
```

Global information about the application/package this component is a part of.

### attributionTags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var attributionTags: Array<String!>!
```

Set of attribution tags that should be automatically applied to this component.

When this component represents an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, `https://developer.android.com/reference/kotlin/android/app/Service.html#`, `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` or `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#`, each instance will be automatically configured with `https://developer.android.com/reference/kotlin/android/content/Context.html#createAttributionContext(kotlin.String)` using the first attribution tag contained here.

Additionally, when this component represents a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` and the sender of a broadcast requires the receiver to hold one or more specific permissions, those permission checks will be performed using each of the attributions tags contained here.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Context.html#createAttributionContext(kotlin.String)`

### descriptionRes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var descriptionRes: Int
```

A string resource identifier (in the package's resources) containing a user-readable description of the component. From the "description" attribute or, if not set, 0.

### directBootAware

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var directBootAware: Boolean
```

Indicates if this component is aware of direct boot lifecycle, and can be safely run before the user has entered their credentials (such as a lock pattern or PIN).

### enabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var enabled: Boolean
```

Indicates whether or not this component may be instantiated. Note that this value can be overridden by the one in its parent `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo`.

### exported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var exported: Boolean
```

Set to true if this component is available for use by other applications. Comes from `https://developer.android.com/reference/kotlin/android/R.attr.html#exported:kotlin.Int` of the \<activity\>, \<receiver\>, \<service\>, or \<provider\> tag.

### processName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var processName: String!
```

The name of the process this component should run in. From the "android:process" attribute or, if not set, the same as applicationInfo.processName.

### splitName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitName: String!
```

The name of the split in which this component is declared. Null if the component was declared in the base APK.
