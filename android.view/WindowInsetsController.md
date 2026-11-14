# WindowInsetsController

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsetsController

Kotlin| [Java](../android/view/WindowInsetsController.md) 
| --- | --- |

```
interface WindowInsetsController
```

| [android.view.WindowInsetsController](../android/view/WindowInsetsController.md) |

Interface to control windows that generate insets. For guidance, see [Hide system bars for immersive mode](https://developer.android.com/develop/ui/views/layout/immersive).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md) Listener to be notified when the set of controllable [WindowInsets.Type](../android/view/WindowInsets.Type.md) controlled by a [WindowInsetsController](../android/view/WindowInsetsController.md) changes. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARANCE_LIGHT_CAPTION_BARS](../android/view/WindowInsetsController.md) When [WindowInsetsController.APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](../android/view/WindowInsetsController.md) is set, changes the foreground color of the caption bars so that the items on the bar can be read clearly on light backgrounds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARANCE_LIGHT_NAVIGATION_BARS](../android/view/WindowInsetsController.md) Changes the foreground color for light navigation bars so that the items on the bar can be read clearly. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARANCE_LIGHT_STATUS_BARS](../android/view/WindowInsetsController.md) Changes the foreground color for light status bars so that the items on the bar can be read clearly. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](../android/view/WindowInsetsController.md) Makes the caption bar transparent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEHAVIOR_DEFAULT](../android/view/WindowInsetsController.md) The default option for [setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](../android/view/WindowInsetsController.md))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](../android/view/WindowInsetsAnimationController.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEHAVIOR_SHOW_BARS_BY_SWIPE](../android/view/WindowInsetsController.md) Option for [setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](../android/view/WindowInsetsController.md))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](../android/view/WindowInsetsAnimationController.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEHAVIOR_SHOW_BARS_BY_TOUCH](../android/view/WindowInsetsController.md) Option for [setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE](../android/view/WindowInsetsController.md) Option for [setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](../android/view/WindowInsetsController.md))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](../android/view/WindowInsetsAnimationController.md)). |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnControllableInsetsChangedListener](../android/view/WindowInsetsController.md))`(`listener:` ` [WindowInsetsController.OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md)`)` Adds a [OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md) to the window insets controller. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [controlWindowInsetsAnimation](../android/view/WindowInsetsController.md))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `durationMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `interpolator:` ` [Interpolator](../android/view/animation/Interpolator.md)?`, `cancellationSignal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`, `listener:` ` [WindowInsetsAnimationControlListener](../android/view/WindowInsetsAnimationControlListener.md)`)` Lets the application control window inset animations in a frame-by-frame manner by modifying the position of the windows in the system causing insets directly. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemBarsAppearance](../android/view/WindowInsetsController.md))`()` Retrieves the requested appearance of system bars. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemBarsBehavior](../android/view/WindowInsetsController.md))`()` Retrieves the requested behavior of system bars. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hide](../android/view/WindowInsetsController.md))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Makes a set of windows causing insets disappear. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnControllableInsetsChangedListener](../android/view/WindowInsetsController.md))`(`listener:` ` [WindowInsetsController.OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md)`)` Removes a [OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md) from the window insets controller. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemBarsAppearance](../android/view/WindowInsetsController.md))`(`appearance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Controls the appearance of system bars. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemBarsBehavior](../android/view/WindowInsetsController.md))`(`behavior:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Controls the behavior of system bars. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](../android/view/WindowInsetsController.md))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Makes a set of windows that cause insets appear on screen. |
| --- | --- |

## Constants

### APPEARANCE_LIGHT_CAPTION_BARS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPEARANCE_LIGHT_CAPTION_BARS: Int
```

When [WindowInsetsController.APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](../android/view/WindowInsetsController.md) is set, changes the foreground color of the caption bars so that the items on the bar can be read clearly on light backgrounds. 

 Value: 256

### APPEARANCE_LIGHT_NAVIGATION_BARS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPEARANCE_LIGHT_NAVIGATION_BARS: Int
```

Changes the foreground color for light navigation bars so that the items on the bar can be read clearly. 

 Value: 16

### APPEARANCE_LIGHT_STATUS_BARS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPEARANCE_LIGHT_STATUS_BARS: Int
```

Changes the foreground color for light status bars so that the items on the bar can be read clearly. 

 Value: 8

### APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND: Int
```

Makes the caption bar transparent. 

 Value: 128

### BEHAVIOR_DEFAULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEHAVIOR_DEFAULT: Int
```

The default option for [setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](../android/view/WindowInsetsController.md))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](../android/view/WindowInsetsAnimationController.md)).

When system bars are hidden in this mode, they can be revealed with system gestures, such as swiping from the edge of the screen where the bar is hidden from.

When the gesture navigation is enabled, the system gestures can be triggered regardless the visibility of system bars. 

 Value: 1

### BEHAVIOR_SHOW_BARS_BY_SWIPE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEHAVIOR_SHOW_BARS_BY_SWIPE: Int
```

**Deprecated:** *Use [BEHAVIOR_DEFAULT](../android/view/WindowInsetsController.md) instead.*

Option for [setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](../android/view/WindowInsetsController.md))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](../android/view/WindowInsetsAnimationController.md)).

When system bars are hidden in this mode, they can be revealed with system gestures, such as swiping from the edge of the screen where the bar is hidden from. 

 Value: 1

### BEHAVIOR_SHOW_BARS_BY_TOUCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEHAVIOR_SHOW_BARS_BY_TOUCH: Int
```

**Deprecated:** *This is not supported on Android [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) and later. Use [BEHAVIOR_DEFAULT](../android/view/WindowInsetsController.md) or [BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE](../android/view/WindowInsetsController.md) instead.*

Option for [setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)). System bars will be forcibly shown on any user interaction on the corresponding display if navigation bars are hidden by [hide(int)](../android/view/WindowInsetsController.md))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](../android/view/WindowInsetsAnimationController.md)). 

 Value: 0

### BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE: Int
```

Option for [setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](../android/view/WindowInsetsController.md))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](../android/view/WindowInsetsAnimationController.md)).

When system bars are hidden in this mode, they can be revealed temporarily with system gestures, such as swiping from the edge of the screen where the bar is hidden from. These transient system bars will overlay app's content, may have some degree of transparency, and will automatically hide after a short timeout. 

 Value: 2

## Public methods

### addOnControllableInsetsChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addOnControllableInsetsChangedListener(listener: WindowInsetsController.OnControllableInsetsChangedListener): Unit
```

Adds a [OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md) to the window insets controller.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [WindowInsetsController.OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md):The listener to add. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsController.OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md)
- [#removeOnControllableInsetsChangedListener(OnControllableInsetsChangedListener)](../android/view/WindowInsetsController.md)) 

### controlWindowInsetsAnimation

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun controlWindowInsetsAnimation(
    types: Int, 
    durationMillis: Long, 
    interpolator: Interpolator?, 
    cancellationSignal: CancellationSignal?, 
    listener: WindowInsetsAnimationControlListener
): Unit
```

Lets the application control window inset animations in a frame-by-frame manner by modifying the position of the windows in the system causing insets directly.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The [WindowInsets.Type](../android/view/WindowInsets.Type.md) s the application has requested to control. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Duration of animation in [java.util.concurrent.TimeUnit#MILLISECONDS](../java/util/concurrent/TimeUnit.md), or -1 if the animation doesn't have a predetermined duration. This value will be passed to [WindowInsetsAnimation.getDurationMillis()](../android/view/WindowInsetsAnimation.md)) |
| `interpolator` | [Interpolator](../android/view/animation/Interpolator.md)?:The interpolator used for this animation, or`null`if this animation doesn't follow an interpolation curve. This value will be passed to [WindowInsetsAnimation.getInterpolator()](../android/view/WindowInsetsAnimation.md))and used to calculate [WindowInsetsAnimation.getInterpolatedFraction()](../android/view/WindowInsetsAnimation.md)). |
| --- | --- |
| `listener` | [WindowInsetsAnimationControlListener](../android/view/WindowInsetsAnimationControlListener.md):The [WindowInsetsAnimationControlListener](../android/view/WindowInsetsAnimationControlListener.md) that gets called when the windows are ready to be controlled, among other callbacks. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](../android/os/CancellationSignal.md)?:A cancellation signal that the caller can use to cancel the request to obtain control, or once they have control, to cancel the control. This value may be`null`. |

**See Also**

