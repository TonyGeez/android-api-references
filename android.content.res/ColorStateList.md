# ColorStateList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorStateList

Kotlin| [Java](../android/content/res/ColorStateList.md) 
| --- | --- |

```
open class ColorStateList : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.res.ColorStateList](../android/content/res/ColorStateList.md) |

Lets you map [android.view.View](../android/view/View.md) state sets to colors.

[android.content.res.ColorStateList](../android/content/res/ColorStateList.md) s are created from XML resource files defined in the "color" subdirectory directory of an application's resource directory. The XML file contains a single "selector" element with a number of "item" elements inside. For example: 

```kotlin
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:state_focused="true"
            android:color="@color/sample_focused" />
    <item android:state_pressed="true"
            android:state_enabled="false"
            android:color="@color/sample_disabled_pressed" />
    <item android:state_enabled="false"
            android:color="@color/sample_disabled_not_pressed" />
    <item android:color="@color/sample_default" />
  </selector>
  
```
This defines a set of state spec / color pairs where each state spec specifies a set of states that a view must either be in or not be in and the color specifies the color associated with that spec.

### State specs

Each item defines a set of state spec and color pairs, where the state spec is a series of attributes set to either`true`or`false`to represent inclusion or exclusion. If an attribute is not specified for an item, it may be any value.

For example, the following item will be matched whenever the focused state is set; any other states may be set or unset: 

```kotlin
<item android:state_focused="true"
          android:color="@color/sample_focused" />
  
```

Typically, a color state list will reference framework-defined state attributes such as [android:state_focused](../android/R.attr.md) or [android:state_enabled](../android/R.attr.md); however, app-defined attributes may also be used.

**Note:**The list of state specs will be matched against in the order that they appear in the XML file. For this reason, more-specific items should be placed earlier in the file. An item with no state spec is considered to match any set of states and is generally useful as a final item to be used as a default.

If an item with no state spec is placed before other items, those items will be ignored.

### Item attributes

Each item must define an [android:color](../android/R.attr.md) attribute, which may be an HTML-style hex color, a reference to a color resource, or -- in API 23 and above -- a theme attribute that resolves to a color.

Starting with API 23, items may optionally define an [android:alpha](../android/R.attr.md) attribute to modify the base color's opacity. This attribute takes a either floating-point value between 0 and 1 or a theme attribute that resolves as such. The item's overall color is calculated by multiplying by the base color's alpha channel by the`alpha`value. For example, the following item represents the theme's accent color at 50% opacity: 

```kotlin
<item android:state_enabled="false"
          android:color="?android:attr/colorAccent"
          android:alpha="0.5" />
  
```

Starting with API 31, items may optionally define an [android:lStar](../android/R.attr.md) attribute to modify the base color's perceptual luminance. This attribute takes either a floating-point value between 0 and 100 or a theme attribute that resolves as such. The item's overall color is calculated by converting the base color to an accessibility friendly color space and setting its L\* to the value specified on the`lStar`attribute. For example, the following item represents the theme's accent color at 50% perceptual luminance: 

```kotlin
<item android:state_enabled="false"
          android:color="?android:attr/colorAccent"
          android:lStar="50" />
  
```

### Developer guide

For more information, see the guide to [Color State List Resource](https://developer.android.com/guide/topics/resources/color-list-resource.html).

## Summary

| XML attributes ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [`android:alpha`](../android/content/res/ColorStateList.md) | Alpha multiplier applied to the base color. |
| [`android:color`](../android/content/res/ColorStateList.md) | Base color for this state. |
| [`android:lStar`](../android/content/res/ColorStateList.md) | Perceptual luminance applied to the base color. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ColorStateList](../android/content/res/ColorStateList.md))`(`states:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!>!`, `colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Creates a ColorStateList that returns the specified mapping from states to colors. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ColorStateList](../android/content/res/ColorStateList.md) | [createFromXml](../android/content/res/ColorStateList.md))`(`r:` ` [Resources](../android/content/res/Resources.md)!`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)!`)` Creates a ColorStateList from an XML document. |
| openstatic [ColorStateList](../android/content/res/ColorStateList.md) | [createFromXml](../android/content/res/ColorStateList.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Creates a ColorStateList from an XML document using given a set of [Resources](../android/content/res/Resources.md) and a [Theme](../android/content/res/Resources.Theme.md). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/content/res/ColorStateList.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](../android/content/res/ColorStateList.md))`()` Returns a mask of the configuration parameters for which this color state list may change, requiring that it be re-created. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColorForState](../android/content/res/ColorStateList.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`, `defaultColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the color associated with the given set of [android.view.View](../android/view/View.md) states. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultColor](../android/content/res/ColorStateList.md))`()` Return the default color in this [ColorStateList](../android/content/res/ColorStateList.md). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpaque](../android/content/res/ColorStateList.md))`()` Indicates whether this color state list is opaque, which means that every color returned from[getColorForState(int[],int)](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList#getColorForState(kotlin.IntArray,%20kotlin.Int))has an alpha value of 255. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](../android/content/res/ColorStateList.md))`()` Indicates whether this color state list contains at least one state spec and the first spec is not empty (e.g. match-all). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/content/res/ColorStateList.md))`()` <br /> |
| --- | --- |
| openstatic [ColorStateList](../android/content/res/ColorStateList.md) | [valueOf](../android/content/res/ColorStateList.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [ColorStateList](../android/content/res/ColorStateList.md) | [withAlpha](../android/content/res/ColorStateList.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new ColorStateList that has the same states and colors as this one but where each color has the specified alpha value (0-255). |
| open [ColorStateList](../android/content/res/ColorStateList.md) | [withLStar](../android/content/res/ColorStateList.md))`(`lStar:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a new ColorStateList that has the same states and colors as this one but where each color has the specified perceived luminosity value (0-100). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/content/res/ColorStateList.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ColorStateList](../android/content/res/ColorStateList.md)!\> | [CREATOR](../android/content/res/ColorStateList.md) <br /> |

## XML attributes

### android:alpha

```
android:alpha
```
Alpha multiplier applied to the base color.

May be a floating point value, such as "`1.2`". 

### android:color

```
android:color
```
Base color for this state.

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:lStar

```
android:lStar
```
Perceptual luminance applied to the base color. From 0 to 100.

May be a floating point value, such as "`1.2`".

## Public constructors

### ColorStateList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorStateList(
    states: Array<IntArray!>!, 
    colors: IntArray!)
