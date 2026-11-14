# Configuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Configuration

Kotlin| [Java](../android/content/res/Configuration.md) 
| --- | --- |

```
class Configuration : Comparable<Configuration!>, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.res.Configuration](../android/content/res/Configuration.md) |

This class describes all device configuration information that can impact the resources the application retrieves. This includes both user-specified configuration options (locale list and scaling) as well as device configurations (such as input modes, screen size and screen orientation).

You can acquire this object from [Resources](../android/content/res/Resources.md), using [android.content.res.Resources#getConfiguration](../android/content/res/Resources.md)). Thus, from an activity, you can get it by chaining the request with android.app.Activity#getResources: 

```kotlin
Configuration config = getResources().getConfiguration();
```

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_MASK](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): bits that encode the dynamic range of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_NO](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_HDR_MASK](../android/content/res/Configuration.md) value indicating that the screen is not HDR (low/standard dynamic range). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_SHIFT](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): bits shift to get the screen dynamic range. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_UNDEFINED](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_HDR_MASK](../android/content/res/Configuration.md) value indicating that it is unknown whether or not the screen is HDR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_YES](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_HDR_MASK](../android/content/res/Configuration.md) value indicating that the screen is HDR (dynamic range). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_UNDEFINED](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): a value indicating that the color mode is undefined |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): bits that encode whether the screen is wide gamut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_WIDE_COLOR_GAMUT_NO](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](../android/content/res/Configuration.md) value indicating that the screen is not wide gamut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_WIDE_COLOR_GAMUT_UNDEFINED](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](../android/content/res/Configuration.md) value indicating that it is unknown whether or not the screen is wide gamut. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_WIDE_COLOR_GAMUT_YES](../android/content/res/Configuration.md) Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](../android/content/res/Configuration.md) value indicating that the screen is wide gamut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_DPI_UNDEFINED](../android/content/res/Configuration.md) Default value for [densityDpi](../android/content/res/Configuration.md) indicating that no width has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_ADJUSTMENT_UNDEFINED](../android/content/res/Configuration.md) An undefined fontWeightAdjustment. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAMMATICAL_GENDER_FEMININE](../android/content/res/Configuration.md) Constant for grammatical gender: to indicate the terms of address the user preferred in an application is feminine. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAMMATICAL_GENDER_MASCULINE](../android/content/res/Configuration.md) Constant for grammatical gender: to indicate the terms of address the user preferred in an application is masculine. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAMMATICAL_GENDER_NEUTRAL](../android/content/res/Configuration.md) Constant for grammatical gender: to indicate the terms of address the user preferred in an application is neuter. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAMMATICAL_GENDER_NOT_SPECIFIED](../android/content/res/Configuration.md) Constant for grammatical gender: to indicate the user has not specified the terms of address for the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HARDKEYBOARDHIDDEN_NO](../android/content/res/Configuration.md) Constant for [hardKeyboardHidden](../android/content/res/Configuration.md), value corresponding to the physical keyboard being exposed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HARDKEYBOARDHIDDEN_UNDEFINED](../android/content/res/Configuration.md) Constant for [hardKeyboardHidden](../android/content/res/Configuration.md): a value indicating that no value has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HARDKEYBOARDHIDDEN_YES](../android/content/res/Configuration.md) Constant for [hardKeyboardHidden](../android/content/res/Configuration.md), value corresponding to the physical keyboard being hidden. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARDHIDDEN_NO](../android/content/res/Configuration.md) Constant for [keyboardHidden](../android/content/res/Configuration.md), value corresponding to the [keysexposed](https://developer.android.com/guide/topics/resources/providing-resources.html#KeyboardAvailQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARDHIDDEN_UNDEFINED](../android/content/res/Configuration.md) Constant for [keyboardHidden](../android/content/res/Configuration.md): a value indicating that no value has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARDHIDDEN_YES](../android/content/res/Configuration.md) Constant for [keyboardHidden](../android/content/res/Configuration.md), value corresponding to the [keyshidden](https://developer.android.com/guide/topics/resources/providing-resources.html#KeyboardAvailQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_12KEY](../android/content/res/Configuration.md) Constant for [keyboard](../android/content/res/Configuration.md), value corresponding to the [12key](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_NOKEYS](../android/content/res/Configuration.md) Constant for [keyboard](../android/content/res/Configuration.md), value corresponding to the [nokeys](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_QWERTY](../android/content/res/Configuration.md) Constant for [keyboard](../android/content/res/Configuration.md), value corresponding to the [qwerty](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_UNDEFINED](../android/content/res/Configuration.md) Constant for [keyboard](../android/content/res/Configuration.md): a value indicating that no value has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MNC_ZERO](../android/content/res/Configuration.md) Constant used to to represent MNC (Mobile Network Code) zero. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATIONHIDDEN_NO](../android/content/res/Configuration.md) Constant for [navigationHidden](../android/content/res/Configuration.md), value corresponding to the [navexposed](https://developer.android.com/guide/topics/resources/providing-resources.html#NavAvailQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATIONHIDDEN_UNDEFINED](../android/content/res/Configuration.md) Constant for [navigationHidden](../android/content/res/Configuration.md): a value indicating that no value has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATIONHIDDEN_YES](../android/content/res/Configuration.md) Constant for [navigationHidden](../android/content/res/Configuration.md), value corresponding to the [navhidden](https://developer.android.com/guide/topics/resources/providing-resources.html#NavAvailQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_DPAD](../android/content/res/Configuration.md) Constant for [navigation](../android/content/res/Configuration.md), value corresponding to the [dpad](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_NONAV](../android/content/res/Configuration.md) Constant for [navigation](../android/content/res/Configuration.md), value corresponding to the [nonav](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_TRACKBALL](../android/content/res/Configuration.md) Constant for [navigation](../android/content/res/Configuration.md), value corresponding to the [trackball](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_UNDEFINED](../android/content/res/Configuration.md) Constant for [navigation](../android/content/res/Configuration.md): a value indicating that no value has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_WHEEL](../android/content/res/Configuration.md) Constant for [navigation](../android/content/res/Configuration.md), value corresponding to the [wheel](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_LANDSCAPE](../android/content/res/Configuration.md) Constant for [orientation](../android/content/res/Configuration.md), value corresponding to the [land](https://developer.android.com/guide/topics/resources/providing-resources.html#OrientationQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_PORTRAIT](../android/content/res/Configuration.md) Constant for [orientation](../android/content/res/Configuration.md), value corresponding to the [port](https://developer.android.com/guide/topics/resources/providing-resources.html#OrientationQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_SQUARE](../android/content/res/Configuration.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_UNDEFINED](../android/content/res/Configuration.md) Constant for [orientation](../android/content/res/Configuration.md): a value indicating that no value has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_LTR](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LAYOUTDIR_MASK](../android/content/res/Configuration.md) value indicating that a layout dir has been set to LTR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_MASK](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): bits that encode the layout direction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_RTL](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LAYOUTDIR_MASK](../android/content/res/Configuration.md) value indicating that a layout dir has been set to RTL. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_SHIFT](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): bits shift to get the layout direction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_UNDEFINED](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LAYOUTDIR_MASK](../android/content/res/Configuration.md) value indicating that no layout dir has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LONG_MASK](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): bits that encode the aspect ratio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LONG_NO](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LONG_MASK](../android/content/res/Configuration.md) value that corresponds to the [notlong](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenAspectQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LONG_UNDEFINED](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LONG_MASK](../android/content/res/Configuration.md) value indicating that no size has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LONG_YES](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LONG_MASK](../android/content/res/Configuration.md) value that corresponds to the [long](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenAspectQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_ROUND_MASK](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): bits that encode roundness of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_ROUND_NO](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_ROUND_MASK](../android/content/res/Configuration.md) value indicating that the screen does not have a rounded shape. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_ROUND_UNDEFINED](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_ROUND_MASK](../android/content/res/Configuration.md) value indicating that it is unknown whether or not the screen has a round shape. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_ROUND_YES](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_ROUND_MASK](../android/content/res/Configuration.md) value indicating that the screen has a rounded shape. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_LARGE](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating the screen is at least approximately 480x640 dp units, corresponds to the [large](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): bits that encode the size. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_NORMAL](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating the screen is at least approximately 320x470 dp units, corresponds to the [normal](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_SMALL](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating the screen is at least approximately 320x426 dp units, corresponds to the [small](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_UNDEFINED](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating that no size has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_XLARGE](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating the screen is at least approximately 720x960 dp units, corresponds to the [xlarge](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_UNDEFINED](../android/content/res/Configuration.md) Constant for [screenLayout](../android/content/res/Configuration.md): a value indicating that screenLayout is undefined |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREEN_HEIGHT_DP_UNDEFINED](../android/content/res/Configuration.md) Default value for [screenHeightDp](../android/content/res/Configuration.md) indicating that no width has been specified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREEN_WIDTH_DP_UNDEFINED](../android/content/res/Configuration.md) Default value for [screenWidthDp](../android/content/res/Configuration.md) indicating that no width has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SMALLEST_SCREEN_WIDTH_DP_UNDEFINED](../android/content/res/Configuration.md) Default value for [smallestScreenWidthDp](../android/content/res/Configuration.md) indicating that no width has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOUCHSCREEN_FINGER](../android/content/res/Configuration.md) Constant for [touchscreen](../android/content/res/Configuration.md), value corresponding to the [finger](https://developer.android.com/guide/topics/resources/providing-resources.html#TouchscreenQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOUCHSCREEN_NOTOUCH](../android/content/res/Configuration.md) Constant for [touchscreen](../android/content/res/Configuration.md), value corresponding to the [notouch](https://developer.android.com/guide/topics/resources/providing-resources.html#TouchscreenQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOUCHSCREEN_STYLUS](../android/content/res/Configuration.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOUCHSCREEN_UNDEFINED](../android/content/res/Configuration.md) Constant for [touchscreen](../android/content/res/Configuration.md): a value indicating that no value has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_NIGHT_MASK](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): bits that encode the night mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_NIGHT_NO](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_NIGHT_MASK](../android/content/res/Configuration.md) value that corresponds to the [notnight](https://developer.android.com/guide/topics/resources/providing-resources.html#NightQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_NIGHT_UNDEFINED](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_NIGHT_MASK](../android/content/res/Configuration.md) value indicating that no mode type has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_NIGHT_YES](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_NIGHT_MASK](../android/content/res/Configuration.md) value that corresponds to the [night](https://developer.android.com/guide/topics/resources/providing-resources.html#NightQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_APPLIANCE](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [appliance](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_CAR](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [car](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_DESK](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [desk](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): bits that encode the mode type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_NORMAL](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to [no UI mode](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier specified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_TELEVISION](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [television](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_UNDEFINED](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value indicating that no mode type has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_VR_HEADSET](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [vrheadset](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_WATCH](../android/content/res/Configuration.md) Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [watch](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Configuration](../android/content/res/Configuration.md))`()` Construct an invalid Configuration. |
| [Configuration](../android/content/res/Configuration.md))`(`o:` ` [Configuration](../android/content/res/Configuration.md)!`)` Makes a deep copy suitable for modification. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../android/content/res/Configuration.md))`(`other:` ` [Configuration](../android/content/res/Configuration.md)!`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/content/res/Configuration.md))`()` Parcelable methods |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [diff](../android/content/res/Configuration.md))`(`delta:` ` [Configuration](../android/content/res/Configuration.md)!`)` Return a bit mask of the differences between this Configuration object and the given one. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/content/res/Configuration.md))`(`that:` ` [Configuration](../android/content/res/Configuration.md)!`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/content/res/Configuration.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [Configuration](../android/content/res/Configuration.md) | [generateDelta](../android/content/res/Configuration.md))`(`base:` ` [Configuration](../android/content/res/Configuration.md)`, `change:` ` [Configuration](../android/content/res/Configuration.md)`)` Generate a delta Configuration between`base`and`change`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGrammaticalGender](../android/content/res/Configuration.md))`()` Returns the user preference for the grammatical gender. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](../android/content/res/Configuration.md))`()` Return the layout direction. |
| [LocaleList](../android/os/LocaleList.md) | [getLocales](../android/content/res/Configuration.md))`()` Get the locale list. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/content/res/Configuration.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLayoutSizeAtLeast](../android/content/res/Configuration.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Check if the Configuration's current [screenLayout](../android/content/res/Configuration.md) is at least the given size. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNightModeActive](../android/content/res/Configuration.md))`()` Retuns whether the configuration is in night mode |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScreenHdr](../android/content/res/Configuration.md))`()` Return whether the screen has a high dynamic range. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScreenRound](../android/content/res/Configuration.md))`()` Return whether the screen has a round shape. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScreenWideColorGamut](../android/content/res/Configuration.md))`()` Return whether the screen has a wide color gamut and wide color gamut rendering is supported by this device. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [needNewResources](../android/content/res/Configuration.md))`(`configChanges:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `interestingChanges:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if a new resource needs to be loaded from the bit set of configuration changes returned by [updateFrom(android.content.res.Configuration)](../android/content/res/Configuration.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFromParcel](../android/content/res/Configuration.md))`(`source:` ` [Parcel](../android/os/Parcel.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutDirection](../android/content/res/Configuration.md))`(`loc:` ` [Locale](../java/util/Locale.md)!`)` Set the layout direction from a Locale. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](../android/content/res/Configuration.md))`(`loc:` ` [Locale](../java/util/Locale.md)?`)` Set the locale list to a list of just one locale. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocales](../android/content/res/Configuration.md))`(`locales:` ` [LocaleList](../android/os/LocaleList.md)?`)` Set the locale list. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTo](../android/content/res/Configuration.md))`(`o:` ` [Configuration](../android/content/res/Configuration.md)!`)` Sets the fields in this object to those in the given Configuration. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setToDefaults](../android/content/res/Configuration.md))`()` Set this object to the system defaults. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/content/res/Configuration.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [updateFrom](../android/content/res/Configuration.md))`(`delta:` ` [Configuration](../android/content/res/Configuration.md)`)` Copies the fields from delta into this Configuration object, keeping track of which ones have changed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/content/res/Configuration.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Configuration](../android/content/res/Configuration.md)!\> | [CREATOR](../android/content/res/Configuration.md) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [colorMode](../android/content/res/Configuration.md) Bit mask of color capabilities of the screen. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [densityDpi](../android/content/res/Configuration.md) The target screen density being rendered to, corresponding to [density](https://developer.android.com/guide/topics/resources/providing-resources.html#DensityQualifier) resource qualifier. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [fontScale](../android/content/res/Configuration.md) Current user preference for the scaling factor for fonts, relative to the base density scaling. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [fontWeightAdjustment](../android/content/res/Configuration.md) Adjustment in text font weight. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hardKeyboardHidden](../android/content/res/Configuration.md) A flag indicating whether the hard keyboard has been hidden. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [keyboard](../android/content/res/Configuration.md) The kind of keyboard attached to the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [keyboardHidden](../android/content/res/Configuration.md) A flag indicating whether any keyboard is available. |
| [Locale](../java/util/Locale.md)! | [locale](../android/content/res/Configuration.md) Current user preference for the locale, corresponding to [locale](https://developer.android.com/guide/topics/resources/providing-resources.html#LocaleQualifier) resource qualifier. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mcc](../android/content/res/Configuration.md) IMSI MCC (Mobile Country Code), corresponding to [mcc](https://developer.android.com/guide/topics/resources/providing-resources.html#MccQualifier) resource qualifier. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mnc](../android/content/res/Configuration.md) IMSI MNC (Mobile Network Code), corresponding to [mnc](https://developer.android.com/guide/topics/resources/providing-resources.html#MccQualifier) resource qualifier. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [navigation](../android/content/res/Configuration.md) The kind of navigation method available on the device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [navigationHidden](../android/content/res/Configuration.md) A flag indicating whether any 5-way or DPAD navigation available. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orientation](../android/content/res/Configuration.md) Overall orientation of the screen. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [screenHeightDp](../android/content/res/Configuration.md) The height of the available screen space in dp units. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [screenLayout](../android/content/res/Configuration.md) Bit mask of overall layout of the screen. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [screenWidthDp](../android/content/res/Configuration.md) The width of the available screen space in dp units. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [smallestScreenWidthDp](../android/content/res/Configuration.md) The smallest screen size an application will see in normal operation. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [touchscreen](../android/content/res/Configuration.md) The kind of touch screen attached to the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [uiMode](../android/content/res/Configuration.md) Bit mask of the ui mode. |

## Constants

### COLOR_MODE_HDR_MASK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_MASK: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): bits that encode the dynamic range of the screen. 

 Value: 12

### COLOR_MODE_HDR_NO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_NO: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_HDR_MASK](../android/content/res/Configuration.md) value indicating that the screen is not HDR (low/standard dynamic range).

Corresponds to the`-lowdr`resource qualifier. 

 Value: 4

### COLOR_MODE_HDR_SHIFT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_SHIFT: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): bits shift to get the screen dynamic range. 

 Value: 2

### COLOR_MODE_HDR_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_UNDEFINED: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_HDR_MASK](../android/content/res/Configuration.md) value indicating that it is unknown whether or not the screen is HDR. 

 Value: 0

### COLOR_MODE_HDR_YES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_YES: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_HDR_MASK](../android/content/res/Configuration.md) value indicating that the screen is HDR (dynamic range).

Corresponds to the`-highdr`resource qualifier. 

 Value: 8

### COLOR_MODE_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_UNDEFINED: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): a value indicating that the color mode is undefined 

 Value: 0

### COLOR_MODE_WIDE_COLOR_GAMUT_MASK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_WIDE_COLOR_GAMUT_MASK: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): bits that encode whether the screen is wide gamut. 

 Value: 3

### COLOR_MODE_WIDE_COLOR_GAMUT_NO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_WIDE_COLOR_GAMUT_NO: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](../android/content/res/Configuration.md) value indicating that the screen is not wide gamut.

Corresponds to the`-nowidecg`resource qualifier. 

 Value: 1

### COLOR_MODE_WIDE_COLOR_GAMUT_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_WIDE_COLOR_GAMUT_UNDEFINED: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](../android/content/res/Configuration.md) value indicating that it is unknown whether or not the screen is wide gamut. 

 Value: 0

### COLOR_MODE_WIDE_COLOR_GAMUT_YES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_WIDE_COLOR_GAMUT_YES: Int
```

Constant for [colorMode](../android/content/res/Configuration.md): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](../android/content/res/Configuration.md) value indicating that the screen is wide gamut.

Corresponds to the`-widecg`resource qualifier. 

 Value: 2

### DENSITY_DPI_UNDEFINED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_DPI_UNDEFINED: Int
```

Default value for [densityDpi](../android/content/res/Configuration.md) indicating that no width has been specified. 

 Value: 0

### FONT_WEIGHT_ADJUSTMENT_UNDEFINED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_ADJUSTMENT_UNDEFINED: Int
```

An undefined fontWeightAdjustment. 

 Value: 2147483647

### GRAMMATICAL_GENDER_FEMININE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAMMATICAL_GENDER_FEMININE: Int
```

Constant for grammatical gender: to indicate the terms of address the user preferred in an application is feminine. 

 Value: 2

### GRAMMATICAL_GENDER_MASCULINE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAMMATICAL_GENDER_MASCULINE: Int
```

Constant for grammatical gender: to indicate the terms of address the user preferred in an application is masculine. 

 Value: 3

### GRAMMATICAL_GENDER_NEUTRAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAMMATICAL_GENDER_NEUTRAL: Int
```

Constant for grammatical gender: to indicate the terms of address the user preferred in an application is neuter. 

 Value: 1

### GRAMMATICAL_GENDER_NOT_SPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAMMATICAL_GENDER_NOT_SPECIFIED: Int
```

Constant for grammatical gender: to indicate the user has not specified the terms of address for the application. 

 Value: 0

### HARDKEYBOARDHIDDEN_NO

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HARDKEYBOARDHIDDEN_NO: Int
```

Constant for [hardKeyboardHidden](../android/content/res/Configuration.md), value corresponding to the physical keyboard being exposed. 

 Value: 1

### HARDKEYBOARDHIDDEN_UNDEFINED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HARDKEYBOARDHIDDEN_UNDEFINED: Int
```

Constant for [hardKeyboardHidden](../android/content/res/Configuration.md): a value indicating that no value has been set. 

 Value: 0

### HARDKEYBOARDHIDDEN_YES

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HARDKEYBOARDHIDDEN_YES: Int
```

Constant for [hardKeyboardHidden](../android/content/res/Configuration.md), value corresponding to the physical keyboard being hidden. 

 Value: 2

### KEYBOARDHIDDEN_NO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARDHIDDEN_NO: Int
```

Constant for [keyboardHidden](../android/content/res/Configuration.md), value corresponding to the [keysexposed](https://developer.android.com/guide/topics/resources/providing-resources.html#KeyboardAvailQualifier) resource qualifier. 

 Value: 1

### KEYBOARDHIDDEN_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARDHIDDEN_UNDEFINED: Int
```

Constant for [keyboardHidden](../android/content/res/Configuration.md): a value indicating that no value has been set. 

 Value: 0

### KEYBOARDHIDDEN_YES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARDHIDDEN_YES: Int
```

Constant for [keyboardHidden](../android/content/res/Configuration.md), value corresponding to the [keyshidden](https://developer.android.com/guide/topics/resources/providing-resources.html#KeyboardAvailQualifier) resource qualifier. 

 Value: 2

### KEYBOARD_12KEY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_12KEY: Int
```

Constant for [keyboard](../android/content/res/Configuration.md), value corresponding to the [12key](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. 

 Value: 3

### KEYBOARD_NOKEYS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_NOKEYS: Int
```

Constant for [keyboard](../android/content/res/Configuration.md), value corresponding to the [nokeys](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. 

 Value: 1

### KEYBOARD_QWERTY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_QWERTY: Int
```

Constant for [keyboard](../android/content/res/Configuration.md), value corresponding to the [qwerty](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. 

 Value: 2

### KEYBOARD_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_UNDEFINED: Int
```

Constant for [keyboard](../android/content/res/Configuration.md): a value indicating that no value has been set. 

 Value: 0

### MNC_ZERO

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MNC_ZERO: Int
```

Constant used to to represent MNC (Mobile Network Code) zero. 0 cannot be used, since it is used to represent an undefined MNC. 

 Value: 65535

### NAVIGATIONHIDDEN_NO

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATIONHIDDEN_NO: Int
```

Constant for [navigationHidden](../android/content/res/Configuration.md), value corresponding to the [navexposed](https://developer.android.com/guide/topics/resources/providing-resources.html#NavAvailQualifier) resource qualifier. 

 Value: 1

### NAVIGATIONHIDDEN_UNDEFINED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATIONHIDDEN_UNDEFINED: Int
```

Constant for [navigationHidden](../android/content/res/Configuration.md): a value indicating that no value has been set. 

 Value: 0

### NAVIGATIONHIDDEN_YES

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATIONHIDDEN_YES: Int
```

Constant for [navigationHidden](../android/content/res/Configuration.md), value corresponding to the [navhidden](https://developer.android.com/guide/topics/resources/providing-resources.html#NavAvailQualifier) resource qualifier. 

 Value: 2

### NAVIGATION_DPAD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_DPAD: Int
```

Constant for [navigation](../android/content/res/Configuration.md), value corresponding to the [dpad](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. 

 Value: 2

### NAVIGATION_NONAV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_NONAV: Int
```

Constant for [navigation](../android/content/res/Configuration.md), value corresponding to the [nonav](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. 

 Value: 1

### NAVIGATION_TRACKBALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_TRACKBALL: Int
```

Constant for [navigation](../android/content/res/Configuration.md), value corresponding to the [trackball](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. 

 Value: 3

### NAVIGATION_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_UNDEFINED: Int
```

Constant for [navigation](../android/content/res/Configuration.md): a value indicating that no value has been set. 

 Value: 0

### NAVIGATION_WHEEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_WHEEL: Int
```

Constant for [navigation](../android/content/res/Configuration.md), value corresponding to the [wheel](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. 

 Value: 4

### ORIENTATION_LANDSCAPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_LANDSCAPE: Int
```

Constant for [orientation](../android/content/res/Configuration.md), value corresponding to the [land](https://developer.android.com/guide/topics/resources/providing-resources.html#OrientationQualifier) resource qualifier. 

 Value: 2

### ORIENTATION_PORTRAIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_PORTRAIT: Int
```

Constant for [orientation](../android/content/res/Configuration.md), value corresponding to the [port](https://developer.android.com/guide/topics/resources/providing-resources.html#OrientationQualifier) resource qualifier. 

 Value: 1

### ORIENTATION_SQUARE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_SQUARE: Int
```

**Deprecated:** *Not currently supported or used.* 

 Value: 3

### ORIENTATION_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_UNDEFINED: Int
```

Constant for [orientation](../android/content/res/Configuration.md): a value indicating that no value has been set. 

 Value: 0

### SCREENLAYOUT_LAYOUTDIR_LTR

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_LTR: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LAYOUTDIR_MASK](../android/content/res/Configuration.md) value indicating that a layout dir has been set to LTR. 

 Value: 64

### SCREENLAYOUT_LAYOUTDIR_MASK

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_MASK: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): bits that encode the layout direction. 

 Value: 192

### SCREENLAYOUT_LAYOUTDIR_RTL

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_RTL: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LAYOUTDIR_MASK](../android/content/res/Configuration.md) value indicating that a layout dir has been set to RTL. 

 Value: 128

### SCREENLAYOUT_LAYOUTDIR_SHIFT

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_SHIFT: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): bits shift to get the layout direction. 

 Value: 6

### SCREENLAYOUT_LAYOUTDIR_UNDEFINED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_UNDEFINED: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LAYOUTDIR_MASK](../android/content/res/Configuration.md) value indicating that no layout dir has been set. 

 Value: 0

### SCREENLAYOUT_LONG_MASK

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LONG_MASK: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): bits that encode the aspect ratio. 

 Value: 48

### SCREENLAYOUT_LONG_NO

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LONG_NO: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LONG_MASK](../android/content/res/Configuration.md) value that corresponds to the [notlong](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenAspectQualifier) resource qualifier. 

 Value: 16

### SCREENLAYOUT_LONG_UNDEFINED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LONG_UNDEFINED: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LONG_MASK](../android/content/res/Configuration.md) value indicating that no size has been set. 

 Value: 0

### SCREENLAYOUT_LONG_YES

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LONG_YES: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_LONG_MASK](../android/content/res/Configuration.md) value that corresponds to the [long](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenAspectQualifier) resource qualifier. 

 Value: 32

### SCREENLAYOUT_ROUND_MASK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_ROUND_MASK: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): bits that encode roundness of the screen. 

 Value: 768

### SCREENLAYOUT_ROUND_NO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_ROUND_NO: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_ROUND_MASK](../android/content/res/Configuration.md) value indicating that the screen does not have a rounded shape. 

 Value: 256

### SCREENLAYOUT_ROUND_UNDEFINED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_ROUND_UNDEFINED: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_ROUND_MASK](../android/content/res/Configuration.md) value indicating that it is unknown whether or not the screen has a round shape. 

 Value: 0

### SCREENLAYOUT_ROUND_YES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_ROUND_YES: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_ROUND_MASK](../android/content/res/Configuration.md) value indicating that the screen has a rounded shape. Corners may not be visible to the user; developers should pay special attention to the [android.view.WindowInsets](../android/view/WindowInsets.md) delivered to views for more information about ensuring content is not obscured.

Corresponds to the`-round`resource qualifier. 

 Value: 512

### SCREENLAYOUT_SIZE_LARGE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_LARGE: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating the screen is at least approximately 480x640 dp units, corresponds to the [large](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

 Value: 3

### SCREENLAYOUT_SIZE_MASK

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_MASK: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): bits that encode the size. 

 Value: 15

