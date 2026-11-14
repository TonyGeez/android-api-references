Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppWidgetProviderInfo

Kotlin | [Java](AppWidgetProviderInfo.md)
| --- | --- |

```
open class AppWidgetProviderInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.appwidget.AppWidgetProviderInfo](AppWidgetProviderInfo.md) |

Describes the meta data for an installed AppWidget provider. The fields in this class correspond to the fields in the `<appwidget-provider>` xml tag.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_BOTH:kotlin.Int` Widget is resizable in both the horizontal and vertical axes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_HORIZONTAL:kotlin.Int` Widget is resizable in the horizontal axis only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_NONE:kotlin.Int` Widget is not resizable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_VERTICAL:kotlin.Int` Widget is resizable in the vertical axis only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_HOME_SCREEN:kotlin.Int` Indicates that the widget can be displayed on the home screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int` Indicates that the widget can be displayed on the keyguard. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_NOT_KEYGUARD:kotlin.Int` Indicates that the widget should never be shown on the keyguard. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_SEARCHBOX:kotlin.Int` Indicates that the widget can be displayed within a space reserved for the search box. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_CONFIGURATION_OPTIONAL:kotlin.Int` The widget provides a default configuration. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_HIDE_FROM_PICKER:kotlin.Int` The widget is added directly by the app, and the host may hide this widget when providing the user with the list of available widgets to choose from. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_RECONFIGURABLE:kotlin.Int` The widget can be reconfigured anytime after it is bound by starting the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#configure:android.content.ComponentName` activity. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| AppWidgetProviderInfo <br /> |
| AppWidgetProviderInfo Unflatten the AppWidgetProviderInfo from a parcel. |

| Public methods ||
|---|---|
| open [AppWidgetProviderInfo](AppWidgetProviderInfo.md)! | clone Creates and returns a copy of this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [ActivityInfo](../android.content.pm/ActivityInfo.md) | getActivityInfo Returns the broadcast receiver that is providing this widget. |
| --- | --- |
| [UserHandle](../android.os/UserHandle.md)! | getProfile Gets the user profile in which the provider resides. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | loadDescription Loads localized description for the app widget. |
| [Drawable](../android.graphics.drawable/Drawable.md)! | loadIcon Loads the icon to display for this AppWidget in the AppWidget picker. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | loadLabel Loads the localized label to display to the user in the AppWidget picker. |
| [Drawable](../android.graphics.drawable/Drawable.md)! | loadPreviewImage Loads a preview of what the AppWidget will look like after it's configured. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AppWidgetProviderInfo](AppWidgetProviderInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#CREATOR:android.os.Parcelable.Creator` Parcelable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#autoAdvanceViewId:kotlin.Int` The view id of the AppWidget subview which should be auto-advanced by the widget's host. |
| [ComponentName](../android.content/ComponentName.md)! | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#configure:android.content.ComponentName` The activity to launch that will configure the AppWidget. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#descriptionRes:kotlin.Int` Resource id for the description of the AppWidget. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#generatedPreviewCategories:kotlin.Int` Flags indicating the widget categories for which generated previews are available. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#icon:kotlin.Int` The icon to display for this AppWidget in the AppWidget picker. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#initialKeyguardLayout:kotlin.Int` The resource id of the initial layout for this AppWidget when it is displayed on keyguard. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#initialLayout:kotlin.Int` The resource id of the initial layout for this AppWidget. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#label:kotlin.String` The label to display to the user in the AppWidget picker. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#maxResizeHeight:kotlin.Int` Maximum height (in px) which the widget can be resized to. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#maxResizeWidth:kotlin.Int` Maximum width (in px) which the widget can be resized to. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#minHeight:kotlin.Int` The default height of the widget when added to a host, in px. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#minResizeHeight:kotlin.Int` Minimum height (in px) which the widget can be resized to. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#minResizeWidth:kotlin.Int` Minimum width (in px) which the widget can be resized to. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#minWidth:kotlin.Int` The default width of the widget when added to a host, in px. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#previewImage:kotlin.Int` A preview of what the AppWidget will look like after it's configured. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#previewLayout:kotlin.Int` The layout resource id of a preview of what the AppWidget will look like after it's configured. |
| [ComponentName](../android.content/ComponentName.md)! | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#provider:android.content.ComponentName` Identity of this AppWidget component. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#resizeMode:kotlin.Int` The rules by which a widget can be resized. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#targetCellHeight:kotlin.Int` The default height of a widget when added to a host, in units of launcher grid cells. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#targetCellWidth:kotlin.Int` The default width of a widget when added to a host, in units of launcher grid cells. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#updatePeriodMillis:kotlin.Int` How often, in milliseconds, that this AppWidget wants to be updated. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#widgetCategory:kotlin.Int` Determines whether this widget can be displayed on the home screen, the keyguard, or both. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#widgetFeatures:kotlin.Int` Flags indicating various features supported by the widget. |
| --- | --- |

