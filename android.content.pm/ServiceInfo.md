Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceInfo

```
open class ServiceInfo : ComponentInfo, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.content.pm.PackageItemInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo) |||
| | ↳ | [android.content.pm.ComponentInfo](https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo) ||
| | | ↳ | [android.content.pm.ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#) |
| --- | --- | --- | --- |

Information you can retrieve about a particular application service. This corresponds to information collected from the AndroidManifest.xml's \<service\> tags.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_ALLOW_SHARED_ISOLATED_PROCESS:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, and this is an `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int` service, the service is allowed to be bound in a shared isolated process with other isolated services. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_EXTERNAL_SERVICE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the service can be bound and run in the calling application's package, rather than the package in which it is declared. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_ISOLATED_PROCESS:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the service will run in its own isolated process. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_NATIVE_SERVICE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the system does not initialize the Android Runtime in a process which runs the service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_SINGLE_USER:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, a single instance of the service will run for all users on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_STOP_WITH_TASK:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the service will automatically be stopped by the system if the user removes a task that is rooted in one of the application's activities. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_USE_APP_ZYGOTE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the service (which must be isolated) will be spawned from an Application Zygote, instead of the regular Zygote. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_CAMERA:kotlin.Int` Constant corresponding to `camera` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_CONNECTED_DEVICE:kotlin.Int` Constant corresponding to `connectedDevice` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_DATA_SYNC:kotlin.Int` Constant corresponding to `dataSync` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_HEALTH:kotlin.Int` Constant corresponding to `health` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_LOCATION:kotlin.Int` Constant corresponding to `location` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MANIFEST:kotlin.Int` A special value indicates to use all types set in manifest file. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PLAYBACK:kotlin.Int` Constant corresponding to `mediaPlayback` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROCESSING:kotlin.Int` Constant corresponding to `mediaProcessing` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION:kotlin.Int` Constant corresponding to `mediaProjection` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MICROPHONE:kotlin.Int` Constant corresponding to `microphone` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_NONE:kotlin.Int` The default foreground service type if not been set in manifest file. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_PHONE_CALL:kotlin.Int` Constant corresponding to `phoneCall` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_REMOTE_MESSAGING:kotlin.Int` Constant corresponding to `remoteMessaging` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` A foreground service type for "short-lived" services, which corresponds to `shortService` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute in the manifest. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SPECIAL_USE:kotlin.Int` Constant corresponding to `specialUse` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SYSTEM_EXEMPTED:kotlin.Int` Constant corresponding to `systemExempted` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#ServiceInfo()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#ServiceInfo(android.content.pm.ServiceInfo)(orig: https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#!)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#dump(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#getForegroundServiceType()()` Return foreground service type specified in the manifest. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#dumpBack(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#dumpFront(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getBannerResource()()`

Return the banner resource identifier to use for this component. If the component defines a banner, that is used; else, the application banner is used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getIconResource()()`

Return the icon resource identifier to use for this component. If the component defines an icon, that is used; else, the application icon is used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getLogoResource()()`

Return the logo resource identifier to use for this component. If the component defines a logo, that is used; else, the application logo is used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#isEnabled()()`

