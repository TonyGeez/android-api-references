# Configuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Configuration

Kotlin| [Java](https://developer.android.com/reference/android/content/res/Configuration "View this page in Java") 
| --- | --- |

```
class Configuration : Comparable<Configuration!>, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.res.Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#) |

This class describes all device configuration information that can impact the resources the application retrieves. This includes both user-specified configuration options (locale list and scaling) as well as device configurations (such as input modes, screen size and screen orientation).

You can acquire this object from [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources), using [android.content.res.Resources#getConfiguration](https://developer.android.com/reference/kotlin/android/content/res/Resources#getConfiguration()). Thus, from an activity, you can get it by chaining the request with android.app.Activity#getResources: 

```kotlin
Configuration config = getResources().getConfiguration();
```

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_MASK:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): bits that encode the dynamic range of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_NO:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_HDR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_MASK:kotlin.Int) value indicating that the screen is not HDR (low/standard dynamic range). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_SHIFT](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_SHIFT:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): bits shift to get the screen dynamic range. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_UNDEFINED:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_HDR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_MASK:kotlin.Int) value indicating that it is unknown whether or not the screen is HDR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_HDR_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_YES:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_HDR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_MASK:kotlin.Int) value indicating that the screen is HDR (dynamic range). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_UNDEFINED:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a value indicating that the color mode is undefined |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_MASK:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): bits that encode whether the screen is wide gamut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_WIDE_COLOR_GAMUT_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_NO:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_MASK:kotlin.Int) value indicating that the screen is not wide gamut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_WIDE_COLOR_GAMUT_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_UNDEFINED:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_MASK:kotlin.Int) value indicating that it is unknown whether or not the screen is wide gamut. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COLOR_MODE_WIDE_COLOR_GAMUT_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_YES:kotlin.Int) Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_MASK:kotlin.Int) value indicating that the screen is wide gamut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_DPI_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#DENSITY_DPI_UNDEFINED:kotlin.Int) Default value for [densityDpi](https://developer.android.com/reference/kotlin/android/content/res/Configuration#densityDpi:kotlin.Int) indicating that no width has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_ADJUSTMENT_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#FONT_WEIGHT_ADJUSTMENT_UNDEFINED:kotlin.Int) An undefined fontWeightAdjustment. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAMMATICAL_GENDER_FEMININE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_FEMININE:kotlin.Int) Constant for grammatical gender: to indicate the terms of address the user preferred in an application is feminine. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAMMATICAL_GENDER_MASCULINE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_MASCULINE:kotlin.Int) Constant for grammatical gender: to indicate the terms of address the user preferred in an application is masculine. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAMMATICAL_GENDER_NEUTRAL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_NEUTRAL:kotlin.Int) Constant for grammatical gender: to indicate the terms of address the user preferred in an application is neuter. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAMMATICAL_GENDER_NOT_SPECIFIED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_NOT_SPECIFIED:kotlin.Int) Constant for grammatical gender: to indicate the user has not specified the terms of address for the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HARDKEYBOARDHIDDEN_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#HARDKEYBOARDHIDDEN_NO:kotlin.Int) Constant for [hardKeyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hardKeyboardHidden:kotlin.Int), value corresponding to the physical keyboard being exposed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HARDKEYBOARDHIDDEN_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#HARDKEYBOARDHIDDEN_UNDEFINED:kotlin.Int) Constant for [hardKeyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hardKeyboardHidden:kotlin.Int): a value indicating that no value has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HARDKEYBOARDHIDDEN_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#HARDKEYBOARDHIDDEN_YES:kotlin.Int) Constant for [hardKeyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hardKeyboardHidden:kotlin.Int), value corresponding to the physical keyboard being hidden. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARDHIDDEN_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARDHIDDEN_NO:kotlin.Int) Constant for [keyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboardHidden:kotlin.Int), value corresponding to the [keysexposed](https://developer.android.com/guide/topics/resources/providing-resources.html#KeyboardAvailQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARDHIDDEN_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARDHIDDEN_UNDEFINED:kotlin.Int) Constant for [keyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboardHidden:kotlin.Int): a value indicating that no value has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARDHIDDEN_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARDHIDDEN_YES:kotlin.Int) Constant for [keyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboardHidden:kotlin.Int), value corresponding to the [keyshidden](https://developer.android.com/guide/topics/resources/providing-resources.html#KeyboardAvailQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_12KEY](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARD_12KEY:kotlin.Int) Constant for [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int), value corresponding to the [12key](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_NOKEYS](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARD_NOKEYS:kotlin.Int) Constant for [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int), value corresponding to the [nokeys](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_QWERTY](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARD_QWERTY:kotlin.Int) Constant for [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int), value corresponding to the [qwerty](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARD_UNDEFINED:kotlin.Int) Constant for [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int): a value indicating that no value has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MNC_ZERO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#MNC_ZERO:kotlin.Int) Constant used to to represent MNC (Mobile Network Code) zero. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATIONHIDDEN_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATIONHIDDEN_NO:kotlin.Int) Constant for [navigationHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigationHidden:kotlin.Int), value corresponding to the [navexposed](https://developer.android.com/guide/topics/resources/providing-resources.html#NavAvailQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATIONHIDDEN_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATIONHIDDEN_UNDEFINED:kotlin.Int) Constant for [navigationHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigationHidden:kotlin.Int): a value indicating that no value has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATIONHIDDEN_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATIONHIDDEN_YES:kotlin.Int) Constant for [navigationHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigationHidden:kotlin.Int), value corresponding to the [navhidden](https://developer.android.com/guide/topics/resources/providing-resources.html#NavAvailQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_DPAD](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_DPAD:kotlin.Int) Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int), value corresponding to the [dpad](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_NONAV](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_NONAV:kotlin.Int) Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int), value corresponding to the [nonav](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_TRACKBALL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_TRACKBALL:kotlin.Int) Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int), value corresponding to the [trackball](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_UNDEFINED:kotlin.Int) Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int): a value indicating that no value has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_WHEEL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_WHEEL:kotlin.Int) Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int), value corresponding to the [wheel](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_LANDSCAPE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_LANDSCAPE:kotlin.Int) Constant for [orientation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#orientation:kotlin.Int), value corresponding to the [land](https://developer.android.com/guide/topics/resources/providing-resources.html#OrientationQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_PORTRAIT](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_PORTRAIT:kotlin.Int) Constant for [orientation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#orientation:kotlin.Int), value corresponding to the [port](https://developer.android.com/guide/topics/resources/providing-resources.html#OrientationQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_SQUARE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_SQUARE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_UNDEFINED:kotlin.Int) Constant for [orientation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#orientation:kotlin.Int): a value indicating that no value has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_LTR](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_LTR:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LAYOUTDIR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_MASK:kotlin.Int) value indicating that a layout dir has been set to LTR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_MASK:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits that encode the layout direction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_RTL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_RTL:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LAYOUTDIR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_MASK:kotlin.Int) value indicating that a layout dir has been set to RTL. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_SHIFT](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_SHIFT:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits shift to get the layout direction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LAYOUTDIR_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_UNDEFINED:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LAYOUTDIR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_MASK:kotlin.Int) value indicating that no layout dir has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LONG_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_MASK:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits that encode the aspect ratio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LONG_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_NO:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LONG_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_MASK:kotlin.Int) value that corresponds to the [notlong](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenAspectQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LONG_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_UNDEFINED:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LONG_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_MASK:kotlin.Int) value indicating that no size has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_LONG_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_YES:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LONG_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_MASK:kotlin.Int) value that corresponds to the [long](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenAspectQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_ROUND_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_MASK:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits that encode roundness of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_ROUND_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_NO:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_ROUND_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_MASK:kotlin.Int) value indicating that the screen does not have a rounded shape. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_ROUND_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_UNDEFINED:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_ROUND_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_MASK:kotlin.Int) value indicating that it is unknown whether or not the screen has a round shape. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_ROUND_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_YES:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_ROUND_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_MASK:kotlin.Int) value indicating that the screen has a rounded shape. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_LARGE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_LARGE:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating the screen is at least approximately 480x640 dp units, corresponds to the [large](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits that encode the size. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_NORMAL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_NORMAL:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating the screen is at least approximately 320x470 dp units, corresponds to the [normal](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_SMALL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_SMALL:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating the screen is at least approximately 320x426 dp units, corresponds to the [small](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_UNDEFINED:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating that no size has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_SIZE_XLARGE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_XLARGE:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating the screen is at least approximately 720x960 dp units, corresponds to the [xlarge](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREENLAYOUT_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_UNDEFINED:kotlin.Int) Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a value indicating that screenLayout is undefined |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREEN_HEIGHT_DP_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREEN_HEIGHT_DP_UNDEFINED:kotlin.Int) Default value for [screenHeightDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenHeightDp:kotlin.Int) indicating that no width has been specified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCREEN_WIDTH_DP_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREEN_WIDTH_DP_UNDEFINED:kotlin.Int) Default value for [screenWidthDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenWidthDp:kotlin.Int) indicating that no width has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SMALLEST_SCREEN_WIDTH_DP_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SMALLEST_SCREEN_WIDTH_DP_UNDEFINED:kotlin.Int) Default value for [smallestScreenWidthDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#smallestScreenWidthDp:kotlin.Int) indicating that no width has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOUCHSCREEN_FINGER](https://developer.android.com/reference/kotlin/android/content/res/Configuration#TOUCHSCREEN_FINGER:kotlin.Int) Constant for [touchscreen](https://developer.android.com/reference/kotlin/android/content/res/Configuration#touchscreen:kotlin.Int), value corresponding to the [finger](https://developer.android.com/guide/topics/resources/providing-resources.html#TouchscreenQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOUCHSCREEN_NOTOUCH](https://developer.android.com/reference/kotlin/android/content/res/Configuration#TOUCHSCREEN_NOTOUCH:kotlin.Int) Constant for [touchscreen](https://developer.android.com/reference/kotlin/android/content/res/Configuration#touchscreen:kotlin.Int), value corresponding to the [notouch](https://developer.android.com/guide/topics/resources/providing-resources.html#TouchscreenQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOUCHSCREEN_STYLUS](https://developer.android.com/reference/kotlin/android/content/res/Configuration#TOUCHSCREEN_STYLUS:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOUCHSCREEN_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#TOUCHSCREEN_UNDEFINED:kotlin.Int) Constant for [touchscreen](https://developer.android.com/reference/kotlin/android/content/res/Configuration#touchscreen:kotlin.Int): a value indicating that no value has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_NIGHT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_MASK:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): bits that encode the night mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_NIGHT_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_NO:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_NIGHT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_MASK:kotlin.Int) value that corresponds to the [notnight](https://developer.android.com/guide/topics/resources/providing-resources.html#NightQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_NIGHT_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_UNDEFINED:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_NIGHT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_MASK:kotlin.Int) value indicating that no mode type has been set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_NIGHT_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_YES:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_NIGHT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_MASK:kotlin.Int) value that corresponds to the [night](https://developer.android.com/guide/topics/resources/providing-resources.html#NightQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_APPLIANCE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_APPLIANCE:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [appliance](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_CAR](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_CAR:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [car](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_DESK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_DESK:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [desk](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): bits that encode the mode type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_NORMAL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_NORMAL:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to [no UI mode](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier specified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_TELEVISION](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_TELEVISION:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [television](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_UNDEFINED:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value indicating that no mode type has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_VR_HEADSET](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_VR_HEADSET:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [vrheadset](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UI_MODE_TYPE_WATCH](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_WATCH:kotlin.Int) Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [watch](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#Configuration())`()` Construct an invalid Configuration. |
| [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#Configuration(android.content.res.Configuration))`(`o:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)!`)` Makes a deep copy suitable for modification. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/android/content/res/Configuration#compareTo(android.content.res.Configuration))`(`other:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)!`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/res/Configuration#describeContents())`()` Parcelable methods |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [diff](https://developer.android.com/reference/kotlin/android/content/res/Configuration#diff(android.content.res.Configuration))`(`delta:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)!`)` Return a bit mask of the differences between this Configuration object and the given one. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/content/res/Configuration#equals(android.content.res.Configuration))`(`that:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)!`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/content/res/Configuration#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#) | [generateDelta](https://developer.android.com/reference/kotlin/android/content/res/Configuration#generateDelta(android.content.res.Configuration,%20android.content.res.Configuration))`(`base:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)`, `change:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)`)` Generate a delta Configuration between`base`and`change`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGrammaticalGender](https://developer.android.com/reference/kotlin/android/content/res/Configuration#getGrammaticalGender())`()` Returns the user preference for the grammatical gender. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](https://developer.android.com/reference/kotlin/android/content/res/Configuration#getLayoutDirection())`()` Return the layout direction. |
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | [getLocales](https://developer.android.com/reference/kotlin/android/content/res/Configuration#getLocales())`()` Get the locale list. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLayoutSizeAtLeast](https://developer.android.com/reference/kotlin/android/content/res/Configuration#isLayoutSizeAtLeast(kotlin.Int))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Check if the Configuration's current [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int) is at least the given size. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNightModeActive](https://developer.android.com/reference/kotlin/android/content/res/Configuration#isNightModeActive())`()` Retuns whether the configuration is in night mode |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScreenHdr](https://developer.android.com/reference/kotlin/android/content/res/Configuration#isScreenHdr())`()` Return whether the screen has a high dynamic range. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScreenRound](https://developer.android.com/reference/kotlin/android/content/res/Configuration#isScreenRound())`()` Return whether the screen has a round shape. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScreenWideColorGamut](https://developer.android.com/reference/kotlin/android/content/res/Configuration#isScreenWideColorGamut())`()` Return whether the screen has a wide color gamut and wide color gamut rendering is supported by this device. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [needNewResources](https://developer.android.com/reference/kotlin/android/content/res/Configuration#needNewResources(kotlin.Int,%20kotlin.Int))`(`configChanges:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `interestingChanges:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if a new resource needs to be loaded from the bit set of configuration changes returned by [updateFrom(android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/content/res/Configuration#updateFrom(android.content.res.Configuration)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFromParcel](https://developer.android.com/reference/kotlin/android/content/res/Configuration#readFromParcel(android.os.Parcel))`(`source:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutDirection](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setLayoutDirection(java.util.Locale))`(`loc:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Set the layout direction from a Locale. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setLocale(java.util.Locale))`(`loc:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)?`)` Set the locale list to a list of just one locale. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocales](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setLocales(android.os.LocaleList))`(`locales:` ` [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)?`)` Set the locale list. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTo](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setTo(android.content.res.Configuration))`(`o:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)!`)` Sets the fields in this object to those in the given Configuration. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setToDefaults](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setToDefaults())`()` Set this object to the system defaults. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/res/Configuration#toString())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [updateFrom](https://developer.android.com/reference/kotlin/android/content/res/Configuration#updateFrom(android.content.res.Configuration))`(`delta:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)`)` Copies the fields from delta into this Configuration object, keeping track of which ones have changed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/res/Configuration#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/res/Configuration#CREATOR:android.os.Parcelable.Creator) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int) Bit mask of color capabilities of the screen. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [densityDpi](https://developer.android.com/reference/kotlin/android/content/res/Configuration#densityDpi:kotlin.Int) The target screen density being rendered to, corresponding to [density](https://developer.android.com/guide/topics/resources/providing-resources.html#DensityQualifier) resource qualifier. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [fontScale](https://developer.android.com/reference/kotlin/android/content/res/Configuration#fontScale:kotlin.Float) Current user preference for the scaling factor for fonts, relative to the base density scaling. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [fontWeightAdjustment](https://developer.android.com/reference/kotlin/android/content/res/Configuration#fontWeightAdjustment:kotlin.Int) Adjustment in text font weight. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hardKeyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hardKeyboardHidden:kotlin.Int) A flag indicating whether the hard keyboard has been hidden. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int) The kind of keyboard attached to the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [keyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboardHidden:kotlin.Int) A flag indicating whether any keyboard is available. |
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)! | [locale](https://developer.android.com/reference/kotlin/android/content/res/Configuration#locale:java.util.Locale) Current user preference for the locale, corresponding to [locale](https://developer.android.com/guide/topics/resources/providing-resources.html#LocaleQualifier) resource qualifier. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mcc](https://developer.android.com/reference/kotlin/android/content/res/Configuration#mcc:kotlin.Int) IMSI MCC (Mobile Country Code), corresponding to [mcc](https://developer.android.com/guide/topics/resources/providing-resources.html#MccQualifier) resource qualifier. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mnc](https://developer.android.com/reference/kotlin/android/content/res/Configuration#mnc:kotlin.Int) IMSI MNC (Mobile Network Code), corresponding to [mnc](https://developer.android.com/guide/topics/resources/providing-resources.html#MccQualifier) resource qualifier. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int) The kind of navigation method available on the device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [navigationHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigationHidden:kotlin.Int) A flag indicating whether any 5-way or DPAD navigation available. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orientation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#orientation:kotlin.Int) Overall orientation of the screen. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [screenHeightDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenHeightDp:kotlin.Int) The height of the available screen space in dp units. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int) Bit mask of overall layout of the screen. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [screenWidthDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenWidthDp:kotlin.Int) The width of the available screen space in dp units. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [smallestScreenWidthDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#smallestScreenWidthDp:kotlin.Int) The smallest screen size an application will see in normal operation. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [touchscreen](https://developer.android.com/reference/kotlin/android/content/res/Configuration#touchscreen:kotlin.Int) The kind of touch screen attached to the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int) Bit mask of the ui mode. |

## Constants

### COLOR_MODE_HDR_MASK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_MASK: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): bits that encode the dynamic range of the screen. 

 Value: 12

### COLOR_MODE_HDR_NO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_NO: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_HDR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_MASK:kotlin.Int) value indicating that the screen is not HDR (low/standard dynamic range).

Corresponds to the`-lowdr`resource qualifier. 

 Value: 4

### COLOR_MODE_HDR_SHIFT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_SHIFT: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): bits shift to get the screen dynamic range. 

 Value: 2

### COLOR_MODE_HDR_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_UNDEFINED: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_HDR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_MASK:kotlin.Int) value indicating that it is unknown whether or not the screen is HDR. 

 Value: 0

### COLOR_MODE_HDR_YES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_HDR_YES: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_HDR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_MASK:kotlin.Int) value indicating that the screen is HDR (dynamic range).

Corresponds to the`-highdr`resource qualifier. 

 Value: 8

### COLOR_MODE_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_UNDEFINED: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a value indicating that the color mode is undefined 

 Value: 0

### COLOR_MODE_WIDE_COLOR_GAMUT_MASK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_WIDE_COLOR_GAMUT_MASK: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): bits that encode whether the screen is wide gamut. 

 Value: 3

### COLOR_MODE_WIDE_COLOR_GAMUT_NO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_WIDE_COLOR_GAMUT_NO: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_MASK:kotlin.Int) value indicating that the screen is not wide gamut.

Corresponds to the`-nowidecg`resource qualifier. 

 Value: 1

### COLOR_MODE_WIDE_COLOR_GAMUT_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_WIDE_COLOR_GAMUT_UNDEFINED: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_MASK:kotlin.Int) value indicating that it is unknown whether or not the screen is wide gamut. 

 Value: 0

### COLOR_MODE_WIDE_COLOR_GAMUT_YES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_MODE_WIDE_COLOR_GAMUT_YES: Int
```

Constant for [colorMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#colorMode:kotlin.Int): a [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_MASK:kotlin.Int) value indicating that the screen is wide gamut.

Corresponds to the`-widecg`resource qualifier. 

 Value: 2

### DENSITY_DPI_UNDEFINED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_DPI_UNDEFINED: Int
```

Default value for [densityDpi](https://developer.android.com/reference/kotlin/android/content/res/Configuration#densityDpi:kotlin.Int) indicating that no width has been specified. 

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

Constant for [hardKeyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hardKeyboardHidden:kotlin.Int), value corresponding to the physical keyboard being exposed. 

 Value: 1

### HARDKEYBOARDHIDDEN_UNDEFINED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HARDKEYBOARDHIDDEN_UNDEFINED: Int
```

Constant for [hardKeyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hardKeyboardHidden:kotlin.Int): a value indicating that no value has been set. 

 Value: 0

### HARDKEYBOARDHIDDEN_YES

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HARDKEYBOARDHIDDEN_YES: Int
```

Constant for [hardKeyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hardKeyboardHidden:kotlin.Int), value corresponding to the physical keyboard being hidden. 

 Value: 2

### KEYBOARDHIDDEN_NO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARDHIDDEN_NO: Int
```

Constant for [keyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboardHidden:kotlin.Int), value corresponding to the [keysexposed](https://developer.android.com/guide/topics/resources/providing-resources.html#KeyboardAvailQualifier) resource qualifier. 

 Value: 1

### KEYBOARDHIDDEN_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARDHIDDEN_UNDEFINED: Int
```

Constant for [keyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboardHidden:kotlin.Int): a value indicating that no value has been set. 

 Value: 0

### KEYBOARDHIDDEN_YES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARDHIDDEN_YES: Int
```

Constant for [keyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboardHidden:kotlin.Int), value corresponding to the [keyshidden](https://developer.android.com/guide/topics/resources/providing-resources.html#KeyboardAvailQualifier) resource qualifier. 

 Value: 2

### KEYBOARD_12KEY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_12KEY: Int
```

Constant for [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int), value corresponding to the [12key](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. 

 Value: 3

### KEYBOARD_NOKEYS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_NOKEYS: Int
```

Constant for [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int), value corresponding to the [nokeys](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. 

 Value: 1

### KEYBOARD_QWERTY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_QWERTY: Int
```

Constant for [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int), value corresponding to the [qwerty](https://developer.android.com/guide/topics/resources/providing-resources.html#ImeQualifier) resource qualifier. 

 Value: 2

### KEYBOARD_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_UNDEFINED: Int
```

Constant for [keyboard](https://developer.android.com/reference/kotlin/android/content/res/Configuration#keyboard:kotlin.Int): a value indicating that no value has been set. 

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

Constant for [navigationHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigationHidden:kotlin.Int), value corresponding to the [navexposed](https://developer.android.com/guide/topics/resources/providing-resources.html#NavAvailQualifier) resource qualifier. 

 Value: 1

### NAVIGATIONHIDDEN_UNDEFINED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATIONHIDDEN_UNDEFINED: Int
```

Constant for [navigationHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigationHidden:kotlin.Int): a value indicating that no value has been set. 

 Value: 0

### NAVIGATIONHIDDEN_YES

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATIONHIDDEN_YES: Int
```

Constant for [navigationHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigationHidden:kotlin.Int), value corresponding to the [navhidden](https://developer.android.com/guide/topics/resources/providing-resources.html#NavAvailQualifier) resource qualifier. 

 Value: 2

### NAVIGATION_DPAD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_DPAD: Int
```

Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int), value corresponding to the [dpad](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. 

 Value: 2

### NAVIGATION_NONAV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_NONAV: Int
```

Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int), value corresponding to the [nonav](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. 

 Value: 1

### NAVIGATION_TRACKBALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_TRACKBALL: Int
```

Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int), value corresponding to the [trackball](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. 

 Value: 3

### NAVIGATION_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_UNDEFINED: Int
```

Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int): a value indicating that no value has been set. 

 Value: 0

### NAVIGATION_WHEEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_WHEEL: Int
```

Constant for [navigation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#navigation:kotlin.Int), value corresponding to the [wheel](https://developer.android.com/guide/topics/resources/providing-resources.html#NavigationQualifier) resource qualifier. 

 Value: 4

### ORIENTATION_LANDSCAPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_LANDSCAPE: Int
```

Constant for [orientation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#orientation:kotlin.Int), value corresponding to the [land](https://developer.android.com/guide/topics/resources/providing-resources.html#OrientationQualifier) resource qualifier. 

 Value: 2

### ORIENTATION_PORTRAIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_PORTRAIT: Int
```

Constant for [orientation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#orientation:kotlin.Int), value corresponding to the [port](https://developer.android.com/guide/topics/resources/providing-resources.html#OrientationQualifier) resource qualifier. 

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

Constant for [orientation](https://developer.android.com/reference/kotlin/android/content/res/Configuration#orientation:kotlin.Int): a value indicating that no value has been set. 

 Value: 0

### SCREENLAYOUT_LAYOUTDIR_LTR

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_LTR: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LAYOUTDIR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_MASK:kotlin.Int) value indicating that a layout dir has been set to LTR. 

 Value: 64

### SCREENLAYOUT_LAYOUTDIR_MASK

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_MASK: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits that encode the layout direction. 

 Value: 192

### SCREENLAYOUT_LAYOUTDIR_RTL

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_RTL: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LAYOUTDIR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_MASK:kotlin.Int) value indicating that a layout dir has been set to RTL. 

 Value: 128

### SCREENLAYOUT_LAYOUTDIR_SHIFT

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_SHIFT: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits shift to get the layout direction. 

 Value: 6

### SCREENLAYOUT_LAYOUTDIR_UNDEFINED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LAYOUTDIR_UNDEFINED: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LAYOUTDIR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_MASK:kotlin.Int) value indicating that no layout dir has been set. 

 Value: 0

### SCREENLAYOUT_LONG_MASK

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LONG_MASK: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits that encode the aspect ratio. 

 Value: 48

### SCREENLAYOUT_LONG_NO

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LONG_NO: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LONG_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_MASK:kotlin.Int) value that corresponds to the [notlong](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenAspectQualifier) resource qualifier. 

 Value: 16

### SCREENLAYOUT_LONG_UNDEFINED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LONG_UNDEFINED: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LONG_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_MASK:kotlin.Int) value indicating that no size has been set. 

 Value: 0

### SCREENLAYOUT_LONG_YES

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_LONG_YES: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_LONG_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_MASK:kotlin.Int) value that corresponds to the [long](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenAspectQualifier) resource qualifier. 

 Value: 32

### SCREENLAYOUT_ROUND_MASK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_ROUND_MASK: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits that encode roundness of the screen. 

 Value: 768

### SCREENLAYOUT_ROUND_NO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_ROUND_NO: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_ROUND_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_MASK:kotlin.Int) value indicating that the screen does not have a rounded shape. 

 Value: 256

### SCREENLAYOUT_ROUND_UNDEFINED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_ROUND_UNDEFINED: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_ROUND_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_MASK:kotlin.Int) value indicating that it is unknown whether or not the screen has a round shape. 

 Value: 0

### SCREENLAYOUT_ROUND_YES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_ROUND_YES: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_ROUND_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_MASK:kotlin.Int) value indicating that the screen has a rounded shape. Corners may not be visible to the user; developers should pay special attention to the [android.view.WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#) delivered to views for more information about ensuring content is not obscured.

Corresponds to the`-round`resource qualifier. 

 Value: 512

### SCREENLAYOUT_SIZE_LARGE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_LARGE: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating the screen is at least approximately 480x640 dp units, corresponds to the [large](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

 Value: 3

### SCREENLAYOUT_SIZE_MASK

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_MASK: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): bits that encode the size. 

 Value: 15

### SCREENLAYOUT_SIZE_NORMAL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_NORMAL: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating the screen is at least approximately 320x470 dp units, corresponds to the [normal](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

 Value: 2

### SCREENLAYOUT_SIZE_SMALL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_SMALL: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating the screen is at least approximately 320x426 dp units, corresponds to the [small](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

 Value: 1

### SCREENLAYOUT_SIZE_UNDEFINED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_UNDEFINED: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating that no size has been set. 

 Value: 0

### SCREENLAYOUT_SIZE_XLARGE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_SIZE_XLARGE: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) value indicating the screen is at least approximately 720x960 dp units, corresponds to the [xlarge](https://developer.android.com/guide/topics/resources/providing-resources.html#ScreenSizeQualifier) resource qualifier. See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

 Value: 4

### SCREENLAYOUT_UNDEFINED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREENLAYOUT_UNDEFINED: Int
```

Constant for [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int): a value indicating that screenLayout is undefined 

 Value: 0

### SCREEN_HEIGHT_DP_UNDEFINED

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREEN_HEIGHT_DP_UNDEFINED: Int
```

Default value for [screenHeightDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenHeightDp:kotlin.Int) indicating that no width has been specified. 

 Value: 0

### SCREEN_WIDTH_DP_UNDEFINED

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCREEN_WIDTH_DP_UNDEFINED: Int
```

Default value for [screenWidthDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenWidthDp:kotlin.Int) indicating that no width has been specified. 

 Value: 0

### SMALLEST_SCREEN_WIDTH_DP_UNDEFINED

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SMALLEST_SCREEN_WIDTH_DP_UNDEFINED: Int
```

Default value for [smallestScreenWidthDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#smallestScreenWidthDp:kotlin.Int) indicating that no width has been specified. 

 Value: 0

### TOUCHSCREEN_FINGER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOUCHSCREEN_FINGER: Int
```

Constant for [touchscreen](https://developer.android.com/reference/kotlin/android/content/res/Configuration#touchscreen:kotlin.Int), value corresponding to the [finger](https://developer.android.com/guide/topics/resources/providing-resources.html#TouchscreenQualifier) resource qualifier. 

 Value: 3

### TOUCHSCREEN_NOTOUCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOUCHSCREEN_NOTOUCH: Int
```

Constant for [touchscreen](https://developer.android.com/reference/kotlin/android/content/res/Configuration#touchscreen:kotlin.Int), value corresponding to the [notouch](https://developer.android.com/guide/topics/resources/providing-resources.html#TouchscreenQualifier) resource qualifier. 

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

Constant for [touchscreen](https://developer.android.com/reference/kotlin/android/content/res/Configuration#touchscreen:kotlin.Int): a value indicating that no value has been set. 

 Value: 0

### UI_MODE_NIGHT_MASK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_NIGHT_MASK: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): bits that encode the night mode. 

 Value: 48

### UI_MODE_NIGHT_NO

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_NIGHT_NO: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_NIGHT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_MASK:kotlin.Int) value that corresponds to the [notnight](https://developer.android.com/guide/topics/resources/providing-resources.html#NightQualifier) resource qualifier. 

 Value: 16

### UI_MODE_NIGHT_UNDEFINED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_NIGHT_UNDEFINED: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_NIGHT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_MASK:kotlin.Int) value indicating that no mode type has been set. 

 Value: 0

### UI_MODE_NIGHT_YES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_NIGHT_YES: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_NIGHT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_MASK:kotlin.Int) value that corresponds to the [night](https://developer.android.com/guide/topics/resources/providing-resources.html#NightQualifier) resource qualifier. 

 Value: 32

### UI_MODE_TYPE_APPLIANCE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_APPLIANCE: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [appliance](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 5

### UI_MODE_TYPE_CAR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_CAR: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [car](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 3

### UI_MODE_TYPE_DESK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_DESK: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [desk](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 2

### UI_MODE_TYPE_MASK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_MASK: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): bits that encode the mode type. 

 Value: 15

### UI_MODE_TYPE_NORMAL

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_NORMAL: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to [no UI mode](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier specified. 

 Value: 1

### UI_MODE_TYPE_TELEVISION

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_TELEVISION: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [television](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 4

### UI_MODE_TYPE_UNDEFINED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_UNDEFINED: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value indicating that no mode type has been set. 

 Value: 0

### UI_MODE_TYPE_VR_HEADSET

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_VR_HEADSET: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [vrheadset](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 7

### UI_MODE_TYPE_WATCH

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UI_MODE_TYPE_WATCH: Int
```

Constant for [uiMode](https://developer.android.com/reference/kotlin/android/content/res/Configuration#uiMode:kotlin.Int): a [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) value that corresponds to the [watch](https://developer.android.com/guide/topics/resources/providing-resources.html#UiModeQualifier) resource qualifier. 

 Value: 6

## Public constructors

### Configuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Configuration()
```

Construct an invalid Configuration. This state is only suitable for constructing a Configuration delta that will be applied to some valid Configuration object. In order to create a valid standalone Configuration, you must call [setToDefaults](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setToDefaults()).

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### diff

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun diff(delta: Configuration!): Int
```

Return a bit mask of the differences between this Configuration object and the given one. Does not change the values of either. Any undefined fields in delta are ignored.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns a bit mask indicating which configuration values have changed. Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) |

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

Caveat: If the any of the Configuration's members becomes undefined, then [updateFrom(android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/content/res/Configuration#updateFrom(android.content.res.Configuration))will treat it as a no-op and not update that member. This is fine for device configurations as no member is ever undefined.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `base` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#):This value cannot be`null`. |
| `change` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------|
| [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#) | This value cannot be`null`. |

### getGrammaticalGender

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGrammaticalGender(): Int
```

Returns the user preference for the grammatical gender. Will be [GRAMMATICAL_GENDER_NOT_SPECIFIED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_NOT_SPECIFIED:kotlin.Int) or [GRAMMATICAL_GENDER_NEUTRAL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_NEUTRAL:kotlin.Int) or [GRAMMATICAL_GENDER_FEMININE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_FEMININE:kotlin.Int) or [GRAMMATICAL_GENDER_MASCULINE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_MASCULINE:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The preferred grammatical gender. Value is [android.content.res.Configuration#GRAMMATICAL_GENDER_NOT_SPECIFIED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_NOT_SPECIFIED:kotlin.Int), [android.content.res.Configuration#GRAMMATICAL_GENDER_NEUTRAL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_NEUTRAL:kotlin.Int), [android.content.res.Configuration#GRAMMATICAL_GENDER_FEMININE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_FEMININE:kotlin.Int), or [android.content.res.Configuration#GRAMMATICAL_GENDER_MASCULINE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#GRAMMATICAL_GENDER_MASCULINE:kotlin.Int) |

### getLayoutDirection

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLayoutDirection(): Int
```

Return the layout direction. Will be either [View.LAYOUT_DIRECTION_LTR](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int) or [View.LAYOUT_DIRECTION_RTL](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns [View.LAYOUT_DIRECTION_RTL](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int) if the configuration is [SCREENLAYOUT_LAYOUTDIR_RTL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_RTL:kotlin.Int), otherwise [View.LAYOUT_DIRECTION_LTR](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int). |

### getLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocales(): LocaleList
```

Get the locale list. This is the preferred way for getting the locales (instead of using the direct accessor to [locale](https://developer.android.com/reference/kotlin/android/content/res/Configuration#locale:java.util.Locale), which would only provide the primary locale).

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------|
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | The locale list. This value cannot be`null`. |

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

Check if the Configuration's current [screenLayout](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenLayout:kotlin.Int) is at least the given size.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired size, either [SCREENLAYOUT_SIZE_SMALL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_SMALL:kotlin.Int), [SCREENLAYOUT_SIZE_NORMAL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_NORMAL:kotlin.Int), [SCREENLAYOUT_SIZE_LARGE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_LARGE:kotlin.Int), or [SCREENLAYOUT_SIZE_XLARGE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_XLARGE:kotlin.Int). |

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

Determines if a new resource needs to be loaded from the bit set of configuration changes returned by [updateFrom(android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/content/res/Configuration#updateFrom(android.content.res.Configuration)).

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configChanges` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mask of changes configurations as returned by [updateFrom(android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/content/res/Configuration#updateFrom(android.content.res.Configuration))Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) |
| `interestingChanges` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the configuration changes that the resource can handle as given in [android.util.TypedValue#changingConfigurations](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#changingConfigurations:kotlin.Int) Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) |

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
| `loc` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The Locale. If null will set the layout direction to [View.LAYOUT_DIRECTION_LTR](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int). If not null will set it to the layout direction corresponding to the Locale. |

**See Also**

- [android.view.View#LAYOUT_DIRECTION_LTR](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int)
- [android.view.View#LAYOUT_DIRECTION_RTL](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int) 

### setLocale

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLocale(loc: Locale?): Unit
```

Set the locale list to a list of just one locale. This will also set the layout direction according to the locale. Note that after this is run, calling`.equals()`on the input locale and the [locale](https://developer.android.com/reference/kotlin/android/content/res/Configuration#locale:java.util.Locale) attribute would return`true`if they are not null, but there is no guarantee that they would be the same object. See also the note about layout direction in [setLocales(android.os.LocaleList)](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setLocales(android.os.LocaleList)).

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `loc` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)?:The locale. Can be null. |

### setLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLocales(locales: LocaleList?): Unit
```

Set the locale list. This is the preferred way for setting up the locales (instead of using the direct accessor or [setLocale(java.util.Locale)](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setLocale(java.util.Locale))). This will also set the layout direction according to the first locale in the list. Note that the layout direction will always come from the first locale in the locale list, even if the locale is not supported by the resources (the resources may only support another locale further down the list which has a different direction).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locales` | [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)?:The locale list. If null, an empty LocaleList will be assigned. |

### setTo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTo(o: Configuration!): Unit
```

Sets the fields in this object to those in the given Configuration.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#)!:The Configuration object used to set the values of this Configuration's fields. |

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
| `delta` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration#):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bit mask of the changed fields, as per [diff](https://developer.android.com/reference/kotlin/android/content/res/Configuration#diff(android.content.res.Configuration))Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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

The [COLOR_MODE_WIDE_COLOR_GAMUT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_MASK:kotlin.Int) bits define the color gamut of the screen. They may be one of [COLOR_MODE_WIDE_COLOR_GAMUT_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_NO:kotlin.Int) or [COLOR_MODE_WIDE_COLOR_GAMUT_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_WIDE_COLOR_GAMUT_YES:kotlin.Int).

The [COLOR_MODE_HDR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_MASK:kotlin.Int) defines the dynamic range of the screen. They may be one of [COLOR_MODE_HDR_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_NO:kotlin.Int) or [COLOR_MODE_HDR_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#COLOR_MODE_HDR_YES:kotlin.Int).

See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

### densityDpi

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var densityDpi: Int
```

The target screen density being rendered to, corresponding to [density](https://developer.android.com/guide/topics/resources/providing-resources.html#DensityQualifier) resource qualifier. Set to [DENSITY_DPI_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#DENSITY_DPI_UNDEFINED:kotlin.Int) if no density is specified. 

### fontScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var fontScale: Float
```

Current user preference for the scaling factor for fonts, relative to the base density scaling.

Note: Please do not use this to hardcode font size equations. The equation for font scaling is now non-linear; this coefficient is no longer used as a direct multiplier to determine font size. It exists for informational purposes only.

Please use [android.util.TypedValue#applyDimension(int, float, DisplayMetrics)](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#applyDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))or [android.util.TypedValue#deriveDimension(int, float, DisplayMetrics)](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#deriveDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))to convert between scaled font size dimensions and pixels. 

### fontWeightAdjustment

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var fontWeightAdjustment: Int
```

Adjustment in text font weight. Used to reflect the current user preference for increasing font weight.

If the text font weight is less than the minimum of 1, 1 will be used. If the font weight exceeds the maximum of 1000, 1000 will be used. 
**See Also**

- [android.graphics.Typeface#create(Typeface, int, boolean)](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#create(android.graphics.Typeface,%20kotlin.Int,%20kotlin.Boolean))
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_MIN](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle.html#FONT_WEIGHT_MIN:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_MAX](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle.html#FONT_WEIGHT_MAX:kotlin.Int) 

### hardKeyboardHidden

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var hardKeyboardHidden: Int
```

A flag indicating whether the hard keyboard has been hidden. This will be set on a device with a mechanism to hide the keyboard from the user, when that mechanism is closed. One of: [HARDKEYBOARDHIDDEN_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#HARDKEYBOARDHIDDEN_NO:kotlin.Int), [HARDKEYBOARDHIDDEN_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#HARDKEYBOARDHIDDEN_YES:kotlin.Int). 

### keyboard

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var keyboard: Int
```

The kind of keyboard attached to the device. One of: [KEYBOARD_NOKEYS](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARD_NOKEYS:kotlin.Int), [KEYBOARD_QWERTY](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARD_QWERTY:kotlin.Int), [KEYBOARD_12KEY](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARD_12KEY:kotlin.Int). 

### keyboardHidden

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var keyboardHidden: Int
```

A flag indicating whether any keyboard is available. Unlike [hardKeyboardHidden](https://developer.android.com/reference/kotlin/android/content/res/Configuration#hardKeyboardHidden:kotlin.Int), this also takes into account a soft keyboard, so if the hard keyboard is hidden but there is soft keyboard available, it will be set to NO. Value is one of: [KEYBOARDHIDDEN_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARDHIDDEN_NO:kotlin.Int), [KEYBOARDHIDDEN_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#KEYBOARDHIDDEN_YES:kotlin.Int). 

### locale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var locale: Locale!
```

**Deprecated:** *Do not set or read this directly. Use [getLocales()](https://developer.android.com/reference/kotlin/android/content/res/Configuration#getLocales())and [setLocales(android.os.LocaleList)](https://developer.android.com/reference/kotlin/android/content/res/Configuration#setLocales(android.os.LocaleList)). If only the primary locale is needed,`getLocales().get(0)`is now the preferred accessor.*

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

IMSI MNC (Mobile Network Code), corresponding to [mnc](https://developer.android.com/guide/topics/resources/providing-resources.html#MccQualifier) resource qualifier. 0 if undefined. Note that the actual MNC may be 0; in order to check for this use the [MNC_ZERO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#MNC_ZERO:kotlin.Int) symbol. 

### navigation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var navigation: Int
```

The kind of navigation method available on the device. One of: [NAVIGATION_NONAV](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_NONAV:kotlin.Int), [NAVIGATION_DPAD](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_DPAD:kotlin.Int), [NAVIGATION_TRACKBALL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_TRACKBALL:kotlin.Int), [NAVIGATION_WHEEL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATION_WHEEL:kotlin.Int). 

### navigationHidden

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var navigationHidden: Int
```

A flag indicating whether any 5-way or DPAD navigation available. This will be set on a device with a mechanism to hide the navigation controls from the user, when that mechanism is closed. One of: [NAVIGATIONHIDDEN_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATIONHIDDEN_NO:kotlin.Int), [NAVIGATIONHIDDEN_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#NAVIGATIONHIDDEN_YES:kotlin.Int). 

### orientation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var orientation: Int
```

Overall orientation of the screen. May be one of [ORIENTATION_LANDSCAPE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_LANDSCAPE:kotlin.Int), [ORIENTATION_PORTRAIT](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_PORTRAIT:kotlin.Int). 
Value is [android.content.res.Configuration#ORIENTATION_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_UNDEFINED:kotlin.Int), [android.content.res.Configuration#ORIENTATION_PORTRAIT](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_PORTRAIT:kotlin.Int), [android.content.res.Configuration#ORIENTATION_LANDSCAPE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_LANDSCAPE:kotlin.Int), or [android.content.res.Configuration#ORIENTATION_SQUARE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#ORIENTATION_SQUARE:kotlin.Int) 

### screenHeightDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var screenHeightDp: Int
```

The height of the available screen space in dp units.**Note:** If the app targets [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int) or after, the height measurement reflects the window size without excluding insets. Otherwise, the measurement excludes window insets even when the app is displayed edge to edge using [Window#setDecorFitsSystemWindows(boolean)](https://developer.android.com/reference/kotlin/android/view/Window.html#setDecorFitsSystemWindows(kotlin.Boolean)). Use [android.view.WindowMetrics#getBounds()](https://developer.android.com/reference/kotlin/android/view/WindowMetrics.html#getBounds())to always obtain the vertical display area available to an app or embedded activity including the area occupied by window insets. A version of the API is also available for use on older platforms through androidx.window.layout.WindowMetrics.

Corresponds to the [available height](https://developer.android.com/guide/topics/resources/providing-resources.html#AvailableWidthHeightQualifier) resource qualifier. Defaults to [SCREEN_HEIGHT_DP_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREEN_HEIGHT_DP_UNDEFINED:kotlin.Int) if no height is specified.

In multi-window mode, equals the height of the available display area of the app window, not the available display area of the device screen (for example, when apps are displayed one above another in split-screen mode in portrait orientation).

For embedded activities, equals the height of the individual activities, not the height of the app window or the device screen.

In multiple-screen scenarios, the height measurement can span screens. For example, if the app is spanning both screens of a dual-screen device rotated 90 degrees (one screen above the other),`screenHeightDp`represents the height of both screens excluding the area occupied by window insets. When the app is restricted to a single screen in a multiple-screen environment,`screenHeightDp`is the height of the screen on which the app is displayed excluding window insets.

If the app targets [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int) or after, it is the same as [android.view.WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics.html#), but is expressed rounded to the nearest dp rather than px.

Otherwise, differs from [android.view.WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics.html#) by not including window insets in the height measurement and by expressing the measurement in dp rather than px. Use`screenHeightDp`to obtain the height of the display area available to an app or embedded activity excluding the area occupied by window insets. 

### screenLayout

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var screenLayout: Int
```

Bit mask of overall layout of the screen. Currently there are four fields:

The [SCREENLAYOUT_SIZE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_MASK:kotlin.Int) bits define the overall size of the screen. They may be one of [SCREENLAYOUT_SIZE_SMALL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_SMALL:kotlin.Int), [SCREENLAYOUT_SIZE_NORMAL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_NORMAL:kotlin.Int), [SCREENLAYOUT_SIZE_LARGE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_LARGE:kotlin.Int), or [SCREENLAYOUT_SIZE_XLARGE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_SIZE_XLARGE:kotlin.Int).

The [SCREENLAYOUT_LONG_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_MASK:kotlin.Int) defines whether the screen is wider/taller than normal. They may be one of [SCREENLAYOUT_LONG_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_NO:kotlin.Int) or [SCREENLAYOUT_LONG_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LONG_YES:kotlin.Int).

The [SCREENLAYOUT_LAYOUTDIR_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_MASK:kotlin.Int) defines whether the screen layout is either LTR or RTL. They may be one of [SCREENLAYOUT_LAYOUTDIR_LTR](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_LTR:kotlin.Int) or [SCREENLAYOUT_LAYOUTDIR_RTL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_LAYOUTDIR_RTL:kotlin.Int).

The [SCREENLAYOUT_ROUND_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_MASK:kotlin.Int) defines whether the screen has a rounded shape. They may be one of [SCREENLAYOUT_ROUND_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_NO:kotlin.Int) or [SCREENLAYOUT_ROUND_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREENLAYOUT_ROUND_YES:kotlin.Int).

See [Supporting Multiple Screens](https://developer.android.com/guide/practices/screens_support.html) for more information. 

### screenWidthDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var screenWidthDp: Int
```

The width of the available screen space in dp units.**Note:** If the app targets [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int) or after, the width measurement reflects the window size without excluding insets. Otherwise, the measurement excludes window insets even when the app is displayed edge to edge using [Window#setDecorFitsSystemWindows(boolean)](https://developer.android.com/reference/kotlin/android/view/Window.html#setDecorFitsSystemWindows(kotlin.Boolean)). Use [android.view.WindowMetrics#getBounds()](https://developer.android.com/reference/kotlin/android/view/WindowMetrics.html#getBounds())to always obtain the horizontal display area available to an app or embedded activity including the area occupied by window insets. A version of the API is also available for use on older platforms through androidx.window.layout.WindowMetrics.

Corresponds to the [available width](https://developer.android.com/guide/topics/resources/providing-resources.html#AvailableWidthHeightQualifier) resource qualifier. Defaults to [SCREEN_WIDTH_DP_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SCREEN_WIDTH_DP_UNDEFINED:kotlin.Int) if no width is specified.

In multi-window mode, equals the width of the available display area of the app window, not the available display area of the device screen (for example, when apps are displayed side by side in split-screen mode in landscape orientation).

For embedded activities, equals the width of the individual activities, not the width of the app window or the device screen.

In multiple-screen scenarios, the width measurement can span screens. For example, if the app is spanning both screens of a dual-screen device (with the screens side by side),`screenWidthDp`represents the width of both screens excluding the area occupied by window insets. When the app is restricted to a single screen in a multiple-screen environment,`screenWidthDp`is the width of the screen on which the app is displayed excluding window insets.

If the app targets [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int) or after, it is the same as [android.view.WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics.html#), but is expressed rounded to the nearest dp rather than px.

Otherwise, differs from [android.view.WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics.html#) by not including window insets in the width measurement and by expressing the measurement in dp rather than px. Use`screenWidthDp`to obtain the width of the display area available to an app or embedded activity excluding the area occupied by window insets. 

### smallestScreenWidthDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var smallestScreenWidthDp: Int
```

The smallest screen size an application will see in normal operation. Corresponds to the [smallest width](https://developer.android.com/guide/topics/resources/providing-resources.html#SmallestScreenWidthQualifier) resource qualifier. This is the smallest value of [screenWidthDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenWidthDp:kotlin.Int) and [screenHeightDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration#screenHeightDp:kotlin.Int) in both portrait and landscape orientations. Defaults to [SMALLEST_SCREEN_WIDTH_DP_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#SMALLEST_SCREEN_WIDTH_DP_UNDEFINED:kotlin.Int) if no width is specified. 

### touchscreen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var touchscreen: Int
```

The kind of touch screen attached to the device. One of: [TOUCHSCREEN_NOTOUCH](https://developer.android.com/reference/kotlin/android/content/res/Configuration#TOUCHSCREEN_NOTOUCH:kotlin.Int), [TOUCHSCREEN_FINGER](https://developer.android.com/reference/kotlin/android/content/res/Configuration#TOUCHSCREEN_FINGER:kotlin.Int). 

### uiMode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var uiMode: Int
```

Bit mask of the ui mode. Currently there are two fields:

The [UI_MODE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_MASK:kotlin.Int) bits define the overall ui mode of the device. They may be one of [UI_MODE_TYPE_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_UNDEFINED:kotlin.Int), [UI_MODE_TYPE_NORMAL](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_NORMAL:kotlin.Int), [UI_MODE_TYPE_DESK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_DESK:kotlin.Int), [UI_MODE_TYPE_CAR](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_CAR:kotlin.Int), [UI_MODE_TYPE_TELEVISION](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_TELEVISION:kotlin.Int), [UI_MODE_TYPE_APPLIANCE](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_APPLIANCE:kotlin.Int), [UI_MODE_TYPE_WATCH](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_WATCH:kotlin.Int), or [UI_MODE_TYPE_VR_HEADSET](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_VR_HEADSET:kotlin.Int).

The [UI_MODE_NIGHT_MASK](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_MASK:kotlin.Int) defines whether the screen is in a special mode. They may be one of [UI_MODE_NIGHT_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_UNDEFINED:kotlin.Int), [UI_MODE_NIGHT_NO](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_NO:kotlin.Int) or [UI_MODE_NIGHT_YES](https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_NIGHT_YES:kotlin.Int).