### SCREENLAYOUT_SIZE_NORMAL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_NORMAL: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating the screen is at least approximately 320x470 dp units, corresponds to the [normal](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

 Value: 2

### SCREENLAYOUT_SIZE_SMALL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_SMALL: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating the screen is at least approximately 320x426 dp units, corresponds to the [small](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

 Value: 1

### SCREENLAYOUT_SIZE_UNDEFINED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_UNDEFINED: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating that no size has been set. 

 Value: 0

### SCREENLAYOUT_SIZE_XLARGE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_XLARGE: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) value indicating the screen is at least approximately 720x960 dp units, corresponds to the [xlarge](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

 Value: 4

### SCREENLAYOUT_UNDEFINED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_UNDEFINED: Int
```

Constant for [screenLayout](../android/content/res/Configuration.md): a value indicating that screenLayout is undefined 

 Value: 0

### SCREEN_HEIGHT_DP_UNDEFINED

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREEN_HEIGHT_DP_UNDEFINED: Int
```

Default value for [screenHeightDp](../android/content/res/Configuration.md) indicating that no width has been specified. 

 Value: 0

### SCREEN_WIDTH_DP_UNDEFINED

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREEN_WIDTH_DP_UNDEFINED: Int
```

Default value for [screenWidthDp](../android/content/res/Configuration.md) indicating that no width has been specified. 

 Value: 0

### SMALLEST_SCREEN_WIDTH_DP_UNDEFINED

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SMALLEST_SCREEN_WIDTH_DP_UNDEFINED: Int
```

