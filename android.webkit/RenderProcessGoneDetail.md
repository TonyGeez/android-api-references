# RenderProcessGoneDetail

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderProcessGoneDetail

Kotlin| [Java](RenderProcessGoneDetail.md) 
| --- | --- |

```
abstract class RenderProcessGoneDetail
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.RenderProcessGoneDetail](RenderProcessGoneDetail.md) |

This class provides more specific information about why the render process exited. The application may use this to decide how to handle the situation.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RenderProcessGoneDetail](RenderProcessGoneDetail.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [didCrash](RenderProcessGoneDetail.md))`()` Indicates whether the render process was observed to crash, or whether it was killed by the system. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [rendererPriorityAtExit](RenderProcessGoneDetail.md))`()` Returns the renderer priority that was set at the time that the renderer exited. |

## Public constructors

### RenderProcessGoneDetail

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RenderProcessGoneDetail()
```

**Deprecated:** *This class should not be constructed by applications.*

## Public methods

### didCrash

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun didCrash(): Boolean
```

Indicates whether the render process was observed to crash, or whether it was killed by the system. If the render process was killed, this is most likely caused by the system being low on memory.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if render process crashed, otherwise it was killed by system. |

### rendererPriorityAtExit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun rendererPriorityAtExit(): Int
```

Returns the renderer priority that was set at the time that the renderer exited. This may be greater than the priority that any individual [WebView](WebView.md) requested using [WebView.setRendererPriorityPolicy](WebView.md)).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the priority of the renderer at exit. Value is [android.webkit.WebView#RENDERER_PRIORITY_WAIVED](WebView.md), [android.webkit.WebView#RENDERER_PRIORITY_BOUND](WebView.md), or [android.webkit.WebView#RENDERER_PRIORITY_IMPORTANT](WebView.md) |
