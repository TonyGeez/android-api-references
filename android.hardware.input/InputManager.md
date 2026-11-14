Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputManager

```
class InputManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.input.InputManager](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#) |

Provides information about input devices and available key layouts.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener` Listens for changes in input devices. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#ACTION_QUERY_KEYBOARD_LAYOUTS:kotlin.String` Broadcast Action: Query available keyboard layouts. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#META_DATA_KEYBOARD_LAYOUTS:kotlin.String` Metadata Key: Keyboard layout metadata associated with `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#ACTION_QUERY_KEYBOARD_LAYOUTS:kotlin.String`. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#addPeripheralCustomization(kotlin.Int,%20kotlin.Int,%20android.hardware.input.CustomizationTrigger,%20android.hardware.input.CustomizationAction)(vendorId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, productId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, trigger: https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger, action: https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationAction)` Adds a new peripheral customization for a given vendor ID and product ID. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [CustomizationTrigger](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger)!, [CustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationAction)!\> | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getAllPeripheralCustomizations(kotlin.Int,%20kotlin.Int)(vendorId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, productId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieves all input customizations for a specific peripheral device. |
| [HostUsiVersion](https://developer.android.com/reference/kotlin/android/hardware/input/HostUsiVersion)? | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getHostUsiVersion(android.view.Display)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#)` Reports the version of the Universal Stylus Initiative (USI) protocol supported by the given display, if any. |
| --- | --- |
| [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice.html#)? | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getInputDevice(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets information about the input device with the specified id. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getInputDeviceIds()()` Gets the ids of all input devices in the system. |
| [InputDevice.ViewBehavior](https://developer.android.com/reference/kotlin/android/view/InputDevice.ViewBehavior.html#)? | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getInputDeviceViewBehavior(kotlin.Int)(deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the `https://developer.android.com/reference/kotlin/android/view/InputDevice.ViewBehavior.html#` of the input device with a given `id`. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getMaximumObscuringOpacityForTouch()()` Returns the maximum allowed obscuring opacity per UID to propagate touches. |
| [CustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationAction)? | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#getPeripheralCustomization(kotlin.Int,%20kotlin.Int,%20android.hardware.input.CustomizationTrigger)(vendorId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, productId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, trigger: https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger)` Retrieves a specific peripheral customization action for a given trigger. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#isButtonAllowedForCustomization(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(vendorId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, productId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, buttonCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if a specific button is allowed for customization on the device(s). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#isKeyAllowedForCustomization(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(vendorId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, productId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets whether a keycode can be customized on a device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#isStylusPointerIconEnabled()()` Check if showing a `https://developer.android.com/reference/kotlin/android/view/PointerIcon.html#` for styluses is enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#registerInputDeviceListener(android.hardware.input.InputManager.InputDeviceListener,%20android.os.Handler)(listener: https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Registers an input device listener to receive notifications about when input devices are added, removed or changed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#removeAllPeripheralCustomizations(kotlin.Int,%20kotlin.Int)(vendorId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, productId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove all peripheral customizations for a given vendor ID and product ID. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#removePeripheralCustomization(kotlin.Int,%20kotlin.Int,%20android.hardware.input.CustomizationTrigger)(vendorId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, productId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, trigger: https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger)` Removes a peripheral customization for a given vendor ID and product ID. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#unregisterInputDeviceListener(android.hardware.input.InputManager.InputDeviceListener)(listener: https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener!)` Unregisters an input device listener. |
| --- | --- |
| [VerifiedInputEvent](https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent.html#)? | `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#verifyInputEvent(android.view.InputEvent)(event: https://developer.android.com/reference/kotlin/android/view/InputEvent.html#)` Verify the details of an `https://developer.android.com/reference/kotlin/android/view/InputEvent.html#` that came from the system. |

## Constants

### ACTION_QUERY_KEYBOARD_LAYOUTS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_QUERY_KEYBOARD_LAYOUTS: String
```

Broadcast Action: Query available keyboard layouts.

The input manager service locates available keyboard layouts by querying broadcast receivers that are registered for this action. An application can offer additional keyboard layouts to the user by declaring a suitable broadcast receiver in its manifest.

Here is an example broadcast receiver declaration that an application might include in its AndroidManifest.xml to advertise keyboard layouts. The meta-data specifies a resource that contains a description of each keyboard layout that is provided by the application.

```kotlin
<code>
  &lt;receiver android:name=".InputDeviceReceiver"
          android:label="@string/keyboard_layouts_label"&gt;
      &lt;intent-filter&gt;
          &lt;action android:name="android.hardware.input.action.QUERY_KEYBOARD_LAYOUTS" /&gt;
      &lt;/intent-filter&gt;
      &lt;meta-data android:name="android.hardware.input.metadata.KEYBOARD_LAYOUTS"
              android:resource="@xml/keyboard_layouts" /&gt;
  &lt;/receiver&gt;
  </code>
```

<br />

In the above example, the `@xml/keyboard_layouts` resource refers to an XML resource whose root element is `<keyboard-layouts>` that contains zero or more `<keyboard-layout>` elements. Each `<keyboard-layout>` element specifies the name, label, and location of a key character map for a particular keyboard layout. The label on the receiver is used to name the collection of keyboard layouts provided by this receiver in the keyboard layout settings.

```kotlin
<code>
  &lt;?xml version="1.0" encoding="utf-8"?&gt;
  &lt;keyboard-layouts xmlns:android="http://schemas.android.com/apk/res/android"&gt;
      &lt;keyboard-layout android:name="keyboard_layout_english_us"
              android:label="@string/keyboard_layout_english_us_label"
              android:keyboardLayout="@raw/keyboard_layout_english_us" /&gt;
  &lt;/keyboard-layouts&gt;
  </code>
```

<br />

The `android:name` attribute specifies an identifier by which the keyboard layout will be known in the package. The `android:label` attribute specifies a human-readable descriptive label to describe the keyboard layout in the user interface, such as "English (US)". The `android:keyboardLayout` attribute refers to a [key character map](https://source.android.com/docs/core/interaction/input/key-character-map-files) resource that defines the keyboard layout. The `android:keyboardLocale` attribute specifies a comma separated list of BCP 47 language tags depicting the locales supported by the keyboard layout. This attribute is optional and will be used for auto layout selection for external physical keyboards. The `android:keyboardLayoutType` attribute specifies the layoutType for the keyboard layout. This can be either empty or one of the following supported layout types: qwerty, qwertz, azerty, dvorak, colemak, workman, extended, turkish_q, turkish_f. This attribute is optional and will be used for auto layout selection for external physical keyboards.

 Value: "android.hardware.input.action.QUERY_KEYBOARD_LAYOUTS"

### META_DATA_KEYBOARD_LAYOUTS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_DATA_KEYBOARD_LAYOUTS: String
```

Metadata Key: Keyboard layout metadata associated with `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#ACTION_QUERY_KEYBOARD_LAYOUTS:kotlin.String`.

Specifies the resource id of a XML resource that describes the keyboard layouts that are provided by the application.

 Value: "android.hardware.input.metadata.KEYBOARD_LAYOUTS"

## Public methods

### addPeripheralCustomization

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addPeripheralCustomization(
    vendorId: Int, 
    productId: Int, 
    trigger: CustomizationTrigger, 
    action: CustomizationAction
): Unit
```

Adds a new peripheral customization for a given vendor ID and product ID.

This will remap a key on all connected peripheral devices matching the vendor and product ID to a different action. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_PERIPHERAL_CUSTOMIZATION:kotlin.String`

| Parameters ||
|---|---|
| `vendorId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the vendor ID of the device |
| `productId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the product ID of the device |
| `trigger` | [CustomizationTrigger](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger): the trigger for the customization. This value cannot be `null`. |
| --- | --- |
| `action` | [CustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationAction): the action to be executed by the trigger. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `CustomizationTrigger` or `CustomizationAction` is unsupported. |
| `java.lang.IllegalStateException` | if no device with `vendorId` and `productId` is connected. |

### getAllPeripheralCustomizations

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAllPeripheralCustomizations(
    vendorId: Int, 
    productId: Int
): MutableMap<CustomizationTrigger!, CustomizationAction!>
```

Retrieves all input customizations for a specific peripheral device. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_PERIPHERAL_CUSTOMIZATION:kotlin.String`

| Parameters ||
|---|---|
| `vendorId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the vendor ID of the device |
| `productId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the product ID of the device |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger!, https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationAction!>` | A map of triggers to actions, or an empty map if none exists. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if no device with `vendorId` and `productId` is connected. |

### getHostUsiVersion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHostUsiVersion(display: Display): HostUsiVersion?
```

Reports the version of the Universal Stylus Initiative (USI) protocol supported by the given display, if any.

| Parameters ||
|---|---|
| `display` | [Display](https://developer.android.com/reference/kotlin/android/view/Display.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/input/HostUsiVersion?` | the USI version supported by the display, or null if the device does not support USI |

**See Also**

### getInputDevice

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputDevice(id: Int): InputDevice?
```

Gets information about the input device with the specified id.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The device id. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#?` | The input device or null if not found. |

### getInputDeviceIds

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputDeviceIds(): IntArray!
```

Gets the ids of all input devices in the system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | The input device ids. |

### getInputDeviceViewBehavior

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputDeviceViewBehavior(deviceId: Int): InputDevice.ViewBehavior?
```

Gets the `https://developer.android.com/reference/kotlin/android/view/InputDevice.ViewBehavior.html#` of the input device with a given `id`.

Use this API to query a fresh view behavior instance whenever the input device changes.

| Parameters ||
|---|---|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the id of the input device whose view behavior is being requested. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/InputDevice.ViewBehavior.html#?` | the view behavior of the input device with the provided id, or `null` if there is not input device with the provided id. |

### getMaximumObscuringOpacityForTouch

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaximumObscuringOpacityForTouch(): Float
```

Returns the maximum allowed obscuring opacity per UID to propagate touches.

For certain window types (eg. `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int`), the decision of honoring `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_NOT_TOUCHABLE:kotlin.Int` or not depends on the combined obscuring opacity of the windows above the touch-consuming window, per UID. Check documentation of `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_NOT_TOUCHABLE:kotlin.Int` for more details.

The value returned is between 0 (inclusive) and 1 (inclusive).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 1.0f inclusive |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_NOT_TOUCHABLE:kotlin.Int`

### getPeripheralCustomization

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPeripheralCustomization(
    vendorId: Int, 
    productId: Int, 
    trigger: CustomizationTrigger
): CustomizationAction?
```

Retrieves a specific peripheral customization action for a given trigger. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_PERIPHERAL_CUSTOMIZATION:kotlin.String`

| Parameters ||
|---|---|
| `vendorId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the vendor ID of the device |
| `productId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the product ID of the device |
| `trigger` | [CustomizationTrigger](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger): This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationAction?` | action or null if none exists. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if no device with `vendorId` and `productId` is connected. |

### isButtonAllowedForCustomization

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isButtonAllowedForCustomization(
    vendorId: Int, 
    productId: Int, 
    buttonCode: Int
): Boolean
```

Checks if a specific button is allowed for customization on the device(s). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_PERIPHERAL_CUSTOMIZATION:kotlin.String`

| Parameters ||
|---|---|
| `vendorId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the vendor ID of the device. |
| `productId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the product ID of the device. |
| `buttonCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the button code to check. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_TERTIARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_BACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_EXTRA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_SIDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_TASK:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the button can be customized on the matching devices, False otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if no device with `vendorId` and `productId` is connected. |

### isKeyAllowedForCustomization

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isKeyAllowedForCustomization(
    vendorId: Int, 
    productId: Int, 
    keyCode: Int
): Boolean
```

Gets whether a keycode can be customized on a device. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_PERIPHERAL_CUSTOMIZATION:kotlin.String`

| Parameters ||
|---|---|
| `vendorId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the vendor ID for the device. |
| `productId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the product ID for the device. |
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the android keycode to check. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F5:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F7:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F9:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F11:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F13:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F15:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F17:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F18:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F19:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F20:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F22:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F23:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_F24:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_ASSIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_BACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_BOOKMARK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_BRIGHTNESS_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_BRIGHTNESS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_CALCULATOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_CALENDAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_CAMERA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_CONTACTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_DICTATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_ENVELOPE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_EXPLORER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_FULLSCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_MEDIA_EJECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_MEDIA_NEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_MEDIA_PLAY_PAUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_MEDIA_PREVIOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_MEDIA_STOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_MENU:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_MOVE_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_MUSIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_NEW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_SCREENSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_SEARCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_SYSRQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_VOLUME_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_VOLUME_MUTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/KeyCustomizationTrigger#CUSTOMIZABLE_KEYCODE_VOLUME_UP:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the keycode can be customized on the device. False otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if no device with `vendorId` and `productId` is connected. |

### isStylusPointerIconEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isStylusPointerIconEnabled(): Boolean
```

Check if showing a `https://developer.android.com/reference/kotlin/android/view/PointerIcon.html#` for styluses is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a pointer icon will be shown over the location of a stylus pointer, false if there is no pointer icon shown for styluses. |

### registerInputDeviceListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerInputDeviceListener(
    listener: InputManager.InputDeviceListener!, 
    handler: Handler!
): Unit
```

Registers an input device listener to receive notifications about when input devices are added, removed or changed.

| Parameters ||
|---|---|
| `listener` | [InputManager.InputDeviceListener](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener)!: The listener to register. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: The handler on which the listener should be invoked, or null if the listener should be invoked on the calling thread's looper. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#unregisterInputDeviceListener(android.hardware.input.InputManager.InputDeviceListener)`

### removeAllPeripheralCustomizations

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeAllPeripheralCustomizations(
    vendorId: Int, 
    productId: Int
): Unit
```

Remove all peripheral customizations for a given vendor ID and product ID.

This will remove all customizations on all connected peripheral devices matching the vendor and product ID. If no customizations exist, this method does nothing. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_PERIPHERAL_CUSTOMIZATION:kotlin.String`

| Parameters ||
|---|---|
| `vendorId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the vendor ID of the device |
| `productId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the product ID of the device |

### removePeripheralCustomization

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removePeripheralCustomization(
    vendorId: Int, 
    productId: Int, 
    trigger: CustomizationTrigger
): Unit
```

Removes a peripheral customization for a given vendor ID and product ID.

This will remove a specific customization on all connected peripheral devices matching the vendor and product ID. If the specified customization does not exist, this method does nothing. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_PERIPHERAL_CUSTOMIZATION:kotlin.String`

| Parameters ||
|---|---|
| `vendorId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the vendor ID of the device |
| `productId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the product ID of the device |
| `trigger` | [CustomizationTrigger](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger): the trigger of the customization to remove. This value cannot be `null`. |
| --- | --- |

### unregisterInputDeviceListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterInputDeviceListener(listener: InputManager.InputDeviceListener!): Unit
```

Unregisters an input device listener.

| Parameters ||
|---|---|
| `listener` | [InputManager.InputDeviceListener](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener)!: The listener to unregister. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager#registerInputDeviceListener(android.hardware.input.InputManager.InputDeviceListener,%20android.os.Handler)`

### verifyInputEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun verifyInputEvent(event: InputEvent): VerifiedInputEvent?
```

Verify the details of an `https://developer.android.com/reference/kotlin/android/view/InputEvent.html#` that came from the system. If the event did not come from the system, or its details could not be verified, then this will return `null`. Receiving `null` does not mean that the event did not originate from the system, just that we were unable to verify it. This can happen for a number of reasons during normal operation.

| Parameters ||
|---|---|
| `event` | [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent.html#): The `https://developer.android.com/reference/kotlin/android/view/InputEvent.html#` to check. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent.html#?` | `https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent.html#`, which is a subset of the provided `https://developer.android.com/reference/kotlin/android/view/InputEvent.html#`, or `null` if the event could not be verified. |
