Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMethodInfo

```
class InputMethodInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.InputMethodInfo](InputMethodInfo.md) |

This class is used to specify meta information of an input method.

It should be defined in an XML resource file with an `<input-method>` element. For more information, see the guide to [Creating an Input Method](https://developer.android.com/guide/topics/text/creating-input-method.html).

## Summary

| XML attributes ||
|---|---|
| [`android:configChanges`](InputMethodInfo.md) | Specify one or more configuration changes that the IME will handle itself. |
| [`android:isDefault`](InputMethodInfo.md) | Set to true in all of the configurations for which this input method should be considered an option as the default. |
| [`android:settingsActivity`](InputMethodInfo.md) | Component name of an activity that allows the user to modify the settings for this service. |
| --- | --- |
| [`android:showInInputMethodPicker`](InputMethodInfo.md) | Specifies whether the IME wants to be shown in the Input Method picker. |
| [`android:supportsInlineSuggestions`](InputMethodInfo.md) | Specifies whether the IME supports showing inline suggestions. |
| [`android:supportsInlineSuggestionsWithTouchExploration`](InputMethodInfo.md) | Specifies whether the IME supports showing inline suggestions when touch exploration is enabled. |
| --- | --- |
| [`android:supportsSwitchingToNextInputMethod`](InputMethodInfo.md) | Set to true if this input method supports ways to switch to a next input method (for example, a globe key.). |
| [`android:suppressesSpellChecker`](InputMethodInfo.md) | Specifies whether the IME suppresses system spell checker. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#ACTION_IME_LANGUAGE_SETTINGS:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()` for the IME language settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#ACTION_STYLUS_HANDWRITING_SETTINGS:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()` for IME that `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#supportsStylusHandwriting()`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#InputMethodInfo(android.content.Context,%20android.content.pm.ResolveInfo)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, service: https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!)` Constructor. |
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#InputMethodInfo(kotlin.String,%20kotlin.String,%20kotlin.CharSequence,%20kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, className: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, label: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, settingsActivity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Temporary API for creating a built-in input method for test. |

