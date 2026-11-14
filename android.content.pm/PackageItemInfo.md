Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackageItemInfo

```
open class PackageItemInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.PackageItemInfo](PackageItemInfo.md) |

Known Direct Subclasses [ApplicationInfo](ApplicationInfo.md), [ComponentInfo](ComponentInfo.md), [InstrumentationInfo](InstrumentationInfo.md), [PermissionGroupInfo](PermissionGroupInfo.md), [PermissionInfo](PermissionInfo.md) [ApplicationInfo](ApplicationInfo.md) Information you can retrieve about a particular application.
[ComponentInfo](ComponentInfo.md) Base class containing information common to all application components (ActivityInfo, ServiceInfo).
[InstrumentationInfo](InstrumentationInfo.md) Information you can retrieve about a particular piece of test instrumentation.
[PermissionGroupInfo](PermissionGroupInfo.md) Information you can retrieve about a particular security permission group known to the system.
[PermissionInfo](PermissionInfo.md) Information you can retrieve about a particular security permission known to the system.
Known Indirect Subclasses [ActivityInfo](ActivityInfo.md), [ProviderInfo](ProviderInfo.md), [ServiceInfo](ServiceInfo.md) [ActivityInfo](ActivityInfo.md) Information you can retrieve about a particular application activity or receiver.
[ProviderInfo](ProviderInfo.md) Holds information about a specific `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`.
[ServiceInfo](ServiceInfo.md) Information you can retrieve about a particular application service.

Base class containing information common to all package items held by the package manager. This provides a very common basic set of attributes: a label, icon, and meta-data. This class is not intended to be used by itself; it is simply here to share common definitions between all items returned by the package manager. As such, it does not itself implement Parcelable, but does provide convenience methods to assist in the implementation of Parcelable in subclasses.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo.DisplayNameComparator` <br /> |

| Public constructors ||
|---|---|
| PackageItemInfo <br /> |
| PackageItemInfo <br /> |

| Protected constructors ||
|---|---|
| PackageItemInfo <br /> |

| Public methods ||
|---|---|
| open [Drawable](../android.graphics.drawable/Drawable.md)! | loadBanner Retrieve the current graphical banner associated with this item. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | loadIcon Retrieve the current graphical icon associated with this item. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | loadLabel Retrieve the current textual label associated with this item. |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | loadLogo Retrieve the current graphical logo associated with this item. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | loadUnbadgedIcon Retrieve the current graphical icon associated with this item without the addition of a work badge if applicable. |
| open [XmlResourceParser](../android.content.res/XmlResourceParser.md)! | loadXmlMetaData Load an XML resource attached to the meta-data of this item. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel <br /> |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dumpBack <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dumpFront <br /> |

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#banner:kotlin.Int` A drawable resource identifier (in the package's resources) of this component's banner. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#icon:kotlin.Int` A drawable resource identifier (in the package's resources) of this component's icon. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#isArchived:kotlin.Boolean` Whether the package is currently in an archived state. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#labelRes:kotlin.Int` A string resource identifier (in the package's resources) of this component's label. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#logo:kotlin.Int` A drawable resource identifier (in the package's resources) of this component's logo. |
| [Bundle](../android.os/Bundle.md)! | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#metaData:android.os.Bundle` Additional meta-data associated with this component. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#name:kotlin.String` Public name of this item. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#nonLocalizedLabel:kotlin.CharSequence` The string provided in the AndroidManifest file, if any. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#packageName:kotlin.String` Name of the package that this item is in. |
| --- | --- |

## Public constructors

### PackageItemInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PackageItemInfo()
```

### PackageItemInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PackageItemInfo(orig: PackageItemInfo!)
```

## Protected constructors

### PackageItemInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected PackageItemInfo(source: Parcel!)
```

## Public methods

### loadBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadBanner(pm: PackageManager!): Drawable!
```

