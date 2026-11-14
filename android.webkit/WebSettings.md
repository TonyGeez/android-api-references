# WebSettings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebSettings

Kotlin| [Java](WebSettings.md) 
| --- | --- |

```
abstract class WebSettings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebSettings](WebSettings.md) |

Manages settings state for a WebView. When a WebView is first created, it obtains a set of default settings. These default settings will be returned from any getter call. A`WebSettings`object obtained from [WebView.getSettings()](WebView.md))is tied to the life of the WebView. If a WebView has been destroyed, any method call on`WebSettings`will throw an [IllegalStateException](../java.lang/IllegalStateException.md).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [LayoutAlgorithm](../android/webkit/WebSettings.LayoutAlgorithm.md) Enum for controlling the layout of html. |
| | [PluginState](../android/webkit/WebSettings.PluginState.md) The plugin state effects how plugins are treated on a page. |
| | [RenderPriority](../android/webkit/WebSettings.RenderPriority.md) <br /> |
| --- | --- |
| | [TextSize](../android/webkit/WebSettings.TextSize.md) Enum for specifying the text size. |
| | [ZoomDensity](../android/webkit/WebSettings.ZoomDensity.md) Enum for specifying the WebView's desired density. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORCE_DARK_AUTO](WebSettings.md) Enable force dark dependent on the state of the WebView parent view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORCE_DARK_OFF](WebSettings.md) Disable force dark, irrespective of the force dark mode of the WebView parent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORCE_DARK_ON](WebSettings.md) Unconditionally enable force dark. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOAD_CACHE_ELSE_NETWORK](WebSettings.md) Use cached resources when they are available, even if they have expired. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOAD_CACHE_ONLY](WebSettings.md) Don't use the network, load from the cache. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOAD_DEFAULT](WebSettings.md) Default cache usage mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOAD_NORMAL](WebSettings.md) Normal cache usage mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOAD_NO_CACHE](WebSettings.md) Don't use the cache, load from the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MENU_ITEM_NONE](WebSettings.md) No menu items should be disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MENU_ITEM_PROCESS_TEXT](WebSettings.md) Disable all the action mode menu items for text processing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MENU_ITEM_SHARE](WebSettings.md) Disable menu item "Share". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MENU_ITEM_WEB_SEARCH](WebSettings.md) Disable menu item "Web Search". |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIXED_CONTENT_ALWAYS_ALLOW](WebSettings.md) In this mode, the WebView will allow a secure origin to load content from any other origin, even if that origin is insecure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIXED_CONTENT_COMPATIBILITY_MODE](WebSettings.md) In this mode, the WebView will attempt to be compatible with the approach of a modern web browser with regard to mixed content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIXED_CONTENT_NEVER_ALLOW](WebSettings.md) In this mode, the WebView will not allow a secure origin to load content from an insecure origin. |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [WebSettings](WebSettings.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [enableSmoothTransition](WebSettings.md))`()` Gets whether the WebView enables smooth transition while panning or zooming. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowContentAccess](WebSettings.md))`()` Gets whether this WebView supports content URL access. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowFileAccess](WebSettings.md))`()` Gets whether this WebView supports file access. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowFileAccessFromFileURLs](WebSettings.md))`()` Gets whether JavaScript running in the context of a file scheme URL can access content from other file scheme URLs. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowUniversalAccessFromFileURLs](WebSettings.md))`()` Gets whether JavaScript running in the context of a file scheme URL can access content from any origin. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBlockNetworkImage](WebSettings.md))`()` Gets whether the WebView does not load image resources from the network. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBlockNetworkLoads](WebSettings.md))`()` Gets whether the WebView does not load any resources from the network. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBuiltInZoomControls](WebSettings.md))`()` Gets whether the zoom mechanisms built into WebView are being used. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCacheMode](WebSettings.md))`()` Gets the current setting for overriding the cache mode. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCursiveFontFamily](WebSettings.md))`()` Gets the cursive font family name. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDatabaseEnabled](WebSettings.md))`()` Gets whether the database storage API is enabled. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDatabasePath](WebSettings.md))`()` Gets the path to where database storage API databases are saved. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultFixedFontSize](WebSettings.md))`()` Gets the default fixed font size. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultFontSize](WebSettings.md))`()` Gets the default font size. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultTextEncodingName](WebSettings.md))`()` Gets the default text encoding name. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultUserAgent](WebSettings.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns the default User-Agent used by a WebView. |
| abstract [WebSettings.ZoomDensity](../android/webkit/WebSettings.ZoomDensity.md)! | [getDefaultZoom](WebSettings.md))`()` Gets the default zoom density of the page. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisabledActionModeMenuItems](WebSettings.md))`()` Gets the action mode menu items that are disabled, expressed in an integer field flag. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDisplayZoomControls](WebSettings.md))`()` Gets whether the WebView displays on-screen zoom controls when using the built-in zoom mechanisms. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDomStorageEnabled](WebSettings.md))`()` Gets whether the DOM Storage APIs are enabled. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFantasyFontFamily](WebSettings.md))`()` Gets the fantasy font family name. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFixedFontFamily](WebSettings.md))`()` Gets the fixed font family name. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getForceDark](WebSettings.md))`()` Get the force dark mode for this WebView. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getJavaScriptCanOpenWindowsAutomatically](WebSettings.md))`()` Gets whether JavaScript can open windows without a user gesture. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getJavaScriptEnabled](WebSettings.md))`()` Gets whether JavaScript is enabled. |
| abstract [WebSettings.LayoutAlgorithm](../android/webkit/WebSettings.LayoutAlgorithm.md)! | [getLayoutAlgorithm](WebSettings.md))`()` Gets the current layout algorithm. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLightTouchEnabled](WebSettings.md))`()` Gets whether light touches are enabled. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLoadWithOverviewMode](WebSettings.md))`()` Gets whether this WebView loads pages in overview mode. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLoadsImagesAutomatically](WebSettings.md))`()` Gets whether the WebView loads image resources. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getMediaPlaybackRequiresUserGesture](WebSettings.md))`()` Gets whether the WebView requires a user gesture to play media. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumFontSize](WebSettings.md))`()` Gets the minimum font size. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumLogicalFontSize](WebSettings.md))`()` Gets the minimum logical font size. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMixedContentMode](WebSettings.md))`()` Gets the current behavior of the WebView with regard to loading insecure content from a secure origin. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getOffscreenPreRaster](WebSettings.md))`()` Gets whether this WebView should raster tiles when it is offscreen but attached to a window. |
| abstract [WebSettings.PluginState](../android/webkit/WebSettings.PluginState.md)! | [getPluginState](WebSettings.md))`()` Gets the current state regarding whether plugins are enabled. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSafeBrowsingEnabled](WebSettings.md))`()` Gets whether Safe Browsing is enabled. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSansSerifFontFamily](WebSettings.md))`()` Gets the sans-serif font family name. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSaveFormData](WebSettings.md))`()` Gets whether the WebView saves form data. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSavePassword](WebSettings.md))`()` Gets whether the WebView saves passwords. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSerifFontFamily](WebSettings.md))`()` Gets the serif font family name. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getStandardFontFamily](WebSettings.md))`()` Gets the standard font family name. |
| open [WebSettings.TextSize](../android/webkit/WebSettings.TextSize.md)! | [getTextSize](WebSettings.md))`()` Gets the text size of the page. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextZoom](WebSettings.md))`()` Gets the text zoom of the page in percent. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseWideViewPort](WebSettings.md))`()` Gets whether the WebView supports the "viewport" HTML meta tag or will use a wide viewport. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUserAgentString](WebSettings.md))`()` Gets the WebView's user-agent string. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAlgorithmicDarkeningAllowed](WebSettings.md))`()` Get if algorithmic darkening is allowed or not for this WebView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlgorithmicDarkeningAllowed](WebSettings.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether algorithmic darkening is allowed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowContentAccess](WebSettings.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables content URL access within WebView. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowFileAccess](WebSettings.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables file access within WebView. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowFileAccessFromFileURLs](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether cross-origin requests in the context of a file scheme URL should be allowed to access content from other file scheme URLs. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowUniversalAccessFromFileURLs](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether cross-origin requests in the context of a file scheme URL should be allowed to access content from*any*origin. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlockNetworkImage](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should not load image resources from the network (resources accessed via http and https URI schemes). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlockNetworkLoads](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should not load resources from the network. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBuiltInZoomControls](WebSettings.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should use its built-in zoom mechanisms. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCacheMode](WebSettings.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Overrides the way the cache is used. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCursiveFontFamily](WebSettings.md))`(`font:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the cursive font family name. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDatabaseEnabled](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the database storage API is enabled. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDatabasePath](WebSettings.md))`(`databasePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the path to where database storage API databases should be saved. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultFixedFontSize](WebSettings.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the default fixed font size. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultFontSize](WebSettings.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the default font size. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultTextEncodingName](WebSettings.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the default text encoding name to use when decoding html pages. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultZoom](WebSettings.md))`(`zoom:` ` [WebSettings.ZoomDensity](../android/webkit/WebSettings.ZoomDensity.md)!`)` Sets the default zoom density of the page. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDisabledActionModeMenuItems](WebSettings.md))`(`menuItems:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Disables the action mode menu items according to`menuItems`flag. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDisplayZoomControls](WebSettings.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should display on-screen zoom controls when using the built-in zoom mechanisms. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDomStorageEnabled](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the DOM storage API is enabled. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableSmoothTransition](WebSettings.md))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView will enable smooth transition while panning or zooming or while the window hosting the WebView does not have focus. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFantasyFontFamily](WebSettings.md))`(`font:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the fantasy font family name. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFixedFontFamily](WebSettings.md))`(`font:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the fixed font family name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setForceDark](WebSettings.md))`(`forceDark:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the force dark mode for this WebView. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGeolocationDatabasePath](WebSettings.md))`(`databasePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the path where the Geolocation databases should be saved. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGeolocationEnabled](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Geolocation is enabled. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setJavaScriptCanOpenWindowsAutomatically](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Allows JavaScript to open windows without a user gesture. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setJavaScriptEnabled](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Tells the WebView to enable JavaScript execution. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutAlgorithm](WebSettings.md))`(`l:` ` [WebSettings.LayoutAlgorithm](../android/webkit/WebSettings.LayoutAlgorithm.md)!`)` Sets the underlying layout algorithm. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLightTouchEnabled](WebSettings.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables using light touches to make a selection and activate mouseovers. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoadWithOverviewMode](WebSettings.md))`(`overview:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView loads pages in overview mode, that is, zooms out the content to fit on screen by width. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoadsImagesAutomatically](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should load image resources. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMediaPlaybackRequiresUserGesture](WebSettings.md))`(`require:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView requires a user gesture to play media. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumFontSize](WebSettings.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum font size. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumLogicalFontSize](WebSettings.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum logical font size. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMixedContentMode](WebSettings.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Configures the WebView's behavior when a secure origin attempts to load a resource from an insecure origin. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNeedInitialFocus](WebSettings.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Tells the WebView whether it needs to set a node to have focus when android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOffscreenPreRaster](WebSettings.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this WebView should raster tiles when it is offscreen but attached to a window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPluginState](WebSettings.md))`(`state:` ` [WebSettings.PluginState](../android/webkit/WebSettings.PluginState.md)!`)` Tells the WebView to enable, disable, or have plugins on demand. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRenderPriority](WebSettings.md))`(`priority:` ` [WebSettings.RenderPriority](../android/webkit/WebSettings.RenderPriority.md)!`)` Sets the CPU scheduling priority of the Render thread. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSafeBrowsingEnabled](WebSettings.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether Safe Browsing is enabled. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSansSerifFontFamily](WebSettings.md))`(`font:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the sans-serif font family name. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSaveFormData](WebSettings.md))`(`save:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should save form data. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSavePassword](WebSettings.md))`(`save:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should save passwords. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSerifFontFamily](WebSettings.md))`(`font:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the serif font family name. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStandardFontFamily](WebSettings.md))`(`font:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the standard font family name. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSupportMultipleWindows](WebSettings.md))`(`support:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should support multiple windows. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSupportZoom](WebSettings.md))`(`support:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should support zooming using its on-screen zoom controls and gestures. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextSize](WebSettings.md))`(`t:` ` [WebSettings.TextSize](../android/webkit/WebSettings.TextSize.md)!`)` Sets the text size of the page. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextZoom](WebSettings.md))`(`textZoom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the text zoom of the page in percent. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseWideViewPort](WebSettings.md))`(`use:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the WebView should enable support for the "viewport" HTML meta tag or should use a wide viewport. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUserAgentString](WebSettings.md))`(`ua:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the WebView's user-agent string. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportMultipleWindows](WebSettings.md))`()` Gets whether the WebView supports multiple windows. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportZoom](WebSettings.md))`()` Gets whether the WebView supports zoom. |
| --- | --- |

## Constants

### FORCE_DARK_AUTO

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORCE_DARK_AUTO: Int
```

**Deprecated:** *refer to [setForceDark](WebSettings.md))*

Enable force dark dependent on the state of the WebView parent view. If the WebView parent view is being automatically force darkened (see: [android.view.View#setForceDarkAllowed](../android.view/View.md))), then WebView content will be rendered so as to emulate a dark theme. WebViews that are not attached to the view hierarchy will not be inverted. 

 Value: 1

**See Also**

- [#setForceDark](WebSettings.md)) 

### FORCE_DARK_OFF

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORCE_DARK_OFF: Int
```

**Deprecated:** *refer to [setForceDark](WebSettings.md))*

Disable force dark, irrespective of the force dark mode of the WebView parent. In this mode, WebView content will always be rendered as-is, regardless of whether native views are being automatically darkened. 

 Value: 0

**See Also**

- [#setForceDark](WebSettings.md)) 

### FORCE_DARK_ON

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORCE_DARK_ON: Int
```

**Deprecated:** *refer to [setForceDark](WebSettings.md))*

Unconditionally enable force dark. In this mode WebView content will always be rendered so as to emulate a dark theme. 

 Value: 2

**See Also**

- [#setForceDark](WebSettings.md)) 

### LOAD_CACHE_ELSE_NETWORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOAD_CACHE_ELSE_NETWORK: Int
```

Use cached resources when they are available, even if they have expired. Otherwise load resources from the network. Use with [setCacheMode](WebSettings.md)). 

 Value: 1

### LOAD_CACHE_ONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOAD_CACHE_ONLY: Int
```

Don't use the network, load from the cache. Use with [setCacheMode](WebSettings.md)). 

 Value: 3

### LOAD_DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOAD_DEFAULT: Int
```

Default cache usage mode. If the navigation type doesn't impose any specific behavior, use cached resources when they are available and not expired, otherwise load resources from the network. Use with [setCacheMode](WebSettings.md)). 

 Value: -1

### LOAD_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOAD_NORMAL: Int
```

**Deprecated:** *This value is obsolete, as from API level [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md) and onwards it has the same effect as [LOAD_DEFAULT](WebSettings.md).*

Normal cache usage mode. Use with [setCacheMode](WebSettings.md)). 

 Value: 0

### LOAD_NO_CACHE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOAD_NO_CACHE: Int
```

Don't use the cache, load from the network. Use with [setCacheMode](WebSettings.md)). 

 Value: 2

### MENU_ITEM_NONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MENU_ITEM_NONE: Int
```

No menu items should be disabled. 

 Value: 0

**See Also**

- [#setDisabledActionModeMenuItems](WebSettings.md)) 

### MENU_ITEM_PROCESS_TEXT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MENU_ITEM_PROCESS_TEXT: Int
```

Disable all the action mode menu items for text processing. By default WebView searches for activities that are able to handle [android.content.Intent#ACTION_PROCESS_TEXT](../android.content/Intent.md) and show them in the action mode menu. If this flag is set via [setDisabledActionModeMenuItems](WebSettings.md)), these menu items will be disabled. 

 Value: 4

**See Also**

- [#setDisabledActionModeMenuItems](WebSettings.md)) 

### MENU_ITEM_SHARE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MENU_ITEM_SHARE: Int
```

Disable menu item "Share". 

 Value: 1

**See Also**

- [#setDisabledActionModeMenuItems](WebSettings.md)) 

### MENU_ITEM_WEB_SEARCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MENU_ITEM_WEB_SEARCH: Int
```

Disable menu item "Web Search". 

 Value: 2

**See Also**

- [#setDisabledActionModeMenuItems](WebSettings.md)) 

### MIXED_CONTENT_ALWAYS_ALLOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIXED_CONTENT_ALWAYS_ALLOW: Int
```

In this mode, the WebView will allow a secure origin to load content from any other origin, even if that origin is insecure. This is the least secure mode of operation for the WebView, and where possible apps should not set this mode. 

 Value: 0

**See Also**

- [#setMixedContentMode](WebSettings.md)) 

### MIXED_CONTENT_COMPATIBILITY_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIXED_CONTENT_COMPATIBILITY_MODE: Int
```

In this mode, the WebView will attempt to be compatible with the approach of a modern web browser with regard to mixed content. Some insecure content may be allowed to be loaded by a secure origin and other types of content will be blocked. The types of content are allowed or blocked may change release to release and are not explicitly defined. This mode is intended to be used by apps that are not in control of the content that they render but desire to operate in a reasonably secure environment. For highest security, apps are recommended to use [MIXED_CONTENT_NEVER_ALLOW](WebSettings.md). 

 Value: 2

**See Also**

- [#setMixedContentMode](WebSettings.md)) 

### MIXED_CONTENT_NEVER_ALLOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIXED_CONTENT_NEVER_ALLOW: Int
```

In this mode, the WebView will not allow a secure origin to load content from an insecure origin. This is the preferred and most secure mode of operation for the WebView and apps are strongly advised to use this mode. 

 Value: 1

**See Also**

- [#setMixedContentMode](WebSettings.md))

## Public constructors

### WebSettings

```
WebSettings()
```

## Public methods

### enableSmoothTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun enableSmoothTransition(): Boolean
```

**Deprecated:** *This method is now obsolete, and will become a no-op in future.*

Gets whether the WebView enables smooth transition while panning or zooming. 
**See Also**

- [#setEnableSmoothTransition](WebSettings.md)) 

### getAllowContentAccess

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllowContentAccess(): Boolean
```

Gets whether this WebView supports content URL access. 
**See Also**

- [#setAllowContentAccess](WebSettings.md)) 

### getAllowFileAccess

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllowFileAccess(): Boolean
```

Gets whether this WebView supports file access. 
**See Also**

- [#setAllowFileAccess](WebSettings.md)) 

### getAllowFileAccessFromFileURLs

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllowFileAccessFromFileURLs(): Boolean
```

Gets whether JavaScript running in the context of a file scheme URL can access content from other file scheme URLs.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether JavaScript running in the context of a file scheme URL can access content from other file scheme URLs |

**See Also**

- [#setAllowFileAccessFromFileURLs](WebSettings.md)) 

### getAllowUniversalAccessFromFileURLs

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllowUniversalAccessFromFileURLs(): Boolean
```

Gets whether JavaScript running in the context of a file scheme URL can access content from any origin. This includes access to content from other file scheme URLs.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether JavaScript running in the context of a file scheme URL can access content from any origin |

**See Also**

- [#setAllowUniversalAccessFromFileURLs](WebSettings.md)) 

### getBlockNetworkImage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBlockNetworkImage(): Boolean
```

Gets whether the WebView does not load image resources from the network.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the WebView does not load image resources from the network |

**See Also**

- [#setBlockNetworkImage](WebSettings.md)) 

### getBlockNetworkLoads

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBlockNetworkLoads(): Boolean
```

Gets whether the WebView does not load any resources from the network.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the WebView does not load any resources from the network |

**See Also**

- [#setBlockNetworkLoads](WebSettings.md)) 

### getBuiltInZoomControls

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBuiltInZoomControls(): Boolean
```

Gets whether the zoom mechanisms built into WebView are being used.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the zoom mechanisms built into WebView are being used |

**See Also**

- [#setBuiltInZoomControls](WebSettings.md)) 

### getCacheMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCacheMode(): Int
```

Gets the current setting for overriding the cache mode.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current setting for overriding the cache mode Value is [android.webkit.WebSettings#LOAD_DEFAULT](WebSettings.md), [android.webkit.WebSettings#LOAD_NORMAL](WebSettings.md), [android.webkit.WebSettings#LOAD_CACHE_ELSE_NETWORK](WebSettings.md), [android.webkit.WebSettings#LOAD_NO_CACHE](WebSettings.md), or [android.webkit.WebSettings#LOAD_CACHE_ONLY](WebSettings.md) |

**See Also**

- [#setCacheMode](WebSettings.md)) 

### getCursiveFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCursiveFontFamily(): String!
```

Gets the cursive font family name.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the cursive font family name as a string |

**See Also**

- [#setCursiveFontFamily](WebSettings.md)) 

### getDatabaseEnabled

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDatabaseEnabled(): Boolean
```

**Deprecated:** *WebSQL is deprecated and this method will become a no-op on all Android versions once support is removed in Chromium. See https://developer.chrome.com/blog/deprecating-web-sql for more information.*

Gets whether the database storage API is enabled.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the database storage API is enabled |

**See Also**

- [#setDatabaseEnabled](WebSettings.md)) 

### getDatabasePath

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDatabasePath(): String!
```

**Deprecated:** *Database paths are managed by the implementation this method is obsolete.*

Gets the path to where database storage API databases are saved.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the String path to the database storage API databases |

**See Also**

- [#setDatabasePath](WebSettings.md)) 

### getDefaultFixedFontSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDefaultFixedFontSize(): Int
```

Gets the default fixed font size.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a non-negative integer between 1 and 72 |

**See Also**

- [#setDefaultFixedFontSize](WebSettings.md)) 

### getDefaultFontSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDefaultFontSize(): Int
```

Gets the default font size.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a non-negative integer between 1 and 72 |

**See Also**

- [#setDefaultFontSize](WebSettings.md)) 

### getDefaultTextEncodingName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDefaultTextEncodingName(): String!
```

Gets the default text encoding name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the default text encoding name as a string |

**See Also**

- [#setDefaultTextEncodingName](WebSettings.md)) 

### getDefaultUserAgent

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefaultUserAgent(context: Context!): String!
```

Returns the default User-Agent used by a WebView. An instance of WebView could use a different User-Agent if a call is made to [WebSettings.setUserAgentString(String)](WebSettings.md)).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:a Context object used to access application assets |

### getDefaultZoom

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDefaultZoom(): WebSettings.ZoomDensity!
```

**Deprecated:** *Will only return the default value.*

Gets the default zoom density of the page. This should be called from the UI thread. This setting is not recommended for use in new applications.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|------------------|
| [WebSettings.ZoomDensity](../android/webkit/WebSettings.ZoomDensity.md)! | the zoom density |

**See Also**

- [#setDefaultZoom](WebSettings.md)) 

### getDisabledActionModeMenuItems

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDisabledActionModeMenuItems(): Int
```

Gets the action mode menu items that are disabled, expressed in an integer field flag. The default value is [MENU_ITEM_NONE](WebSettings.md)

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | all the disabled menu item flags combined with bitwise OR. Value is either`0`or a combination of [android.webkit.WebSettings#MENU_ITEM_NONE](WebSettings.md), [android.webkit.WebSettings#MENU_ITEM_SHARE](WebSettings.md), [android.webkit.WebSettings#MENU_ITEM_WEB_SEARCH](WebSettings.md), and [android.webkit.WebSettings#MENU_ITEM_PROCESS_TEXT](WebSettings.md) |

### getDisplayZoomControls

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDisplayZoomControls(): Boolean
```

Gets whether the WebView displays on-screen zoom controls when using the built-in zoom mechanisms.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the WebView displays on-screen zoom controls when using the built-in zoom mechanisms |

**See Also**

- [#setDisplayZoomControls](WebSettings.md)) 

### getDomStorageEnabled

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDomStorageEnabled(): Boolean
```

Gets whether the DOM Storage APIs are enabled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the DOM Storage APIs are enabled |

**See Also**

- [#setDomStorageEnabled](WebSettings.md)) 

### getFantasyFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFantasyFontFamily(): String!
```

Gets the fantasy font family name.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the fantasy font family name as a string |

**See Also**

- [#setFantasyFontFamily](WebSettings.md)) 

### getFixedFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFixedFontFamily(): String!
```

Gets the fixed font family name.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the fixed font family name as a string |

**See Also**

- [#setFixedFontFamily](WebSettings.md)) 

### getForceDark

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getForceDark(): Int
```

**Deprecated:** *refer to [setForceDark](WebSettings.md)).*

Get the force dark mode for this WebView. The default force dark mode is [FORCE_DARK_AUTO](WebSettings.md).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the currently set force dark mode. Value is [android.webkit.WebSettings#FORCE_DARK_OFF](WebSettings.md), [android.webkit.WebSettings#FORCE_DARK_AUTO](WebSettings.md), or [android.webkit.WebSettings#FORCE_DARK_ON](WebSettings.md) |

**See Also**

- [#setForceDark](WebSettings.md)) 

### getJavaScriptCanOpenWindowsAutomatically

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getJavaScriptCanOpenWindowsAutomatically(): Boolean
```

Gets whether JavaScript can open windows without a user gesture.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if JavaScript can open windows without a user gesture using`window.open()` |

**See Also**

- [#setJavaScriptCanOpenWindowsAutomatically](WebSettings.md)) 

### getJavaScriptEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getJavaScriptEnabled(): Boolean
```

Gets whether JavaScript is enabled.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if JavaScript is enabled |

**See Also**

- [#setJavaScriptEnabled](WebSettings.md)) 

### getLayoutAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLayoutAlgorithm(): WebSettings.LayoutAlgorithm!
```

Gets the current layout algorithm.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [WebSettings.LayoutAlgorithm](../android/webkit/WebSettings.LayoutAlgorithm.md)! | the layout algorithm in use, as a [LayoutAlgorithm](../android/webkit/WebSettings.LayoutAlgorithm.md) value |

**See Also**

- [#setLayoutAlgorithm](WebSettings.md)) 

### getLightTouchEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLightTouchEnabled(): Boolean
```

**Deprecated:** *This setting is obsolete.*

Gets whether light touches are enabled. 
**See Also**

- [#setLightTouchEnabled](WebSettings.md)) 

### getLoadWithOverviewMode

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLoadWithOverviewMode(): Boolean
```

Gets whether this WebView loads pages in overview mode.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether this WebView loads pages in overview mode |

**See Also**

- [#setLoadWithOverviewMode](WebSettings.md)) 

### getLoadsImagesAutomatically

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLoadsImagesAutomatically(): Boolean
```

Gets whether the WebView loads image resources. This includes images embedded using the data URI scheme.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the WebView loads image resources |

**See Also**

- [#setLoadsImagesAutomatically](WebSettings.md)) 

### getMediaPlaybackRequiresUserGesture

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMediaPlaybackRequiresUserGesture(): Boolean
```

Gets whether the WebView requires a user gesture to play media.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the WebView requires a user gesture to play media |

**See Also**

- [#setMediaPlaybackRequiresUserGesture](WebSettings.md)) 

### getMinimumFontSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMinimumFontSize(): Int
```

Gets the minimum font size.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a non-negative integer between 1 and 72 |

**See Also**

- [#setMinimumFontSize](WebSettings.md)) 

### getMinimumLogicalFontSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMinimumLogicalFontSize(): Int
```

Gets the minimum logical font size.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a non-negative integer between 1 and 72 |

**See Also**

- [#setMinimumLogicalFontSize](WebSettings.md)) 

### getMixedContentMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMixedContentMode(): Int
```

Gets the current behavior of the WebView with regard to loading insecure content from a secure origin.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current setting, one of [MIXED_CONTENT_NEVER_ALLOW](WebSettings.md), [MIXED_CONTENT_ALWAYS_ALLOW](WebSettings.md) or [MIXED_CONTENT_COMPATIBILITY_MODE](WebSettings.md). |

### getOffscreenPreRaster

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOffscreenPreRaster(): Boolean
```

Gets whether this WebView should raster tiles when it is offscreen but attached to a window.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this WebView will raster tiles when it is offscreen but attached to a window. |

### getPluginState

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPluginState(): WebSettings.PluginState!
```

**Deprecated:** *Plugins are not supported in API level [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md) or later; enabling plugins is a no-op.*

Gets the current state regarding whether plugins are enabled.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [WebSettings.PluginState](../android/webkit/WebSettings.PluginState.md)! | the plugin state as a [PluginState](../android/webkit/WebSettings.PluginState.md) value |

**See Also**

- [#setPluginState](WebSettings.md)) 

### getSafeBrowsingEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSafeBrowsingEnabled(): Boolean
```

Gets whether Safe Browsing is enabled. See [setSafeBrowsingEnabled](WebSettings.md)).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if Safe Browsing is enabled and`false`otherwise. |

### getSansSerifFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSansSerifFontFamily(): String!
```

Gets the sans-serif font family name.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the sans-serif font family name as a string |

**See Also**

- [#setSansSerifFontFamily](WebSettings.md)) 

### getSaveFormData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSaveFormData(): Boolean
```

**Deprecated:** *In Android O and afterwards, this function does not have any effect. Form data will be filled from the platform's autofill service if applicable.*

Gets whether the WebView saves form data. In [android.os.Build.VERSION_CODES#O](../android/os/Build.VERSION_CODES.md), the platform has implemented a fully functional Autofill feature to store form data. Therefore, the Webview form data save feature is disabled.

Note that the feature will continue to be supported on older versions of Android as before.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the WebView saves form data |

**See Also**

- [#setSaveFormData](WebSettings.md)) 

### getSavePassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSavePassword(): Boolean
```

**Deprecated:** *Saving passwords in WebView will not be supported in future versions.*

Gets whether the WebView saves passwords.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the WebView saves passwords |

**See Also**

- [#setSavePassword](WebSettings.md)) 

### getSerifFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSerifFontFamily(): String!
```

Gets the serif font family name. The default is "serif".

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the serif font family name as a string |

**See Also**

- [#setSerifFontFamily](WebSettings.md)) 

### getStandardFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getStandardFontFamily(): String!
```

Gets the standard font family name.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the standard font family name as a string |

**See Also**

- [#setStandardFontFamily](WebSettings.md)) 

### getTextSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextSize(): WebSettings.TextSize!
```

**Deprecated:** *Use [getTextZoom](WebSettings.md))instead.*

Gets the text size of the page. If the text size was previously specified in percent using [setTextZoom](WebSettings.md)), this will return the closest matching [TextSize](../android/webkit/WebSettings.TextSize.md).

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [WebSettings.TextSize](../android/webkit/WebSettings.TextSize.md)! | the text size as a [TextSize](../android/webkit/WebSettings.TextSize.md) value |

**See Also**

- [#setTextSize](WebSettings.md)) 

### getTextZoom

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTextZoom(): Int
```

Gets the text zoom of the page in percent.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the text zoom of the page in percent |

**See Also**

- [#setTextZoom](WebSettings.md)) 

### getUseWideViewPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUseWideViewPort(): Boolean
```

Gets whether the WebView supports the "viewport" HTML meta tag or will use a wide viewport.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the WebView supports the viewport meta tag |

**See Also**

- [#setUseWideViewPort](WebSettings.md)) 

### getUserAgentString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUserAgentString(): String!
```

Gets the WebView's user-agent string.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the WebView's user-agent string |

**See Also**

- [#setUserAgentString](WebSettings.md)) 

### isAlgorithmicDarkeningAllowed

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAlgorithmicDarkeningAllowed(): Boolean
```

Get if algorithmic darkening is allowed or not for this WebView. The default is false.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | if the algorithmic darkening is allowed or not. |

**See Also**

- [#setAlgorithmicDarkeningAllowed](WebSettings.md)) 

### setAlgorithmicDarkeningAllowed

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlgorithmicDarkeningAllowed(allow: Boolean): Unit
```

Control whether algorithmic darkening is allowed.

**Note:** This API and the behaviour described only apply to apps with`targetSdkVersion`≥ [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md).

WebView always sets the media query`prefers-color-scheme`according to the app's theme attribute [isLightTheme](../android/R.styleable.md), i.e.`prefers-color-scheme`is`light`if isLightTheme is true or not specified, otherwise it is`dark`. This means that the web content's light or dark style will be applied automatically to match the app's theme if the content supports it.

Algorithmic darkening is disallowed by default.

If the app's theme is dark and it allows algorithmic darkening, WebView will attempt to darken web content using an algorithm, if the content doesn't define its own dark styles and doesn't explicitly disable darkening.

If Android is applying Force Dark to WebView then WebView will ignore the value of this setting and behave as if it were set to true.

The deprecated [setForceDark](WebSettings.md))and related API are no-ops in apps with`targetSdkVersion`≥ [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md), but they still apply to apps with`targetSdkVersion`\< [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md).

The below table summarizes how APIs work with different apps.

| App | Web content which uses`prefers-color-scheme` | Web content which does not use`prefers-color-scheme` |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| App with`isLightTheme`True or not set | Renders with the light theme defined by the content author. | Renders with the default styling defined by the content author. |
| App with Android forceDark in effect | Renders with the dark theme defined by the content author. | Renders with the styling modified to dark colors by an algorithm if allowed by the content author. |
| App with`isLightTheme`False,`targetSdkVersion`\< [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md), and has`FORCE_DARK_AUTO` | Renders with the dark theme defined by the content author. | Renders with the default styling defined by the content author. |
| --- | --- | --- |
| App with`isLightTheme`False,`targetSdkVersion`≥ [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md), and`setAlgorithmicDarkening(false)` | Renders with the dark theme defined by the content author. | Renders with the default styling defined by the content author. |
| App with`isLightTheme`False,`targetSdkVersion`≥ [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md), and`setAlgorithmicDarkening(true)` | Renders with the dark theme defined by the content author. | Renders with the styling modified to dark colors by an algorithm if allowed by the content author. |

<br />

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `allow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):allow algorithmic darkening or not. |

### setAllowContentAccess

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowContentAccess(allow: Boolean): Unit
```

Enables or disables content URL access within WebView. Content URL access allows WebView to load content from a content provider installed in the system. The default is enabled. 

### setAllowFileAccess

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowFileAccess(allow: Boolean): Unit
```

Enables or disables file access within WebView. Note that this enables or disables file system access only. Assets and resources are still accessible using file:///android_asset and file:///android_res.

**Note:** Apps should not open`file://`URLs from any external source in WebView, don't enable this if your app accepts arbitrary URLs from external sources. It's recommended to always use [androidx.webkit.WebViewAssetLoader](../androidx/webkit/WebViewAssetLoader.md) to access files including assets and resources over`http(s)://`schemes, instead of`file://`URLs. To prevent possible security issues targeting [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) and earlier, you should explicitly set this value to`false`.

The default value is`true`for apps targeting [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) and below, and`false`when targeting [android.os.Build.VERSION_CODES#R](../android/os/Build.VERSION_CODES.md) and above. 

### setAllowFileAccessFromFileURLs

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowFileAccessFromFileURLs(flag: Boolean): Unit
```

**Deprecated:** *This setting is not secure, please use [androidx.webkit.WebViewAssetLoader](../androidx/webkit/WebViewAssetLoader.md) to load file content securely.*

Sets whether cross-origin requests in the context of a file scheme URL should be allowed to access content from other file scheme URLs. Note that some accesses such as image HTML elements don't follow same-origin rules and aren't affected by this setting.

**Don't** enable this setting if you open files that may be created or altered by external sources. Enabling this setting allows malicious scripts loaded in a`file://`context to access arbitrary local files including WebView cookies and app private data.

Loading content via`file://`URLs is generally discouraged. See the note in [setAllowFileAccess](WebSettings.md)).

Note that the value of this setting is ignored if the value of [getAllowUniversalAccessFromFileURLs](WebSettings.md))is`true`. The default value is`true`for apps targeting [android.os.Build.VERSION_CODES#ICE_CREAM_SANDWICH_MR1](../android/os/Build.VERSION_CODES.md) and below, and`false`when targeting [android.os.Build.VERSION_CODES#JELLY_BEAN](../android/os/Build.VERSION_CODES.md) and above. To prevent possible violation of same domain policy when targeting [android.os.Build.VERSION_CODES#ICE_CREAM_SANDWICH_MR1](../android/os/Build.VERSION_CODES.md) and earlier, you should explicitly set this value to`false`.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether JavaScript running in the context of a file scheme URL should be allowed to access content from other file scheme URLs |

### setAllowUniversalAccessFromFileURLs

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAllowUniversalAccessFromFileURLs(flag: Boolean): Unit
```

**Deprecated:** *This setting is not secure, please use [androidx.webkit.WebViewAssetLoader](../androidx/webkit/WebViewAssetLoader.md) to load file content securely.*

Sets whether cross-origin requests in the context of a file scheme URL should be allowed to access content from*any*origin. This includes access to content from other file scheme URLs or web contexts. Note that some access such as image HTML elements doesn't follow same-origin rules and isn't affected by this setting.

**Don't** enable this setting if you open files that may be created or altered by external sources. Enabling this setting allows malicious scripts loaded in a`file://`context to launch cross-site scripting attacks, either accessing arbitrary local files including WebView cookies, app private data or even credentials used on arbitrary web sites.

Loading content via`file://`URLs is generally discouraged. See the note in [setAllowFileAccess](WebSettings.md)).

The default value is`true`for apps targeting [android.os.Build.VERSION_CODES#ICE_CREAM_SANDWICH_MR1](../android/os/Build.VERSION_CODES.md) and below, and`false`when targeting [android.os.Build.VERSION_CODES#JELLY_BEAN](../android/os/Build.VERSION_CODES.md) and above. To prevent possible violation of same domain policy when targeting [android.os.Build.VERSION_CODES#ICE_CREAM_SANDWICH_MR1](../android/os/Build.VERSION_CODES.md) and earlier, you should explicitly set this value to`false`.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether JavaScript running in the context of a file scheme URL should be allowed to access content from any origin |

### setBlockNetworkImage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlockNetworkImage(flag: Boolean): Unit
```

Sets whether the WebView should not load image resources from the network (resources accessed via http and https URI schemes). Note that this method has no effect unless [getLoadsImagesAutomatically](WebSettings.md))returns`true`. Also note that disabling all network loads using [setBlockNetworkLoads](WebSettings.md))will also prevent network images from loading, even if this flag is set to false. When the value of this setting is changed from`true`to`false`, network images resources referenced by content currently displayed by the WebView are fetched automatically. The default is`false`.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the WebView should not load image resources from the network |

**See Also**

- [#setBlockNetworkLoads](WebSettings.md)) 

### setBlockNetworkLoads

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlockNetworkLoads(flag: Boolean): Unit
```

Sets whether the WebView should not load resources from the network. Use [setBlockNetworkImage](WebSettings.md))to only avoid loading image resources. Note that if the value of this setting is changed from`true`to`false`, network resources referenced by content currently displayed by the WebView are not fetched until [android.webkit.WebView#reload](WebView.md))is called. If the application does not have the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission, attempts to set a value of`false`will cause a [java.lang.SecurityException](../java.lang/SecurityException.md) to be thrown. The default value is`false`if the application has the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission, otherwise it is`true`.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`means block network loads by the WebView |

**See Also**

- [android.webkit.WebView#reload](WebView.md)) 

### setBuiltInZoomControls

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBuiltInZoomControls(enabled: Boolean): Unit
```

Sets whether the WebView should use its built-in zoom mechanisms. The built-in zoom mechanisms comprise on-screen zoom controls, which are displayed over the WebView's content, and the use of a pinch gesture to control zooming. Whether or not these on-screen controls are displayed can be set with [setDisplayZoomControls](WebSettings.md)). The default is`false`.

The built-in mechanisms are the only currently supported zoom mechanisms, so it is recommended that this setting is always enabled. However, on-screen zoom controls are deprecated in Android (see [android.widget.ZoomButtonsController](../android.widget/ZoomButtonsController.md)) so it's recommended to disable [setDisplayZoomControls](WebSettings.md)).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the WebView should use its built-in zoom mechanisms |

### setCacheMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCacheMode(mode: Int): Unit
```

Overrides the way the cache is used. The way the cache is used is based on the navigation type. For a normal page load, the cache is checked and content is re-validated as needed. When navigating back, content is not revalidated, instead the content is just retrieved from the cache. This method allows the client to override this behavior by specifying one of [LOAD_DEFAULT](WebSettings.md), [LOAD_CACHE_ELSE_NETWORK](WebSettings.md), [LOAD_NO_CACHE](WebSettings.md) or [LOAD_CACHE_ONLY](WebSettings.md). The default value is [LOAD_DEFAULT](WebSettings.md).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode to use Value is [android.webkit.WebSettings#LOAD_DEFAULT](WebSettings.md), [android.webkit.WebSettings#LOAD_NORMAL](WebSettings.md), [android.webkit.WebSettings#LOAD_CACHE_ELSE_NETWORK](WebSettings.md), [android.webkit.WebSettings#LOAD_NO_CACHE](WebSettings.md), or [android.webkit.WebSettings#LOAD_CACHE_ONLY](WebSettings.md) |

### setCursiveFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCursiveFontFamily(font: String!): Unit
```

Sets the cursive font family name. The default is "cursive".

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `font` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a font family name |

### setDatabaseEnabled

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDatabaseEnabled(flag: Boolean): Unit
```

**Deprecated:** *WebSQL is deprecated and this method will become a no-op on all Android versions once support is removed in Chromium. See https://developer.chrome.com/blog/deprecating-web-sql for more information.*

Sets whether the database storage API is enabled. The default value is false. See also [setDatabasePath](WebSettings.md))for how to correctly set up the database storage API. This setting is global in effect, across all WebView instances in a process. Note you should only modify this setting prior to making**any**WebView page load within a given process, as the WebView implementation may ignore changes to this setting after that point.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the WebView should use the database storage API |

### setDatabasePath

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDatabasePath(databasePath: String!): Unit
```

**Deprecated:** *Database paths are managed by the implementation and calling this method will have no effect.*

Sets the path to where database storage API databases should be saved. In order for the database storage API to function correctly, this method must be called with a path to which the application can write. This method should only be called once: repeated calls are ignored.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `databasePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a path to the directory where databases should be saved. |

### setDefaultFixedFontSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDefaultFixedFontSize(size: Int): Unit
```

Sets the default fixed font size. The default is 16.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a non-negative integer between 1 and 72. Any number outside the specified range will be pinned. |

### setDefaultFontSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDefaultFontSize(size: Int): Unit
```

Sets the default font size. The default is 16.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a non-negative integer between 1 and 72. Any number outside the specified range will be pinned. |

### setDefaultTextEncodingName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDefaultTextEncodingName(encoding: String!): Unit
```

Sets the default text encoding name to use when decoding html pages. The default is "UTF-8".

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------|
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the text encoding name |

### setDefaultZoom

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDefaultZoom(zoom: WebSettings.ZoomDensity!): Unit
```

**Deprecated:** *This method is no longer supported, see the function documentation for recommended alternatives.*

Sets the default zoom density of the page. This must be called from the UI thread. The default is [ZoomDensity.MEDIUM](../android/webkit/WebSettings.ZoomDensity.md). This setting is not recommended for use in new applications. If the WebView is utilized to display mobile-oriented pages, the desired effect can be achieved by adjusting 'width' and 'initial-scale' attributes of page's 'meta viewport' tag. For pages lacking the tag, [android.webkit.WebView#setInitialScale](WebView.md))and [setUseWideViewPort](WebSettings.md))can be used.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `zoom` | [WebSettings.ZoomDensity](../android/webkit/WebSettings.ZoomDensity.md)!:the zoom density |

### setDisabledActionModeMenuItems

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDisabledActionModeMenuItems(menuItems: Int): Unit
```

Disables the action mode menu items according to`menuItems`flag.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menuItems` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer field flag for the menu items to be disabled. Value is either`0`or a combination of [android.webkit.WebSettings#MENU_ITEM_NONE](WebSettings.md), [android.webkit.WebSettings#MENU_ITEM_SHARE](WebSettings.md), [android.webkit.WebSettings#MENU_ITEM_WEB_SEARCH](WebSettings.md), and [android.webkit.WebSettings#MENU_ITEM_PROCESS_TEXT](WebSettings.md) |

### setDisplayZoomControls

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDisplayZoomControls(enabled: Boolean): Unit
```

Sets whether the WebView should display on-screen zoom controls when using the built-in zoom mechanisms. See [setBuiltInZoomControls](WebSettings.md)). The default is`true`. However, on-screen zoom controls are deprecated in Android (see [android.widget.ZoomButtonsController](../android.widget/ZoomButtonsController.md)) so it's recommended to set this to`false`.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the WebView should display on-screen zoom controls |

### setDomStorageEnabled

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDomStorageEnabled(flag: Boolean): Unit
```

Sets whether the DOM storage API is enabled. The default value is`false`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the WebView should use the DOM storage API |

### setEnableSmoothTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEnableSmoothTransition(enable: Boolean): Unit
```

**Deprecated:** *This method is now obsolete, and will become a no-op in future.*

Sets whether the WebView will enable smooth transition while panning or zooming or while the window hosting the WebView does not have focus. If it is`true`, WebView will choose a solution to maximize the performance. e.g. the WebView's content may not be updated during the transition. If it is false, WebView will keep its fidelity. The default value is`false`. 

### setFantasyFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFantasyFontFamily(font: String!): Unit
```

Sets the fantasy font family name. The default is "fantasy".

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `font` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a font family name |

### setFixedFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFixedFontFamily(font: String!): Unit
```

Sets the fixed font family name. The default is "monospace".

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `font` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a font family name |

### setForceDark

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setForceDark(forceDark: Int): Unit
```

**Deprecated:** *The "force dark" model previously implemented by WebView was complex and didn't interoperate well with current Web standards for`prefers-color-scheme`and`color-scheme`. In apps with`targetSdkVersion`≥ [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md) this API is a no-op and WebView will always use the dark style defined by web content authors if the app's theme is dark. To customize the behavior, refer to [setAlgorithmicDarkeningAllowed](WebSettings.md)).*

Set the force dark mode for this WebView.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `forceDark` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the force dark mode to set. Value is [android.webkit.WebSettings#FORCE_DARK_OFF](WebSettings.md), [android.webkit.WebSettings#FORCE_DARK_AUTO](WebSettings.md), or [android.webkit.WebSettings#FORCE_DARK_ON](WebSettings.md) |

**See Also**

- [#getForceDark](WebSettings.md)) 

### setGeolocationDatabasePath

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setGeolocationDatabasePath(databasePath: String!): Unit
```

**Deprecated:** *Geolocation database are managed by the implementation and calling this method will have no effect.*

Sets the path where the Geolocation databases should be saved. In order for Geolocation permissions and cached positions to be persisted, this method must be called with a path to which the application can write.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `databasePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a path to the directory where databases should be saved. |

### setGeolocationEnabled

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setGeolocationEnabled(flag: Boolean): Unit
```

Sets whether Geolocation is enabled. The default is`true`.

Please note that in order for the Geolocation API to be usable by a page in the WebView, the following requirements must be met:

- an application must have permission to access the device location, see [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md), [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md);
- an application must provide an implementation of the [WebChromeClient.onGeolocationPermissionsShowPrompt](WebChromeClient.md))callback to receive notifications that a page is requesting access to location via the JavaScript Geolocation API.

<br />

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether Geolocation should be enabled |

### setJavaScriptCanOpenWindowsAutomatically

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setJavaScriptCanOpenWindowsAutomatically(flag: Boolean): Unit
```

Allows JavaScript to open windows without a user gesture. This applies to the JavaScript function`window.open()`. The default is`false`: attempts without a user gesture will fail and do nothing.

This is not affected by the [setSupportMultipleWindows](WebSettings.md))setting; the user gesture requirement is enforced even if multiple windows are disabled.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if JavaScript can open windows without a user gesture. |

### setJavaScriptEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setJavaScriptEnabled(flag: Boolean): Unit
```

Tells the WebView to enable JavaScript execution.**The default is`false`.**

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the WebView should execute JavaScript |

### setLayoutAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLayoutAlgorithm(l: WebSettings.LayoutAlgorithm!): Unit
```

Sets the underlying layout algorithm. This will cause a re-layout of the WebView. The default is [LayoutAlgorithm.NARROW_COLUMNS](../android/webkit/WebSettings.LayoutAlgorithm.md).

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [WebSettings.LayoutAlgorithm](../android/webkit/WebSettings.LayoutAlgorithm.md)!:the layout algorithm to use, as a [LayoutAlgorithm](../android/webkit/WebSettings.LayoutAlgorithm.md) value |

### setLightTouchEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLightTouchEnabled(enabled: Boolean): Unit
```

**Deprecated:** *From [android.os.Build.VERSION_CODES#JELLY_BEAN](../android/os/Build.VERSION_CODES.md) this setting is obsolete and has no effect.*

Enables using light touches to make a selection and activate mouseovers. 

### setLoadWithOverviewMode

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLoadWithOverviewMode(overview: Boolean): Unit
```

Sets whether the WebView loads pages in overview mode, that is, zooms out the content to fit on screen by width. This setting is taken into account when the content width is greater than the width of the WebView control, for example, when [getUseWideViewPort](WebSettings.md))is enabled. The default is`false`. 

### setLoadsImagesAutomatically

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLoadsImagesAutomatically(flag: Boolean): Unit
```

Sets whether the WebView should load image resources. Note that this method controls loading of all images, including those embedded using the data URI scheme. Use [setBlockNetworkImage](WebSettings.md))to control loading only of images specified using network URI schemes. Note that if the value of this setting is changed from`false`to`true`, all images resources referenced by content currently displayed by the WebView are loaded automatically. The default is`true`.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the WebView should load image resources |

### setMediaPlaybackRequiresUserGesture

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setMediaPlaybackRequiresUserGesture(require: Boolean): Unit
```

Sets whether the WebView requires a user gesture to play media. The default is`true`.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `require` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the WebView requires a user gesture to play media |

### setMinimumFontSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setMinimumFontSize(size: Int): Unit
```

Sets the minimum font size. The default is 8.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a non-negative integer between 1 and 72. Any number outside the specified range will be pinned. |

### setMinimumLogicalFontSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setMinimumLogicalFontSize(size: Int): Unit
```

Sets the minimum logical font size. The default is 8.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a non-negative integer between 1 and 72. Any number outside the specified range will be pinned. |

### setMixedContentMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setMixedContentMode(mode: Int): Unit
```

Configures the WebView's behavior when a secure origin attempts to load a resource from an insecure origin. By default, apps that target [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md) or below default to [MIXED_CONTENT_ALWAYS_ALLOW](WebSettings.md). Apps targeting [android.os.Build.VERSION_CODES#LOLLIPOP](../android/os/Build.VERSION_CODES.md) default to [MIXED_CONTENT_NEVER_ALLOW](WebSettings.md). The preferred and most secure mode of operation for the WebView is [MIXED_CONTENT_NEVER_ALLOW](WebSettings.md) and use of [MIXED_CONTENT_ALWAYS_ALLOW](WebSettings.md) is strongly discouraged.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The mixed content mode to use. One of [MIXED_CONTENT_NEVER_ALLOW](WebSettings.md), [MIXED_CONTENT_ALWAYS_ALLOW](WebSettings.md) or [MIXED_CONTENT_COMPATIBILITY_MODE](WebSettings.md). |

### setNeedInitialFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNeedInitialFocus(flag: Boolean): Unit
```

Tells the WebView whether it needs to set a node to have focus when android.webkit.WebView#requestFocus(int,android.graphics.Rect) is called. The default value is`true`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the WebView needs to set a node |

### setOffscreenPreRaster

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOffscreenPreRaster(enabled: Boolean): Unit
```

Sets whether this WebView should raster tiles when it is offscreen but attached to a window. Turning this on can avoid rendering artifacts when animating an offscreen WebView on-screen. Offscreen WebViews in this mode use more memory. The default value is false. 
Please follow these guidelines to limit memory usage:

- WebView size should be not be larger than the device screen size.
- Limit use of this mode to a small number of WebViews. Use it for visible WebViews and WebViews about to be animated to visible.

<br />

### setPluginState

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPluginState(state: WebSettings.PluginState!): Unit
```

**Deprecated:** *Plugins are not supported in API level [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md) or later; enabling plugins is a no-op.*

Tells the WebView to enable, disable, or have plugins on demand. On demand mode means that if a plugin exists that can handle the embedded content, a placeholder icon will be shown instead of the plugin. When the placeholder is clicked, the plugin will be enabled. The default is [PluginState.OFF](../android/webkit/WebSettings.PluginState.md).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [WebSettings.PluginState](../android/webkit/WebSettings.PluginState.md)!:a PluginState value |

### setRenderPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setRenderPriority(priority: WebSettings.RenderPriority!): Unit
```

**Deprecated:** *This is no longer supported. See [WebView.setRendererPriorityPolicy](WebView.md))if you instead want to control how freely the system should kill the renderer process under low memory conditions.*

Sets the CPU scheduling priority of the Render thread. Unlike the other settings, this one only needs to be called once per process. The default value is [RenderPriority.NORMAL](../android/webkit/WebSettings.RenderPriority.md).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [WebSettings.RenderPriority](../android/webkit/WebSettings.RenderPriority.md)!:the priority |

### setSafeBrowsingEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSafeBrowsingEnabled(enabled: Boolean): Unit
```

Sets whether Safe Browsing is enabled. Safe Browsing allows WebView to protect against malware and phishing attacks by verifying the links.

Safe Browsing can be disabled for all WebViews using a manifest tag (read [general Safe Browsing info](WebView.md)). The manifest tag has a lower precedence than this API.

Safe Browsing is enabled by default for devices which support it.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether Safe Browsing is enabled. |

### setSansSerifFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSansSerifFontFamily(font: String!): Unit
```

Sets the sans-serif font family name. The default is "sans-serif".

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `font` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a font family name |

### setSaveFormData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSaveFormData(save: Boolean): Unit
```

**Deprecated:** *In Android O and afterwards, this function does not have any effect. Form data will be saved to platform's autofill service if applicable.*

Sets whether the WebView should save form data. In [android.os.Build.VERSION_CODES#O](../android/os/Build.VERSION_CODES.md), the platform has implemented a fully functional Autofill feature to store form data. Therefore, the Webview form data save feature is disabled.

Note that the feature will continue to be supported on older versions of Android as before. 
**See Also**

- [#getSaveFormData](WebSettings.md)) 

### setSavePassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSavePassword(save: Boolean): Unit
```

**Deprecated:** *Saving passwords in WebView will not be supported in future versions.*

Sets whether the WebView should save passwords. The default is`true`. 

### setSerifFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSerifFontFamily(font: String!): Unit
```

Sets the serif font family name. The default is "sans-serif".

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `font` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a font family name |

### setStandardFontFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setStandardFontFamily(font: String!): Unit
```

Sets the standard font family name. The default is "sans-serif".

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `font` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a font family name |

### setSupportMultipleWindows

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSupportMultipleWindows(support: Boolean): Unit
```

Sets whether the WebView should support multiple windows.

If set to`true`, the [WebChromeClient.onCreateWindow](WebChromeClient.md))callback must be implemented by the application to handle the creation of new windows.

The default is`false`. When multiple window support is disabled, requests to open new windows (either from the`window.open()`JavaScript API or from links with`target="_blank"`) will instead be treated as top-level navigations, replacing the current page in the same WebView.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------|
| `support` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to support multiple windows |

### setSupportZoom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSupportZoom(support: Boolean): Unit
```

Sets whether the WebView should support zooming using its on-screen zoom controls and gestures. The particular zoom mechanisms that should be used can be set with [setBuiltInZoomControls](WebSettings.md)). This setting does not affect zooming performed using the [WebView.zoomIn()](WebView.md))and [WebView.zoomOut()](WebView.md))methods. The default is`true`.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `support` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the WebView should support zoom |

### setTextSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTextSize(t: WebSettings.TextSize!): Unit
```

**Deprecated:** *Use [setTextZoom](WebSettings.md))instead.*

Sets the text size of the page. The default is [TextSize.NORMAL](../android/webkit/WebSettings.TextSize.md).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [WebSettings.TextSize](../android/webkit/WebSettings.TextSize.md)!:the text size as a [TextSize](../android/webkit/WebSettings.TextSize.md) value |

### setTextZoom

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTextZoom(textZoom: Int): Unit
```

Sets the text zoom of the page in percent. The default is 100.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------|
| `textZoom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the text zoom in percent |

### setUseWideViewPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setUseWideViewPort(use: Boolean): Unit
```

Sets whether the WebView should enable support for the "viewport" HTML meta tag or should use a wide viewport. When the value of the setting is`false`, the layout width is always set to the width of the WebView control in device-independent (CSS) pixels. When the value is`true`and the page contains the viewport meta tag, the value of the width specified in the tag is used. If the page does not contain the tag or does not provide a width, then a wide viewport will be used.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `use` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to enable support for the viewport meta tag |

### setUserAgentString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setUserAgentString(ua: String?): Unit
```

Sets the WebView's user-agent string. If the string is`null`or empty, the system default value will be used.

If the user-agent is overridden in this way, the values of the User-Agent Client Hints headers and`navigator.userAgentData`for this WebView could be changed.

See [androidx.webkit.WebSettingsCompat #setUserAgentMetadata(WebSettings,UserAgentMetadata)](https://developer.android.com/reference/androidx/webkit/WebSettingsCompat #setUserAgentMetadata(WebSettings,UserAgentMetadata))for details.

Note that starting from [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md) Android version, changing the user-agent while loading a web page causes WebView to initiate loading once again.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------|
| `ua` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:new user-agent string This value may be`null`. |

### supportMultipleWindows

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportMultipleWindows(): Boolean
```

Gets whether the WebView supports multiple windows.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the WebView supports multiple windows |

**See Also**

- [#setSupportMultipleWindows](WebSettings.md)) 

### supportZoom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportZoom(): Boolean
```

Gets whether the WebView supports zoom.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the WebView supports zoom |

**See Also**

- [#setSupportZoom](WebSettings.md))
