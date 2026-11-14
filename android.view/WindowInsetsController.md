# WindowInsetsController

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsetsController

Kotlin| [Java](https://developer.android.com/reference/android/view/WindowInsetsController "View this page in Java") 

```
interface WindowInsetsController
```

| [android.view.WindowInsetsController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#) |

Interface to control windows that generate insets. For guidance, see [Hide system bars for immersive mode](https://developer.android.com/develop/ui/views/layout/immersive).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener) Listener to be notified when the set of controllable [WindowInsets.Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) controlled by a [WindowInsetsController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#) changes. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARANCE_LIGHT_CAPTION_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS:kotlin.Int) When [WindowInsetsController.APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND:kotlin.Int) is set, changes the foreground color of the caption bars so that the items on the bar can be read clearly on light backgrounds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARANCE_LIGHT_NAVIGATION_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS:kotlin.Int) Changes the foreground color for light navigation bars so that the items on the bar can be read clearly. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARANCE_LIGHT_STATUS_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS:kotlin.Int) Changes the foreground color for light status bars so that the items on the bar can be read clearly. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND:kotlin.Int) Makes the caption bar transparent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEHAVIOR_DEFAULT](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_DEFAULT:kotlin.Int) The default option for [setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#hide(kotlin.Int))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEHAVIOR_SHOW_BARS_BY_SWIPE](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_SHOW_BARS_BY_SWIPE:kotlin.Int) Option for [setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#hide(kotlin.Int))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEHAVIOR_SHOW_BARS_BY_TOUCH](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_SHOW_BARS_BY_TOUCH:kotlin.Int) Option for [setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE:kotlin.Int) Option for [setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#hide(kotlin.Int))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float)). |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#addOnControllableInsetsChangedListener(android.view.WindowInsetsController.OnControllableInsetsChangedListener))`(`listener:` ` [WindowInsetsController.OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener)`)` Adds a [OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener) to the window insets controller. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `durationMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `interpolator:` ` [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `listener:` ` [WindowInsetsAnimationControlListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener)`)` Lets the application control window inset animations in a frame-by-frame manner by modifying the position of the windows in the system causing insets directly. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemBarsAppearance](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#getSystemBarsAppearance())`()` Retrieves the requested appearance of system bars. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemBarsBehavior](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#getSystemBarsBehavior())`()` Retrieves the requested behavior of system bars. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hide](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#hide(kotlin.Int))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Makes a set of windows causing insets disappear. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#removeOnControllableInsetsChangedListener(android.view.WindowInsetsController.OnControllableInsetsChangedListener))`(`listener:` ` [WindowInsetsController.OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener)`)` Removes a [OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener) from the window insets controller. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemBarsAppearance](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsAppearance(kotlin.Int,%20kotlin.Int))`(`appearance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Controls the appearance of system bars. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemBarsBehavior](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int))`(`behavior:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Controls the behavior of system bars. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#show(kotlin.Int))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Makes a set of windows that cause insets appear on screen. |

## Constants

### APPEARANCE_LIGHT_CAPTION_BARS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPEARANCE_LIGHT_CAPTION_BARS: Int
```

When [WindowInsetsController.APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND:kotlin.Int) is set, changes the foreground color of the caption bars so that the items on the bar can be read clearly on light backgrounds. 

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

The default option for [setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#hide(kotlin.Int))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float)).

When system bars are hidden in this mode, they can be revealed with system gestures, such as swiping from the edge of the screen where the bar is hidden from.

When the gesture navigation is enabled, the system gestures can be triggered regardless the visibility of system bars. 

 Value: 1

### BEHAVIOR_SHOW_BARS_BY_SWIPE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEHAVIOR_SHOW_BARS_BY_SWIPE: Int
```

**Deprecated:** *Use [BEHAVIOR_DEFAULT](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_DEFAULT:kotlin.Int) instead.*

Option for [setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#hide(kotlin.Int))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float)).

When system bars are hidden in this mode, they can be revealed with system gestures, such as swiping from the edge of the screen where the bar is hidden from. 

 Value: 1

### BEHAVIOR_SHOW_BARS_BY_TOUCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEHAVIOR_SHOW_BARS_BY_TOUCH: Int
```

**Deprecated:** *This is not supported on Android [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) and later. Use [BEHAVIOR_DEFAULT](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_DEFAULT:kotlin.Int) or [BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE:kotlin.Int) instead.*

Option for [setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)). System bars will be forcibly shown on any user interaction on the corresponding display if navigation bars are hidden by [hide(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#hide(kotlin.Int))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float)). 

 Value: 0

### BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE: Int
```

Option for [setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)): Window would like to remain interactive when hiding navigation bars by calling [hide(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#hide(kotlin.Int))or [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float)).

When system bars are hidden in this mode, they can be revealed temporarily with system gestures, such as swiping from the edge of the screen where the bar is hidden from. These transient system bars will overlay app's content, may have some degree of transparency, and will automatically hide after a short timeout. 

 Value: 2

## Public methods

### addOnControllableInsetsChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addOnControllableInsetsChangedListener(listener: WindowInsetsController.OnControllableInsetsChangedListener): Unit
```

Adds a [OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener) to the window insets controller.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [WindowInsetsController.OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener):The listener to add. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsController.OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener)
- [#removeOnControllableInsetsChangedListener(OnControllableInsetsChangedListener)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#removeOnControllableInsetsChangedListener(android.view.WindowInsetsController.OnControllableInsetsChangedListener)) 

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
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The [WindowInsets.Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s the application has requested to control. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Duration of animation in [java.util.concurrent.TimeUnit#MILLISECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#), or -1 if the animation doesn't have a predetermined duration. This value will be passed to [WindowInsetsAnimation.getDurationMillis()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getDurationMillis()) |
| `interpolator` | [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)?:The interpolator used for this animation, or`null`if this animation doesn't follow an interpolation curve. This value will be passed to [WindowInsetsAnimation.getInterpolator()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getInterpolator())and used to calculate [WindowInsetsAnimation.getInterpolatedFraction()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getInterpolatedFraction()). |
| `listener` | [WindowInsetsAnimationControlListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener):The [WindowInsetsAnimationControlListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener) that gets called when the windows are ready to be controlled, among other callbacks. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A cancellation signal that the caller can use to cancel the request to obtain control, or once they have control, to cancel the control. This value may be`null`. |

**See Also**

- [android.view.WindowInsetsAnimation#getFraction()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getFraction())
- [android.view.WindowInsetsAnimation#getInterpolatedFraction()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getInterpolatedFraction())
- [android.view.WindowInsetsAnimation#getInterpolator()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getInterpolator())
- [android.view.WindowInsetsAnimation#getDurationMillis()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getDurationMillis()) 

### getSystemBarsAppearance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemBarsAppearance(): Int
```

Retrieves the requested appearance of system bars.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The requested bitmask of system bar appearance controlled by this window. Value is either`0`or a combination of android.view.WindowInsetsController.APPEARANCE_OPAQUE_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_OPAQUE_NAVIGATION_BARS, android.view.WindowInsetsController.APPEARANCE_LOW_PROFILE_BARS, [android.view.WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS:kotlin.Int), [android.view.WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS:kotlin.Int), android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_NAVIGATION_BARS, [android.view.WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND:kotlin.Int), [android.view.WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS:kotlin.Int), and android.view.WindowInsetsController.APPEARANCE_FORCE_LIGHT_NAVIGATION_BARS |

**See Also**

- [#setSystemBarsAppearance(int, int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsAppearance(kotlin.Int,%20kotlin.Int))
- [android.R.attr#windowLightStatusBar](https://developer.android.com/reference/kotlin/android/R.attr.html#windowLightStatusBar:kotlin.Int)
- [android.R.attr#windowLightNavigationBar](https://developer.android.com/reference/kotlin/android/R.attr.html#windowLightNavigationBar:kotlin.Int) 

### getSystemBarsBehavior

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemBarsBehavior(): Int
```

Retrieves the requested behavior of system bars.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the system bar behavior controlled by this window. Value is [android.view.WindowInsetsController#BEHAVIOR_DEFAULT](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_DEFAULT:kotlin.Int), or [android.view.WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE:kotlin.Int) |

**See Also**

- [#setSystemBarsBehavior(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#setSystemBarsBehavior(kotlin.Int)) 

### hide

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hide(types: Int): Unit
```

Makes a set of windows causing insets disappear.

Note that if the window currently doesn't have control over a certain type, it will apply the change as soon as the window gains control. The app can listen to the event by observing [View.onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets))and checking visibility with [WindowInsets.isVisible](https://developer.android.com/reference/kotlin/android/view/WindowInsets#isVisible(kotlin.Int)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitmask of [WindowInsets.Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) specifying what windows the app would like to make disappear. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

### removeOnControllableInsetsChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeOnControllableInsetsChangedListener(listener: WindowInsetsController.OnControllableInsetsChangedListener): Unit
```

Removes a [OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener) from the window insets controller.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [WindowInsetsController.OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener):The listener to remove. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsController.OnControllableInsetsChangedListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.OnControllableInsetsChangedListener)
- [#addOnControllableInsetsChangedListener(OnControllableInsetsChangedListener)](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#addOnControllableInsetsChangedListener(android.view.WindowInsetsController.OnControllableInsetsChangedListener)) 

### setSystemBarsAppearance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSystemBarsAppearance(
    appearance: Int, 
    mask: Int
): Unit
```

Controls the appearance of system bars.

For example, the following statement adds [APPEARANCE_LIGHT_STATUS_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS:kotlin.Int): 

```kotlin
setSystemBarsAppearance(APPEARANCE_LIGHT_STATUS_BARS, APPEARANCE_LIGHT_STATUS_BARS)
  
```
And the following statement clears it: 

```kotlin
setSystemBarsAppearance(0, APPEARANCE_LIGHT_STATUS_BARS)
  
```

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `appearance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Bitmask of appearance flags. Value is either`0`or a combination of android.view.WindowInsetsController.APPEARANCE_OPAQUE_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_OPAQUE_NAVIGATION_BARS, android.view.WindowInsetsController.APPEARANCE_LOW_PROFILE_BARS, [android.view.WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS:kotlin.Int), [android.view.WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS:kotlin.Int), android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_NAVIGATION_BARS, [android.view.WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND:kotlin.Int), [android.view.WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS:kotlin.Int), and android.view.WindowInsetsController.APPEARANCE_FORCE_LIGHT_NAVIGATION_BARS |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Specifies which flags of appearance should be changed. Value is either`0`or a combination of android.view.WindowInsetsController.APPEARANCE_OPAQUE_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_OPAQUE_NAVIGATION_BARS, android.view.WindowInsetsController.APPEARANCE_LOW_PROFILE_BARS, [android.view.WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_STATUS_BARS:kotlin.Int), [android.view.WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_NAVIGATION_BARS:kotlin.Int), android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_STATUS_BARS, android.view.WindowInsetsController.APPEARANCE_SEMI_TRANSPARENT_NAVIGATION_BARS, [android.view.WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_TRANSPARENT_CAPTION_BAR_BACKGROUND:kotlin.Int), [android.view.WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#APPEARANCE_LIGHT_CAPTION_BARS:kotlin.Int), and android.view.WindowInsetsController.APPEARANCE_FORCE_LIGHT_NAVIGATION_BARS |

**See Also**

- [#getSystemBarsAppearance](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#getSystemBarsAppearance()) 

### setSystemBarsBehavior

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSystemBarsBehavior(behavior: Int): Unit
```

Controls the behavior of system bars.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `behavior` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Determines how the bars behave when being hidden by the application. Value is [android.view.WindowInsetsController#BEHAVIOR_DEFAULT](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_DEFAULT:kotlin.Int), or [android.view.WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#BEHAVIOR_SHOW_TRANSIENT_BARS_BY_SWIPE:kotlin.Int) |

**See Also**

- [#getSystemBarsBehavior](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#getSystemBarsBehavior()) 

### show

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun show(types: Int): Unit
```

Makes a set of windows that cause insets appear on screen.

Note that if the window currently doesn't have control over a certain type, it will apply the change as soon as the window gains control. The app can listen to the event by observing [View.onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets))and checking visibility with [WindowInsets.isVisible](https://developer.android.com/reference/kotlin/android/view/WindowInsets#isVisible(kotlin.Int)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitmask of [WindowInsets.Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) specifying what windows the app would like to make appear on screen. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |
