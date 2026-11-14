Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayManager

```
class DisplayManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.display.DisplayManager](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#) |

Manages the properties of attached displays.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener` Listens for changes in available display devices. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#BRIGHTNESS_UNIT_PERCENTAGE:kotlin.Int` Brightness value type where the value is in the range \[0, 100\] and when set, the brightness UI slider will show the same value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#BRIGHTNESS_UNIT_RAW:kotlin.Int` Brightness value type where the value is in the system range \[0. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#DISPLAY_CATEGORY_BUILT_IN_DISPLAYS:kotlin.String` Display category: Built in displays. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#DISPLAY_CATEGORY_PRESENTATION:kotlin.String` Display category: Presentation displays. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_ADDED:kotlin.Long` Event type for when a new display is added. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_BRIGHTNESS:kotlin.Long` Event type to register for a display's brightness changes. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_CHANGED:kotlin.Long` Event type for when a display is changed. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_REFRESH_RATE:kotlin.Long` Event type for when a display's refresh rate changes. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_REMOVED:kotlin.Long` Event type for when a display is removed. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_STATE:kotlin.Long` Event type for when a display state changes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#MATCH_CONTENT_FRAMERATE_ALWAYS:kotlin.Int` Refresh rate switches between all refresh rates are allowed even if they have visual interruptions for the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#MATCH_CONTENT_FRAMERATE_NEVER:kotlin.Int` No mode switching is allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#MATCH_CONTENT_FRAMERATE_SEAMLESSS_ONLY:kotlin.Int` Only refresh rate switches without visual interruptions are allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#MATCH_CONTENT_FRAMERATE_UNKNOWN:kotlin.Int` Match content frame rate user preference is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int` Virtual display flag: Allows content to be mirrored on private displays when no content is being shown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int` Virtual display flag: Only show this display's own content; do not mirror the content of another display. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PRESENTATION:kotlin.Int` Virtual display flag: Create a presentation display. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int` Virtual display flag: Create a public display. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_SECURE:kotlin.Int` Virtual display flag: Create a secure display. |

