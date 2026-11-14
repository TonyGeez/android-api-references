# PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PopupWindow

Kotlin| [Java](https://developer.android.com/reference/android/widget/PopupWindow "View this page in Java") 
| --- | --- |

```
open class PopupWindow
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#) |

This class represents a popup window that can be used to display an arbitrary view. The popup window is a floating container that appears on top of the current activity.

### Animation

On all versions of Android, popup window enter and exit animations may be specified by calling [setAnimationStyle(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setAnimationStyle(kotlin.Int))and passing the resource ID for an animation style that defines`windowEnterAnimation`and`windowExitAnimation`. For example, passing [android.R.style#Animation_Dialog](https://developer.android.com/reference/kotlin/android/R.style.html#Animation_Dialog:kotlin.Int) will give a scale and alpha animation. 
A window animation style may also be specified in the popup window's style XML via the [popupAnimationStyle](https://developer.android.com/reference/kotlin/android/R.styleable.html#PopupWindow_popupAnimationStyle:kotlin.Int) attribute.

Starting with API 23, more complex popup window enter and exit transitions may be specified by calling either [setEnterTransition(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setEnterTransition(android.transition.Transition))or [setExitTransition(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setExitTransition(android.transition.Transition))and passing a [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#). 
Popup enter and exit transitions may also be specified in the popup window's style XML via the [popupEnterTransition](https://developer.android.com/reference/kotlin/android/R.styleable.html#PopupWindow_popupEnterTransition:kotlin.Int) and [popupExitTransition](https://developer.android.com/reference/kotlin/android/R.styleable.html#PopupWindow_popupExitTransition:kotlin.Int) attributes, respectively.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupWindow.OnDismissListener) Listener that is called when this popup window is dismissed. |

| XML attributes ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [`android:overlapAnchor`](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#attr_PopupWindow) | Whether the popup window should overlap its anchor view. |
| [`android:popupAnimationStyle`](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#attr_PopupWindow) | The animation style to use for the popup window. |
| [`android:popupBackground`](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#attr_PopupWindow) | The background to use for the popup window. |
| --- | --- |
| [`android:popupElevation`](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#attr_PopupWindow) | Window elevation to use for the popup window. |
| [`android:popupEnterTransition`](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#attr_PopupWindow) | Transition used to move views into the popup window. |
| [`android:popupExitTransition`](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#attr_PopupWindow) | Transition used to move views out of the popup window. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_METHOD_FROM_FOCUSABLE](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_FROM_FOCUSABLE:kotlin.Int) Mode for [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)): the requirements for the input method should be based on the focusability of the popup. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_METHOD_NEEDED](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_NEEDED:kotlin.Int) Mode for [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)): this popup always needs to work with an input method, regardless of whether it is focusable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_METHOD_NOT_NEEDED](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_NOT_NEEDED:kotlin.Int) Mode for [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)): this popup never needs to work with an input method, regardless of whether it is focusable. |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow())`()` Create a new empty, non focusable popup window of dimension (0,0). |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Create a new empty, non focusable popup window of dimension (0,0). |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` Create a new empty, non focusable popup window of dimension (0,0). |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new empty, non focusable popup window of dimension (0,0). |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new, empty, non focusable popup window of dimension (0,0). |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow(android.view.View))`(`contentView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Create a new non focusable popup window which can display the contentView. |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow(android.view.View,%20kotlin.Int,%20kotlin.Int))`(`contentView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new non focusable popup window which can display the contentView. |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`contentView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `focusable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a new popup window which can display the contentView. |
| [PopupWindow](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#PopupWindow(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new empty, non focusable popup window. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#dismiss())`()` Disposes of the popup window. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAnimationStyle](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getAnimationStyle())`()` Return the animation style to use the popup appears and disappears |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | [getBackground](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getBackground())`()` Return the drawable used as the popup window's background. |
| --- | --- |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getContentView](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getContentView())`()` Return the view used as the content of the popup window. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getElevation](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getElevation())`()` <br /> |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)? | [getEnterTransition](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getEnterTransition())`()` Returns the enter transition to be used when the popup window is shown. |
| --- | --- |
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)? | [getEpicenterBounds](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getEpicenterBounds())`()` Returns bounds which are used as a center of the enter and exit transitions. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)? | [getExitTransition](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getExitTransition())`()` Returns the exit transition to be used when the popup window is dismissed. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getHeight())`()` Returns the popup's requested height. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputMethodMode](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getInputMethodMode())`()` Return the current value in [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxAvailableHeight](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getMaxAvailableHeight(android.view.View))`(`anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Returns the maximum height that is available for the popup to be completely shown. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxAvailableHeight](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getMaxAvailableHeight(android.view.View,%20kotlin.Int))`(`anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `yOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the maximum height that is available for the popup to be completely shown. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxAvailableHeight](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getMaxAvailableHeight(android.view.View,%20kotlin.Int,%20kotlin.Boolean))`(`anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `yOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ignoreBottomDecorations:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the maximum height that is available for the popup to be completely shown, optionally ignoring any bottom decorations such as the input method. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getOverlapAnchor](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getOverlapAnchor())`()` Returns whether the popup window should overlap its anchor view when displayed as a drop-down. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoftInputMode](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getSoftInputMode())`()` Returns the current value in [setSoftInputMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setSoftInputMode(kotlin.Int)). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getWidth())`()` Returns the popup's requested width. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWindowLayoutType](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getWindowLayoutType())`()` Returns the layout type for this window. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAboveAnchor](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isAboveAnchor())`()` Indicates whether the popup is showing above (the y coordinate of the popup's bottom is less than the y coordinate of the anchor) or below the anchor view (the y coordinate of the popup is greater than y coordinate of the anchor's bottom). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAttachedInDecor](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isAttachedInDecor())`()` Indicates whether the popup window will be attached in the decor frame of its parent window. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClippedToScreen](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isClippedToScreen())`()` Indicates whether this popup will be clipped to the screen and not to the containing window |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClippingEnabled](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isClippingEnabled())`()` Indicates whether clipping of the popup window is enabled. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFocusable](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isFocusable())`()` Indicate whether the popup window can grab the focus. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLaidOutInScreen](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isLaidOutInScreen())`()` Indicates whether the popup window will be forced into using absolute screen coordinates for positioning. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOutsideTouchable](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isOutsideTouchable())`()` Indicates whether the popup window will be informed of touch events outside of its window. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShowing](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing())`()` Indicate whether this popup window is showing on screen. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSplitTouchEnabled](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isSplitTouchEnabled())`()` Indicates whether the popup window supports splitting touches. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTouchModal](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isTouchModal())`()` Indicates whether outside touches will be sent to this window or other windows behind it |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTouchable](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isTouchable())`()` Indicates whether the popup window receives touch events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimationStyle](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setAnimationStyle(kotlin.Int))`(`animationStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the animation style resource for this popup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttachedInDecor](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setAttachedInDecor(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This will attach the popup window to the decor frame of the parent window to avoid overlaping with screen decorations like the navigation bar. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBackgroundDrawable](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setBackgroundDrawable(android.graphics.drawable.Drawable))`(`background:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!`)` Specifies the background drawable for this popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClippingEnabled](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setClippingEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Allows the popup window to extend beyond the bounds of the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentView](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setContentView(android.view.View))`(`contentView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Change the popup's content. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElevation](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setElevation(kotlin.Float))`(`elevation:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the elevation for this popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterTransition](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setEnterTransition(android.transition.Transition))`(`enterTransition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)?`)` Sets the enter transition to be used when the popup window is shown. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEpicenterBounds](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setEpicenterBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`)` Sets the bounds used as the epicenter of the enter and exit transitions. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitTransition](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setExitTransition(android.transition.Transition))`(`exitTransition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)?`)` Sets the exit transition to be used when the popup window is dismissed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFocusable](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setFocusable(kotlin.Boolean))`(`focusable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Changes the focusability of the popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHeight](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setHeight(kotlin.Int))`(`height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the popup's requested height. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIgnoreCheekPress](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setIgnoreCheekPress())`()` Set the flag on popup to ignore cheek press events; by default this flag is set to false which means the popup will not ignore cheek press dispatch events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputMethodMode](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Control how the popup operates with an input method: one of [INPUT_METHOD_FROM_FOCUSABLE](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_FROM_FOCUSABLE:kotlin.Int), [INPUT_METHOD_NEEDED](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_NEEDED:kotlin.Int), or [INPUT_METHOD_NOT_NEEDED](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_NOT_NEEDED:kotlin.Int). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIsClippedToScreen](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setIsClippedToScreen(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Clip this popup window to the screen, but not to the containing window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIsLaidOutInScreen](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setIsLaidOutInScreen(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Allows the popup window to force the flag [WindowManager.LayoutParams.FLAG_LAYOUT_IN_SCREEN](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_LAYOUT_IN_SCREEN:kotlin.Int), overriding default behavior. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setOnDismissListener(android.widget.PopupWindow.OnDismissListener))`(`onDismissListener:` ` [PopupWindow.OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupWindow.OnDismissListener)!`)` Sets the listener to be called when the window is dismissed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutsideTouchable](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setOutsideTouchable(kotlin.Boolean))`(`touchable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Controls whether the pop-up will be informed of touch events outside of its window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOverlapAnchor](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setOverlapAnchor(kotlin.Boolean))`(`overlapAnchor:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the popup window should overlap its anchor view when displayed as a drop-down. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoftInputMode](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setSoftInputMode(kotlin.Int))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the operating mode for the soft input area. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSplitTouchEnabled](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setSplitTouchEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Allows the popup window to split touches across other windows that also support split touch. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTouchInterceptor](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setTouchInterceptor(android.view.View.OnTouchListener))`(`l:` ` [View.OnTouchListener](https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener.html#)!`)` Set a callback for all touch events being dispatched to the popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTouchModal](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setTouchModal(kotlin.Boolean))`(`touchModal:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this window is touch modal or if outside touches will be sent to other windows behind it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTouchable](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setTouchable(kotlin.Boolean))`(`touchable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Changes the touchability of the popup window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWidth](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setWidth(kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the popup's requested width. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWindowLayoutMode](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setWindowLayoutMode(kotlin.Int,%20kotlin.Int))`(`widthSpec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `heightSpec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the width and height measure specs that are given to the window manager by the popup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWindowLayoutType](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setWindowLayoutType(kotlin.Int))`(`layoutType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the layout type for this window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showAsDropDown](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#showAsDropDown(android.view.View))`(`anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Display the content view in a popup window anchored to the bottom-left corner of the anchor view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showAsDropDown](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#showAsDropDown(android.view.View,%20kotlin.Int,%20kotlin.Int))`(`anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `xoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Display the content view in a popup window anchored to the bottom-left corner of the anchor view offset by the specified x and y coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showAsDropDown](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#showAsDropDown(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `xoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Displays the content view in a popup window anchored to the corner of another view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showAtLocation](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#showAtLocation(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`parent:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Display the content view in a popup window at the specified location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())`()` Updates the state of the popup window, if it is currently being displayed, from the currently set state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update(android.view.View,%20kotlin.Int,%20kotlin.Int))`(`anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the position and the dimension of the popup window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `xoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the position and the dimension of the popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the dimension of the popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the position and the dimension of the popup window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `force:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Updates the position and the dimension of the popup window. |

## XML attributes

### android:overlapAnchor

```
android:overlapAnchor
```
Whether the popup window should overlap its anchor view.

May be a boolean value, such as "`true`" or "`false`". 

### android:popupAnimationStyle

```
android:popupAnimationStyle
```
The animation style to use for the popup window.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:popupBackground

```
android:popupBackground
```
The background to use for the popup window.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:popupElevation

```
android:popupElevation
```
Window elevation to use for the popup window.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:popupEnterTransition

```
android:popupEnterTransition
```
Transition used to move views into the popup window.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:popupExitTransition

```
android:popupExitTransition
```
Transition used to move views out of the popup window.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

## Constants

### INPUT_METHOD_FROM_FOCUSABLE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_FROM_FOCUSABLE: Int
```

Mode for [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)): the requirements for the input method should be based on the focusability of the popup. That is if it is focusable than it needs to work with the input method, else it doesn't. 

 Value: 0

### INPUT_METHOD_NEEDED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_NEEDED: Int
```

Mode for [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)): this popup always needs to work with an input method, regardless of whether it is focusable. This means that it will always be displayed so that the user can also operate the input method while it is shown. 

 Value: 1

