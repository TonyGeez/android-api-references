# AnimatedStateListDrawable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatedStateListDrawable

Kotlin| [Java](../android/graphics/drawable/AnimatedStateListDrawable.md) 
| --- | --- |

```
open class AnimatedStateListDrawable : StateListDrawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](../android/graphics/drawable/Drawable.md) ||||
| | ↳ | [android.graphics.drawable.DrawableContainer](../android/graphics/drawable/DrawableContainer.md) |||
| | | ↳ | [android.graphics.drawable.StateListDrawable](../android/graphics/drawable/StateListDrawable.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.graphics.drawable.AnimatedStateListDrawable](../android/graphics/drawable/AnimatedStateListDrawable.md) |

Drawable containing a set of Drawable keyframes where the currently displayed keyframe is chosen based on the current state set. Animations between keyframes may optionally be defined using transition elements.

This drawable can be defined in an XML file with the` <animated-selector>`element. Each keyframe Drawable is defined in a nested`<item>`element. Transitions are defined in a nested`<transition>`element.

## Summary

| XML attributes ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`android:state_activated`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. |
| [`android:state_active`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is considered "active" by its host. |
| [`android:state_checkable`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State identifier indicating that the object may display a check mark. |
| --- | --- |
| [`android:state_checked`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State identifier indicating that the object is currently checked. |
| [`android:state_enabled`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view is enabled. |
| [`android:state_first`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is in the first position in an ordered set. |
| --- | --- |
| [`android:state_focused`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view has input focus. |
| [`android:state_last`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is in the last position in an ordered set. |
| [`android:state_middle`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is in the middle position in an ordered set. |
| --- | --- |
| [`android:state_pressed`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when the user is pressing down in a view. |
| [`android:state_selected`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view (or one of its parents) is currently selected. |
| [`android:state_single`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is considered "single" by its host. |
| --- | --- |
| [`android:state_window_focused`](../android/graphics/drawable/AnimatedStateListDrawable.md) | State value for StateListDrawable , set when a view's window has input focus. |

| Inherited XML attributes ||
|---|---|
| From class [StateListDrawable](../android/graphics/drawable/StateListDrawable.md) |---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [android:constantSize](../android/graphics/drawable/StateListDrawable.md) | If true, the drawable's reported internal size will remain constant as the state changes; the size is the maximum of all of the states. If false, the size will vary based on the current state. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_activated](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. This is an alternative representation of state_checked for when the state should be propagated down the view hierarchy. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_active](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is considered "active" by its host. Actual usage may vary between views. Consult the host view documentation for details. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_checkable](../android/graphics/drawable/StateListDrawable.md) | State identifier indicating that the object may display a check mark. See [android.R.attr#state_checked](../android/R.attr.md) for the identifier that indicates whether it is actually checked. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_checked](../android/graphics/drawable/StateListDrawable.md) | State identifier indicating that the object is currently checked. See [android.R.attr#state_checkable](../android/R.attr.md) for an additional identifier that can indicate if any object may ever display a check, regardless of whether state_checked is currently set. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_enabled](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view is enabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_first](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the first position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_focused](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view has input focus. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_last](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the last position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_middle](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the middle position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_pressed](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when the user is pressing down in a view. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_selected](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view (or one of its parents) is currently selected. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_single](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is considered "single" by its host. Actual usage may vary between views. Consult the host view documentation for details. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:state_window_focused](../android/graphics/drawable/StateListDrawable.md) | State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view's window has input focus. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:variablePadding](../android/graphics/drawable/StateListDrawable.md) | If true, allows the drawable's padding to change based on the current state that is selected. If false, the padding will stay the same (based on the maximum padding of all the states). Enabling this feature requires that the owner of the drawable deal with performing layout when the state changes, which is often not supported. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:visible](../android/graphics/drawable/StateListDrawable.md) | Indicates whether the drawable should be initially visible. May be a boolean value, such as "`true`" or "`false`". <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimatedStateListDrawable](../android/graphics/drawable/AnimatedStateListDrawable.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addState](../android/graphics/drawable/AnimatedStateListDrawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`, `drawable:` ` [Drawable](../android/graphics/drawable/Drawable.md)`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a new drawable to the set of keyframes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTransition](../android/graphics/drawable/AnimatedStateListDrawable.md))`(`fromId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `transition:` `T`, `reversible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adds a new transition between keyframes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](../android/graphics/drawable/AnimatedStateListDrawable.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)!`)` Applies the specified theme to this Drawable and its children. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](../android/graphics/drawable/AnimatedStateListDrawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Inflate this Drawable from an XML resource optionally styled by a theme. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](../android/graphics/drawable/AnimatedStateListDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](../android/graphics/drawable/AnimatedStateListDrawable.md))`()` <br /> |
| --- | --- |
| open [Drawable](../android/graphics/drawable/Drawable.md) | [mutate](../android/graphics/drawable/AnimatedStateListDrawable.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](../android/graphics/drawable/AnimatedStateListDrawable.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](../android/graphics/drawable/AnimatedStateListDrawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConstantState](../android/graphics/drawable/AnimatedStateListDrawable.md))`(`state:` ` [DrawableContainer.DrawableContainerState](../android/graphics/drawable/DrawableContainer.DrawableContainerState.md)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [StateListDrawable](../android/graphics/drawable/StateListDrawable.md) |------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addState](../android/graphics/drawable/StateListDrawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `drawable:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` <br /> Add a new image/string ID to the set of images. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findStateDrawableIndex](../android/graphics/drawable/StateListDrawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Gets the index of the drawable with the provided state set. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStateCount](../android/graphics/drawable/StateListDrawable.md))`()` <br /> Gets the number of states contained in this drawable. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [getStateDrawable](../android/graphics/drawable/StateListDrawable.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the drawable at an index. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getStateSet](../android/graphics/drawable/StateListDrawable.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the state set at an index. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](../android/graphics/drawable/StateListDrawable.md))`()` <br /> | ||
| From class [DrawableContainer](../android/graphics/drawable/DrawableContainer.md) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/graphics/drawable/DrawableContainer.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](../android/graphics/drawable/DrawableContainer.md))`()` <br /> Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](../android/graphics/drawable/Drawable.md))or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold. <br /> | | [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | [getConstantState](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [getCurrent](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](../android/graphics/drawable/DrawableContainer.md))`(`outRect:` ` [Rect](../android/graphics/Rect.md)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Insets](../android/graphics/Insets.md) | [getOpticalInsets](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](../android/graphics/drawable/DrawableContainer.md))`(`outline:` ` [Outline](../android/graphics/Outline.md)`)` <br /> Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default [android.view.ViewOutlineProvider](../android/view/ViewOutlineProvider.md) to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](../android/graphics/drawable/DrawableContainer.md))`(`padding:` ` [Rect](../android/graphics/Rect.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateDrawable](../android/graphics/drawable/DrawableContainer.md))`(`who:` ` [Drawable](../android/graphics/drawable/Drawable.md)`)` <br /> Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](../android/graphics/drawable/DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](../android/graphics/drawable/DrawableContainer.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](../android/graphics/drawable/DrawableContainer.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](../android/graphics/drawable/DrawableContainer.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleDrawable](../android/graphics/drawable/DrawableContainer.md))`(`who:` ` [Drawable](../android/graphics/drawable/Drawable.md)`, `what:` ` [Runnable](../java/lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call [android.os.Handler#postAtTime(Runnable, Object, long)](../android/os/Handler.md))with the parameters (what, who, when) to perform the scheduling. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [selectDrawable](../android/graphics/drawable/DrawableContainer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the currently displayed drawable by index. If an invalid index is specified, the current drawable will be set to`null`and the index will be set to`-1`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](../android/graphics/drawable/DrawableContainer.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](../android/graphics/drawable/DrawableContainer.md))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](../android/graphics/drawable/DrawableContainer.md))`(`colorFilter:` ` [ColorFilter](../android/graphics/ColorFilter.md)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](../android/graphics/drawable/DrawableContainer.md))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterFadeDuration](../android/graphics/drawable/DrawableContainer.md))`(`ms:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the global fade duration when a new drawable is entering the scene. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitFadeDuration](../android/graphics/drawable/DrawableContainer.md))`(`ms:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the global fade duration when a new drawable is leaving the scene. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](../android/graphics/drawable/DrawableContainer.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](../android/graphics/drawable/DrawableContainer.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](../android/graphics/drawable/DrawableContainer.md))`(`blendMode:` ` [BlendMode](../android/graphics/BlendMode.md)!`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](../android/graphics/BlendMode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](../android/graphics/drawable/DrawableContainer.md))`(`tint:` ` [ColorStateList](../android/content/res/ColorStateList.md)?`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](../android/graphics/drawable/DrawableContainer.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleDrawable](../android/graphics/drawable/DrawableContainer.md))`(`who:` ` [Drawable](../android/graphics/drawable/Drawable.md)`, `what:` ` [Runnable](../java/lang/Runnable.md)`)` <br /> A Drawable can call this to unschedule an action previously scheduled with [scheduleDrawable](../android/graphics/drawable/Drawable.Callback.md)). An implementation can generally simply call [android.os.Handler#removeCallbacks(Runnable, Object)](../android/os/Handler.md))with the parameters (what, who) to unschedule the drawable. <br /> | ||
| From class [Drawable](../android/graphics/drawable/Drawable.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](../android/graphics/drawable/Drawable.md))`()` <br /> Removes the color filter for this drawable. <br /> | | [Rect](../android/graphics/Rect.md) | [copyBounds](../android/graphics/drawable/Drawable.md))`()` <br /> Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](../android/graphics/drawable/Drawable.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)`)` <br /> Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [createFromPath](../android/graphics/drawable/Drawable.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a drawable from file path name. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [createFromResourceStream](../android/graphics/drawable/Drawable.md))`(`res:` ` [Resources](../android/content/res/Resources.md)?`, `value:` ` [TypedValue](../android/util/TypedValue.md)?`, `is:` ` [InputStream](../java/io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [createFromResourceStream](../android/graphics/drawable/Drawable.md))`(`res:` ` [Resources](../android/content/res/Resources.md)?`, `value:` ` [TypedValue](../android/util/TypedValue.md)?`, `is:` ` [InputStream](../java/io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)? | [createFromStream](../android/graphics/drawable/Drawable.md))`(`is:` ` [InputStream](../java/io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [createFromXml](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`)` <br /> Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [createFromXml](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [createFromXmlInner](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`)` <br /> Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md) | [createFromXmlInner](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from inside an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns`null`if the tag is not a valid drawable. <br /> | | [Rect](../android/graphics/Rect.md) | [getBounds](../android/graphics/drawable/Drawable.md))`()` <br /> Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)? | [getCallback](../android/graphics/drawable/Drawable.md))`()` <br /> Return the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation attached to this Drawable. <br /> | | [ColorFilter](../android/graphics/ColorFilter.md)? | [getColorFilter](../android/graphics/drawable/Drawable.md))`()` <br /> Returns the current color filter, or`null`if none set. <br /> | | [Rect](../android/graphics/Rect.md) | [getDirtyBounds](../android/graphics/drawable/Drawable.md))`()` <br /> Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](../android/graphics/drawable/Drawable.md))`()` <br /> Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](../android/graphics/drawable/Drawable.md))`()` <br /> Retrieve the current level. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](../android/graphics/drawable/Drawable.md))`()` <br /> Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_selected](../android/R.attr.md), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](../android/graphics/Region.md)? | [getTransparentRegion](../android/graphics/drawable/Drawable.md))`()` <br /> Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`)` <br /> Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](../android/graphics/drawable/Drawable.md))`(`r:` ` [Resources](../android/content/res/Resources.md)`, `parser:` ` [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](../android/graphics/drawable/Drawable.md))`()` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](../android/graphics/drawable/Drawable.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](../android/graphics/drawable/Drawable.md))`()` <br /> Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](../android/graphics/RenderNode.md) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](../android/graphics/drawable/Drawable.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](../android/graphics/drawable/Drawable.md))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](../android/graphics/drawable/Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](../android/graphics/drawable/Drawable.md))`(`what:` ` [Runnable](../java/lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](../android/graphics/drawable/Drawable.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](../android/graphics/drawable/Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](../android/graphics/drawable/Drawable.md))`(`cb:` ` [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)?`)` <br /> Bind a [Callback](../android/graphics/drawable/Drawable.Callback.md) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](../android/graphics/drawable/Drawable.md))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](../android/graphics/drawable/Drawable.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` <br /> Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md))which constructs a [PorterDuffColorFilter](../android/graphics/PorterDuffColorFilter.md). **Note:** Setting a color filter disables [tint](../android/graphics/drawable/Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](../android/graphics/drawable/Drawable.md))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](../android/graphics/drawable/Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](../android/graphics/drawable/Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](../android/graphics/drawable/Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](../android/graphics/drawable/Drawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_pressed](../android/R.attr.md)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](../android/graphics/drawable/Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](../android/graphics/drawable/Drawable.md))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](../android/graphics/drawable/Drawable.md)). To clear the tint, pass`null`to [setTintList(android.content.res.ColorStateList)](../android/graphics/drawable/Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](../android/graphics/drawable/Drawable.md))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](../android/graphics/drawable/Drawable.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](../android/graphics/drawable/Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](../android/graphics/drawable/Drawable.md))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](../android/graphics/drawable/Drawable.md))`(`what:` ` [Runnable](../java/lang/Runnable.md)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## XML attributes

### android:state_activated

```
android:state_activated
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. This is an alternative representation of state_checked for when the state should be propagated down the view hierarchy.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_active

```
android:state_active
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is considered "active" by its host. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_checkable

```
android:state_checkable
```
State identifier indicating that the object may display a check mark. See [android.R.attr#state_checked](../android/R.attr.md) for the identifier that indicates whether it is actually checked.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_checked

```
android:state_checked
```
State identifier indicating that the object is currently checked. See [android.R.attr#state_checkable](../android/R.attr.md) for an additional identifier that can indicate if any object may ever display a check, regardless of whether state_checked is currently set.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_enabled

```
android:state_enabled
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view is enabled.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_first

```
android:state_first
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the first position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_focused

```
android:state_focused
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view has input focus.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_last

```
android:state_last
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the last position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_middle

```
android:state_middle
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the middle position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_pressed

```
android:state_pressed
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when the user is pressing down in a view.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_selected

```
android:state_selected
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view (or one of its parents) is currently selected.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_single

```
android:state_single
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is considered "single" by its host. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_window_focused

```
android:state_window_focused
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view's window has input focus.

May be a boolean value, such as "`true`" or "`false`".

## Public constructors

### AnimatedStateListDrawable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnimatedStateListDrawable()
```

## Public methods

### addState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addState(
    stateSet: IntArray, 
    drawable: Drawable, 
    id: Int
): Unit
```

Add a new drawable to the set of keyframes.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stateSet` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):An array of resource IDs to associate with the keyframe This value cannot be`null`. |
| `drawable` | [Drawable](../android/graphics/drawable/Drawable.md):The drawable to show when in the specified state, may not be null |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unique identifier for the keyframe |
| --- | --- |

### addTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T> addTransition(
    fromId: Int, 
    toId: Int, 
    transition: T, 
    reversible: Boolean
): Unit where T : Drawable!, T : Animatable!
```

Adds a new transition between keyframes.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique identifier of the starting keyframe |
| `toId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique identifier of the ending keyframe |
| `transition` | T:An [Animatable](../android/graphics/drawable/Animatable.md) drawable to use as a transition, may not be null |
| --- | --- |
| `reversible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the transition can be reversed |

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyTheme(theme: Resources.Theme!): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `t` | the theme to apply This value cannot be`null`. |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)!:This value may be`null`. |

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
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Resources](../android/content/res/Resources.md):This value cannot be`null`. |
| `parser` | [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md):This value cannot be`null`. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md):This value cannot be`null`. |
| --- | --- |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?:This value may be`null`. |

| Exceptions ||
|-----------------------------------------|---|
| `org.xmlpull.v1.XmlPullParserException` | |
| `java.io.IOException` | |

### isStateful

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStateful(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this drawable changes its appearance based on state, false otherwise. |

### jumpToCurrentState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun jumpToCurrentState(): Unit
```  

### mutate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mutate(): Drawable
```

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------|
| [Drawable](../android/graphics/drawable/Drawable.md) | This drawable. This value cannot be`null`. |

### setVisible

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVisible(
    visible: Boolean, 
    restart: Boolean
): Boolean
```

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true if visible, false if not. |
| `restart` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):You can supply true here to force the drawable to behave as if it has just become visible, even if it had last been set visible. Used for example to force animations to restart. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Returns true if the new visibility is different than its previous state. |

## Protected methods

### onStateChange

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStateChange(stateSet: IntArray): Boolean
```

| Parameters ||
|---------|-----------------------------|
| `state` | This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |

### setConstantState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setConstantState(state: DrawableContainer.DrawableContainerState): Unit
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [DrawableContainer.DrawableContainerState](../android/graphics/drawable/DrawableContainer.DrawableContainerState.md):This value cannot be`null`. |