Retrieve the current graphical banner associated with this item. This will call back on the given PackageManager to load the banner from the application.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `pm` | [PackageManager](PackageManager.md)!: A PackageManager from which the banner can be loaded; usually the PackageManager from which you originally retrieved this item. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | Returns a Drawable containing the item's banner. If the item does not have a banner, this method will return null. |

### loadIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadIcon(pm: PackageManager!): Drawable!
```

Retrieve the current graphical icon associated with this item. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `pm` | [PackageManager](PackageManager.md)!: A PackageManager from which the icon can be loaded; usually the PackageManager from which you originally retrieved this item. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | Returns a Drawable containing the item's icon. If the item does not have an icon, the item's default icon is returned such as the default activity icon. |

### loadLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadLabel(pm: PackageManager): CharSequence
```

Retrieve the current textual label associated with this item. This will call back on the given PackageManager to load the label from the application.

| Parameters ||
|---|---|
| `pm` | [PackageManager](PackageManager.md): A PackageManager from which the label can be loaded; usually the PackageManager from which you originally retrieved this item. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | Returns a CharSequence containing the item's label. If the item does not have a label, its name is returned. This value cannot be `null`. |

### loadLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadLogo(pm: PackageManager!): Drawable!
```

Retrieve the current graphical logo associated with this item. This will call back on the given PackageManager to load the logo from the application.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `pm` | [PackageManager](PackageManager.md)!: A PackageManager from which the logo can be loaded; usually the PackageManager from which you originally retrieved this item. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | Returns a Drawable containing the item's logo. If the item does not have a logo, this method will return null. |

### loadUnbadgedIcon

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadUnbadgedIcon(pm: PackageManager!): Drawable!
```

Retrieve the current graphical icon associated with this item without the addition of a work badge if applicable. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `pm` | [PackageManager](PackageManager.md)!: A PackageManager from which the icon can be loaded; usually the PackageManager from which you originally retrieved this item. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | Returns a Drawable containing the item's icon. If the item does not have an icon, the item's default icon is returned such as the default activity icon. |

### loadXmlMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadXmlMetaData(
    pm: PackageManager!, 
    name: String!
): XmlResourceParser!
```

Load an XML resource attached to the meta-data of this item. This will retrieved the name meta-data entry, and if defined call back on the given PackageManager to load its XML file from the application.

| Parameters ||
|---|---|
| `pm` | [PackageManager](PackageManager.md)!: A PackageManager from which the XML can be loaded; usually the PackageManager from which you originally retrieved this item. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the meta-date you would like to load. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!` | Returns an XmlPullParser you can use to parse the XML file assigned as the given meta-data. If the meta-data name is not defined or the XML resource could not be found, null is returned. |

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

### banner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var banner: Int
```

A drawable resource identifier (in the package's resources) of this component's banner. From the "banner" attribute or, if not set, 0.

### icon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var icon: Int
```

A drawable resource identifier (in the package's resources) of this component's icon. From the "icon" attribute or, if not set, 0.

### isArchived

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var isArchived: Boolean
```

Whether the package is currently in an archived state.

Packages can be archived through requestArchive and do not have any APKs stored on the device, but do keep the data directory.

### labelRes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var labelRes: Int
```

A string resource identifier (in the package's resources) of this component's label. From the "label" attribute or, if not set, 0.

### logo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var logo: Int
```

A drawable resource identifier (in the package's resources) of this component's logo. Logos may be larger/wider than icons and are displayed by certain UI elements in place of a name or name/icon combination. From the "logo" attribute or, if not set, 0.

### metaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var metaData: Bundle!
```

Additional meta-data associated with this component. This field will only be filled in if you set the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` flag when requesting the info.

### name

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var name: String!
```

Public name of this item. From the "android:name" attribute.

### nonLocalizedLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var nonLocalizedLabel: CharSequence!
```

The string provided in the AndroidManifest file, if any. You probably don't want to use this. You probably want getApplicationLabel

### packageName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var packageName: String!
```

Name of the package that this item is in.