| Public methods ||
|---|---|
| [Intent](../android.content/Intent.md)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#createImeLanguageSettingsActivityIntent()()` Returns `https://developer.android.com/reference/kotlin/android/content/Intent.html#` for IME language settings activity with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()``https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#ACTION_IME_LANGUAGE_SETTINGS:kotlin.String`. |
| [Intent](../android.content/Intent.md)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#createStylusHandwritingSettingsActivityIntent()()` Returns `https://developer.android.com/reference/kotlin/android/content/Intent.html#` for stylus handwriting settings activity with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()``https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#ACTION_STYLUS_HANDWRITING_SETTINGS:kotlin.String` if IME `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#supportsStylusHandwriting()`, else `null` if there are no associated settings for stylus handwriting / handwriting is not supported or if `https://developer.android.com/reference/kotlin/android/R.styleable.html#InputMethod_stylusHandwritingSettingsActivity:kotlin.Int` is not defined. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#dump(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Used to test whether the given parameter object is an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#` and its Id is the same to this one. |
| [ComponentName](../android.content/ComponentName.md)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getComponent()()` Return the component of the service that implements this input method. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getConfigChanges()()` Returns the bit mask of kinds of configuration changes that this IME can handle itself (without being restarted by the system). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getId()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getIsDefaultResourceId()()` Return the resource identifier of a resource inside of this input method's . |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getPackageName()()` Return the . |
| [ServiceInfo](../android.content.pm/ServiceInfo.md)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getServiceInfo()()` Return the raw information about the Service implementing this input method. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getServiceName()()` Return the class name of the service component that implements this input method. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getSettingsActivity()()` Return the class name of an activity that provides a settings UI for the input method. |
| [InputMethodSubtype](InputMethodSubtype.md)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getSubtypeAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the Input Method's subtype at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getSubtypeCount()()` Return the count of the subtypes of Input Method. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#hashCode()()` Returns a hash code value for the object. |
| [Drawable](../android.graphics.drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#loadIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!)` Load the user-displayed icon for this input method. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#loadLabel(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!)` Load the user-displayed label for this input method. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#shouldShowInInputMethodPicker()()` Returns `true` if this input method should be shown in menus for selecting an Input Method, such as the system Input Method Picker. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#supportsConnectionlessStylusHandwriting()()` Returns whether the IME supports connectionless stylus handwriting sessions. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#supportsStylusHandwriting()()` Returns if IME supports handwriting using stylus input. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#suppressesSpellChecker()()` Return `true` if this input method suppresses spell checker. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InputMethodInfo](InputMethodInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#CREATOR:android.os.Parcelable.Creator` Used to make this class parcelable. |

## XML attributes

### android:configChanges

```
android:configChanges
```
Specify one or more configuration changes that the IME will handle itself. If not specified, the IME will be restarted if any of these configuration changes happen in the system. Otherwise, the IME will remain running and its android.inputmethodservice.InputMethodService#onConfigurationChanged method is called with the new configuration.

Note that all of these configuration changes can impact the resource values seen by the application, so you will generally need to re-retrieve all resources (including view layouts, drawables, etc) to correctly handle any configuration change.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---|---|---|
| assetsPaths | 80000000 | The assets paths have changed. For example a runtime overlay is installed and enabled. Corresponds to `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int`. |
| colorMode | 4000 | The color mode of the screen has changed (color gamut or dynamic range). By default from Android 17, we don't recreate the activity even the app doesn't specify colorMode in configChanges. If the app wants to recreate the activity, specify colorMode in recreateOnConfigChanges. |
| density | 1000 | The display density has changed. This might be caused by the user specifying a different display scale, or it might be caused by a different display being activated. |
| --- | --- | --- |
| fontScale | 40000000 | The font scaling factor has changed, that is the user has selected a new global font size. |
| fontWeightAdjustment | 10000000 | The font weight adjustment value has changed. Used to reflect the user increasing font weight. |
| grammaticalGender | 8000 | The grammatical gender has changed, for example the user set the grammatical gender from the UI. |
| --- | --- | --- |
| keyboard | 10 | The keyboard type has changed, for example the user has plugged in an external keyboard. By default from Android 17, we don't recreate the activity even the app doesn't specify keyboard in configChanges. If the app wants to recreate the activity, specify keyboard in recreateOnConfigChanges. |
| keyboardHidden | 20 | The keyboard or navigation accessibility has changed, for example the user has slid the keyboard out to expose it. Note that despite its name, this applied to any accessibility: keyboard or navigation. By default from Android 17, we don't recreate the activity even the app doesn't specify keyboardHidden in configChanges. If the app wants to recreate the activity, specify keyboardHidden in recreateOnConfigChanges. |
| layoutDirection | 2000 | The layout direction has changed. For example going from LTR to RTL. |
| --- | --- | --- |
| locale | 4 | The locale has changed, that is the user has selected a new language that text should be displayed in. |
| mcc | 1 | The IMSI MCC has changed, that is a SIM has been detected and updated the Mobile Country Code. By default from Android O, we don't recreate the activity even the app doesn't specify mcc in configChanges. If the app wants to recreate the activity, specify mcc in recreateOnConfigChanges. |
| mnc | 2 | The IMSI MNC has changed, that is a SIM has been detected and updated the Mobile Network Code. By default from Android O, we don't recreate the activity even the app doesn't specify mnc in configChanges. If the app wants to recreate the acvitity, specify mnc in recreateOnConfigChanges. |
| --- | --- | --- |
| navigation | 40 | The navigation type has changed. Should never normally happen. By default from Android 17, we don't recreate the activity even the app doesn't specify navigation in configChanges. If the app wants to recreate the activity, specify navigation in recreateOnConfigChanges. |
| orientation | 80 | The screen orientation has changed, that is the user has rotated the device. |
| resourcesUnused | 8000000 | This is probably not the flag you want, the resources compiler supports a less dangerous version of it, 'allKnown', that only suppresses all currently existing configuration change restarts depending on your target SDK rather than whatever the latest SDK supports, allowing the application to work with resources on future Platform versions. Activity doesn't use Android Resources at all and doesn't need to be restarted on any configuration changes. This overrides all other flags, and this is recommended to be used individually. Corresponds to `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int`. |
| --- | --- | --- |
| screenLayout | 100 | The screen layout has changed. This might be caused by a different display being activated. |
| screenSize | 400 | The current available screen size has changed. If applications don't target at least `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB_MR2:kotlin.Int` then the activity will always handle this itself (the change will not result in a restart). This represents a change in the currently available size, so will change when the user switches between landscape and portrait. |
| smallestScreenSize | 800 | The physical screen size has changed. If applications don't target at least `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB_MR2:kotlin.Int` then the activity will always handle this itself (the change will not result in a restart). This represents a change in size regardless of orientation, so will only change when the actual physical screen size has changed such as switching to an external display. |
| --- | --- | --- |
| touchscreen | 8 | The touchscreen has changed, for example the user has moved the app across displays with different touchscreen abilities. By default from Android 17, we don't recreate the activity even the app doesn't specify touchscreen in configChanges. If the app wants to recreate the activity, specify touchscreen in recreateOnConfigChanges. |
| uiMode | 200 | The global user interface mode has changed. For example, going in or out of car mode, night mode changing, etc. |

### android:isDefault

```
android:isDefault
```
Set to true in all of the configurations for which this input method should be considered an option as the default.

May be a boolean value, such as "`true`" or "`false`".

### android:settingsActivity

```
android:settingsActivity
```
Component name of an activity that allows the user to modify the settings for this service.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

### android:showInInputMethodPicker

```
android:showInInputMethodPicker
```
Specifies whether the IME wants to be shown in the Input Method picker. Defaults to true. Set this to false if the IME is intended to be accessed programmatically.

Note: This functions as a hint to the system, which may choose to ignore this preference in certain situations or in future releases.

May be a boolean value, such as "`true`" or "`false`".

### android:supportsInlineSuggestions

```
android:supportsInlineSuggestions
```
Specifies whether the IME supports showing inline suggestions.

May be a boolean value, such as "`true`" or "`false`".

### android:supportsInlineSuggestionsWithTouchExploration

```
android:supportsInlineSuggestionsWithTouchExploration
```
Specifies whether the IME supports showing inline suggestions when touch exploration is enabled. This does nothing if supportsInlineSuggestions is false. The default value is false and most IMEs should not set this to true since the older menu-style Autofill works better with touch exploration. This attribute should be set to true in special situations, such as if this is an accessibility-focused IME which blocks user interaction with the app window while the IME is displayed.

May be a boolean value, such as "`true`" or "`false`".

### android:supportsSwitchingToNextInputMethod

```
android:supportsSwitchingToNextInputMethod
```
Set to true if this input method supports ways to switch to a next input method (for example, a globe key.). When this is true and InputMethodManager#shouldOfferSwitchingToNextInputMethod() returns true, the IME has to offer ways to invoke InputMethodManager#switchToNextInputMethod() accordingly.

Note that the system determines the most appropriate next input method and subtype in order to provide the consistent user experience in switching between IMEs and subtypes.

May be a boolean value, such as "`true`" or "`false`".

### android:suppressesSpellChecker

```
android:suppressesSpellChecker
```
Specifies whether the IME suppresses system spell checker. The default value is false. If an IME sets this attribute to true, the system spell checker will be disabled while the IME has an active input session.

May be a boolean value, such as "`true`" or "`false`".

## Constants

### ACTION_IME_LANGUAGE_SETTINGS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_IME_LANGUAGE_SETTINGS: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()` for the IME language settings.

 Value: "android.view.inputmethod.action.IME_LANGUAGE_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#createImeLanguageSettingsActivityIntent()`

### ACTION_STYLUS_HANDWRITING_SETTINGS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_STYLUS_HANDWRITING_SETTINGS: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()` for IME that `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#supportsStylusHandwriting()`.

 Value: "android.view.inputmethod.action.STYLUS_HANDWRITING_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#createStylusHandwritingSettingsActivityIntent()`

## Public constructors

### InputMethodInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InputMethodInfo(
    context: Context!, 
    service: ResolveInfo!)
