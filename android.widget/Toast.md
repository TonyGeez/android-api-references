# Toast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Toast

Kotlin| [Java](https://developer.android.com/reference/android/widget/Toast "View this page in Java") 
| --- | --- |

```
open class Toast
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.Toast](https://developer.android.com/reference/kotlin/android/widget/Toast#) |

A toast is a view containing a quick little message for the user. The toast class helps you create and show those. {@more}

When the view is shown to the user, appears as a floating view over the application. It will never receive focus. The user will probably be in the middle of typing something else. The idea is to be as unobtrusive as possible, while still showing the user the information you want them to see. Two examples are the volume control, and the brief message saying that your settings have been saved.

The easiest way to use this class is to call one of the static methods that constructs everything you need and returns a new Toast object.

Note that [Snackbars](https://developer.android.com/reference/com/google/android/material/snackbar/Snackbar) are preferred for brief messages while the app is in the foreground.

Note that toasts being sent from the background are rate limited, so avoid sending such toasts in quick succession.

Starting with Android 12 (API level 31), apps targeting Android 12 or newer will have their toasts limited to two lines.
|
| ### Developer Guides
|
| For information about creating Toast notifications, read the [Toast Notifications](https://developer.android.com/guide/topics/ui/notifiers/toasts.html) developer guide.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/widget/Toast.Callback) Callback object to be called when the toast is shown or hidden. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_LONG](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_LONG:kotlin.Int) Show the view or text notification for a long period of time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_SHORT:kotlin.Int) Show the view or text notification for a short period of time. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Toast](https://developer.android.com/reference/kotlin/android/widget/Toast#Toast(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Construct an empty Toast object. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallback](https://developer.android.com/reference/kotlin/android/widget/Toast#addCallback(android.widget.Toast.Callback))`(`callback:` ` [Toast.Callback](https://developer.android.com/reference/kotlin/android/widget/Toast.Callback)`)` Adds a callback to be notified when the toast is shown or hidden. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/widget/Toast#cancel())`()` Close the view if it's showing, or don't show it if it isn't showing yet. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuration](https://developer.android.com/reference/kotlin/android/widget/Toast#getDuration())`()` Return the duration. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGravity](https://developer.android.com/reference/kotlin/android/widget/Toast#getGravity())`()` Get the location at which the notification should appear on the screen. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHorizontalMargin](https://developer.android.com/reference/kotlin/android/widget/Toast#getHorizontalMargin())`()` Return the horizontal margin. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVerticalMargin](https://developer.android.com/reference/kotlin/android/widget/Toast#getVerticalMargin())`()` Return the vertical margin. |
| --- | --- |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | [getView](https://developer.android.com/reference/kotlin/android/widget/Toast#getView())`()` Return the view. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getXOffset](https://developer.android.com/reference/kotlin/android/widget/Toast#getXOffset())`()` Return the X offset in pixels to apply to the gravity's location. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYOffset](https://developer.android.com/reference/kotlin/android/widget/Toast#getYOffset())`()` Return the Y offset in pixels to apply to the gravity's location. |
| --- | --- |
| openstatic [Toast](https://developer.android.com/reference/kotlin/android/widget/Toast#)! | [makeText](https://developer.android.com/reference/kotlin/android/widget/Toast#makeText(android.content.Context,%20kotlin.Int,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Make a standard toast that just contains text from a resource. |
| openstatic [Toast](https://developer.android.com/reference/kotlin/android/widget/Toast#)! | [makeText](https://developer.android.com/reference/kotlin/android/widget/Toast#makeText(android.content.Context,%20kotlin.CharSequence,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Make a standard toast that just contains text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallback](https://developer.android.com/reference/kotlin/android/widget/Toast#removeCallback(android.widget.Toast.Callback))`(`callback:` ` [Toast.Callback](https://developer.android.com/reference/kotlin/android/widget/Toast.Callback)`)` Removes a callback previously added with [addCallback(android.widget.Toast.Callback)](https://developer.android.com/reference/kotlin/android/widget/Toast#addCallback(android.widget.Toast.Callback)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDuration](https://developer.android.com/reference/kotlin/android/widget/Toast#setDuration(kotlin.Int))`(`duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set how long to show the view for. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGravity](https://developer.android.com/reference/kotlin/android/widget/Toast#setGravity(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the location at which the notification should appear on the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMargin](https://developer.android.com/reference/kotlin/android/widget/Toast#setMargin(kotlin.Float,%20kotlin.Float))`(`horizontalMargin:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `verticalMargin:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the margins of the view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](https://developer.android.com/reference/kotlin/android/widget/Toast#setText(kotlin.Int))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Update the text in a Toast that was previously created using one of the makeText() methods. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](https://developer.android.com/reference/kotlin/android/widget/Toast#setText(kotlin.CharSequence))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Update the text in a Toast that was previously created using one of the makeText() methods. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setView](https://developer.android.com/reference/kotlin/android/widget/Toast#setView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Set the view to show. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](https://developer.android.com/reference/kotlin/android/widget/Toast#show())`()` Show the view for the specified duration. |

## Constants

### LENGTH_LONG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_LONG: Int
```

Show the view or text notification for a long period of time. This time could be user-definable. 

 Value: 1

**See Also**

- [#setDuration](https://developer.android.com/reference/kotlin/android/widget/Toast#setDuration(kotlin.Int)) 

### LENGTH_SHORT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_SHORT: Int
```

Show the view or text notification for a short period of time. This time could be user-definable. This is the default. 

 Value: 0

**See Also**

- [#setDuration](https://developer.android.com/reference/kotlin/android/widget/Toast#setDuration(kotlin.Int))

## Public constructors

### Toast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Toast(context: Context!)
```

Construct an empty Toast object. You must call [setView](https://developer.android.com/reference/kotlin/android/widget/Toast#setView(android.view.View))before you can call [show](https://developer.android.com/reference/kotlin/android/widget/Toast#show()).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context to use. Usually your [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) object. |

## Public methods

### addCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCallback(callback: Toast.Callback): Unit
```

Adds a callback to be notified when the toast is shown or hidden. Note that if the toast is blocked for some reason you won't get a call back.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Toast.Callback](https://developer.android.com/reference/kotlin/android/widget/Toast.Callback):This value cannot be`null`. |

**See Also**

- [#removeCallback(Callback)](https://developer.android.com/reference/kotlin/android/widget/Toast#removeCallback(android.widget.Toast.Callback)) 

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

Close the view if it's showing, or don't show it if it isn't showing yet. You do not normally have to call this. Normally view will disappear on its own after the appropriate duration. 

### getDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDuration(): Int
```

Return the duration.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.widget.Toast#LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_SHORT:kotlin.Int), or [android.widget.Toast#LENGTH_LONG](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_LONG:kotlin.Int) |

**See Also**

- [#setDuration](https://developer.android.com/reference/kotlin/android/widget/Toast#setDuration(kotlin.Int)) 

### getGravity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGravity(): Int
```

Get the location at which the notification should appear on the screen.

**Warning:** Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), for apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 
**See Also**

- [android.view.Gravity](https://developer.android.com/reference/kotlin/android/view/Gravity.html#)
- [#getGravity](https://developer.android.com/reference/kotlin/android/widget/Toast#getGravity()) 

### getHorizontalMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHorizontalMargin(): Float
```

Return the horizontal margin.

**Warning:** Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), for apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 

### getVerticalMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVerticalMargin(): Float
```

Return the vertical margin.

**Warning:** Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), for apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 

### getView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(): View?
```

**Deprecated:** *Custom toast views are deprecated. Apps can create a standard text toast with the [makeText(android.content.Context,java.lang.CharSequence,int)](https://developer.android.com/reference/kotlin/android/widget/Toast#makeText(android.content.Context,%20kotlin.CharSequence,%20kotlin.Int))method, or use a [Snackbar](https://developer.android.com/reference/com/google/android/material/snackbar/Snackbar) when in the foreground. Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher that are in the background will not have custom toast views displayed.*

Return the view.

Toasts constructed with [Toast(android.content.Context)](https://developer.android.com/reference/kotlin/android/widget/Toast#Toast(android.content.Context))that haven't called [setView(android.view.View)](https://developer.android.com/reference/kotlin/android/widget/Toast#setView(android.view.View))with a non-`null`view will return`null`here.

Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), in apps targeting API level [android.os.Build.VERSION_CODES#R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher, toasts constructed with [makeText(android.content.Context,java.lang.CharSequence,int)](https://developer.android.com/reference/kotlin/android/widget/Toast#makeText(android.content.Context,%20kotlin.CharSequence,%20kotlin.Int))or its variants will also return`null`here unless they had called [setView(android.view.View)](https://developer.android.com/reference/kotlin/android/widget/Toast#setView(android.view.View))with a non-`null`view. If you want to be notified when the toast is shown or hidden, use [addCallback(android.widget.Toast.Callback)](https://developer.android.com/reference/kotlin/android/widget/Toast#addCallback(android.widget.Toast.Callback)). 
**See Also**

- [#setView](https://developer.android.com/reference/kotlin/android/widget/Toast#setView(android.view.View)) 

### getXOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getXOffset(): Int
```

Return the X offset in pixels to apply to the gravity's location.

**Warning:** Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), for apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 

### getYOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYOffset(): Int
```

Return the Y offset in pixels to apply to the gravity's location.

**Warning:** Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), for apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 

### makeText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun makeText(
    context: Context!, 
    resId: Int, 
    duration: Int
): Toast!
```

Make a standard toast that just contains text from a resource.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context to use. Usually your [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) object. |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the string resource to use. Can be formatted text. |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How long to display the message. Either [LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_SHORT:kotlin.Int) or [LENGTH_LONG](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_LONG:kotlin.Int) Value is [android.widget.Toast#LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_SHORT:kotlin.Int), or [android.widget.Toast#LENGTH_LONG](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_LONG:kotlin.Int) |
| --- | --- |

| Exceptions ||
|---------------------------------------------------|---------------------------------|
| `android.content.res.Resources.NotFoundException` | if the resource can't be found. |

### makeText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun makeText(
    context: Context!, 
    text: CharSequence!, 
    duration: Int
): Toast!
```

Make a standard toast that just contains text.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context to use. Usually your [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) object. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text to show. Can be formatted text. |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How long to display the message. Either [LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_SHORT:kotlin.Int) or [LENGTH_LONG](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_LONG:kotlin.Int) Value is [android.widget.Toast#LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_SHORT:kotlin.Int), or [android.widget.Toast#LENGTH_LONG](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_LONG:kotlin.Int) |
| --- | --- |

### removeCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeCallback(callback: Toast.Callback): Unit
```

Removes a callback previously added with [addCallback(android.widget.Toast.Callback)](https://developer.android.com/reference/kotlin/android/widget/Toast#addCallback(android.widget.Toast.Callback)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Toast.Callback](https://developer.android.com/reference/kotlin/android/widget/Toast.Callback):This value cannot be`null`. |

### setDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDuration(duration: Int): Unit
```

Set how long to show the view for.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.widget.Toast#LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_SHORT:kotlin.Int), or [android.widget.Toast#LENGTH_LONG](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_LONG:kotlin.Int) |

**See Also**

- [#LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_SHORT:kotlin.Int)
- [#LENGTH_LONG](https://developer.android.com/reference/kotlin/android/widget/Toast#LENGTH_LONG:kotlin.Int) 

### setGravity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGravity(
    gravity: Int, 
    xOffset: Int, 
    yOffset: Int
): Unit
```

Set the location at which the notification should appear on the screen.

**Warning:** Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), for apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher, this method is a no-op when called on text toasts. 
**See Also**

- [android.view.Gravity](https://developer.android.com/reference/kotlin/android/view/Gravity.html#)
- [#getGravity](https://developer.android.com/reference/kotlin/android/widget/Toast#getGravity()) 

### setMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMargin(
    horizontalMargin: Float, 
    verticalMargin: Float
): Unit
```

Set the margins of the view.

**Warning:** Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), for apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher, this method is a no-op when called on text toasts.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `horizontalMargin` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The horizontal margin, in percentage of the container width, between the container's edges and the notification |
| `verticalMargin` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The vertical margin, in percentage of the container height, between the container's edges and the notification |

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setText(resId: Int): Unit
```

Update the text in a Toast that was previously created using one of the makeText() methods.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new text for the Toast. |

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setText(s: CharSequence!): Unit
```

Update the text in a Toast that was previously created using one of the makeText() methods.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The new text for the Toast. |

### setView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setView(view: View!): Unit
```

**Deprecated:** *Custom toast views are deprecated. Apps can create a standard text toast with the [makeText(android.content.Context,java.lang.CharSequence,int)](https://developer.android.com/reference/kotlin/android/widget/Toast#makeText(android.content.Context,%20kotlin.CharSequence,%20kotlin.Int))method, or use a [Snackbar](https://developer.android.com/reference/com/google/android/material/snackbar/Snackbar) when in the foreground. Starting from Android [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), apps targeting API level [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher that are in the background will not have custom toast views displayed.*

Set the view to show. 
**See Also**

- [#getView](https://developer.android.com/reference/kotlin/android/widget/Toast#getView()) 

### show

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun show(): Unit
```

Show the view for the specified duration.

Note that toasts being sent from the background are rate limited, so avoid sending such toasts in quick succession.
