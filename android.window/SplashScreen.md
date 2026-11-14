# SplashScreen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SplashScreen

Kotlin| [Java](../android/window/SplashScreen.md) 
| --- | --- |

```
interface SplashScreen
```

| [android.window.SplashScreen](../android/window/SplashScreen.md) |

The interface that apps use to talk to the splash screen.

Each splash screen instance is bound to a particular [Activity](../android/app/Activity.md). To obtain a [SplashScreen](../android/window/SplashScreen.md) for an Activity, use`Activity.getSplashScreen()`to get the SplashScreen.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnExitAnimationListener](../android/window/SplashScreen.OnExitAnimationListener.md) Listens for the splash screen exit event. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPLASH_SCREEN_STYLE_ICON](../android/window/SplashScreen.md) Flag to be used with [ActivityOptions.setSplashScreenStyle](../android/app/ActivityOptions.md)), to show the splash screen icon of the launched activity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPLASH_SCREEN_STYLE_SOLID_COLOR](../android/window/SplashScreen.md) Flag to be used with [ActivityOptions.setSplashScreenStyle](../android/app/ActivityOptions.md)), to avoid showing the splash screen icon of the launched activity |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearOnExitAnimationListener](../android/window/SplashScreen.md))`()` Clear exist listener |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnExitAnimationListener](../android/window/SplashScreen.md))`(`listener:` ` [SplashScreen.OnExitAnimationListener](../android/window/SplashScreen.OnExitAnimationListener.md)`)` Specifies whether an [Activity](../android/app/Activity.md) wants to handle the splash screen animation on its own. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSplashScreenTheme](../android/window/SplashScreen.md))`(`themeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Overrides the theme used for the [SplashScreen](../android/window/SplashScreen.md) s of this application. |
| --- | --- |

## Constants

### SPLASH_SCREEN_STYLE_ICON

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPLASH_SCREEN_STYLE_ICON: Int
```

Flag to be used with [ActivityOptions.setSplashScreenStyle](../android/app/ActivityOptions.md)), to show the splash screen icon of the launched activity. 

 Value: 1

### SPLASH_SCREEN_STYLE_SOLID_COLOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPLASH_SCREEN_STYLE_SOLID_COLOR: Int
```

Flag to be used with [ActivityOptions.setSplashScreenStyle](../android/app/ActivityOptions.md)), to avoid showing the splash screen icon of the launched activity 

 Value: 0

## Public methods

### clearOnExitAnimationListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearOnExitAnimationListener(): Unit
```

Clear exist listener 
**See Also**

- [#setOnExitAnimationListener](../android/window/SplashScreen.md)) 

### setOnExitAnimationListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOnExitAnimationListener(listener: SplashScreen.OnExitAnimationListener): Unit
```

Specifies whether an [Activity](../android/app/Activity.md) wants to handle the splash screen animation on its own. Normally the splash screen will show on screen before the content of the activity has been drawn, and disappear when the activity is showing on the screen. With this listener set, the activity will receive [OnExitAnimationListener.onSplashScreenExit](../android/window/SplashScreen.OnExitAnimationListener.md))callback if splash screen is showed, then the activity can create its own exit animation based on the SplashScreenView.

Note that this method must be called before splash screen leave, so it only takes effect during or before [Activity.onResume](../android/app/Activity.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SplashScreen.OnExitAnimationListener](../android/window/SplashScreen.OnExitAnimationListener.md):the listener for receive the splash screen with This value cannot be`null`. |

**See Also**

- [android.window.SplashScreen.OnExitAnimationListener#onSplashScreenExit(SplashScreenView)](../android/window/SplashScreen.OnExitAnimationListener.md)) 

### setSplashScreenTheme

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSplashScreenTheme(themeId: Int): Unit
```

Overrides the theme used for the [SplashScreen](../android/window/SplashScreen.md) s of this application.

By default, the [SplashScreen](../android/window/SplashScreen.md) uses the theme set in the manifest. This method overrides and persists the theme used for the [SplashScreen](../android/window/SplashScreen.md) of this application.

To reset to the default theme, set this the themeId to [Resources.ID_NULL](../android/content/res/Resources.md).

**Note:**Internally, the theme name is resolved and persisted. This means that the theme name must be stable across versions, otherwise it won't be found after your application is updated.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `themeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the splashscreen theme to be used in place of the one defined in the manifest. |