Return whether this component and its enclosing application are enabled.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadBanner(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

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
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int` Options that have been set in the service declaration in the manifest. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#permission:kotlin.String` Optional name of a permission required to be able to access this Service. |
| --- | --- |

Inherited properties From class `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo` `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo!` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#applicationInfo:android.content.pm.ApplicationInfo`

Global information about the application/package this component is a part of.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#attributionTags:kotlin.Array`

Set of attribution tags that should be automatically applied to this component.

When this component represents an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, `https://developer.android.com/reference/kotlin/android/app/Service.html#`, `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` or `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#`, each instance will be automatically configured with `https://developer.android.com/reference/kotlin/android/content/Context.html#createAttributionContext(kotlin.String)` using the first attribution tag contained here.

Additionally, when this component represents a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` and the sender of a broadcast requires the receiver to hold one or more specific permissions, those permission checks will be performed using each of the attributions tags contained here.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#descriptionRes:kotlin.Int`

A string resource identifier (in the package's resources) containing a user-readable description of the component. From the "description" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#directBootAware:kotlin.Boolean`

Indicates if this component is aware of direct boot lifecycle, and can be safely run before the user has entered their credentials (such as a lock pattern or PIN).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#enabled:kotlin.Boolean`

Indicates whether or not this component may be instantiated. Note that this value can be overridden by the one in its parent `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#exported:kotlin.Boolean`

Set to true if this component is available for use by other applications. Comes from `https://developer.android.com/reference/kotlin/android/R.attr.html#exported:kotlin.Int` of the \<activity\>, \<receiver\>, \<service\>, or \<provider\> tag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#processName:kotlin.String`

The name of the process this component should run in. From the "android:process" attribute or, if not set, the same as applicationInfo.processName.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#splitName:kotlin.String`

The name of the split in which this component is declared. Null if the component was declared in the base APK.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#banner:kotlin.Int`

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

## Constants

### FLAG_ALLOW_SHARED_ISOLATED_PROCESS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOW_SHARED_ISOLATED_PROCESS: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, and this is an `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int` service, the service is allowed to be bound in a shared isolated process with other isolated services. Note that these other isolated services can also belong to other apps from different vendors. Shared isolated processes are created when using the `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int` during service binding. Note that when this flag is used, the `https://developer.android.com/reference/kotlin/android/R.attr.html#process:kotlin.Int` attribute is ignored when the process is bound into a shared isolated process by a client.

 Value: 16

### FLAG_EXTERNAL_SERVICE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_EXTERNAL_SERVICE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the service can be bound and run in the calling application's package, rather than the package in which it is declared. Set from `https://developer.android.com/reference/kotlin/android/R.attr.html#externalService:kotlin.Int` attribute.

 Value: 4

### FLAG_ISOLATED_PROCESS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ISOLATED_PROCESS: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the service will run in its own isolated process. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int` attribute.

 Value: 2

### FLAG_NATIVE_SERVICE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_NATIVE_SERVICE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the system does not initialize the Android Runtime in a process which runs the service. Instead the system loads a library into the process and then starts the service from the entrypoint function in the library. The library and the entrypoint names are specified in metadata to the service tag. This flag is ignored if `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_ISOLATED_PROCESS:kotlin.Int` is false or isn't specified. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#nativeService:kotlin.Int` attribute.

 Value: 32

### FLAG_SINGLE_USER

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SINGLE_USER: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, a single instance of the service will run for all users on the device. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#singleUser:kotlin.Int` attribute.

 Value: 1073741824

### FLAG_STOP_WITH_TASK

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_STOP_WITH_TASK: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the service will automatically be stopped by the system if the user removes a task that is rooted in one of the application's activities. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#stopWithTask:kotlin.Int` attribute.

 Value: 1

### FLAG_USE_APP_ZYGOTE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_USE_APP_ZYGOTE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#flags:kotlin.Int`: If set, the service (which must be isolated) will be spawned from an Application Zygote, instead of the regular Zygote. The Application Zygote will pre-initialize the application's class loader, and call a static callback into the application to allow it to perform application-specific preloads (such as loading a shared library). Therefore, spawning from the Application Zygote will typically reduce the service launch time and reduce its memory usage. The downside of using this flag is that you will have an additional process (the app zygote itself) that is taking up memory. Whether actual memory usage is improved therefore strongly depends on the number of isolated services that an application starts, and how much memory those services save by preloading. Therefore, it is recommended to measure memory usage under typical workloads to determine whether it makes sense to use this flag.

 Value: 8

### FOREGROUND_SERVICE_TYPE_CAMERA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_CAMERA: Int
```

Constant corresponding to `camera` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Use the camera device or record video. For apps with `targetSdkVersion` `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` and above, a foreground service will not be able to access the camera if this type is not specified in the manifest and in `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification,%20kotlin.Int)`.

Starting foreground service with this type from apps targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and later, will require permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_CAMERA:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String`.

 Value: 64

### FOREGROUND_SERVICE_TYPE_CONNECTED_DEVICE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_CONNECTED_DEVICE: Int
```

Constant corresponding to `connectedDevice` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Auto, bluetooth, TV or other devices connection, monitoring and interaction.

Starting foreground service with this type from apps targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and later, will require permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_CONNECTED_DEVICE:kotlin.String` and one of the following permissions: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_NETWORK_STATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_MULTICAST_STATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#TRANSMIT_IR:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#UWB_RANGING:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RANGING:kotlin.String`, or has been granted the access to one of the attached USB devices/accessories.

 Value: 16

### FOREGROUND_SERVICE_TYPE_DATA_SYNC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_DATA_SYNC: Int
```

Constant corresponding to `dataSync` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Data(photo, file, account) upload/download, backup/restore, import/export, fetch, transfer over network between device and cloud.

This type has time limit of 6 hours starting from Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`. A foreground service of this type must be stopped within the timeout by `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` or their overloads). `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)` will also work, which will demote the service to a "background" service, which will soon be stopped by the system.