```

Constructor.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: The Context in which we are parsing the input method. |
| `service` | [ResolveInfo](../android.content.pm/ResolveInfo.md)!: The ResolveInfo returned from the package manager about this input method's component. |

### InputMethodInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InputMethodInfo(
    packageName: String!, 
    className: String!, 
    label: CharSequence!, 
    settingsActivity: String!)
```

Temporary API for creating a built-in input method for test.

## Public methods

### createImeLanguageSettingsActivityIntent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createImeLanguageSettingsActivityIntent(): Intent?
```

Returns `https://developer.android.com/reference/kotlin/android/content/Intent.html#` for IME language settings activity with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()``https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#ACTION_IME_LANGUAGE_SETTINGS:kotlin.String`. If `https://developer.android.com/reference/kotlin/android/R.styleable.html#InputMethod_languageSettingsActivity:kotlin.Int` is not defined, tries to fall back to the IME general settings activity. If `https://developer.android.com/reference/kotlin/android/R.styleable.html#InputMethod_settingsActivity:kotlin.Int` is also not defined, returns `null`.

To launch IME language settings, use this method to get the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to launch the IME language settings activity.

e.g.

```kotlin
<code>startActivity(createImeLanguageSettingsActivityIntent());</code>
```

<br />

### createStylusHandwritingSettingsActivityIntent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createStylusHandwritingSettingsActivityIntent(): Intent?
```

Returns `https://developer.android.com/reference/kotlin/android/content/Intent.html#` for stylus handwriting settings activity with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()``https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#ACTION_STYLUS_HANDWRITING_SETTINGS:kotlin.String` if IME `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#supportsStylusHandwriting()`, else `null` if there are no associated settings for stylus handwriting / handwriting is not supported or if `https://developer.android.com/reference/kotlin/android/R.styleable.html#InputMethod_stylusHandwritingSettingsActivity:kotlin.Int` is not defined.