### INPUT_METHOD_NOT_NEEDED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_NOT_NEEDED: Int
```

Mode for [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)): this popup never needs to work with an input method, regardless of whether it is focusable. This means that it will always be displayed to use as much space on the screen as needed, regardless of whether this covers the input method. 

 Value: 2

## Public constructors

### PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow()
```

Create a new empty, non focusable popup window of dimension (0,0).

The popup does not provide any background. This should be handled by the content view. 

### PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow(context: Context!)
```

Create a new empty, non focusable popup window of dimension (0,0).

The popup does provide a background. 

### PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow(
    context: Context!, 
    attrs: AttributeSet!)
```

Create a new empty, non focusable popup window of dimension (0,0).

The popup does provide a background. 

### PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```

Create a new empty, non focusable popup window of dimension (0,0).

The popup does provide a background. 

### PopupWindow

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

Create a new, empty, non focusable popup window of dimension (0,0).

The popup does not provide a background. 

### PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow(contentView: View!)
```

Create a new non focusable popup window which can display the contentView. The dimension of the window are (0,0).

The popup does not provide any background. This should be handled by the content view.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------|
| `contentView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the popup's content |

### PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow(
    contentView: View!, 
    width: Int, 
    height: Int)
```

Create a new non focusable popup window which can display the contentView. The dimension of the window must be passed to this constructor.

The popup does not provide any background. This should be handled by the content view.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------|
| `contentView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the popup's content |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup's width |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup's height |
| --- | --- |

### PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow(
    contentView: View!, 
    width: Int, 
    height: Int, 
    focusable: Boolean)
```

Create a new popup window which can display the contentView. The dimension of the window must be passed to this constructor.

The popup does not provide any background. This should be handled by the content view.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `contentView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the popup's content |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup's width |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup's height |
| --- | --- |
| `focusable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the popup can be focused, false otherwise |

### PopupWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupWindow(
    width: Int, 
    height: Int)
```

Create a new empty, non focusable popup window. The dimension of the window must be passed to this constructor.

The popup does not provide any background. This should be handled by the content view.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup's width |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup's height |

## Public methods

### dismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dismiss(): Unit
```

Disposes of the popup window. This method can be invoked only after [showAsDropDown(android.view.View)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#showAsDropDown(android.view.View))has been executed. Failing that, calling this method will have no effect. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#showAsDropDown(android.view.View)> 

### getAnimationStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimationStyle(): Int
```

Return the animation style to use the popup appears and disappears

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the animation style to use the popup appears and disappears |

### getBackground

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBackground(): Drawable!
```

Return the drawable used as the popup window's background.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | the background drawable or`null`if not set |

**See Also**

- [#setBackgroundDrawable(Drawable)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setBackgroundDrawable(android.graphics.drawable.Drawable)) 

### getContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentView(): View!
```