If the service isn't stopped within the timeout, `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)` will be called.

Also note, even though `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_DATA_SYNC:kotlin.Int` can be used on Android versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, since `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)` did not exist on such versions, it will never be called. Because of this, developers must make sure to stop the foreground service even if `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)` is not called on such versions.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)`

### FOREGROUND_SERVICE_TYPE_HEALTH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_HEALTH: Int
```

Constant corresponding to `health` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Health, wellness and fitness.

The caller app is required to have the permissions `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_HEALTH:kotlin.String` and one of the following permissions: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACTIVITY_RECOGNITION:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#HIGH_SAMPLING_RATE_SENSORS:kotlin.String`. `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions.html#READ_HEART_RATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions.html#READ_SKIN_TEMPERATURE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions.html#READ_OXYGEN_SATURATION:kotlin.String`, `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions.html#READ_BLOOD_PRESSURE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions.html#READ_HEART_RATE_VARIABILITY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions.html#READ_RESPIRATORY_RATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions.html#READ_VO2_MAX:kotlin.String`,. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_HEALTH:kotlin.String`

 Value: 256

### FOREGROUND_SERVICE_TYPE_LOCATION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_LOCATION: Int
```

Constant corresponding to `location` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. GPS, map, navigation location update.

Starting foreground service with this type from apps targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and later, will require permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_LOCATION:kotlin.String` and one of the following permissions: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

 Value: 8

### FOREGROUND_SERVICE_TYPE_MANIFEST

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_MANIFEST: Int
```

A special value indicates to use all types set in manifest file.

 Value: -1

### FOREGROUND_SERVICE_TYPE_MEDIA_PLAYBACK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_MEDIA_PLAYBACK: Int
```

Constant corresponding to `mediaPlayback` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Music, video, news or other media playback.

Starting foreground service with this type from apps targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and later, will require permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_MEDIA_PLAYBACK:kotlin.String`.

 Value: 2

### FOREGROUND_SERVICE_TYPE_MEDIA_PROCESSING

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_MEDIA_PROCESSING: Int
```

Constant corresponding to `mediaProcessing` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Media processing use cases such as video or photo editing and processing. This type has time limit of 6 hours. A foreground service of this type must be stopped within the timeout by `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` or their overloads). `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)` will also work, which will demote the service to a "background" service, which will soon be stopped by the system.

If the service isn't stopped within the timeout, `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)` will be called.

Also note, even though `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROCESSING:kotlin.Int` was added in Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, it can be also used on prior android versions (just like other new foreground service types can be used). However, because `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)` did not exist on prior versions, it will never be called on such versions. Because of this, developers must make sure to stop the foreground service even if `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)` is not called on such versions. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_MEDIA_PROCESSING:kotlin.String`

 Value: 8192

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)`

### FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION: Int
```

Constant corresponding to `mediaProjection` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute.

To capture through `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.html#`, an app must start a foreground service with the type corresponding to this constant. This type should only be used for `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.html#`. Capturing screen contents via `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.html#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20android.hardware.display.VirtualDisplay.Callback,%20android.os.Handler)` conveniently allows recording, presenting screen contents into a meeting, taking screenshots, or several other scenarios.

