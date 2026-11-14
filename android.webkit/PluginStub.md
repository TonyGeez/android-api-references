# PluginStub

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PluginStub

Kotlin| [Java](https://developer.android.com/reference/android/webkit/PluginStub "View this page in Java") 

```
interface PluginStub
```

| [android.webkit.PluginStub](https://developer.android.com/reference/kotlin/android/webkit/PluginStub#) |

This interface is used to implement plugins in a WebView. A plugin package may extend this class and implement the abstract functions to create embedded or fullscreeen views displayed in a WebView. The PluginStub implementation will be provided the same NPP instance that is created through the native interface.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getEmbeddedView](https://developer.android.com/reference/kotlin/android/webkit/PluginStub#getEmbeddedView(kotlin.Int,%20android.content.Context))`(`NPP:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Return a custom embedded view to draw the plugin. |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getFullScreenView](https://developer.android.com/reference/kotlin/android/webkit/PluginStub#getFullScreenView(kotlin.Int,%20android.content.Context))`(`NPP:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Return a custom full-screen view to be displayed when the user requests a plugin display as full-screen. |

## Public methods

### getEmbeddedView

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEmbeddedView(
    NPP: Int, 
    context: Context!
): View!
```

Return a custom embedded view to draw the plugin.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `NPP` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The native NPP instance. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The current application's Context. |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | A custom View that will be managed by WebView. |

### getFullScreenView

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFullScreenView(
    NPP: Int, 
    context: Context!
): View!
```

Return a custom full-screen view to be displayed when the user requests a plugin display as full-screen. Note that the application may choose not to display this View as completely full-screen.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `NPP` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The native NPP instance. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The current application's Context. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | A custom View that will be managed by the application. |