Return the view used as the content of the popup window.

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) representing the popup's content |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setContentView(android.view.View)> 

### getElevation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getElevation(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the elevation for this popup window in pixels |

**See Also**

- [#setElevation(float)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setElevation(kotlin.Float)) 

### getEnterTransition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEnterTransition(): Transition?
```

Returns the enter transition to be used when the popup window is shown.

| Return ||
|---------------------------------------------------------------------------------------------------|------------------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)? | the enter transition, or`null`if not set |

**See Also**

- [#setEnterTransition(Transition)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setEnterTransition(android.transition.Transition)) 

### getEpicenterBounds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEpicenterBounds(): Rect?
```

Returns bounds which are used as a center of the enter and exit transitions.

<br />

Transitions use Rect, referred to as the epicenter, to orient the direction of travel. For popup windows, the anchor view bounds are used as the default epicenter.

See [Transition.setEpicenterCallback(EpicenterCallback)](https://developer.android.com/reference/kotlin/android/transition/Transition.html#setEpicenterCallback(android.transition.Transition.EpicenterCallback))for more information about how transition epicenters work.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)? | bounds relative to anchor view, or`null`if not set |

**See Also**

- [#setEpicenterBounds(Rect)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setEpicenterBounds(android.graphics.Rect)) 

### getExitTransition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExitTransition(): Transition?
```

Returns the exit transition to be used when the popup window is dismissed.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)? | the exit transition, or`null`if not set |

**See Also**

- [#setExitTransition(Transition)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setExitTransition(android.transition.Transition)) 

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

Returns the popup's requested height. May be a layout constant such as [LayoutParams.WRAP_CONTENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int) or [LayoutParams.MATCH_PARENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int).

The actual size of the popup may depend on other factors such as clipping and window layout.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the popup height in pixels or a layout constant |

**See Also**

- [#setHeight(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setHeight(kotlin.Int)) 

### getInputMethodMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputMethodMode(): Int
```

Return the current value in [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)). 
**See Also**

- [#setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int)) 

### getMaxAvailableHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxAvailableHeight(anchor: View): Int
```

Returns the maximum height that is available for the popup to be completely shown. It is recommended that this height be the maximum for the popup's height, otherwise it is possible that the popup will be clipped.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):The view on which the popup window must be anchored. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The maximum available height for the popup to be completely shown. |

### getMaxAvailableHeight

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxAvailableHeight(
    anchor: View, 
    yOffset: Int
): Int
```

Returns the maximum height that is available for the popup to be completely shown. It is recommended that this height be the maximum for the popup's height, otherwise it is possible that the popup will be clipped.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):The view on which the popup window must be anchored. This value cannot be`null`. |
| `yOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):y offset from the view's bottom edge |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The maximum available height for the popup to be completely shown. |

### getMaxAvailableHeight

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxAvailableHeight(
    anchor: View, 
    yOffset: Int, 
    ignoreBottomDecorations: Boolean
): Int
```

Returns the maximum height that is available for the popup to be completely shown, optionally ignoring any bottom decorations such as the input method. It is recommended that this height be the maximum for the popup's height, otherwise it is possible that the popup will be clipped.

| Parameters ||
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):The view on which the popup window must be anchored. This value cannot be`null`. |
| `yOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):y offset from the view's bottom edge |
| `ignoreBottomDecorations` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, the height returned will be all the way to the bottom of the display, ignoring any bottom decorations |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The maximum available height for the popup to be completely shown. |

### getOverlapAnchor

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOverlapAnchor(): Boolean
```

Returns whether the popup window should overlap its anchor view when displayed as a drop-down.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the popup should overlap its anchor. |

**See Also**

- [#setOverlapAnchor(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setOverlapAnchor(kotlin.Boolean)) 

### getSoftInputMode

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSoftInputMode(): Int
```

Returns the current value in [setSoftInputMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setSoftInputMode(kotlin.Int)).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_UNSPECIFIED:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_UNCHANGED](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_UNCHANGED:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_HIDDEN](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_HIDDEN:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_ALWAYS_HIDDEN](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_ALWAYS_HIDDEN:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_VISIBLE](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_VISIBLE:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_ALWAYS_VISIBLE](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_ALWAYS_VISIBLE:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_ADJUST_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_UNSPECIFIED:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_ADJUST_RESIZE](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_RESIZE:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_ADJUST_PAN](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_PAN:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_ADJUST_NOTHING](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_NOTHING:kotlin.Int), and [android.view.WindowManager.LayoutParams#SOFT_INPUT_IS_FORWARD_NAVIGATION](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_IS_FORWARD_NAVIGATION:kotlin.Int) |

**See Also**

- [#setSoftInputMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setSoftInputMode(kotlin.Int))
- [android.view.WindowManager.LayoutParams#softInputMode](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#softInputMode:kotlin.Int) 

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

Returns the popup's requested width. May be a layout constant such as [LayoutParams.WRAP_CONTENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int) or [LayoutParams.MATCH_PARENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int).

The actual size of the popup may depend on other factors such as clipping and window layout.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the popup width in pixels or a layout constant |

**See Also**

- [#setWidth(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setWidth(kotlin.Int)) 

### getWindowLayoutType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindowLayoutType(): Int
```

Returns the layout type for this window. 
**See Also**

- [#setWindowLayoutType(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setWindowLayoutType(kotlin.Int)) 

### isAboveAnchor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAboveAnchor(): Boolean
```

Indicates whether the popup is showing above (the y coordinate of the popup's bottom is less than the y coordinate of the anchor) or below the anchor view (the y coordinate of the popup is greater than y coordinate of the anchor's bottom). The value returned by this method is meaningful only after [showAsDropDown(android.view.View)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#showAsDropDown(android.view.View))or [showAsDropDown(android.view.View,int,int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#showAsDropDown(android.view.View,%20kotlin.Int,%20kotlin.Int))was invoked.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this popup is showing above the anchor view, false otherwise. |

### isAttachedInDecor

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAttachedInDecor(): Boolean
```

Indicates whether the popup window will be attached in the decor frame of its parent window.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the window will be attached to the decor frame of its parent window. |

**See Also**

- [#setAttachedInDecor(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setAttachedInDecor(kotlin.Boolean))
- [android.view.WindowManager.LayoutParams#FLAG_LAYOUT_ATTACHED_IN_DECOR](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_LAYOUT_ATTACHED_IN_DECOR:kotlin.Int) 

### isClippedToScreen

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClippedToScreen(): Boolean
```

Indicates whether this popup will be clipped to the screen and not to the containing window

<br />

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if popup will be clipped to the screen instead of the window, false otherwise |

**See Also**

- [#setIsClippedToScreen(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setIsClippedToScreen(kotlin.Boolean)) 

### isClippingEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClippingEnabled(): Boolean
```

Indicates whether clipping of the popup window is enabled.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the clipping is enabled, false otherwise |

**See Also**

- [#setClippingEnabled(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setClippingEnabled(kotlin.Boolean)) 

### isFocusable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFocusable(): Boolean
```

Indicate whether the popup window can grab the focus.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the popup is focusable, false otherwise |

**See Also**

- [#setFocusable(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setFocusable(kotlin.Boolean)) 

### isLaidOutInScreen

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLaidOutInScreen(): Boolean
```

Indicates whether the popup window will be forced into using absolute screen coordinates for positioning.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the window will always be positioned in screen coordinates. |

**See Also**

- [#setIsLaidOutInScreen(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setIsLaidOutInScreen(kotlin.Boolean)) 

### isOutsideTouchable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOutsideTouchable(): Boolean
```

Indicates whether the popup window will be informed of touch events outside of its window.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the popup is outside touchable, false otherwise |

**See Also**

- [#setOutsideTouchable(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setOutsideTouchable(kotlin.Boolean)) 

### isShowing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isShowing(): Boolean
```

Indicate whether this popup window is showing on screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the popup is showing, false otherwise |

### isSplitTouchEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSplitTouchEnabled(): Boolean
```

Indicates whether the popup window supports splitting touches.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the touch splitting is enabled, false otherwise |

**See Also**

- [#setSplitTouchEnabled(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setSplitTouchEnabled(kotlin.Boolean)) 

### isTouchModal

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTouchModal(): Boolean
```

Indicates whether outside touches will be sent to this window or other windows behind it

<br />

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if touches will be sent to this window, false otherwise |

**See Also**

- [#setTouchModal(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setTouchModal(kotlin.Boolean)) 

### isTouchable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTouchable(): Boolean
```

Indicates whether the popup window receives touch events.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the popup is touchable, false otherwise |

**See Also**

- [#setTouchable(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setTouchable(kotlin.Boolean)) 

### setAnimationStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAnimationStyle(animationStyle: Int): Unit
```

Change the animation style resource for this popup.

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `animationStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):animation style to use when the popup appears and disappears. Set to -1 for the default animation, 0 for no animation, or a resource identifier for an explicit animation. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()> 

### setAttachedInDecor

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAttachedInDecor(enabled: Boolean): Unit
```

This will attach the popup window to the decor frame of the parent window to avoid overlaping with screen decorations like the navigation bar. Overrides the default behavior of the flag [WindowManager.LayoutParams.FLAG_LAYOUT_ATTACHED_IN_DECOR](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_LAYOUT_ATTACHED_IN_DECOR:kotlin.Int).

By default the flag is set on SDK version [Build.VERSION_CODES.LOLLIPOP_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int) or greater and cleared on lesser SDK versions.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the popup should be attached to the decor frame of its parent window. |

**See Also**

- [android.view.WindowManager.LayoutParams#FLAG_LAYOUT_ATTACHED_IN_DECOR](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_LAYOUT_ATTACHED_IN_DECOR:kotlin.Int) 

### setBackgroundDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBackgroundDrawable(background: Drawable!): Unit
```

Specifies the background drawable for this popup window. The background can be set to`null`.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| `background` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!:the popup's background |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getBackground()> 

### setClippingEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setClippingEnabled(enabled: Boolean): Unit
```

Allows the popup window to extend beyond the bounds of the screen. By default the window is clipped to the screen boundaries. Setting this to false will allow windows to be accurately positioned.

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):false if the window should be allowed to extend outside of the screen |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isClippingEnabled()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()> 

### setContentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentView(contentView: View!): Unit
```

Change the popup's content. The content is represented by an instance of [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#).

This method has no effect if called when the popup is showing.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------|
| `contentView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the new content for the popup |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getContentView()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing()> 

### setElevation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setElevation(elevation: Float): Unit
```

Specifies the elevation for this popup window.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------|
| `elevation` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the popup's elevation in pixels |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getElevation()> 

### setEnterTransition

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnterTransition(enterTransition: Transition?): Unit
```

Sets the enter transition to be used when the popup window is shown.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `enterTransition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)?:the enter transition, or`null`to clear |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getEnterTransition()> 

### setEpicenterBounds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEpicenterBounds(bounds: Rect?): Unit
```

Sets the bounds used as the epicenter of the enter and exit transitions.

Transitions use Rect, referred to as the epicenter, to orient the direction of travel. For popup windows, the anchor view bounds are used as the default epicenter.

See [Transition.setEpicenterCallback(EpicenterCallback)](https://developer.android.com/reference/kotlin/android/transition/Transition.html#setEpicenterCallback(android.transition.Transition.EpicenterCallback))for more information about how transition epicenters work.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the epicenter bounds relative to the anchor view, or`null`to use the default epicenter |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getEpicenterBounds()> 

### setExitTransition

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExitTransition(exitTransition: Transition?): Unit
```

Sets the exit transition to be used when the popup window is dismissed.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `exitTransition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)?:the exit transition, or`null`to clear |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getExitTransition()> 

### setFocusable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFocusable(focusable: Boolean): Unit
```

Changes the focusability of the popup window. When focusable, the window will grab the focus from the current focused widget if the popup contains a focusable [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). By default a popup window is not focusable.

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `focusable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the popup should grab focus, false otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isFocusable()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()> 

### setHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHeight(height: Int): Unit
```

Sets the popup's requested height. May be a layout constant such as [LayoutParams.WRAP_CONTENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int) or [LayoutParams.MATCH_PARENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int).

The actual size of the popup may depend on other factors such as clipping and window layout.

If the popup is showing, calling this method will take effect the next time the popup is shown.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup height in pixels or a layout constant |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getHeight()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing()> 

### setIgnoreCheekPress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIgnoreCheekPress(): Unit
```

Set the flag on popup to ignore cheek press events; by default this flag is set to false which means the popup will not ignore cheek press dispatch events.

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()> 

### setInputMethodMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInputMethodMode(mode: Int): Unit
```

Control how the popup operates with an input method: one of [INPUT_METHOD_FROM_FOCUSABLE](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_FROM_FOCUSABLE:kotlin.Int), [INPUT_METHOD_NEEDED](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_NEEDED:kotlin.Int), or [INPUT_METHOD_NOT_NEEDED](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#INPUT_METHOD_NOT_NEEDED:kotlin.Int).

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getInputMethodMode()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()> 

### setIsClippedToScreen

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIsClippedToScreen(enabled: Boolean): Unit
```

Clip this popup window to the screen, but not to the containing window.

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to clip to the screen. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isClippedToScreen()> 

### setIsLaidOutInScreen

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIsLaidOutInScreen(enabled: Boolean): Unit
```

Allows the popup window to force the flag [WindowManager.LayoutParams.FLAG_LAYOUT_IN_SCREEN](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_LAYOUT_IN_SCREEN:kotlin.Int), overriding default behavior. This will cause the popup to be positioned in absolute screen coordinates.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the popup should always be positioned in screen coordinates |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isLaidOutInScreen()> 

### setOnDismissListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDismissListener(onDismissListener: PopupWindow.OnDismissListener!): Unit
```

Sets the listener to be called when the window is dismissed.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `onDismissListener` | [PopupWindow.OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupWindow.OnDismissListener)!:The listener. |

### setOutsideTouchable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOutsideTouchable(touchable: Boolean): Unit
```

Controls whether the pop-up will be informed of touch events outside of its window. This only makes sense for pop-ups that are touchable but not focusable, which means touches outside of the window will be delivered to the window behind. The default is false.

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `touchable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the popup should receive outside touch events, false otherwise |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isOutsideTouchable()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()> 

### setOverlapAnchor

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOverlapAnchor(overlapAnchor: Boolean): Unit
```

Sets whether the popup window should overlap its anchor view when displayed as a drop-down.

If the popup is showing, calling this method will take effect only the next time the popup is shown.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `overlapAnchor` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the popup should overlap its anchor. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getOverlapAnchor()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing()> 

### setSoftInputMode

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSoftInputMode(mode: Int): Unit
```

Sets the operating mode for the soft input area.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired mode, see [android.view.WindowManager.LayoutParams#softInputMode](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#softInputMode:kotlin.Int) for the full list Value is either`0`or a combination of [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_UNSPECIFIED:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_UNCHANGED](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_UNCHANGED:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_HIDDEN](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_HIDDEN:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_ALWAYS_HIDDEN](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_ALWAYS_HIDDEN:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_VISIBLE](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_VISIBLE:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_STATE_ALWAYS_VISIBLE](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_ALWAYS_VISIBLE:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_ADJUST_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_UNSPECIFIED:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_ADJUST_RESIZE](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_RESIZE:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_ADJUST_PAN](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_PAN:kotlin.Int), [android.view.WindowManager.LayoutParams#SOFT_INPUT_ADJUST_NOTHING](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_NOTHING:kotlin.Int), and [android.view.WindowManager.LayoutParams#SOFT_INPUT_IS_FORWARD_NAVIGATION](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_IS_FORWARD_NAVIGATION:kotlin.Int) |

**See Also**

- [android.view.WindowManager.LayoutParams#softInputMode](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#softInputMode:kotlin.Int)
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getSoftInputMode()> 

### setSplitTouchEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSplitTouchEnabled(enabled: Boolean): Unit
```

Allows the popup window to split touches across other windows that also support split touch. When this flag is false, the first pointer that goes down determines the window to which all subsequent touches go until all pointers go up. When this flag is true, each pointer (not necessarily the first) that goes down determines the window to which all subsequent touches of that pointer will go until that pointer goes up thereby enabling touches with multiple pointers to be split across multiple windows.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the split touches should be enabled, false otherwise |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isSplitTouchEnabled()> 

### setTouchInterceptor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTouchInterceptor(l: View.OnTouchListener!): Unit
```

Set a callback for all touch events being dispatched to the popup window. 

### setTouchModal

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTouchModal(touchModal: Boolean): Unit
```

Set whether this window is touch modal or if outside touches will be sent to other windows behind it.

<br />

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `touchModal` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to sent all outside touches to this window, false to other windows behind it |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isTouchModal()> 

### setTouchable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTouchable(touchable: Boolean): Unit
```

Changes the touchability of the popup window. When touchable, the window will receive touch events, otherwise touch events will go to the window below it. By default the window is touchable.

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to one of the [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update())methods.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `touchable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the popup should receive touch events, false otherwise |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isTouchable()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()> 

### setWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWidth(width: Int): Unit
```

Sets the popup's requested width. May be a layout constant such as [LayoutParams.WRAP_CONTENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int) or [LayoutParams.MATCH_PARENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int).

The actual size of the popup may depend on other factors such as clipping and window layout.

If the popup is showing, calling this method will take effect the next time the popup is shown.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup width in pixels or a layout constant |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#getWidth()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#isShowing()> 

### setWindowLayoutMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWindowLayoutMode(
    widthSpec: Int, 
    heightSpec: Int
): Unit
```

**Deprecated:** *Use [setWidth(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setWidth(kotlin.Int))and [setHeight(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setHeight(kotlin.Int)).*

Change the width and height measure specs that are given to the window manager by the popup. By default these are 0, meaning that the current width or height is requested as an explicit size from the window manager. You can supply [ViewGroup.LayoutParams.WRAP_CONTENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int) or [ViewGroup.LayoutParams.MATCH_PARENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int) to have that measure spec supplied instead, replacing the absolute width and height that has been set in the popup.

If the popup is showing, calling this method will take effect only the next time the popup is shown.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `widthSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an explicit width measure spec mode, either [ViewGroup.LayoutParams.WRAP_CONTENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int), [ViewGroup.LayoutParams.MATCH_PARENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int), or 0 to use the absolute width. |
| `heightSpec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an explicit height measure spec mode, either [ViewGroup.LayoutParams.WRAP_CONTENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int), [ViewGroup.LayoutParams.MATCH_PARENT](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int), or 0 to use the absolute height. |

### setWindowLayoutType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWindowLayoutType(layoutType: Int): Unit
```

Set the layout type for this window.

See [WindowManager.LayoutParams.type](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#type:kotlin.Int) for possible values.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------|
| `layoutType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Layout type for this window. |

**See Also**

- [android.view.WindowManager.LayoutParams#type](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#type:kotlin.Int) 

### showAsDropDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun showAsDropDown(anchor: View!): Unit
```

Display the content view in a popup window anchored to the bottom-left corner of the anchor view. If there is not enough room on screen to show the popup in its entirety, this method tries to find a parent scroll view to scroll. If no parent scroll view can be scrolled, the bottom-left corner of the popup is pinned at the top left corner of the anchor view.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the view on which to pin the popup window |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#dismiss()> 

### showAsDropDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun showAsDropDown(
    anchor: View!, 
    xoff: Int, 
    yoff: Int
): Unit
```

Display the content view in a popup window anchored to the bottom-left corner of the anchor view offset by the specified x and y coordinates. If there is not enough room on screen to show the popup in its entirety, this method tries to find a parent scroll view to scroll. If no parent scroll view can be scrolled, the bottom-left corner of the popup is pinned at the top left corner of the anchor view.

If the view later scrolls to move`anchor`to a different location, the popup will be moved correspondingly.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the view on which to pin the popup window |
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A horizontal offset from the anchor in pixels |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A vertical offset from the anchor in pixels |
| --- | --- |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#dismiss()> 

### showAsDropDown

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun showAsDropDown(
    anchor: View!, 
    xoff: Int, 
    yoff: Int, 
    gravity: Int
): Unit
```

Displays the content view in a popup window anchored to the corner of another view. The window is positioned according to the specified gravity and offset by the specified x and y coordinates.

If there is not enough room on screen to show the popup in its entirety, this method tries to find a parent scroll view to scroll. If no parent view can be scrolled, the specified vertical gravity will be ignored and the popup will anchor itself such that it is visible.

If the view later scrolls to move`anchor`to a different location, the popup will be moved correspondingly.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the view on which to pin the popup window |
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A horizontal offset from the anchor in pixels |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A vertical offset from the anchor in pixels |
| --- | --- |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Alignment of the popup relative to the anchor |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupWindow#dismiss()> 

### showAtLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun showAtLocation(
    parent: View!, 
    gravity: Int, 
    x: Int, 
    y: Int
): Unit
```

Display the content view in a popup window at the specified location. If the popup window cannot fit on screen, it will be clipped. See [android.view.WindowManager.LayoutParams](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#) for more information on how gravity and the x and y parameters are related. Specifying a gravity of [android.view.Gravity#NO_GRAVITY](https://developer.android.com/reference/kotlin/android/view/Gravity.html#NO_GRAVITY:kotlin.Int) is similar to specifying`Gravity.LEFT | Gravity.TOP`.
| --- | --- |

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:a parent view to get the [android.view.View#getWindowToken()](https://developer.android.com/reference/kotlin/android/view/View.html#getWindowToken())token from |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the gravity which controls the placement of the popup window |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup's x location offset |
| --- | --- |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the popup's y location offset |

### update

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(): Unit
```

Updates the state of the popup window, if it is currently being displayed, from the currently set state.

This includes:

- [setClippingEnabled(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setClippingEnabled(kotlin.Boolean))
- [setFocusable(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setFocusable(kotlin.Boolean))
- [setIgnoreCheekPress()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setIgnoreCheekPress())
- [setInputMethodMode(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setInputMethodMode(kotlin.Int))
- [setTouchable(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setTouchable(kotlin.Boolean))
- [setAnimationStyle(int)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setAnimationStyle(kotlin.Int))
- [setTouchModal(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setTouchModal(kotlin.Boolean))(boolean)}
- [setIsClippedToScreen(boolean)](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#setIsClippedToScreen(kotlin.Boolean)) 

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    anchor: View!, 
    width: Int, 
    height: Int
): Unit
```

Updates the position and the dimension of the popup window.

Calling this function also updates the window with the current popup state as described for [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the popup's anchor view |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new width in pixels, must be \>= 0 or -1 to ignore |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new height in pixels, must be \>= 0 or -1 to ignore |
| --- | --- |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    anchor: View!, 
    xoff: Int, 
    yoff: Int, 
    width: Int, 
    height: Int
): Unit
```

Updates the position and the dimension of the popup window.

Width and height can be set to -1 to update location only. Calling this function also updates the window with the current popup state as described for [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()).

If the view later scrolls to move`anchor`to a different location, the popup will be moved correspondingly.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the popup's anchor view |
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):x offset from the view's left edge |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):y offset from the view's bottom edge |
| --- | --- |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new width in pixels, must be \>= 0 or -1 to ignore |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new height in pixels, must be \>= 0 or -1 to ignore |

### update

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    width: Int, 
    height: Int
): Unit
```

Updates the dimension of the popup window.

Calling this function also updates the window with the current popup state as described for [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new width in pixels, must be \>= 0 or -1 to ignore |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new height in pixels, must be \>= 0 or -1 to ignore |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    x: Int, 
    y: Int, 
    width: Int, 
    height: Int
): Unit
```

Updates the position and the dimension of the popup window.

Width and height can be set to -1 to update location only. Calling this function also updates the window with the current popup state as described for [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new x location |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new y location |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new width in pixels, must be \>= 0 or -1 to ignore |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new height in pixels, must be \>= 0 or -1 to ignore |

### update

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    x: Int, 
    y: Int, 
    width: Int, 
    height: Int, 
    force: Boolean
): Unit
```

Updates the position and the dimension of the popup window.

Width and height can be set to -1 to update location only. Calling this function also updates the window with the current popup state as described for [update()](https://developer.android.com/reference/kotlin/android/widget/PopupWindow#update()).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new x location |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new y location |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new width in pixels, must be \>= 0 or -1 to ignore |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new height in pixels, must be \>= 0 or -1 to ignore |
| `force` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to reposition the window even if the specified position already seems to correspond to the LayoutParams,`false`to only reposition if needed |
