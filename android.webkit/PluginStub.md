# PluginStub

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PluginStub

Kotlin| [Java](PluginStub.md) 
| --- | --- |

```
interface PluginStub
```

| [android.webkit.PluginStub](PluginStub.md) |

This interface is used to implement plugins in a WebView. A plugin package may extend this class and implement the abstract functions to create embedded or fullscreeen views displayed in a WebView. The PluginStub implementation will be provided the same NPP instance that is created through the native interface.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [View](../android.view/View.md)! | [getEmbeddedView](PluginStub.md))`(`NPP:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [Context](../android.content/Context.md)!`)` Return a custom embedded view to draw the plugin. |
| abstract [View](../android.view/View.md)! | [getFullScreenView](PluginStub.md))`(`NPP:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [Context](../android.content/Context.md)!`)` Return a custom full-screen view to be displayed when the user requests a plugin display as full-screen. |

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
| `context` | [Context](../android.content/Context.md)!:The current application's Context. |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------|
| [View](../android.view/View.md)! | A custom View that will be managed by WebView. |

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
| `context` | [Context](../android.content/Context.md)!:The current application's Context. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------|
| [View](../android.view/View.md)! | A custom View that will be managed by the application. |