Default value for [smallestScreenWidthDp](../android/content/res/Configuration.md) indicating that no width has been specified. 

 Value: 0

### TOUCHSCREEN_FINGER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOUCHSCREEN_FINGER: Int
```

Constant for [touchscreen](../android/content/res/Configuration.md), value corresponding to the [finger](https://developer.android.com/guide/topics/resources/providing-resources.html#TouchscreenQualifier) resource qualifier. 

 Value: 3

### TOUCHSCREEN_NOTOUCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOUCHSCREEN_NOTOUCH: Int
```

Constant for [touchscreen](../android/content/res/Configuration.md), value corresponding to the [notouch](https://developer.android.com/guide/topics/resources/providing-resources.html#TouchscreenQualifier) resource qualifier. 

 Value: 1

### TOUCHSCREEN_STYLUS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOUCHSCREEN_STYLUS: Int
```

**Deprecated:** *Not currently supported or used.* 

 Value: 2

### TOUCHSCREEN_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOUCHSCREEN_UNDEFINED: Int
```

Constant for [touchscreen](../android/content/res/Configuration.md): a value indicating that no value has been set. 

 Value: 0

### UI_MODE_NIGHT_MASK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_NIGHT_MASK: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): bits that encode the night mode. 

 Value: 48

### UI_MODE_NIGHT_NO

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_NIGHT_NO: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_NIGHT_MASK](../android/content/res/Configuration.md) value that corresponds to the [notnight](https://developer.android.com/guide/topics/resources/providing-resources.html#NightQualifier) resource qualifier. 

 Value: 16

### UI_MODE_NIGHT_UNDEFINED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_NIGHT_UNDEFINED: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_NIGHT_MASK](../android/content/res/Configuration.md) value indicating that no mode type has been set. 

 Value: 0

### UI_MODE_NIGHT_YES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_NIGHT_YES: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_NIGHT_MASK](../android/content/res/Configuration.md) value that corresponds to the [night](https://developer.android.com/guide/topics/resources/providing-resources.html#NightQualifier) resource qualifier. 

 Value: 32

### UI_MODE_TYPE_APPLIANCE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_APPLIANCE: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [appliance](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 5

### UI_MODE_TYPE_CAR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_CAR: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [car](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 3

### UI_MODE_TYPE_DESK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_DESK: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [desk](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 2

### UI_MODE_TYPE_MASK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_MASK: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): bits that encode the mode type. 

 Value: 15

### UI_MODE_TYPE_NORMAL

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_NORMAL: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to [no UI mode](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier specified. 

 Value: 1

### UI_MODE_TYPE_TELEVISION

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_TELEVISION: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [television](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 4

### UI_MODE_TYPE_UNDEFINED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_UNDEFINED: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value indicating that no mode type has been set. 

 Value: 0

### UI_MODE_TYPE_VR_HEADSET

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_VR_HEADSET: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [vrheadset](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 7

### UI_MODE_TYPE_WATCH

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_WATCH: Int
```

Constant for [uiMode](../android/content/res/Configuration.md): a [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) value that corresponds to the [watch](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 6

## Public constructors

### Configuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Configuration()
```

Construct an invalid Configuration. This state is only suitable for constructing a Configuration delta that will be applied to some valid Configuration object. In order to create a valid standalone Configuration, you must call [setToDefaults](../android/content/res/Configuration.md)).

Example: 

```kotlin
Configuration validConfig = new Configuration();
      validConfig.setToDefaults();
 
      Configuration deltaOnlyConfig = new Configuration();
      deltaOnlyConfig.orientation = Configuration.ORIENTATION_LANDSCAPE;
 
      validConfig.updateFrom(deltaOnlyConfig);
  
```  

### Configuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Configuration(o: Configuration!)
```

Makes a deep copy suitable for modification.

## Public methods

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Configuration!): Int
```

| Parameters ||
|-----|----------------------------|
| `o` | the object to be compared. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Parcelable methods

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### diff

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun diff(delta: Configuration!): Int
```

Return a bit mask of the differences between this Configuration object and the given one. Does not change the values of either. Any undefined fields in delta are ignored.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns a bit mask indicating which configuration values have changed. Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android/content/pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android/content/pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android/content/pm/ActivityInfo.md) |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(that: Configuration!): Boolean
```  

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `that` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### generateDelta

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun generateDelta(
    base: Configuration, 
    change: Configuration
): Configuration
```

Generate a delta Configuration between`base`and`change`. The resulting delta can be used with .

<br />

Caveat: If the any of the Configuration's members becomes undefined, then [updateFrom(android.content.res.Configuration)](../android/content/res/Configuration.md))will treat it as a no-op and not update that member. This is fine for device configurations as no member is ever undefined.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `base` | [Configuration](../android/content/res/Configuration.md):This value cannot be`null`. |
| `change` | [Configuration](../android/content/res/Configuration.md):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------|
| [Configuration](../android/content/res/Configuration.md) | This value cannot be`null`. |

### getGrammaticalGender

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGrammaticalGender(): Int
```

Returns the user preference for the grammatical gender. Will be [GRAMMATICAL_GENDER_NOT_SPECIFIED](../android/content/res/Configuration.md) or [GRAMMATICAL_GENDER_NEUTRAL](../android/content/res/Configuration.md) or [GRAMMATICAL_GENDER_FEMININE](../android/content/res/Configuration.md) or [GRAMMATICAL_GENDER_MASCULINE](../android/content/res/Configuration.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The preferred grammatical gender. Value is [android.content.res.Configuration#GRAMMATICAL_GENDER_NOT_SPECIFIED](../android/content/res/Configuration.md), [android.content.res.Configuration#GRAMMATICAL_GENDER_NEUTRAL](../android/content/res/Configuration.md), [android.content.res.Configuration#GRAMMATICAL_GENDER_FEMININE](../android/content/res/Configuration.md), or [android.content.res.Configuration#GRAMMATICAL_GENDER_MASCULINE](../android/content/res/Configuration.md) |

### getLayoutDirection

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLayoutDirection(): Int
```

Return the layout direction. Will be either [View.LAYOUT_DIRECTION_LTR](../android/view/View.md) or [View.LAYOUT_DIRECTION_RTL](../android/view/View.md).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns [View.LAYOUT_DIRECTION_RTL](../android/view/View.md) if the configuration is [SCREENLAYOUT_LAYOUTDIR_RTL](../android/content/res/Configuration.md), otherwise [View.LAYOUT_DIRECTION_LTR](../android/view/View.md). |

### getLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocales(): LocaleList
```

Get the locale list. This is the preferred way for getting the locales (instead of using the direct accessor to [locale](../android/content/res/Configuration.md), which would only provide the primary locale).

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------|
| [LocaleList](../android/os/LocaleList.md) | The locale list. This value cannot be`null`. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isLayoutSizeAtLeast

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLayoutSizeAtLeast(size: Int): Boolean
```

Check if the Configuration's current [screenLayout](../android/content/res/Configuration.md) is at least the given size.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired size, either [SCREENLAYOUT_SIZE_SMALL](../android/content/res/Configuration.md), [SCREENLAYOUT_SIZE_NORMAL](../android/content/res/Configuration.md), [SCREENLAYOUT_SIZE_LARGE](../android/content/res/Configuration.md), or [SCREENLAYOUT_SIZE_XLARGE](../android/content/res/Configuration.md). |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the current screen layout size is at least the given size. |

### isNightModeActive

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isNightModeActive(): Boolean
```

Retuns whether the configuration is in night mode

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if night mode is active and false otherwise |

### isScreenHdr

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isScreenHdr(): Boolean
```

Return whether the screen has a high dynamic range.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the screen has a high dynamic range, false otherwise |

### isScreenRound

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isScreenRound(): Boolean
```

Return whether the screen has a round shape. Apps may choose to change styling based on this property, such as the alignment or layout of text or informational icons.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the screen is rounded, false otherwise |

### isScreenWideColorGamut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isScreenWideColorGamut(): Boolean
```

Return whether the screen has a wide color gamut and wide color gamut rendering is supported by this device. When true, it implies the screen is colorspace aware but not necessarily color-managed. The final colors may still be changed by the screen depending on user settings.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the screen has a wide color gamut and wide color gamut rendering is supported, false otherwise |

### needNewResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun needNewResources(
    configChanges: Int, 
    interestingChanges: Int
): Boolean
```

Determines if a new resource needs to be loaded from the bit set of configuration changes returned by [updateFrom(android.content.res.Configuration)](../android/content/res/Configuration.md)).

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configChanges` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mask of changes configurations as returned by [updateFrom(android.content.res.Configuration)](../android/content/res/Configuration.md))Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android/content/pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android/content/pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android/content/pm/ActivityInfo.md) |
| `interestingChanges` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the configuration changes that the resource can handle as given in [android.util.TypedValue#changingConfigurations](../android/util/TypedValue.md) Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android/content/pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android/content/pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android/content/pm/ActivityInfo.md) |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the resource needs to be loaded,`false`otherwise |

### readFromParcel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readFromParcel(source: Parcel!): Unit
```  

### setLayoutDirection

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLayoutDirection(loc: Locale!): Unit
```

Set the layout direction from a Locale.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `loc` | [Locale](../java/util/Locale.md)!:The Locale. If null will set the layout direction to [View.LAYOUT_DIRECTION_LTR](../android/view/View.md). If not null will set it to the layout direction corresponding to the Locale. |

**See Also**

- [android.view.View#LAYOUT_DIRECTION_LTR](../android/view/View.md)
- [android.view.View#LAYOUT_DIRECTION_RTL](../android/view/View.md) 

### setLocale

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLocale(loc: Locale?): Unit
```

Set the locale list to a list of just one locale. This will also set the layout direction according to the locale. Note that after this is run, calling`.equals()`on the input locale and the [locale](../android/content/res/Configuration.md) attribute would return`true`if they are not null, but there is no guarantee that they would be the same object. See also the note about layout direction in [setLocales(android.os.LocaleList)](../android/content/res/Configuration.md)).

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `loc` | [Locale](../java/util/Locale.md)?:The locale. Can be null. |

### setLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLocales(locales: LocaleList?): Unit
```

Set the locale list. This is the preferred way for setting up the locales (instead of using the direct accessor or [setLocale(java.util.Locale)](../android/content/res/Configuration.md))). This will also set the layout direction according to the first locale in the list. Note that the layout direction will always come from the first locale in the locale list, even if the locale is not supported by the resources (the resources may only support another locale further down the list which has a different direction).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locales` | [LocaleList](../android/os/LocaleList.md)?:The locale list. If null, an empty LocaleList will be assigned. |

### setTo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTo(o: Configuration!): Unit
```

Sets the fields in this object to those in the given Configuration.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Configuration](../android/content/res/Configuration.md)!:The Configuration object used to set the values of this Configuration's fields. |

### setToDefaults

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setToDefaults(): Unit
```

Set this object to the system defaults. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### updateFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateFrom(delta: Configuration): Int
```

Copies the fields from delta into this Configuration object, keeping track of which ones have changed. Any undefined fields in`delta`are ignored and not copied in to the current Configuration.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `delta` | [Configuration](../android/content/res/Configuration.md):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bit mask of the changed fields, as per [diff](../android/content/res/Configuration.md))Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android/content/pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android/content/pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android/content/pm/ActivityInfo.md) |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
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
static val CREATOR: Parcelable.Creator<Configuration!>
```  

### colorMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var colorMode: Int
```

Bit mask of color capabilities of the screen. Currently there are two fields:

The [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](../android/content/res/Configuration.md) bits define the color gamut of the screen. They may be one of [COLOR_MODE_WIDE_COLOR_GAMUT_NO](../android/content/res/Configuration.md) or [COLOR_MODE_WIDE_COLOR_GAMUT_YES](../android/content/res/Configuration.md).

The [COLOR_MODE_HDR_MASK](../android/content/res/Configuration.md) defines the dynamic range of the screen. They may be one of [COLOR_MODE_HDR_NO](../android/content/res/Configuration.md) or [COLOR_MODE_HDR_YES](../android/content/res/Configuration.md).

See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

### densityDpi

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var densityDpi: Int
```

The target screen density being rendered to, corresponding to [density](https://developer.android.com/guide/topics/resources/providing-resources.html#DensityQualifier) resource qualifier. Set to [DENSITY_DPI_UNDEFINED](../android/content/res/Configuration.md) if no density is specified. 

### fontScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var fontScale: Float
```

Current user preference for the scaling factor for fonts, relative to the base density scaling.

Note: Please do not use this to hardcode font size equations. The equation for font scaling is now non-linear; this coefficient is no longer used as a direct multiplier to determine font size. It exists for informational purposes only.

Please use [android.util.TypedValue#applyDimension(int, float, DisplayMetrics)](../android/util/TypedValue.md))or [android.util.TypedValue#deriveDimension(int, float, DisplayMetrics)](../android/util/TypedValue.md))to convert between scaled font size dimensions and pixels. 

### fontWeightAdjustment

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var fontWeightAdjustment: Int
```

Adjustment in text font weight. Used to reflect the current user preference for increasing font weight.

If the text font weight is less than the minimum of 1, 1 will be used. If the font weight exceeds the maximum of 1000, 1000 will be used. 
**See Also**

- [android.graphics.Typeface#create(Typeface, int, boolean)](../android/graphics/Typeface.md))
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_MIN](../android/graphics/fonts/FontStyle.md)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_MAX](../android/graphics/fonts/FontStyle.md) 

### hardKeyboardHidden

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var hardKeyboardHidden: Int
```

A flag indicating whether the hard keyboard has been hidden. This will be set on a device with a mechanism to hide the keyboard from the user, when that mechanism is closed. One of: [HARDKEYBOARDHIDDEN_NO](../android/content/res/Configuration.md), [HARDKEYBOARDHIDDEN_YES](../android/content/res/Configuration.md). 

### keyboard

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var keyboard: Int
```

The kind of keyboard attached to the device. One of: [KEYBOARD_NOKEYS](../android/content/res/Configuration.md), [KEYBOARD_QWERTY](../android/content/res/Configuration.md), [KEYBOARD_12KEY](../android/content/res/Configuration.md). 

### keyboardHidden

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var keyboardHidden: Int
```

A flag indicating whether any keyboard is available. Unlike [hardKeyboardHidden](../android/content/res/Configuration.md), this also takes into account a soft keyboard, so if the hard keyboard is hidden but there is soft keyboard available, it will be set to NO. Value is one of: [KEYBOARDHIDDEN_NO](../android/content/res/Configuration.md), [KEYBOARDHIDDEN_YES](../android/content/res/Configuration.md). 

### locale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var locale: Locale!
```

**Deprecated:** *Do not set or read this directly. Use [getLocales()](../android/content/res/Configuration.md))and [setLocales(android.os.LocaleList)](../android/content/res/Configuration.md)). If only the primary locale is needed,`getLocales().get(0)`is now the preferred accessor.*

Current user preference for the locale, corresponding to [locale](https://developer.android.com/guide/topics/resources/providing-resources.html#LocaleQualifier) resource qualifier. 

### mcc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var mcc: Int
```

IMSI MCC (Mobile Country Code), corresponding to [mcc](https://developer.android.com/guide/topics/resources/providing-resources.html#MccQualifier) resource qualifier. 0 if undefined. 

### mnc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var mnc: Int
```

IMSI MNC (Mobile Network Code), corresponding to [mnc](https://developer.android.com/guide/topics/resources/providing-resources.html#MccQualifier) resource qualifier. 0 if undefined. Note that the actual MNC may be 0; in order to check for this use the [MNC_ZERO](../android/content/res/Configuration.md) symbol. 

### navigation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var navigation: Int
```

The kind of navigation method available on the device. One of: [NAVIGATION_NONAV](../android/content/res/Configuration.md), [NAVIGATION_DPAD](../android/content/res/Configuration.md), [NAVIGATION_TRACKBALL](../android/content/res/Configuration.md), [NAVIGATION_WHEEL](../android/content/res/Configuration.md). 

### navigationHidden

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var navigationHidden: Int
```

A flag indicating whether any 5-way or DPAD navigation available. This will be set on a device with a mechanism to hide the navigation controls from the user, when that mechanism is closed. One of: [NAVIGATIONHIDDEN_NO](../android/content/res/Configuration.md), [NAVIGATIONHIDDEN_YES](../android/content/res/Configuration.md). 

### orientation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var orientation: Int
```

Overall orientation of the screen. May be one of [ORIENTATION_LANDSCAPE](../android/content/res/Configuration.md), [ORIENTATION_PORTRAIT](../android/content/res/Configuration.md). 
Value is [android.content.res.Configuration#ORIENTATION_UNDEFINED](../android/content/res/Configuration.md), [android.content.res.Configuration#ORIENTATION_PORTRAIT](../android/content/res/Configuration.md), [android.content.res.Configuration#ORIENTATION_LANDSCAPE](../android/content/res/Configuration.md), or [android.content.res.Configuration#ORIENTATION_SQUARE](../android/content/res/Configuration.md) 

### screenHeightDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var screenHeightDp: Int
```

The height of the available screen space in dp units.**Note:** If the app targets [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md) or after, the height measurement reflects the window size without excluding insets. Otherwise, the measurement excludes window insets even when the app is displayed edge to edge using [Window#setDecorFitsSystemWindows(boolean)](../android/view/Window.md)). Use [android.view.WindowMetrics#getBounds()](../android/view/WindowMetrics.md))to always obtain the vertical display area available to an app or embedded activity including the area occupied by window insets. A version of the API is also available for use on older platforms through androidx.window.layout.WindowMetrics.

Corresponds to the [available height](https://developer.android.com/guide/topics/resources/providing-resources.html#AvailableWidthHeightQualifier) resource qualifier. Defaults to [SCREEN_HEIGHT_DP_UNDEFINED](../android/content/res/Configuration.md) if no height is specified.

In multi-window mode, equals the height of the available display area of the app window, not the available display area of the device screen (for example, when apps are displayed one above another in split-screen mode in portrait orientation).

For embedded activities, equals the height of the individual activities, not the height of the app window or the device screen.

In multiple-screen scenarios, the height measurement can span screens. For example, if the app is spanning both screens of a dual-screen device rotated 90 degrees (one screen above the other),`screenHeightDp`represents the height of both screens excluding the area occupied by window insets. When the app is restricted to a single screen in a multiple-screen environment,`screenHeightDp`is the height of the screen on which the app is displayed excluding window insets.

If the app targets [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md) or after, it is the same as [android.view.WindowMetrics](../android/view/WindowMetrics.md), but is expressed rounded to the nearest dp rather than px.

Otherwise, differs from [android.view.WindowMetrics](../android/view/WindowMetrics.md) by not including window insets in the height measurement and by expressing the measurement in dp rather than px. Use`screenHeightDp`to obtain the height of the display area available to an app or embedded activity excluding the area occupied by window insets. 

### screenLayout

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var screenLayout: Int
```

Bit mask of overall layout of the screen. Currently there are four fields:

The [SCREENLAYOUT_SIZE_MASK](../android/content/res/Configuration.md) bits define the overall size of the screen. They may be one of [SCREENLAYOUT_SIZE_SMALL](../android/content/res/Configuration.md), [SCREENLAYOUT_SIZE_NORMAL](../android/content/res/Configuration.md), [SCREENLAYOUT_SIZE_LARGE](../android/content/res/Configuration.md), or [SCREENLAYOUT_SIZE_XLARGE](../android/content/res/Configuration.md).

The [SCREENLAYOUT_LONG_MASK](../android/content/res/Configuration.md) defines whether the screen is wider/taller than normal. They may be one of [SCREENLAYOUT_LONG_NO](../android/content/res/Configuration.md) or [SCREENLAYOUT_LONG_YES](../android/content/res/Configuration.md).

The [SCREENLAYOUT_LAYOUTDIR_MASK](../android/content/res/Configuration.md) defines whether the screen layout is either LTR or RTL. They may be one of [SCREENLAYOUT_LAYOUTDIR_LTR](../android/content/res/Configuration.md) or [SCREENLAYOUT_LAYOUTDIR_RTL](../android/content/res/Configuration.md).

The [SCREENLAYOUT_ROUND_MASK](../android/content/res/Configuration.md) defines whether the screen has a rounded shape. They may be one of [SCREENLAYOUT_ROUND_NO](../android/content/res/Configuration.md) or [SCREENLAYOUT_ROUND_YES](../android/content/res/Configuration.md).

See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

### screenWidthDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var screenWidthDp: Int
```

The width of the available screen space in dp units.**Note:** If the app targets [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md) or after, the width measurement reflects the window size without excluding insets. Otherwise, the measurement excludes window insets even when the app is displayed edge to edge using [Window#setDecorFitsSystemWindows(boolean)](../android/view/Window.md)). Use [android.view.WindowMetrics#getBounds()](../android/view/WindowMetrics.md))to always obtain the horizontal display area available to an app or embedded activity including the area occupied by window insets. A version of the API is also available for use on older platforms through androidx.window.layout.WindowMetrics.

Corresponds to the [available width](https://developer.android.com/guide/topics/resources/providing-resources.html#AvailableWidthHeightQualifier) resource qualifier. Defaults to [SCREEN_WIDTH_DP_UNDEFINED](../android/content/res/Configuration.md) if no width is specified.

In multi-window mode, equals the width of the available display area of the app window, not the available display area of the device screen (for example, when apps are displayed side by side in split-screen mode in landscape orientation).

For embedded activities, equals the width of the individual activities, not the width of the app window or the device screen.

In multiple-screen scenarios, the width measurement can span screens. For example, if the app is spanning both screens of a dual-screen device (with the screens side by side),`screenWidthDp`represents the width of both screens excluding the area occupied by window insets. When the app is restricted to a single screen in a multiple-screen environment,`screenWidthDp`is the width of the screen on which the app is displayed excluding window insets.

If the app targets [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md) or after, it is the same as [android.view.WindowMetrics](../android/view/WindowMetrics.md), but is expressed rounded to the nearest dp rather than px.

Otherwise, differs from [android.view.WindowMetrics](../android/view/WindowMetrics.md) by not including window insets in the width measurement and by expressing the measurement in dp rather than px. Use`screenWidthDp`to obtain the width of the display area available to an app or embedded activity excluding the area occupied by window insets. 

### smallestScreenWidthDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var smallestScreenWidthDp: Int
```

The smallest screen size an application will see in normal operation. Corresponds to the [smallest width](https://developer.android.com/guide/topics/resources/providing-resources.html#SmallestScreenWidthQualifier) resource qualifier. This is the smallest value of [screenWidthDp](../android/content/res/Configuration.md) and [screenHeightDp](../android/content/res/Configuration.md) in both portrait and landscape orientations. Defaults to [SMALLEST_SCREEN_WIDTH_DP_UNDEFINED](../android/content/res/Configuration.md) if no width is specified. 

### touchscreen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var touchscreen: Int
```

The kind of touch screen attached to the device. One of: [TOUCHSCREEN_NOTOUCH](../android/content/res/Configuration.md), [TOUCHSCREEN_FINGER](../android/content/res/Configuration.md). 

### uiMode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var uiMode: Int
```

Bit mask of the ui mode. Currently there are two fields:

The [UI_MODE_TYPE_MASK](../android/content/res/Configuration.md) bits define the overall ui mode of the device. They may be one of [UI_MODE_TYPE_UNDEFINED](../android/content/res/Configuration.md), [UI_MODE_TYPE_NORMAL](../android/content/res/Configuration.md), [UI_MODE_TYPE_DESK](../android/content/res/Configuration.md), [UI_MODE_TYPE_CAR](../android/content/res/Configuration.md), [UI_MODE_TYPE_TELEVISION](../android/content/res/Configuration.md), [UI_MODE_TYPE_APPLIANCE](../android/content/res/Configuration.md), [UI_MODE_TYPE_WATCH](../android/content/res/Configuration.md), or [UI_MODE_TYPE_VR_HEADSET](../android/content/res/Configuration.md).

The [UI_MODE_NIGHT_MASK](../android/content/res/Configuration.md) defines whether the screen is in a special mode. They may be one of [UI_MODE_NIGHT_UNDEFINED](../android/content/res/Configuration.md), [UI_MODE_NIGHT_NO](../android/content/res/Configuration.md) or [UI_MODE_NIGHT_YES](../android/content/res/Configuration.md).