```

Creates a ColorStateList that returns the specified mapping from states to colors.

## Public methods

### createFromXml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromXml(
    r: Resources!, 
    parser: XmlPullParser!
): ColorStateList
```

**Deprecated:** *Use #createFromXml(Resources, XmlPullParser parser, Theme)*

Creates a ColorStateList from an XML document.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Resources](../android/content/res/Resources.md)!:Resources against which the ColorStateList should be inflated. |
| `parser` | [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)!:Parser for the XML document defining the ColorStateList. |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [ColorStateList](../android/content/res/ColorStateList.md) | A new color state list. This value cannot be`null`. |

### createFromXml

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromXml(
    r: Resources, 
    parser: XmlPullParser, 
    theme: Resources.Theme?
): ColorStateList
```

Creates a ColorStateList from an XML document using given a set of [Resources](../android/content/res/Resources.md) and a [Theme](../android/content/res/Resources.Theme.md).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Resources](../android/content/res/Resources.md):Resources against which the ColorStateList should be inflated. This value cannot be`null`. |
| `parser` | [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md):Parser for the XML document defining the ColorStateList. This value cannot be`null`. |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?:Optional theme to apply to the color state list, may be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [ColorStateList](../android/content/res/ColorStateList.md) | A new color state list. This value cannot be`null`. |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getChangingConfigurations

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChangingConfigurations(): Int
```

Returns a mask of the configuration parameters for which this color state list may change, requiring that it be re-created.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a mask of the changing configuration parameters, as defined by [android.content.pm.ActivityInfo](../android/content/pm/ActivityInfo.md) Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android/content/pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android/content/pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android/content/pm/ActivityInfo.md) |

**See Also**

- [android.content.pm.ActivityInfo](../android/content/pm/ActivityInfo.md) 

### getColorForState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorForState(
    stateSet: IntArray?, 
    defaultColor: Int
): Int
```

Return the color associated with the given set of [android.view.View](../android/view/View.md) states.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stateSet` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?:an array of [android.view.View](../android/view/View.md) states This value may be`null`. |
| `defaultColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the color to return if there's no matching state spec in this [ColorStateList](../android/content/res/ColorStateList.md) that matches the stateSet. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the color associated with that set of states in this [ColorStateList](../android/content/res/ColorStateList.md). |

### getDefaultColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultColor(): Int
```

Return the default color in this [ColorStateList](../android/content/res/ColorStateList.md).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the default color in this [ColorStateList](../android/content/res/ColorStateList.md). |

### isOpaque

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpaque(): Boolean
```

Indicates whether this color state list is opaque, which means that every color returned from[getColorForState(int[],int)](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList#getColorForState(kotlin.IntArray,%20kotlin.Int))has an alpha value of 255.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this color state list is opaque. |

### isStateful

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStateful(): Boolean
```

Indicates whether this color state list contains at least one state spec and the first spec is not empty (e.g. match-all).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this color state list changes color based on state, false otherwise. |

**See Also**

- [#getColorForState(int[], int)](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList#getColorForState(kotlin.IntArray,%20kotlin.Int)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(color: Int): ColorStateList
```

| Return ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ColorStateList](../android/content/res/ColorStateList.md) | A ColorStateList containing a single color. This value cannot be`null`. |

### withAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withAlpha(alpha: Int): ColorStateList
```

Creates a new ColorStateList that has the same states and colors as this one but where each color has the specified alpha value (0-255).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new alpha channel value (0-255). |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [ColorStateList](../android/content/res/ColorStateList.md) | A new color state list. This value cannot be`null`. |

### withLStar

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withLStar(lStar: Float): ColorStateList
```

Creates a new ColorStateList that has the same states and colors as this one but where each color has the specified perceived luminosity value (0-100).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `lStar` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Target perceptual luminance (0-100). |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [ColorStateList](../android/content/res/ColorStateList.md) | A new color state list. This value cannot be`null`. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ColorStateList!>
```