| Public methods ||
|---|---|
| [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay)? | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#createVirtualDisplay(android.hardware.display.VirtualDisplayConfig)(config: https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig)` Creates a virtual display. |
| [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay)? | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#createVirtualDisplay(android.hardware.display.VirtualDisplayConfig,%20android.os.Handler,%20android.hardware.display.VirtualDisplay.Callback)(config: https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, callback: https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.Callback?)` Creates a virtual display. |
| [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay)! | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, densityDpi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a virtual display. |
| [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay)! | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20kotlin.Int,%20android.hardware.display.VirtualDisplay.Callback,%20android.os.Handler)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, densityDpi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, callback: https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.Callback?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Creates a virtual display. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getBrightness(kotlin.Int,%20kotlin.Int)(displayId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, unit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the brightness of the specified display in the specified brightness unit. |
| [Display](https://developer.android.com/reference/kotlin/android/view/Display.html#)! | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getDisplay(kotlin.Int)(displayId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets information about a logical display. |
| [DisplayTopology](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayTopology)? | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getDisplayTopology()()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Display](https://developer.android.com/reference/kotlin/android/view/Display.html#)!\>! | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getDisplays()()` Gets all currently valid logical displays. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Display](https://developer.android.com/reference/kotlin/android/view/Display.html#)!\>! | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getDisplays(kotlin.String)(category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets all currently valid logical displays of the specified category. |
| [HdrConversionMode](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getHdrConversionMode()()` Returns the `https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode` of the device, which is set by the user. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getMatchContentFrameRateUserPreference()()` Returns the user preference for "Match content frame rate". |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#registerDisplayListener(android.hardware.display.DisplayManager.DisplayListener,%20android.os.Handler)(listener: https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Registers a display listener to receive notifications about when displays are added, removed or changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#registerDisplayListener(java.util.concurrent.Executor,%20kotlin.Long,%20android.hardware.display.DisplayManager.DisplayListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, eventFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, listener: https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener)` Registers a display listener to receive notifications about given display event types. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#registerTopologyListener(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/hardware/display/DisplayTopology!>)` Register a listener to receive display topology updates. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#setBrightness(kotlin.Int,%20kotlin.Float,%20kotlin.Int)(displayId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, unit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the brightness of the specified display. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#unregisterDisplayListener(android.hardware.display.DisplayManager.DisplayListener)(listener: https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener!)` Unregisters a display listener. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#unregisterTopologyListener(java.util.function.Consumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/hardware/display/DisplayTopology!>)` Unregister a display topology listener. |

## Constants

### BRIGHTNESS_UNIT_PERCENTAGE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BRIGHTNESS_UNIT_PERCENTAGE: Int
```

Brightness value type where the value is in the range \[0, 100\] and when set, the brightness UI slider will show the same value. It gets converted from the user-perception scale to the power scale and mapped to the current brightness range. The current brightness range may change over time depending on the device state (such as the brightness of the ambient environment). When this type is used, 0 and 100 map to the current brightness minimum and maximum respectively.

 Value: 1

### BRIGHTNESS_UNIT_RAW

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BRIGHTNESS_UNIT_RAW: Int
```

Brightness value type where the value is in the system range \[0.0f, 1.0f\]. The specific implementation of this unit might be device-dependent and it might differ from the brightness percentage seen by the user on the brightness slider.

 Value: 3

### DISPLAY_CATEGORY_BUILT_IN_DISPLAYS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY_CATEGORY_BUILT_IN_DISPLAYS: String
```

Display category: Built in displays.

This category can be used to identify displays that are built into the device. The displays that are returned may be inactive or disabled at the current moment. The returned displays are useful in identifying the various sizes of built-in displays. The id from `https://developer.android.com/reference/kotlin/android/view/Display.html#getDisplayId()` is not guaranteed to be stable and may change when the display becomes active.

 Value: "android.hardware.display.category.BUILT_IN_DISPLAYS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getDisplays(kotlin.String)`

### DISPLAY_CATEGORY_PRESENTATION

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY_CATEGORY_PRESENTATION: String
```

Display category: Presentation displays.

This category can be used to identify secondary displays that are suitable for use as presentation displays such as external or wireless displays. Applications may automatically project their content to presentation displays to provide richer second screen experiences.

 Value: "android.hardware.display.category.PRESENTATION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Presentation.html#`
- `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_PRESENTATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getDisplays(kotlin.String)`

### EVENT_TYPE_DISPLAY_ADDED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_TYPE_DISPLAY_ADDED: Long
```

Event type for when a new display is added. This notification is sent through the `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayAdded(kotlin.Int)` callback method

 Value: 1L

**See Also**

### EVENT_TYPE_DISPLAY_BRIGHTNESS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_TYPE_DISPLAY_BRIGHTNESS: Long
```

Event type to register for a display's brightness changes. This notification is sent through the `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayChanged(kotlin.Int)` callback method. New brightness values can be retrieved via android.view.Display#getBrightnessInfo().

 Value: 32L

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#registerDisplayListener(java.util.concurrent.Executor,%20kotlin.Long,%20android.hardware.display.DisplayManager.DisplayListener)`

### EVENT_TYPE_DISPLAY_CHANGED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_TYPE_DISPLAY_CHANGED: Long
```

Event type for when a display is changed. `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayChanged(kotlin.Int)` callback is triggered whenever the properties of a `https://developer.android.com/reference/kotlin/android/view/Display.html#`, such as size, state, density are modified. This event is not triggered for refresh rate changes as they can change very often. To monitor refresh rate changes, subscribe to `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_REFRESH_RATE:kotlin.Long`.

 Value: 4L

**See Also**

### EVENT_TYPE_DISPLAY_REFRESH_RATE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_TYPE_DISPLAY_REFRESH_RATE: Long
```

Event type for when a display's refresh rate changes. `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayChanged(kotlin.Int)` callback is triggered whenever the refresh rate of the display changes. New refresh rate values can be retrieved via `https://developer.android.com/reference/kotlin/android/view/Display.html#getRefreshRate()`.

 Value: 8L

**See Also**

### EVENT_TYPE_DISPLAY_REMOVED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_TYPE_DISPLAY_REMOVED: Long
```

Event type for when a display is removed. This notification is sent through the `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayRemoved(kotlin.Int)` callback method

 Value: 2L

**See Also**

### EVENT_TYPE_DISPLAY_STATE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_TYPE_DISPLAY_STATE: Long
```

Event type for when a display state changes. `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayChanged(kotlin.Int)` callback is triggered whenever the state of the display changes. New state values can be retrieved via `https://developer.android.com/reference/kotlin/android/view/Display.html#getState()`.

 Value: 16L

**See Also**

### MATCH_CONTENT_FRAMERATE_ALWAYS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CONTENT_FRAMERATE_ALWAYS: Int
```

Refresh rate switches between all refresh rates are allowed even if they have visual interruptions for the user.

 Value: 2

### MATCH_CONTENT_FRAMERATE_NEVER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CONTENT_FRAMERATE_NEVER: Int
```

No mode switching is allowed.

 Value: 0

### MATCH_CONTENT_FRAMERATE_SEAMLESSS_ONLY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CONTENT_FRAMERATE_SEAMLESSS_ONLY: Int
```

Only refresh rate switches without visual interruptions are allowed.

 Value: 1

### MATCH_CONTENT_FRAMERATE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CONTENT_FRAMERATE_UNKNOWN: Int
```

Match content frame rate user preference is unknown.

 Value: -1

### VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR: Int
```

Virtual display flag: Allows content to be mirrored on private displays when no content is being shown.

This flag is mutually exclusive with `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int`. If both flags are specified then the own-content only behavior will be applied.

The behavior of this flag is implied whenever `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int` is set and `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int` has not been set. This flag is only required to override the default behavior when creating a private display.

Creating an auto-mirroing virtual display requires the CAPTURE_VIDEO_OUTPUT or CAPTURE_SECURE_VIDEO_OUTPUT permission. These permissions are reserved for use by system components and are not available to third-party applications. Alternatively, an appropriate `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.html#` may be used to create an auto-mirroring virtual display.

A private mirroring virtual display will still have its own lock screen, unless #VIRTUAL_DISPLAY_FLAG_ALWAYS_UNLOCKED is set.

 Value: 16

**See Also**

### VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY: Int
```

Virtual display flag: Only show this display's own content; do not mirror the content of another display.

This flag is used in conjunction with `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int`. Ordinarily public virtual displays will automatically mirror the content of the default display if they have no windows of their own. When this flag is specified, the virtual display will only ever show its own content and will be blanked instead if it has no windows.

This flag is mutually exclusive with `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int`. If both flags are specified then the own-content only behavior will be applied.

This behavior of this flag is implied whenever neither `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int` nor `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int` have been set. This flag is only required to override the default behavior when creating a public display.

 Value: 8

**See Also**

### VIRTUAL_DISPLAY_FLAG_PRESENTATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIRTUAL_DISPLAY_FLAG_PRESENTATION: Int
```

Virtual display flag: Create a presentation display.

### Presentation virtual displays

<br />

When this flag is set, the virtual display is registered as a presentation display in the `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#DISPLAY_CATEGORY_PRESENTATION:kotlin.String`. Applications may automatically project their content to presentation displays to provide richer second screen experiences.

### Non-presentation virtual displays

When this flag is not set, the virtual display is not registered as a presentation display. Applications can still project their content on the display but they will typically not do so automatically. This option is appropriate for more special-purpose displays.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Presentation.html#`
- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#DISPLAY_CATEGORY_PRESENTATION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_PRESENTATION:kotlin.Int`

### VIRTUAL_DISPLAY_FLAG_PUBLIC

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIRTUAL_DISPLAY_FLAG_PUBLIC: Int
```

Virtual display flag: Create a public display.

### Public virtual displays

<br />

When this flag is set, the virtual display is public.

A public virtual display behaves just like most any other display that is connected to the system such as an external or wireless display. Applications can open windows on the display and the system may mirror the contents of other displays onto it.

Creating a public virtual display that isn't restricted to own-content only implicitly creates an auto-mirroring display. See `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int` for restrictions on who is allowed to create an auto-mirroring display.

### Private virtual displays

When this flag is not set, the virtual display is private as defined by the `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_PRIVATE:kotlin.Int` display flag.

A private virtual display belongs to the application that created it. Only the owner of a private virtual display and the apps that are already on that display are allowed to place windows upon it. More precisely, the only processes that are allowed to enumerate or interact with the private display are those that have the same UID as the application that originally created the private virtual display or as the activities that are already on that display.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int`

### VIRTUAL_DISPLAY_FLAG_SECURE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIRTUAL_DISPLAY_FLAG_SECURE: Int
```

Virtual display flag: Create a secure display.

### Secure virtual displays

<br />

When this flag is set, the virtual display is considered secure as defined by the `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_SECURE:kotlin.Int` display flag. The caller promises to take reasonable measures, such as over-the-air encryption, to prevent the contents of the display from being intercepted or recorded on a persistent medium.

Creating a secure virtual display requires the CAPTURE_SECURE_VIDEO_OUTPUT permission. This permission is reserved for use by system components and is not available to third-party applications.

### Non-secure virtual displays

When this flag is not set, the virtual display is considered unsecure. The content of secure windows will be blanked if shown on this display.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_SECURE:kotlin.Int`

## Public methods

### createVirtualDisplay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createVirtualDisplay(config: VirtualDisplayConfig): VirtualDisplay?
```

Creates a virtual display.

| Parameters ||
|---|---|
| `config` | [VirtualDisplayConfig](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#createVirtualDisplay(android.hardware.display.VirtualDisplayConfig,%20android.os.Handler,%20android.hardware.display.VirtualDisplay.Callback)`

### createVirtualDisplay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createVirtualDisplay(
    config: VirtualDisplayConfig, 
    handler: Handler?, 
    callback: VirtualDisplay.Callback?
): VirtualDisplay?
```

Creates a virtual display.

The content of a virtual display is rendered to a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` provided by the application.

The virtual display should be `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay#release()` when no longer needed. Because a virtual display renders to a surface provided by the application, it will be released automatically when the process terminates and all remaining windows on it will be forcibly removed.

The behavior of the virtual display depends on the flags that are provided to this method. By default, virtual displays are created to be private, non-presentation and unsecure. Permissions may be required to use certain flags.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT_WATCH:kotlin.Int`, the surface may be attached or detached dynamically using `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay#setSurface(android.view.Surface)`. Previously, the surface had to be non-null when #createVirtualDisplay was called and could not be changed for the lifetime of the display.

Detaching the surface that backs a virtual display has a similar effect to turning off the screen.

| Parameters ||
|---|---|
| `config` | [VirtualDisplayConfig](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig): The configuration of the virtual display, must be non-null. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: The handler on which the listener should be invoked, or null if the listener should be invoked on the calling thread's looper. |
| `callback` | [VirtualDisplay.Callback](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.Callback)?: Callback to call when the state of the `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay` changes. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay?` | The newly created virtual display, or null if the application could not create the virtual display. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have permission to create a virtual display with flags specified in the configuration. |

### createVirtualDisplay

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createVirtualDisplay(
    name: String, 
    width: Int, 
    height: Int, 
    densityDpi: Int, 
    surface: Surface?, 
    flags: Int
): VirtualDisplay!
```

Creates a virtual display.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 1 or greater |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 1 or greater |
| `densityDpi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 1 or greater |
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)?: This value may be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PRESENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_SECURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20kotlin.Int,%20android.hardware.display.VirtualDisplay.Callback,%20android.os.Handler)`

### createVirtualDisplay

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createVirtualDisplay(
    name: String, 
    width: Int, 
    height: Int, 
    densityDpi: Int, 
    surface: Surface?, 
    flags: Int, 
    callback: VirtualDisplay.Callback?, 
    handler: Handler?
): VirtualDisplay!
```

Creates a virtual display.

The content of a virtual display is rendered to a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` provided by the application.

The virtual display should be `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay#release()` when no longer needed. Because a virtual display renders to a surface provided by the application, it will be released automatically when the process terminates and all remaining windows on it will be forcibly removed.

The behavior of the virtual display depends on the flags that are provided to this method. By default, virtual displays are created to be private, non-presentation and unsecure. Permissions may be required to use certain flags.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT_WATCH:kotlin.Int`, the surface may be attached or detached dynamically using `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay#setSurface(android.view.Surface)`. Previously, the surface had to be non-null when #createVirtualDisplay was called and could not be changed for the lifetime of the display.

Detaching the surface that backs a virtual display has a similar effect to turning off the screen.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the virtual display, must be non-empty. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the virtual display in pixels, must be greater than 0. Value is 1 or greater |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the virtual display in pixels, must be greater than 0. Value is 1 or greater |
| `densityDpi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The density of the virtual display in dpi, must be greater than 0. Value is 1 or greater |
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)?: The surface to which the content of the virtual display should be rendered, or null if there is none initially. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A combination of virtual display flags: `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PRESENTATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_SECURE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_PRESENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_SECURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int` |
| `callback` | [VirtualDisplay.Callback](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.Callback)?: Callback to call when the state of the `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay` changes. This value may be `null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: The handler on which the listener should be invoked, or null if the listener should be invoked on the calling thread's looper. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay!` | The newly created virtual display, or null if the application could not create the virtual display. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have permission to create a virtual display with the specified flags. |

### getBrightness

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBrightness(
    displayId: Int, 
    unit: Int
): Float
```

Gets the brightness of the specified display in the specified brightness unit.

| Parameters ||
|---|---|
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The display of which brightness value to get from. |
| `unit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit of the brightness value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#BRIGHTNESS_UNIT_PERCENTAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#BRIGHTNESS_UNIT_RAW:kotlin.Int` |

### getDisplay

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplay(displayId: Int): Display!
```

Gets information about a logical display. The display metrics may be adjusted to provide compatibility for legacy applications.

| Parameters ||
|---|---|
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The logical display id. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Display.html#!` | The display object, or null if there is no valid display with the given id. |

### getDisplayTopology

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayTopology(): DisplayTopology?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayTopology?` | The current display topology that represents the relative positions of extended displays. It only includes the displays that can be reached with the mouse cursor. This value may be `null`. |

### getDisplays

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplays(): Array<Display!>!
```

Gets all currently valid logical displays.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/view/Display.html#!>!` | An array containing all displays. |

### getDisplays

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplays(category: String!): Array<Display!>!
```

Gets all currently valid logical displays of the specified category.

When there are multiple displays in a category the returned displays are sorted of preference. For example, if the requested category is `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#DISPLAY_CATEGORY_PRESENTATION:kotlin.String` and there are multiple presentation displays then the displays are sorted so that the first display in the returned array is the most preferred presentation display. The application may simply use the first display or allow the user to choose.

| Parameters ||
|---|---|
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The requested display category or null to return all displays. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/view/Display.html#!>!` | An array containing all displays sorted by order of preference. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#DISPLAY_CATEGORY_PRESENTATION:kotlin.String`

### getHdrConversionMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHdrConversionMode(): HdrConversionMode
```

Returns the `https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode` of the device, which is set by the user. When `https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#getConversionMode()` is `https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_SYSTEM:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#getPreferredHdrOutputType()` depicts the systemPreferredHdrOutputType. The HDR conversion mode chosen by user which considers the app override is returned. Apps can override HDR conversion using `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#setHdrConversionEnabled(kotlin.Boolean)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode` | This value cannot be `null`. |

### getMatchContentFrameRateUserPreference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMatchContentFrameRateUserPreference(): Int
```

Returns the user preference for "Match content frame rate".

Never: Even if the app requests it, the device will never try to match its output to the original frame rate of the content.

Seamless: If the app requests it, the device will match its output to the original frame rate of the content, ONLY if the display can transition seamlessly.

Always: If the app requests it, the device will match its output to the original frame rate of the content. This may cause the screen to go blank for a second when exiting or entering a video playback.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#MATCH_CONTENT_FRAMERATE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#MATCH_CONTENT_FRAMERATE_NEVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#MATCH_CONTENT_FRAMERATE_SEAMLESSS_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#MATCH_CONTENT_FRAMERATE_ALWAYS:kotlin.Int` |

### registerDisplayListener

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerDisplayListener(
    listener: DisplayManager.DisplayListener!, 
    handler: Handler!
): Unit
```

Registers a display listener to receive notifications about when displays are added, removed or changed. Because of the high frequency at which the refresh rate can change, clients will be registered for refresh rate change callbacks only when they request for refresh rate data(`https://developer.android.com/reference/kotlin/android/view/Display.html#getRefreshRate()`. Or alternately, you can consider using `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#registerDisplayListener(java.util.concurrent.Executor,%20kotlin.Long,%20android.hardware.display.DisplayManager.DisplayListener)` and explicitly subscribe to `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_REFRESH_RATE:kotlin.Long` event We encourage to use `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#registerDisplayListener(java.util.concurrent.Executor,%20kotlin.Long,%20android.hardware.display.DisplayManager.DisplayListener)` instead to subscribe for explicit events of interest

| Parameters ||
|---|---|
| `listener` | [DisplayManager.DisplayListener](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener)!: The listener to register. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: The handler on which the listener should be invoked, or null if the listener should be invoked on the calling thread's looper. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#unregisterDisplayListener(android.hardware.display.DisplayManager.DisplayListener)`

### registerDisplayListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerDisplayListener(
    executor: Executor, 
    eventFilter: Long, 
    listener: DisplayManager.DisplayListener
): Unit
```

Registers a display listener to receive notifications about given display event types.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor for the thread that will be receiving the callbacks. Cannot be null. |
| `eventFilter` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): A bitmask of the event types for which this listener is subscribed. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_ADDED:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_CHANGED:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_REMOVED:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_REFRESH_RATE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_STATE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#EVENT_TYPE_DISPLAY_BRIGHTNESS:kotlin.Long` |
| `listener` | [DisplayManager.DisplayListener](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener): The listener to register. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#registerDisplayListener(android.hardware.display.DisplayManager.DisplayListener,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#unregisterDisplayListener(android.hardware.display.DisplayManager.DisplayListener)`

### registerTopologyListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerTopologyListener(
    executor: Executor, 
    listener: Consumer<DisplayTopology!>
): Unit
```

Register a listener to receive display topology updates.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor specifying the thread on which the callbacks will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [DisplayTopology](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayTopology)!\>: The listener. This value cannot be `null`. |

### setBrightness

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setBrightness(
    displayId: Int, 
    value: Float, 
    unit: Int
): Unit
```

Sets the brightness of the specified display. Accepts different brightness units.

The brightness value, regardless of the unit, might be adjusted by the system to reflect the current system setting and constraints.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SETTINGS:kotlin.String`

| Parameters ||
|---|---|
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The logical display ID |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The brightness value to set |
| `unit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit of the brightness value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#BRIGHTNESS_UNIT_PERCENTAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#BRIGHTNESS_UNIT_RAW:kotlin.Int` |

### unregisterDisplayListener

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterDisplayListener(listener: DisplayManager.DisplayListener!): Unit
```

Unregisters a display listener.

| Parameters ||
|---|---|
| `listener` | [DisplayManager.DisplayListener](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener)!: The listener to unregister. |

**See Also**

### unregisterTopologyListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterTopologyListener(listener: Consumer<DisplayTopology!>): Unit
```

Unregister a display topology listener.

| Parameters ||
|---|---|
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [DisplayTopology](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayTopology)!\>: The listener to unregister. This value cannot be `null`. |