Starting foreground service with this type from apps targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and later, will require permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_MEDIA_PROJECTION:kotlin.String`, and the user must have allowed the screen capture request from this app.

 Value: 32

### FOREGROUND_SERVICE_TYPE_MICROPHONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_MICROPHONE: Int
```

Constant corresponding to `microphone` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Use the microphone device or record audio. For apps with `targetSdkVersion` `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` and above, a foreground service will not be able to access the microphone if this type is not specified in the manifest and in `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification,%20kotlin.Int)`.

Starting foreground service with this type from apps targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and later, will require permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_MICROPHONE:kotlin.String` and one of the following permissions: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAPTURE_AUDIO_OUTPUT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECORD_AUDIO:kotlin.String`.

 Value: 128

### FOREGROUND_SERVICE_TYPE_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_NONE: Int
```

**Deprecated:** *Do not use.*

The default foreground service type if not been set in manifest file.

Apps targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and later should NOT use this type, calling `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification,%20kotlin.Int)` with this type will get a `https://developer.android.com/reference/kotlin/android/app/InvalidForegroundServiceTypeException.html#`.

 Value: 0

### FOREGROUND_SERVICE_TYPE_PHONE_CALL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_PHONE_CALL: Int
```

Constant corresponding to `phoneCall` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Ongoing operations related to phone calls, video conferencing, or similar interactive communication.

Starting foreground service with this type from apps targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and later, will require permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_PHONE_CALL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String` or holding the default `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_DIALER:kotlin.String`.

 Value: 4

### FOREGROUND_SERVICE_TYPE_REMOTE_MESSAGING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_REMOTE_MESSAGING: Int
```

Constant corresponding to `remoteMessaging` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Messaging use cases which host local server to relay messages across devices. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_REMOTE_MESSAGING:kotlin.String`

 Value: 512

### FOREGROUND_SERVICE_TYPE_SHORT_SERVICE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_SHORT_SERVICE: Int
```

A foreground service type for "short-lived" services, which corresponds to `shortService` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute in the manifest.

Unlike other foreground service types, this type is not associated with a specific use case, and it will not require any special permissions (besides `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE:kotlin.String`). However, this type has the following restrictions.

- The type has a 3 minute timeout. A foreground service of this type must be stopped within the timeout by `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` or their overloads). `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)` will also work, which will demote the service to a "background" service, which will soon be stopped by the system.

 If the service isn't stopped within the timeout, `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)` will be called. Note, even when the system calls this callback, it will not stop the service automatically. You still need to stop the service using one of the aforementioned ways even when you get this callback.

 If the service is still not stopped after the callback, the app will be declared an ANR, after a short grace period of several seconds.
- A foreground service of this type cannot be made "sticky" (see `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int`). That is, if an app is killed due to a crash or out-of memory while it's running a short foregorund-service, the system will not restart the service.
- Other foreground services cannot be started from short foreground services. Unlike other foreground service types, when an app is running in the background while only having a "short" foreground service, it's not allowed to start other foreground services, due to the restriction describe here: [FOREGROUND_SERVICE_TYPE_SHORT_SERVICE](https://developer.android.com/guide/components/foreground-services#background-start-restrictions>
 Restrictions on background starts
 </a>
 <li>
 You can combine multiple foreground services types with <code>|</code>s, and you can
| --- | --- |
 combine
 <code><a docref=). with other types as well. However, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` is for situations where you have no other valid foreground services to use and the timeout is long enough for the task, and if you can use other types, there's no point using this type. For this reason, if `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` is combined with other foreground service types, the system will simply ignore it, and as a result, none of the above restrictions will apply (e.g. there'll be no timeout).

Also note, even though `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` was added on Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, it can be also used on on prior android versions (just like other new foreground service types can be used). However, because `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)` did not exist on prior versions, it will never called on such versions. Because of this, developers must make sure to stop the foreground service even if `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)` is not called on such versions.

 Value: 2048

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)`

### FOREGROUND_SERVICE_TYPE_SPECIAL_USE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_SPECIAL_USE: Int
```

Constant corresponding to `specialUse` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. Use cases that can't be categorized into any other foreground service types, but also can't use `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#` APIs.

The use of this foreground service type may be restricted. Additionally, apps must declare a service-level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PROPERTY_SPECIAL_USE_FGS_SUBTYPE:kotlin.String` in `AndroidManifest.xml` as a hint of what the exact use case here is. Here is an example:

```kotlin
<uses-permission
       android:name="android.permission.FOREGROUND_SERVICE_SPECIAL_USE"
   />
   <service
       android:name=".MySpecialForegroundService"
       android:foregroundServiceType="specialUse">
       <property
           android:name="android.app.PROPERTY_SPECIAL_USE_FGS_SUBTYPE"
           android:value="foo"
       />
  </service>
  
```
In a future release of Android, if the above foreground service type `foo` is supported by the platform, to offer the backward compatibility, the app could specify the `android:maxSdkVersion` attribute in the \<uses-permission\> section, and also add the foreground service type `foo` into the `android:foregroundServiceType`, therefore the same app could be installed in both platforms.

```kotlin
<uses-permission
       android:name="android.permission.FOREGROUND_SERVICE_SPECIAL_USE"
       android:maxSdkVersion="last_sdk_version_without_type_foo"
   />
   <service
       android:name=".MySpecialForegroundService"
       android:foregroundServiceType="specialUse|foo">
       <property
           android:name="android.app.PROPERTY_SPECIAL_USE_FGS_SUBTYPE"
           android:value="foo"
       />
  </service>
  
```
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_SPECIAL_USE:kotlin.String`

 Value: 1073741824

### FOREGROUND_SERVICE_TYPE_SYSTEM_EXEMPTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_TYPE_SYSTEM_EXEMPTED: Int
```

Constant corresponding to `systemExempted` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` attribute. The system exempted foreground service use cases.

Note, apps are allowed to use this type only in the following cases:

- App has a UID \< `https://developer.android.com/reference/kotlin/android/os/Process.html#FIRST_APPLICATION_UID:kotlin.Int`
- App is on Doze allowlist
- Device is running in [Demo Mode](https://android.googlesource.com/platform/frameworks/base/+/master/packages/SystemUI/docs/demo_mode.md)
- [Device owner app](https://source.android.com/devices/tech/admin/provision)
- [Profile owner apps](https://source.android.com/devices/tech/admin/managed-profiles)
- Persistent apps
- [Carrier privileged apps](https://source.android.com/docs/core/connect/carrier)
- Apps that have the `android.app.role.RoleManager#ROLE_EMERGENCY` role
- Headless system apps
- [Device admin apps](https://developer.android.com/guide/topics/admin/device-admin)
- Active VPN apps
- Apps holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_EXACT_ALARM:kotlin.String` permission.

<br />

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE_SYSTEM_EXEMPTED:kotlin.String`

 Value: 1024

## Public constructors

### ServiceInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ServiceInfo()
```

### ServiceInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ServiceInfo(orig: ServiceInfo!)
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

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```

### getForegroundServiceType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getForegroundServiceType(): Int
```

Return foreground service type specified in the manifest..

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | foreground service type specified in the manifest. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MANIFEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_DATA_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PLAYBACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_PHONE_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_LOCATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_CONNECTED_DEVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_CAMERA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MICROPHONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_HEALTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_REMOTE_MESSAGING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SYSTEM_EXEMPTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROCESSING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SPECIAL_USE:kotlin.Int` |

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

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ServiceInfo!>
```

### flags

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var flags: Int
```

Options that have been set in the service declaration in the manifest. These include: `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_STOP_WITH_TASK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_ISOLATED_PROCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_SINGLE_USER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FLAG_NATIVE_SERVICE:kotlin.Int`.

### permission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var permission: String!
```

Optional name of a permission required to be able to access this Service. From the "permission" attribute.
