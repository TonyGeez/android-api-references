# Toast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Toast

Kotlin| [Java](../android/widget/Toast.md) 
| --- | --- |

```
open class Toast
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.Toast](../android/widget/Toast.md) |

A toast is a view containing a quick little message for the user. The toast class helps you create and show those. {@more}

When the view is shown to the user, appears as a floating view over the application. It will never receive focus. The user will probably be in the middle of typing something else. The idea is to be as unobtrusive as possible, while still showing the user the information you want them to see. Two examples are the volume control, and the brief message saying that your settings have been saved.

The easiest way to use this class is to call one of the static methods that constructs everything you need and returns a new Toast object.

Note that [Snackbars](../com/google/android/material/snackbar/Snackbar.md) are preferred for brief messages while the app is in the foreground.

Note that toasts being sent from the background are rate limited, so avoid sending such toasts in quick succession.

Starting with Android 12 (API level 31), apps targeting Android 12 or newer will have their toasts limited to two lines.
|
| ### Developer Guides
|
| For information about creating Toast notifications, read the [Toast Notifications](https://developer.android.com/guide/topics/ui/notifiers/toasts.html) developer guide.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/widget/Toast.Callback.md) Callback object to be called when the toast is shown or hidden. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_LONG](../android/widget/Toast.md) Show the view or text notification for a long period of time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_SHORT](../android/widget/Toast.md) Show the view or text notification for a short period of time. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Toast](../android/widget/Toast.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Construct an empty Toast object. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallback](../android/widget/Toast.md))`(`callback:` ` [Toast.Callback](../android/widget/Toast.Callback.md)`)` Adds a callback to be notified when the toast is shown or hidden. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/widget/Toast.md))`()` Close the view if it's showing, or don't show it if it isn't showing yet. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuration](../android/widget/Toast.md))`()` Return the duration. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGravity](../android/widget/Toast.md))`()` Get the location at which the notification should appear on the screen. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHorizontalMargin](../android/widget/Toast.md))`()` Return the horizontal margin. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVerticalMargin](../android/widget/Toast.md))`()` Return the vertical margin. |
| --- | --- |
| open [View](../android/view/View.md)? | [getView](../android/widget/Toast.md))`()` Return the view. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getXOffset](../android/widget/Toast.md))`()` Return the X offset in pixels to apply to the gravity's location. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYOffset](../android/widget/Toast.md))`()` Return the Y offset in pixels to apply to the gravity's location. |
| --- | --- |
| openstatic [Toast](../android/widget/Toast.md)! | [makeText](../android/widget/Toast.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Make a standard toast that just contains text from a resource. |
| openstatic [Toast](../android/widget/Toast.md)! | [makeText](../android/widget/Toast.md))`(`context:` ` [Context](../android/content/Context.md)!`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Make a standard toast that just contains text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallback](../android/widget/Toast.md))`(`callback:` ` [Toast.Callback](../android/widget/Toast.Callback.md)`)` Removes a callback previously added with [addCallback(android.widget.Toast.Callback)](../android/widget/Toast.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDuration](../android/widget/Toast.md))`(`duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set how long to show the view for. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGravity](../android/widget/Toast.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the location at which the notification should appear on the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMargin](../android/widget/Toast.md))`(`horizontalMargin:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `verticalMargin:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the margins of the view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](../android/widget/Toast.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Update the text in a Toast that was previously created using one of the makeText() methods. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](../android/widget/Toast.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Update the text in a Toast that was previously created using one of the makeText() methods. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setView](../android/widget/Toast.md))`(`view:` ` [View](../android/view/View.md)!`)` Set the view to show. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](../android/widget/Toast.md))`()` Show the view for the specified duration. |

## Constants

### LENGTH_LONG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_LONG: Int
```

Show the view or text notification for a long period of time. This time could be user-definable. 

 Value: 1

**See Also**

- [#setDuration](../android/widget/Toast.md)) 

### LENGTH_SHORT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_SHORT: Int
```

Show the view or text notification for a short period of time. This time could be user-definable. This is the default. 

 Value: 0

**See Also**

- [#setDuration](../android/widget/Toast.md))

## Public constructors

### Toast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Toast(context: Context!)
```

Construct an empty Toast object. You must call [setView](../android/widget/Toast.md))before you can call [show](../android/widget/Toast.md)).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The context to use. Usually your [android.app.Activity](../android/app/Activity.md) object. |

## Public methods

### addCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCallback(callback: Toast.Callback): Unit
```

Adds a callback to be notified when the toast is shown or hidden. Note that if the toast is blocked for some reason you won't get a call back.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Toast.Callback](../android/widget/Toast.Callback.md):This value cannot be`null`. |

**See Also**

- [#removeCallback(Callback)](../android/widget/Toast.md)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.widget.Toast#LENGTH_SHORT](../android/widget/Toast.md), or [android.widget.Toast#LENGTH_LONG](../android/widget/Toast.md) |

**See Also**

- [#setDuration](../android/widget/Toast.md)) 

### getGravity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGravity(): Int
```