To launch stylus settings, use this method to get the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to launch the stylus handwriting settings activity.

e.g.

```kotlin
<code>startActivity(createStylusHandwritingSettingsActivityIntent());</code>
```

<br />

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getSettingsActivity()`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#supportsStylusHandwriting()`

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### dump

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```

### equals

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Used to test whether the given parameter object is an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#` and its Id is the same to this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given parameter object is an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#` and its Id is the same to this one. |

### getComponent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComponent(): ComponentName!
```

Return the component of the service that implements this input method.

### getConfigChanges

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConfigChanges(): Int
```

Returns the bit mask of kinds of configuration changes that this IME can handle itself (without being restarted by the system).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int` |

### getId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String!
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a unique ID for this input method, which is guaranteed to be the same as the result of `getComponent().flattenToShortString()`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#unflattenFromString(kotlin.String)`

### getIsDefaultResourceId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIsDefaultResourceId(): Int
```

Return the resource identifier of a resource inside of this input method's .apk that determines whether it should be considered a default input method for the system.

### getPackageName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String!
```

Return the .apk package that implements this input method.

### getServiceInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceInfo(): ServiceInfo!
```

Return the raw information about the Service implementing this input method. Do not modify the returned object.

### getServiceName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceName(): String!
```

Return the class name of the service component that implements this input method.

### getSettingsActivity

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSettingsActivity(): String!
```

Return the class name of an activity that provides a settings UI for the input method. You can launch this activity be starting it with an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` whose action is MAIN and with an explicit `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` composed of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#getPackageName()` and the class name returned here.

A null will be returned if there is no settings activity associated with the input method.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#createStylusHandwritingSettingsActivityIntent()`

### getSubtypeAt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubtypeAt(index: Int): InputMethodSubtype!
```

Return the Input Method's subtype at the specified index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the subtype to return. |

### getSubtypeCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubtypeCount(): Int
```

Return the count of the subtypes of Input Method.

### hashCode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### loadIcon

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadIcon(pm: PackageManager!): Drawable!
```

Load the user-displayed icon for this input method.

| Parameters ||
|---|---|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!: Supply a PackageManager used to load the input method's resources. |

### loadLabel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadLabel(pm: PackageManager!): CharSequence!
```

Load the user-displayed label for this input method.

| Parameters ||
|---|---|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!: Supply a PackageManager used to load the input method's resources. |

### shouldShowInInputMethodPicker

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun shouldShowInInputMethodPicker(): Boolean
```

Returns `true` if this input method should be shown in menus for selecting an Input Method, such as the system Input Method Picker. This is `false` if the IME is intended to be accessed programmatically.

### supportsConnectionlessStylusHandwriting

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun supportsConnectionlessStylusHandwriting(): Boolean
```

Returns whether the IME supports connectionless stylus handwriting sessions.

### supportsStylusHandwriting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun supportsStylusHandwriting(): Boolean
```

Returns if IME supports handwriting using stylus input.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo#createStylusHandwritingSettingsActivityIntent()`

### suppressesSpellChecker

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun suppressesSpellChecker(): Boolean
```

Return `true` if this input method suppresses spell checker.

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<InputMethodInfo!>
```

Used to make this class parcelable.
