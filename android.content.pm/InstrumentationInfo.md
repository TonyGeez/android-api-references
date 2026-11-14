Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstrumentationInfo

```
open class InstrumentationInfo : PackageItemInfo, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.pm.PackageItemInfo](PackageItemInfo.md) ||
| | ↳ | [android.content.pm.InstrumentationInfo](InstrumentationInfo.md) |

Information you can retrieve about a particular piece of test instrumentation. This corresponds to information collected from the AndroidManifest.xml's \<instrumentation\> tag.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| InstrumentationInfo <br /> |
| InstrumentationInfo <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

Inherited functions From class PackageItemInfo `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dumpBack

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dumpFront

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` loadBanner

Retrieve the current graphical banner associated with this item. This will call back on the given PackageManager to load the banner from the application.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` loadIcon

Retrieve the current graphical icon associated with this item. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` loadLabel

Retrieve the current textual label associated with this item. This will call back on the given PackageManager to load the label from the application.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` loadLogo

Retrieve the current graphical logo associated with this item. This will call back on the given PackageManager to load the logo from the application.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` loadUnbadgedIcon

Retrieve the current graphical icon associated with this item without the addition of a work badge if applicable. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!` loadXmlMetaData

Load an XML resource attached to the meta-data of this item. This will retrieved the name meta-data entry, and if defined call back on the given PackageManager to load its XML file from the application.

<br />

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InstrumentationInfo](InstrumentationInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#dataDir:kotlin.String` Full path to a directory assigned to the package for its persistent data. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#functionalTest:kotlin.Boolean` Specifies whether or not to run this instrumentation as a functional test |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#handleProfiling:kotlin.Boolean` Specifies whether or not this instrumentation will handle profiling. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#publicSourceDir:kotlin.String` Full path to the publicly available parts of `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#sourceDir:kotlin.String`, including resources and manifest. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#sourceDir:kotlin.String` Full path to the base APK for this application. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitNames:kotlin.Array` The names of all installed split APKs, ordered lexicographically. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitPublicSourceDirs:kotlin.Array` Full path to the publicly available parts of `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitSourceDirs:kotlin.Array`, including resources and manifest. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitSourceDirs:kotlin.Array` Full paths to zero or more split APKs, indexed by the same order as `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitNames:kotlin.Array`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#targetPackage:kotlin.String` The name of the application package being instrumented. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#targetProcesses:kotlin.String` Names of the process(es) this instrumentation will run in. |

Inherited properties From class PackageItemInfo `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#banner:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's banner. From the "banner" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#icon:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's icon. From the "icon" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#isArchived:kotlin.Boolean`

Whether the package is currently in an archived state.

Packages can be archived through requestArchive and do not have any APKs stored on the device, but do keep the data directory.

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

The string provided in the AndroidManifest file, if any. You probably don't want to use this. You probably want getApplicationLabel

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#packageName:kotlin.String`

Name of the package that this item is in.

<br />

## Public constructors

### InstrumentationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InstrumentationInfo()
```

### InstrumentationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InstrumentationInfo(orig: InstrumentationInfo!)
```

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

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
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<InstrumentationInfo!>
```

### dataDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var dataDir: String!
```

Full path to a directory assigned to the package for its persistent data.

### functionalTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var functionalTest: Boolean
```

Specifies whether or not to run this instrumentation as a functional test

### handleProfiling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var handleProfiling: Boolean
```

Specifies whether or not this instrumentation will handle profiling.

### publicSourceDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var publicSourceDir: String!
```

Full path to the publicly available parts of `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#sourceDir:kotlin.String`, including resources and manifest. This may be different from `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#sourceDir:kotlin.String` if an application is forward locked.

### sourceDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var sourceDir: String!
```

Full path to the base APK for this application.

### splitNames

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitNames: Array<String!>!
```

The names of all installed split APKs, ordered lexicographically.

### splitPublicSourceDirs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitPublicSourceDirs: Array<String!>!
```

Full path to the publicly available parts of `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitSourceDirs:kotlin.Array`, including resources and manifest. This may be different from `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitSourceDirs:kotlin.Array` if an application is forward locked.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitSourceDirs:kotlin.Array`

### splitSourceDirs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitSourceDirs: Array<String!>!
```

Full paths to zero or more split APKs, indexed by the same order as `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo#splitNames:kotlin.Array`.

### targetPackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var targetPackage: String!
```

The name of the application package being instrumented. From the "package" attribute.

### targetProcesses

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var targetProcesses: String!
```

Names of the process(es) this instrumentation will run in. If not specified, only runs in the main process of the targetPackage. Can either be a comma-separated list of process names or '\*' for any process that launches to run targetPackage code.