- [android.view.WindowInsetsAnimation#getFraction()](../android/view/WindowInsetsAnimation.md))
- [android.view.WindowInsetsAnimation#getInterpolatedFraction()](../android/view/WindowInsetsAnimation.md))
- [android.view.WindowInsetsAnimation#getInterpolator()](../android/view/WindowInsetsAnimation.md))
- [android.view.WindowInsetsAnimation#getDurationMillis()](../android/view/WindowInsetsAnimation.md)) 

### getSystemBarsAppearance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemBarsAppearance(): Int
```

Retrieves the requested appearance of system bars.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The requested bitmask of system bar appearance controlled by this window. Value is either`0`or a combination of android.view.WindowInsetsController.APPEARANCE_OPAQUE_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_OPAQUE_NAVIGATION_BARS, android.view.WindowInsetsController.APPEARANCE_LOW_PROFILE_BARS, [android.view.WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS](../android/view/WindowInsetsController.md), [android.view.WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS](../android/view/WindowInsetsController.md), android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_NAVIGATION_BARS, [android.view.WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](../android/view/WindowInsetsController.md), [android.view.WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS](../android/view/WindowInsetsController.md), and android.view.WindowInsetsController.APPEARANCE_FORCE_LIGHT_NAVIGATION_BARS |

**See Also**

- [#setSystemBarsAppearance(int, int)](../android/view/WindowInsetsController.md))
- [android.R.attr#windowLightStatusBar](../android/R.attr.md)
- [android.R.attr#windowLightNavigationBar](../android/R.attr.md) 

### getSystemBarsBehavior

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemBarsBehavior(): Int
```

Retrieves the requested behavior of system bars.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the system bar behavior controlled by this window. Value is [android.view.WindowInsetsController#BEHAVIOR_DEFAULT](../android/view/WindowInsetsController.md), or [android.view.WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE](../android/view/WindowInsetsController.md) |

**See Also**

- [#setSystemBarsBehavior(int)](../android/view/WindowInsetsController.md)) 

### hide

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hide(types: Int): Unit
```

Makes a set of windows causing insets disappear.

Note that if the window currently doesn't have control over a certain type, it will apply the change as soon as the window gains control. The app can listen to the event by observing [View.onApplyWindowInsets](../android/view/View.md))and checking visibility with [WindowInsets.isVisible](../android/view/WindowInsets.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitmask of [WindowInsets.Type](../android/view/WindowInsets.Type.md) specifying what windows the app would like to make disappear. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

### removeOnControllableInsetsChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeOnControllableInsetsChangedListener(listener: WindowInsetsController.OnControllableInsetsChangedListener): Unit
```

Removes a [OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md) from the window insets controller.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [WindowInsetsController.OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md):The listener to remove. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsController.OnControllableInsetsChangedListener](../android/view/WindowInsetsController.OnControllableInsetsChangedListener.md)
- [#addOnControllableInsetsChangedListener(OnControllableInsetsChangedListener)](../android/view/WindowInsetsController.md)) 

### setSystemBarsAppearance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSystemBarsAppearance(
    appearance: Int, 
    mask: Int
): Unit
```

Controls the appearance of system bars.

For example, the following statement adds [APPEARANCE_LIGHT_STATUS_BARS](../android/view/WindowInsetsController.md): 

```kotlin
setSystemBarsAppearance(APPEARANCE_LIGHT_STATUS_BARS, APPEARANCE_LIGHT_STATUS_BARS)
  
```
And the following statement clears it: 

```kotlin
setSystemBarsAppearance(0, APPEARANCE_LIGHT_STATUS_BARS)
  
```

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `appearance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Bitmask of appearance flags. Value is either`0`or a combination of android.view.WindowInsetsController.APPEARANCE_OPAQUE_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_OPAQUE_NAVIGATION_BARS, android.view.WindowInsetsController.APPEARANCE_LOW_PROFILE_BARS, [android.view.WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS](../android/view/WindowInsetsController.md), [android.view.WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS](../android/view/WindowInsetsController.md), android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_NAVIGATION_BARS, [android.view.WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](../android/view/WindowInsetsController.md), [android.view.WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS](../android/view/WindowInsetsController.md), and android.view.WindowInsetsController.APPEARANCE_FORCE_LIGHT_NAVIGATION_BARS |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Specifies which flags of appearance should be changed. Value is either`0`or a combination of android.view.WindowInsetsController.APPEARANCE_OPAQUE_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_OPAQUE_NAVIGATION_BARS, android.view.WindowInsetsController.APPEARANCE_LOW_PROFILE_BARS, [android.view.WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS](../android/view/WindowInsetsController.md), [android.view.WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS](../android/view/WindowInsetsController.md), android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_NAVIGATION_BARS, [android.view.WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](../android/view/WindowInsetsController.md), [android.view.WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS](../android/view/WindowInsetsController.md), and android.view.WindowInsetsController.APPEARANCE_FORCE_LIGHT_NAVIGATION_BARS |

**See Also**

- [#getSystemBarsAppearance](../android/view/WindowInsetsController.md)) 

### setSystemBarsBehavior

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSystemBarsBehavior(behavior: Int): Unit
```

Controls the behavior of system bars.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `behavior` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Determines how the bars behave when being hidden by the application. Value is [android.view.WindowInsetsController#BEHAVIOR_DEFAULT](../android/view/WindowInsetsController.md), or [android.view.WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE](../android/view/WindowInsetsController.md) |

**See Also**

- [#getSystemBarsBehavior](../android/view/WindowInsetsController.md)) 

### show

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun show(types: Int): Unit
```

Makes a set of windows that cause insets appear on screen.

Note that if the window currently doesn't have control over a certain type, it will apply the change as soon as the window gains control. The app can listen to the event by observing [View.onApplyWindowInsets](../android/view/View.md))and checking visibility with [WindowInsets.isVisible](../android/view/WindowInsets.md)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitmask of [WindowInsets.Type](../android/view/WindowInsets.Type.md) specifying what windows the app would like to make appear on screen. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |
