Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StateListDrawable

Kotlin | [Java](https://developer.android.com/reference/android/graphics/drawable/StateListDrawable "View this page in Java")
| --- | --- |

```
open class StateListDrawable : DrawableContainer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) |||
| | ↳ | [android.graphics.drawable.DrawableContainer](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer) ||
| | | ↳ | [android.graphics.drawable.StateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [AnimatedStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedStateListDrawable) |---|---| | [AnimatedStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedStateListDrawable) | Drawable containing a set of Drawable keyframes where the currently displayed keyframe is chosen based on the current state set. | |
| --- | --- | --- | --- | --- | --- | --- |

Lets you assign a number of graphic images to a single Drawable and swap out the visible item by a string ID value.

<br />

It can be defined in an XML file with the `<selector>` element. Each state Drawable is defined in a nested `<item>` element. For more information, see the guide to [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

## Summary

| XML attributes ||
|---|---|
| [`android:constantSize`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | If true, the drawable's reported internal size will remain constant as the state changes; the size is the maximum of all of the states. |
| [`android:state_activated`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. |
| [`android:state_active`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view or drawable is considered "active" by its host. |
| --- | --- |
| [`android:state_checkable`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State identifier indicating that the object may display a check mark. |
| [`android:state_checked`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State identifier indicating that the object is currently checked. |
| [`android:state_enabled`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view is enabled. |
| --- | --- |
| [`android:state_first`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view or drawable is in the first position in an ordered set. |
| [`android:state_focused`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view has input focus. |
| [`android:state_last`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view or drawable is in the last position in an ordered set. |
| --- | --- |
| [`android:state_middle`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view or drawable is in the middle position in an ordered set. |
| [`android:state_pressed`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when the user is pressing down in a view. |
| [`android:state_selected`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view (or one of its parents) is currently selected. |
| --- | --- |
| [`android:state_single`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view or drawable is considered "single" by its host. |
| [`android:state_window_focused`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | State value for StateListDrawable , set when a view's window has input focus. |
| [`android:variablePadding`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | If true, allows the drawable's padding to change based on the current state that is selected. |
| --- | --- |
| [`android:visible`](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#attr_StateListDrawable) | Indicates whether the drawable should be initially visible. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#StateListDrawable()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#addState(kotlin.IntArray,%20android.graphics.drawable.Drawable)(stateSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!)` Add a new image/string ID to the set of images. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#applyTheme(android.content.res.Resources.Theme)(theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)` Applies the specified theme to this Drawable and its children. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#findStateDrawableIndex(kotlin.IntArray)(stateSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Gets the index of the drawable with the provided state set. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateCount()()` Gets the number of states contained in this drawable. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateDrawable(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the drawable at an index. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateSet(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the state set at an index. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#hasFocusStateSpecified()()` Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Inflate this Drawable from an XML resource optionally styled by a theme. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#isStateful()()` Indicates whether this drawable will change its appearance based on state. |
| --- | --- |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#mutate()()` Make this drawable mutable. |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#onStateChange(kotlin.IntArray)(stateSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Override this in your subclass to change appearance if you recognize the specified state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#setConstantState(android.graphics.drawable.DrawableContainer.DrawableContainerState)(state: https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer.DrawableContainerState)` <br /> |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#canApplyTheme()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#draw(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)` Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getAlpha()()` Gets the current alpha value for the drawable. 0 means fully transparent, 255 means fully opaque. This method is implemented by Drawable subclasses and the value returned is specific to how that class treats alpha. The default return value is 255 if the class does not override this method to return a value specific to its use of alpha. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getChangingConfigurations()()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)` or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getConstantState()()` Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getCurrent()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getHotspotBounds(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Populates `outRect` with the hotspot bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getIntrinsicHeight()()` Returns the drawable's intrinsic height. Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getIntrinsicWidth()()` Returns the drawable's intrinsic width. Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getMinimumHeight()()` Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getMinimumWidth()()` Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getOpacity()()` Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`: `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int`. An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT. Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)` to perform a standard reduction of two opacities to the appropriate single output. Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)` or #setColorFilter methods. Some subclasses, such as `https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable`, `https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable`, and `https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable`, do account for the value of `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)`, but the general behavior is dependent upon the implementation of the subclass. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Insets.html#` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getOpticalInsets()()` Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getOutline(android.graphics.Outline)(outline: https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)` Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#` to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#getPadding(android.graphics.Rect)(padding: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#invalidateDrawable(android.graphics.drawable.Drawable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)` Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#isAutoMirrored()()` Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#jumpToCurrentState()()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#onBoundsChange(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Override this in your subclass to change appearance if you vary based on the bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#onLayoutDirectionChanged(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the drawable's resolved layout direction changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#onLevelChange(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Override this in your subclass to change appearance if you vary based on level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable, what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call `https://developer.android.com/reference/kotlin/android/os/Handler.html#postAtTime(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long)` with the parameters (what, who, when) to perform the scheduling. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#selectDrawable(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the currently displayed drawable by index. If an invalid index is specified, the current drawable will be set to `null` and the index will be set to `-1`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setAlpha(kotlin.Int)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setAutoMirrored(kotlin.Boolean)(mirrored: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setColorFilter(android.graphics.ColorFilter)(colorFilter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?)` Specify an optional color filter for the drawable. If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas. Pass `null` to remove any existing color filter. **Note:** Setting a non-`null` color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setDither(kotlin.Boolean)(dither: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setEnterFadeDuration(kotlin.Int)(ms: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Change the global fade duration when a new drawable is entering the scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setExitFadeDuration(kotlin.Int)(ms: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Change the global fade duration when a new drawable is leaving the scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setHotspot(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Specifies the hotspot's location within the drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setTintBlendMode(android.graphics.BlendMode)(blendMode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#!)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`. **Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setTintList(android.content.res.ColorStateList)(tint: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?)` Specifies tint color for this drawable as a color state list. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`. **Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#setVisible(kotlin.Boolean,%20kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, restart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer#unscheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable, what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` A Drawable can call this to unschedule an action previously scheduled with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)`. An implementation can generally simply call `https://developer.android.com/reference/kotlin/android/os/Handler.html#removeCallbacks(java.lang.Runnable,%20kotlin.Any)` with the parameters (what, who) to unschedule the drawable. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter()()` Removes the color filter for this drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds()()` Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String)(pathName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Create a drawable from file path name. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#?, value: https://developer.android.com/reference/kotlin/android/util/TypedValue.html#?, is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#?, value: https://developer.android.com/reference/kotlin/android/util/TypedValue.html#?, is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, opts: https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#?)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String)(is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Create a drawable from an inputstream <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)` Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Create a drawable from an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)` Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Create a drawable from inside an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds()()` Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback()()` Return the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation attached to this Drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getColorFilter()()` Returns the current color filter, or `null` if none set. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds()()` Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection()()` Returns the resolved layout direction for this Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel()()` Retrieve the current level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState()()` Describes the current state, as a union of primitive states, such as `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int`, etc. Some drawables may modify their imagery based on the selected state. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Region.html#?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getTransparentRegion()()` Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)` Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()()` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isFilterBitmap()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isProjected()()` Whether this drawable requests projection. Indicates that the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#` this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)(op1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, op2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long)(what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback)(cb: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?)` Bind a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` object to this Drawable. Required for clients that want to support animated drawables. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)(configs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)` Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` which constructs a `https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#`. **Note:** Setting a color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setFilterBitmap(kotlin.Boolean)(filter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()` in order to have itself redrawn, *and* true will be returned from this function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray)(stateSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \[`https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int`\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()` in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int)(tintColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`. To clear the tint, pass `null` to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`. **Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode)(tintMode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`. **Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable)(what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## XML attributes

### android:constantSize

```
android:constantSize
```
If true, the drawable's reported internal size will remain constant as the state changes; the size is the maximum of all of the states. If false, the size will vary based on the current state.

May be a boolean value, such as "`true`" or "`false`".

### android:state_activated

```
android:state_activated
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. This is an alternative representation of state_checked for when the state should be propagated down the view hierarchy.

May be a boolean value, such as "`true`" or "`false`".

### android:state_active

```
android:state_active
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view or drawable is considered "active" by its host. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_checkable

```
android:state_checkable
```
State identifier indicating that the object may display a check mark. See `https://developer.android.com/reference/kotlin/android/R.attr.html#state_checked:kotlin.Int` for the identifier that indicates whether it is actually checked.

May be a boolean value, such as "`true`" or "`false`".

### android:state_checked

```
android:state_checked
```
State identifier indicating that the object is currently checked. See `https://developer.android.com/reference/kotlin/android/R.attr.html#state_checkable:kotlin.Int` for an additional identifier that can indicate if any object may ever display a check, regardless of whether state_checked is currently set.

May be a boolean value, such as "`true`" or "`false`".

### android:state_enabled

```
android:state_enabled
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view is enabled.

May be a boolean value, such as "`true`" or "`false`".

### android:state_first

```
android:state_first
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view or drawable is in the first position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_focused

```
android:state_focused
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view has input focus.

May be a boolean value, such as "`true`" or "`false`".

### android:state_last

```
android:state_last
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view or drawable is in the last position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_middle

```
android:state_middle
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view or drawable is in the middle position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_pressed

```
android:state_pressed
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when the user is pressing down in a view.

May be a boolean value, such as "`true`" or "`false`".

### android:state_selected

```
android:state_selected
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view (or one of its parents) is currently selected.

May be a boolean value, such as "`true`" or "`false`".

### android:state_single

```
android:state_single
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view or drawable is considered "single" by its host. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_window_focused

```
android:state_window_focused
```
State value for `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#`, set when a view's window has input focus.

May be a boolean value, such as "`true`" or "`false`".

### android:variablePadding

```
android:variablePadding
```
If true, allows the drawable's padding to change based on the current state that is selected. If false, the padding will stay the same (based on the maximum padding of all the states). Enabling this feature requires that the owner of the drawable deal with performing layout when the state changes, which is often not supported.

May be a boolean value, such as "`true`" or "`false`".

### android:visible

```
android:visible
```
Indicates whether the drawable should be initially visible.

May be a boolean value, such as "`true`" or "`false`".

## Public constructors

### StateListDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StateListDrawable()
```

## Public methods

### addState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addState(
    stateSet: IntArray!, 
    drawable: Drawable!
): Unit
```

Add a new image/string ID to the set of images.

| Parameters ||
|---|---|
| `stateSet` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: An array of resource Ids to associate with the image. Switch to this image by calling setState(). |
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)!: The image to show. Note this must be a unique Drawable that is not shared between any other View or Drawable otherwise the results are undefined and can lead to unexpected rendering behavior |

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyTheme(theme: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|---|---|
| `t` | the theme to apply. This value cannot be `null`. |

### findStateDrawableIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findStateDrawableIndex(stateSet: IntArray): Int
```

Gets the index of the drawable with the provided state set.

| Parameters ||
|---|---|
| `stateSet` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the state set to look up. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the provided state set, or -1 if not found |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateDrawable(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateSet(kotlin.Int)`

### getStateCount

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStateCount(): Int
```

Gets the number of states contained in this drawable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of states contained in this drawable. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateSet(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateDrawable(kotlin.Int)`

### getStateDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStateDrawable(index: Int): Drawable?
```

Gets the drawable at an index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the drawable. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | The drawable at the index. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateCount()`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateSet(kotlin.Int)`

### getStateSet

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStateSet(index: Int): IntArray
```

Gets the state set at an index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the state set. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | The state set at the index. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateCount()`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable#getStateDrawable(kotlin.Int)`

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFocusStateSpecified(): Boolean
```

Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`.

Note: A View uses a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` instance as its background and it changes its appearance based on a state. On keyboard devices, it should specify its `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` to make sure the user knows which view is holding the focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` is specified for this drawable. |

### inflate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun inflate(
    r: Resources, 
    parser: XmlPullParser, 
    attrs: AttributeSet, 
    theme: Resources.Theme?
): Unit
```

Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource.

| Parameters ||
|---|---|
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): Resources used to resolve attribute values. This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): XML parser from which to inflate this Drawable. This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): Base set of attribute values. This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: Theme to apply, may be null |

| Exceptions ||
|---|---|
| `java.io.IOException` | |
| `org.xmlpull.v1.XmlPullParserException` | |

### isStateful

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStateful(): Boolean
```

Indicates whether this drawable will change its appearance based on state. Clients can use this to determine whether it is necessary to calculate their state and call setState.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this drawable changes its appearance based on state, false otherwise. |

### mutate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mutate(): Drawable
```

Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | This drawable. This value cannot be `null`. |

## Protected methods

### onStateChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onStateChange(stateSet: IntArray): Boolean
```

Override this in your subclass to change appearance if you recognize the specified state.

| Parameters ||
|---|---|
| `state` | This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |

### setConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setConstantState(state: DrawableContainer.DrawableContainerState): Unit
```

| Parameters ||
|---|---|
| `state` | [DrawableContainer.DrawableContainerState](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer.DrawableContainerState): This value cannot be `null`. |