Get the location at which the notification should appear on the screen.

**Warning:** Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), for apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 
**See Also**

- [android.view.Gravity](../android/view/Gravity.md)
- [#getGravity](../android/widget/Toast.md)) 

### getHorizontalMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHorizontalMargin(): Float
```

Return the horizontal margin.

**Warning:** Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), for apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 

### getVerticalMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVerticalMargin(): Float
```

Return the vertical margin.

**Warning:** Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), for apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 

### getView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(): View?
```

**Deprecated:** *Custom toast views are deprecated. Apps can create a standard text toast with the [makeText(android.content.Context,java.lang.CharSequence,int)](../android/widget/Toast.md))method, or use a [Snackbar](../com/google/android/material/snackbar/Snackbar.md) when in the foreground. Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher that are in the background will not have custom toast views displayed.*

Return the view.

Toasts constructed with [Toast(android.content.Context)](../android/widget/Toast.md))that haven't called [setView(android.view.View)](../android/widget/Toast.md))with a non-`null`view will return`null`here.

Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), in apps targeting API level [android.os.Build.VERSION_CODES#R](../android/os/Build.VERSION_CODES.md) or higher, toasts constructed with [makeText(android.content.Context,java.lang.CharSequence,int)](../android/widget/Toast.md))or its variants will also return`null`here unless they had called [setView(android.view.View)](../android/widget/Toast.md))with a non-`null`view. If you want to be notified when the toast is shown or hidden, use [addCallback(android.widget.Toast.Callback)](../android/widget/Toast.md)). 
**See Also**

- [#setView](../android/widget/Toast.md)) 

### getXOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getXOffset(): Int
```

Return the X offset in pixels to apply to the gravity's location.

**Warning:** Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), for apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 

### getYOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYOffset(): Int
```

Return the Y offset in pixels to apply to the gravity's location.

**Warning:** Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), for apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher, this method shouldn't be called on text toasts as its return value may not reflect actual value since text toasts are not rendered by the app anymore. 

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
| `context` | [Context](../android/content/Context.md)!:The context to use. Usually your [android.app.Activity](../android/app/Activity.md) object. |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the string resource to use. Can be formatted text. |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How long to display the message. Either [LENGTH_SHORT](../android/widget/Toast.md) or [LENGTH_LONG](../android/widget/Toast.md) Value is [android.widget.Toast#LENGTH_SHORT](../android/widget/Toast.md), or [android.widget.Toast#LENGTH_LONG](../android/widget/Toast.md) |
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
| `context` | [Context](../android/content/Context.md)!:The context to use. Usually your [android.app.Activity](../android/app/Activity.md) object. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text to show. Can be formatted text. |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How long to display the message. Either [LENGTH_SHORT](../android/widget/Toast.md) or [LENGTH_LONG](../android/widget/Toast.md) Value is [android.widget.Toast#LENGTH_SHORT](../android/widget/Toast.md), or [android.widget.Toast#LENGTH_LONG](../android/widget/Toast.md) |
| --- | --- |

### removeCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeCallback(callback: Toast.Callback): Unit
```

Removes a callback previously added with [addCallback(android.widget.Toast.Callback)](../android/widget/Toast.md)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Toast.Callback](../android/widget/Toast.Callback.md):This value cannot be`null`. |

### setDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDuration(duration: Int): Unit
```

Set how long to show the view for.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.widget.Toast#LENGTH_SHORT](../android/widget/Toast.md), or [android.widget.Toast#LENGTH_LONG](../android/widget/Toast.md) |

**See Also**

- [#LENGTH_SHORT](../android/widget/Toast.md)
- [#LENGTH_LONG](../android/widget/Toast.md) 

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

**Warning:** Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), for apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher, this method is a no-op when called on text toasts. 
**See Also**

- [android.view.Gravity](../android/view/Gravity.md)
- [#getGravity](../android/widget/Toast.md)) 

### setMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMargin(
    horizontalMargin: Float, 
    verticalMargin: Float
): Unit
```

Set the margins of the view.

**Warning:** Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), for apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher, this method is a no-op when called on text toasts.

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

**Deprecated:** *Custom toast views are deprecated. Apps can create a standard text toast with the [makeText(android.content.Context,java.lang.CharSequence,int)](../android/widget/Toast.md))method, or use a [Snackbar](../com/google/android/material/snackbar/Snackbar.md) when in the foreground. Starting from Android [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md), apps targeting API level [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or higher that are in the background will not have custom toast views displayed.*

Set the view to show. 
**See Also**

- [#getView](../android/widget/Toast.md)) 

### show

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun show(): Unit
```

Show the view for the specified duration.

Note that toasts being sent from the background are rate limited, so avoid sending such toasts in quick succession.
