# SplashScreen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SplashScreen

Kotlin| [Java](https://developer.android.com/reference/android/window/SplashScreen "View this page in Java") 

```
interface SplashScreen
```

| [android.window.SplashScreen](https://developer.android.com/reference/kotlin/android/window/SplashScreen#) |

The interface that apps use to talk to the splash screen.

Each splash screen instance is bound to a particular [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#). To obtain a [SplashScreen](https://developer.android.com/reference/kotlin/android/window/SplashScreen#) for an Activity, use`Activity.getSplashScreen()`to get the SplashScreen.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnExitAnimationListener](https://developer.android.com/reference/kotlin/android/window/SplashScreen.OnExitAnimationListener) Listens for the splash screen exit event. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPLASH_SCREEN_STYLE_ICON](https://developer.android.com/reference/kotlin/android/window/SplashScreen#SPLASH_SCREEN_STYLE_ICON:kotlin.Int) Flag to be used with [ActivityOptions.setSplashScreenStyle](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#setSplashScreenStyle(kotlin.Int)), to show the splash screen icon of the launched activity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPLASH_SCREEN_STYLE_SOLID_COLOR](https://developer.android.com/reference/kotlin/android/window/SplashScreen#SPLASH_SCREEN_STYLE_SOLID_COLOR:kotlin.Int) Flag to be used with [ActivityOptions.setSplashScreenStyle](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#setSplashScreenStyle(kotlin.Int)), to avoid showing the splash screen icon of the launched activity |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearOnExitAnimationListener](https://developer.android.com/reference/kotlin/android/window/SplashScreen#clearOnExitAnimationListener())`()` Clear exist listener |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnExitAnimationListener](https://developer.android.com/reference/kotlin/android/window/SplashScreen#setOnExitAnimationListener(android.window.SplashScreen.OnExitAnimationListener))`(`listener:` ` [SplashScreen.OnExitAnimationListener](https://developer.android.com/reference/kotlin/android/window/SplashScreen.OnExitAnimationListener)`)` Specifies whether an [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) wants to handle the splash screen animation on its own. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSplashScreenTheme](https://developer.android.com/reference/kotlin/android/window/SplashScreen#setSplashScreenTheme(kotlin.Int))`(`themeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Overrides the theme used for the [SplashScreen](https://developer.android.com/reference/kotlin/android/window/SplashScreen#) s of this application. |

## Constants

### SPLASH_SCREEN_STYLE_ICON

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPLASH_SCREEN_STYLE_ICON: Int
```

Flag to be used with [ActivityOptions.setSplashScreenStyle](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#setSplashScreenStyle(kotlin.Int)), to show the splash screen icon of the launched activity. 

 Value: 1

### SPLASH_SCREEN_STYLE_SOLID_COLOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPLASH_SCREEN_STYLE_SOLID_COLOR: Int
```

Flag to be used with [ActivityOptions.setSplashScreenStyle](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#setSplashScreenStyle(kotlin.Int)), to avoid showing the splash screen icon of the launched activity 

 Value: 0

## Public methods

### clearOnExitAnimationListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearOnExitAnimationListener(): Unit
```

Clear exist listener 
**See Also**

- [#setOnExitAnimationListener](https://developer.android.com/reference/kotlin/android/window/SplashScreen#setOnExitAnimationListener(android.window.SplashScreen.OnExitAnimationListener)) 

### setOnExitAnimationListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOnExitAnimationListener(listener: SplashScreen.OnExitAnimationListener): Unit
```

Specifies whether an [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) wants to handle the splash screen animation on its own. Normally the splash screen will show on screen before the content of the activity has been drawn, and disappear when the activity is showing on the screen. With this listener set, the activity will receive [OnExitAnimationListener.onSplashScreenExit](https://developer.android.com/reference/kotlin/android/window/SplashScreen.OnExitAnimationListener#onSplashScreenExit(android.window.SplashScreenView))callback if splash screen is showed, then the activity can create its own exit animation based on the SplashScreenView.

Note that this method must be called before splash screen leave, so it only takes effect during or before [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity.html#onResume()).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SplashScreen.OnExitAnimationListener](https://developer.android.com/reference/kotlin/android/window/SplashScreen.OnExitAnimationListener):the listener for receive the splash screen with This value cannot be`null`. |

**See Also**

- [android.window.SplashScreen.OnExitAnimationListener#onSplashScreenExit(SplashScreenView)](https://developer.android.com/reference/kotlin/android/window/SplashScreen.OnExitAnimationListener#onSplashScreenExit(android.window.SplashScreenView)) 

### setSplashScreenTheme

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSplashScreenTheme(themeId: Int): Unit
```

Overrides the theme used for the [SplashScreen](https://developer.android.com/reference/kotlin/android/window/SplashScreen#) s of this application.

By default, the [SplashScreen](https://developer.android.com/reference/kotlin/android/window/SplashScreen#) uses the theme set in the manifest. This method overrides and persists the theme used for the [SplashScreen](https://developer.android.com/reference/kotlin/android/window/SplashScreen#) of this application.

To reset to the default theme, set this the themeId to [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int).

**Note:**Internally, the theme name is resolved and persisted. This means that the theme name must be stable across versions, otherwise it won't be found after your application is updated.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `themeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the splashscreen theme to be used in place of the one defined in the manifest. |