## Constants

### RESIZE_BOTH

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESIZE_BOTH: Int
```

Widget is resizable in both the horizontal and vertical axes.

 Value: 3

### RESIZE_HORIZONTAL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESIZE_HORIZONTAL: Int
```

Widget is resizable in the horizontal axis only.

 Value: 1

### RESIZE_NONE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESIZE_NONE: Int
```

Widget is not resizable.

 Value: 0

### RESIZE_VERTICAL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESIZE_VERTICAL: Int
```

Widget is resizable in the vertical axis only.

 Value: 2

### WIDGET_CATEGORY_HOME_SCREEN

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_CATEGORY_HOME_SCREEN: Int
```

Indicates that the widget can be displayed on the home screen. This is the default value.

 Value: 1

### WIDGET_CATEGORY_KEYGUARD

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_CATEGORY_KEYGUARD: Int
```

Indicates that the widget can be displayed on the keyguard.

 Value: 2

### WIDGET_CATEGORY_NOT_KEYGUARD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_CATEGORY_NOT_KEYGUARD: Int
```

Indicates that the widget should never be shown on the keyguard.

Some keyguard style features may decide that `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int` isn't required to be added by an app to show on the feature when chosen by a user. This category allows for a stronger statement about placement of the widget that, even in the above case, this widget should not be offered on the keyguard.

Setting this category doesn't change the behavior of AppWidgetManager queries, it is the responsibility of the widget surface to respect this value.

 Value: 8

### WIDGET_CATEGORY_SEARCHBOX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_CATEGORY_SEARCHBOX: Int
```

Indicates that the widget can be displayed within a space reserved for the search box.

 Value: 4

### WIDGET_FEATURE_CONFIGURATION_OPTIONAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_FEATURE_CONFIGURATION_OPTIONAL: Int
```

The widget provides a default configuration. The host may choose not to launch the provided configuration activity.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#widgetFeatures:kotlin.Int`

### WIDGET_FEATURE_HIDE_FROM_PICKER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_FEATURE_HIDE_FROM_PICKER: Int
```

The widget is added directly by the app, and the host may hide this widget when providing the user with the list of available widgets to choose from.

 Value: 2

**See Also**

- requestPinAppWidget
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#widgetFeatures:kotlin.Int`

### WIDGET_FEATURE_RECONFIGURABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_FEATURE_RECONFIGURABLE: Int
```

The widget can be reconfigured anytime after it is bound by starting the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#configure:android.content.ComponentName` activity.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#widgetFeatures:kotlin.Int`

## Public constructors

### AppWidgetProviderInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AppWidgetProviderInfo()
```

### AppWidgetProviderInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AppWidgetProviderInfo(in: Parcel!)
```

Unflatten the AppWidgetProviderInfo from a parcel.

## Public methods

### clone

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): AppWidgetProviderInfo!
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#!` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getActivityInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityInfo(): ActivityInfo
```

Returns the broadcast receiver that is providing this widget.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#` | This value cannot be `null`. |

### getProfile

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProfile(): UserHandle!
```

Gets the user profile in which the provider resides.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!` | The hosting user profile. |

### loadDescription

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadDescription(context: Context): CharSequence?
```

Loads localized description for the app widget.

Description is intended to be displayed in the UI of the widget picker.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): Context for accessing resources. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | CharSequence for app widget description for the current locale. This value may be `null`. |

### loadIcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadIcon(
    context: Context, 
    density: Int
): Drawable!
```

Loads the icon to display for this AppWidget in the AppWidget picker. If not supplied in the xml, the application icon will be used. A client can optionally provide a desired density such as `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#DENSITY_LOW:kotlin.Int` `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#DENSITY_MEDIUM:kotlin.Int`, etc. If no density is provided, the density of the current display will be used.

The loaded icon corresponds to the `android:icon` attribute in the `<receiver>` element in the AndroidManifest.xml file.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): Context for accessing resources. This value cannot be `null`. |
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The optional desired density as per `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#densityDpi:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | The provider icon. |

### loadLabel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadLabel(packageManager: PackageManager!): String!
```

Loads the localized label to display to the user in the AppWidget picker.

| Parameters ||
|---|---|
| `packageManager` | [PackageManager](../android.content.pm/PackageManager.md)!: Package manager instance for loading resources. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The label for the current locale. |

### loadPreviewImage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadPreviewImage(
    context: Context, 
    density: Int
): Drawable!
```

Loads a preview of what the AppWidget will look like after it's configured. A client can optionally provide a desired density such as `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#DENSITY_LOW:kotlin.Int` `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#DENSITY_MEDIUM:kotlin.Int`, etc. If no density is provided, the density of the current display will be used.

The loaded image corresponds to the `android:previewImage` attribute in the `<receiver>` element in the AndroidManifest.xml file.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): Context for accessing resources. This value cannot be `null`. |
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The optional desired density as per `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#densityDpi:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | The widget preview image or null if preview image is not available. |

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    out: Parcel, 
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

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AppWidgetProviderInfo!>
```

Parcelable.Creator that instantiates AppWidgetProviderInfo objects

### autoAdvanceViewId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var autoAdvanceViewId: Int
```

The view id of the AppWidget subview which should be auto-advanced by the widget's host.

This field corresponds to the `android:autoAdvanceViewId` attribute in the AppWidget meta-data file.

### configure

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var configure: ComponentName!
```

The activity to launch that will configure the AppWidget.

This class name of field corresponds to the `android:configure` attribute in the AppWidget meta-data file. The package name always corresponds to the package containing the AppWidget provider.

### descriptionRes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var descriptionRes: Int
```

Resource id for the description of the AppWidget.

This field corresponds to the `android:description` attribute in the AppWidget meta-data file.

### generatedPreviewCategories

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var generatedPreviewCategories: Int
```

Flags indicating the widget categories for which generated previews are available. These correspond to the previews set by this provider with setWidgetPreview.
**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_HOME_SCREEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_SEARCHBOX:kotlin.Int`
- getWidgetPreview

### icon

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var icon: Int
```

The icon to display for this AppWidget in the AppWidget picker. If not supplied in the xml, the application icon will be used.

This field corresponds to the `android:icon` attribute in the `<receiver>` element in the AndroidManifest.xml file.

### initialKeyguardLayout

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var initialKeyguardLayout: Int
```

The resource id of the initial layout for this AppWidget when it is displayed on keyguard. This parameter only needs to be provided if the widget can be displayed on the keyguard, see `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#widgetCategory:kotlin.Int`.

This field corresponds to the `android:initialKeyguardLayout` attribute in the AppWidget meta-data file.

### initialLayout

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var initialLayout: Int
```

The resource id of the initial layout for this AppWidget. This should be displayed until the RemoteViews for the AppWidget is available.

This field corresponds to the `android:initialLayout` attribute in the AppWidget meta-data file.

### label

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var label: String!
```

**Deprecated:** *Use loadLabel.*

The label to display to the user in the AppWidget picker.

### maxResizeHeight

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var maxResizeHeight: Int
```

Maximum height (in px) which the widget can be resized to. This field has no effect if it is smaller than minHeight or if vertical resizing isn't enabled (see `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#resizeMode:kotlin.Int`).

This field corresponds to the `android:maxResizeHeight` attribute in the AppWidget meta-data file.

### maxResizeWidth

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var maxResizeWidth: Int
```

Maximum width (in px) which the widget can be resized to. This field has no effect if it is smaller than minWidth or if horizontal resizing isn't enabled (see `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#resizeMode:kotlin.Int`).

This field corresponds to the `android:maxResizeWidth` attribute in the AppWidget meta-data file.

### minHeight

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var minHeight: Int
```

The default height of the widget when added to a host, in px. The widget will get at least this height, and will often be given more, depending on the host.

This field corresponds to the `android:minHeight` attribute in the AppWidget meta-data file.

### minResizeHeight

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var minResizeHeight: Int
```

Minimum height (in px) which the widget can be resized to. This field has no effect if it is greater than minHeight or if vertical resizing isn't enabled (see `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#resizeMode:kotlin.Int`).

This field corresponds to the `android:minResizeHeight` attribute in the AppWidget meta-data file.

### minResizeWidth

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var minResizeWidth: Int
```

Minimum width (in px) which the widget can be resized to. This field has no effect if it is greater than minWidth or if horizontal resizing isn't enabled (see `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#resizeMode:kotlin.Int`).

This field corresponds to the `android:minResizeWidth` attribute in the AppWidget meta-data file.

### minWidth

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var minWidth: Int
```

The default width of the widget when added to a host, in px. The widget will get at least this width, and will often be given more, depending on the host.

This field corresponds to the `android:minWidth` attribute in the AppWidget meta-data file.

### previewImage

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var previewImage: Int
```

A preview of what the AppWidget will look like after it's configured. If not supplied, the AppWidget's icon will be used.

This field corresponds to the `android:previewImage` attribute in the AppWidget meta-data file.

### previewLayout

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var previewLayout: Int
```

The layout resource id of a preview of what the AppWidget will look like after it's configured.

Unlike previewImage, previewLayout can better showcase AppWidget in different locales, system themes, display sizes \& density etc.

If supplied, this will take precedence over the previewImage on supported widget hosts. Otherwise, previewImage will be used.

This field corresponds to the `android:previewLayout` attribute in the AppWidget meta-data file.

### provider

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var provider: ComponentName!
```

Identity of this AppWidget component. This component should be a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#`, and it will be sent the AppWidget intents `https://developer.android.com/reference/kotlin/android/appwidget/package-summary`.

This field corresponds to the `android:name` attribute in the `<receiver>` element in the AndroidManifest.xml file.

### resizeMode

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var resizeMode: Int
```

The rules by which a widget can be resized. See `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_HORIZONTAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_VERTICAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_BOTH:kotlin.Int`.

This field corresponds to the `android:resizeMode` attribute in the AppWidget meta-data file. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_HORIZONTAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#RESIZE_VERTICAL:kotlin.Int`

### targetCellHeight

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var targetCellHeight: Int
```

The default height of a widget when added to a host, in units of launcher grid cells.

This field corresponds to the `android:targetCellHeight` attribute in the AppWidget meta-data file.

### targetCellWidth

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var targetCellWidth: Int
```

The default width of a widget when added to a host, in units of launcher grid cells.

This field corresponds to the `android:targetCellWidth` attribute in the AppWidget meta-data file.

### updatePeriodMillis

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var updatePeriodMillis: Int
```

How often, in milliseconds, that this AppWidget wants to be updated. The AppWidget manager may place a limit on how often a AppWidget is updated.

This field corresponds to the `android:updatePeriodMillis` attribute in the AppWidget meta-data file.

**Note:** Updates requested with `updatePeriodMillis` will not be delivered more than once every 30 minutes.

### widgetCategory

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var widgetCategory: Int
```

Determines whether this widget can be displayed on the home screen, the keyguard, or both. A widget which is displayed on both needs to ensure that it follows the design guidelines for both widget classes. This can be achieved by querying the AppWidget options in its widget provider's update method.

This field corresponds to the `widgetCategory` attribute in the AppWidget meta-data file. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_HOME_SCREEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_SEARCHBOX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_NOT_KEYGUARD:kotlin.Int`

### widgetFeatures

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var widgetFeatures: Int
```

Flags indicating various features supported by the widget. These are hints to the widget host, and do not actually change the behavior of the widget. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_RECONFIGURABLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_HIDE_FROM_PICKER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_CONFIGURATION_OPTIONAL:kotlin.Int`

<br />

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_RECONFIGURABLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_HIDE_FROM_PICKER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_FEATURE_CONFIGURATION_OPTIONAL:kotlin.Int`
