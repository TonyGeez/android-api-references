Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StateListDrawable

Kotlin | [Java](StateListDrawable.md)
| --- | --- |

```
open class StateListDrawable : DrawableContainer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](Drawable.md) |||
| | ↳ | [android.graphics.drawable.DrawableContainer](DrawableContainer.md) ||
| | | ↳ | [android.graphics.drawable.StateListDrawable](StateListDrawable.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [AnimatedStateListDrawable](AnimatedStateListDrawable.md) |---|---| | [AnimatedStateListDrawable](AnimatedStateListDrawable.md) | Drawable containing a set of Drawable keyframes where the currently displayed keyframe is chosen based on the current state set. | |
| --- | --- | --- | --- | --- | --- | --- |

Lets you assign a number of graphic images to a single Drawable and swap out the visible item by a string ID value.

<br />

It can be defined in an XML file with the `<selector>` element. Each state Drawable is defined in a nested `<item>` element. For more information, see the guide to [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

## Summary

| XML attributes ||
|---|---|
| [`android:constantSize`](StateListDrawable.md) | If true, the drawable's reported internal size will remain constant as the state changes; the size is the maximum of all of the states. |
| [`android:state_activated`](StateListDrawable.md) | State value for StateListDrawable , set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. |
| [`android:state_active`](StateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is considered "active" by its host. |
| --- | --- |
| [`android:state_checkable`](StateListDrawable.md) | State identifier indicating that the object may display a check mark. |
| [`android:state_checked`](StateListDrawable.md) | State identifier indicating that the object is currently checked. |
| [`android:state_enabled`](StateListDrawable.md) | State value for StateListDrawable , set when a view is enabled. |
| --- | --- |
| [`android:state_first`](StateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is in the first position in an ordered set. |
| [`android:state_focused`](StateListDrawable.md) | State value for StateListDrawable , set when a view has input focus. |
| [`android:state_last`](StateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is in the last position in an ordered set. |
| --- | --- |
| [`android:state_middle`](StateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is in the middle position in an ordered set. |
| [`android:state_pressed`](StateListDrawable.md) | State value for StateListDrawable , set when the user is pressing down in a view. |
| [`android:state_selected`](StateListDrawable.md) | State value for StateListDrawable , set when a view (or one of its parents) is currently selected. |
| --- | --- |
| [`android:state_single`](StateListDrawable.md) | State value for StateListDrawable , set when a view or drawable is considered "single" by its host. |
| [`android:state_window_focused`](StateListDrawable.md) | State value for StateListDrawable , set when a view's window has input focus. |
| [`android:variablePadding`](StateListDrawable.md) | If true, allows the drawable's padding to change based on the current state that is selected. |
| --- | --- |
| [`android:visible`](StateListDrawable.md) | Indicates whether the drawable should be initially visible. |

| Public constructors ||
|---|---|
| StateListDrawable <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addState Add a new image/string ID to the set of images. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | applyTheme Applies the specified theme to this Drawable and its children. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | findStateDrawableIndex Gets the index of the drawable with the provided state set. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStateCount Gets the number of states contained in this drawable. |
| open [Drawable](Drawable.md)? | getStateDrawable Gets the drawable at an index. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | getStateSet Gets the state set at an index. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasFocusStateSpecified Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | inflate Inflate this Drawable from an XML resource optionally styled by a theme. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isStateful Indicates whether this drawable will change its appearance based on state. |
| --- | --- |
| open [Drawable](Drawable.md) | mutate Make this drawable mutable. |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onStateChange Override this in your subclass to change appearance if you recognize the specified state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setConstantState <br /> |

| Inherited functions ||
|---|---|
| From class DrawableContainer |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | canApplyTheme <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | draw Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getAlpha Gets the current alpha value for the drawable. 0 means fully transparent, 255 means fully opaque. This method is implemented by Drawable subclasses and the value returned is specific to how that class treats alpha. The default return value is 255 if the class does not override this method to return a value specific to its use of alpha. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getChangingConfigurations Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through setChangingConfigurations or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState?` | getConstantState Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable. <br /> | | Drawable | getCurrent <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | getHotspotBounds Populates `outRect` with the hotspot bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getIntrinsicHeight Returns the drawable's intrinsic height. Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getIntrinsicWidth Returns the drawable's intrinsic width. Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMinimumHeight Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMinimumWidth Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getOpacity Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`: `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int`. An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT. Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method resolveOpacity to perform a standard reduction of two opacities to the appropriate single output. Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the setAlpha or #setColorFilter methods. Some subclasses, such as BitmapDrawable, ColorDrawable, and GradientDrawable, do account for the value of setAlpha, but the general behavior is dependent upon the implementation of the subclass. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Insets.html#` | getOpticalInsets Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | getOutline Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#` to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getPadding Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invalidateDrawable Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isAutoMirrored Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | jumpToCurrentState If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onBoundsChange Override this in your subclass to change appearance if you vary based on the bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onLayoutDirectionChanged Called when the drawable's resolved layout direction changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onLevelChange Override this in your subclass to change appearance if you vary based on level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | scheduleDrawable A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call postAtTime with the parameters (what, who, when) to perform the scheduling. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | selectDrawable Sets the currently displayed drawable by index. If an invalid index is specified, the current drawable will be set to `null` and the index will be set to `-1`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setAlpha Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setAutoMirrored Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setColorFilter Specify an optional color filter for the drawable. If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas. Pass `null` to remove any existing color filter. **Note:** Setting a non-`null` color filter disables setTintList. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDither Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setEnterFadeDuration Change the global fade duration when a new drawable is entering the scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setExitFadeDuration Change the global fade duration when a new drawable is leaving the scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setHotspot Specifies the hotspot's location within the drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setHotspotBounds Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTintBlendMode Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`. **Note:** Setting a color filter via setColorFilter <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTintList Specifies tint color for this drawable as a color state list. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to setColorFilter. **Note:** Setting a color filter via setColorFilter or setColorFilter overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | setVisible Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unscheduleDrawable A Drawable can call this to unschedule an action previously scheduled with scheduleDrawable. An implementation can generally simply call removeCallbacks with the parameters (what, who) to unschedule the drawable. <br /> | ||
| From class Drawable |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | clearColorFilter Removes the color filter for this drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | copyBounds Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | copyBounds Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | Drawable | createFromPath Create a drawable from file path name. <br /> | | Drawable | createFromResourceStream Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | Drawable | createFromResourceStream Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | Drawable | createFromStream Create a drawable from an inputstream <br /> | | Drawable | createFromXml Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | Drawable | createFromXml Create a drawable from an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | Drawable | createFromXmlInner Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | Drawable | createFromXmlInner Create a drawable from inside an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | getBounds Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?` | getCallback Return the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation attached to this Drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?` | getColorFilter Returns the current color filter, or `null` if none set. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | getDirtyBounds Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getLayoutDirection Returns the resolved layout direction for this Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getLevel Retrieve the current level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | getState Describes the current state, as a union of primitive states, such as `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int`, etc. Some drawables may modify their imagery based on the selected state. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Region.html#?` | getTransparentRegion Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | inflate Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | inflate Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invalidateSelf Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isFilterBitmap <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isProjected Whether this drawable requests projection. Indicates that the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#` this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isVisible <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | resolveOpacity Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing getOpacity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | scheduleSelf Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setBounds Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setBounds Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setCallback Bind a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` object to this Drawable. Required for clients that want to support animated drawables. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setChangingConfigurations Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setColorFilter Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for setColorFilter which constructs a `https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#`. **Note:** Setting a color filter disables setTintList. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFilterBitmap Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | setLayoutDirection Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | setLevel Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling invalidateSelf in order to have itself redrawn, *and* true will be returned from this function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | setState Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \[`https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int`\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling invalidateSelf in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTint Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to setColorFilter. To clear the tint, pass `null` to setTintList. **Note:** Setting a color filter via setColorFilter or setColorFilter overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTintMode Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`. **Note:** Setting a color filter via setColorFilter or setColorFilter overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unscheduleSelf Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

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
State value for StateListDrawable, set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. This is an alternative representation of state_checked for when the state should be propagated down the view hierarchy.

May be a boolean value, such as "`true`" or "`false`".

### android:state_active

```
android:state_active
```
State value for StateListDrawable, set when a view or drawable is considered "active" by its host. Actual usage may vary between views. Consult the host view documentation for details.

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
State value for StateListDrawable, set when a view is enabled.

May be a boolean value, such as "`true`" or "`false`".

### android:state_first

```
android:state_first
```
State value for StateListDrawable, set when a view or drawable is in the first position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_focused

```
android:state_focused
```
State value for StateListDrawable, set when a view has input focus.

May be a boolean value, such as "`true`" or "`false`".

### android:state_last

```
android:state_last
```
State value for StateListDrawable, set when a view or drawable is in the last position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_middle

```
android:state_middle
```
State value for StateListDrawable, set when a view or drawable is in the middle position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_pressed

```
android:state_pressed
```
State value for StateListDrawable, set when the user is pressing down in a view.

May be a boolean value, such as "`true`" or "`false`".

### android:state_selected

```
android:state_selected
```
State value for StateListDrawable, set when a view (or one of its parents) is currently selected.

May be a boolean value, such as "`true`" or "`false`".

### android:state_single

```
android:state_single
```
State value for StateListDrawable, set when a view or drawable is considered "single" by its host. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`".

### android:state_window_focused

```
android:state_window_focused
```
State value for StateListDrawable, set when a view's window has input focus.

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
| `drawable` | [Drawable](Drawable.md)!: The image to show. Note this must be a unique Drawable that is not shared between any other View or Drawable otherwise the results are undefined and can lead to unexpected rendering behavior |

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

- getStateDrawable
- getStateSet

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

- getStateSet
- getStateDrawable

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
| Drawable | The drawable at the index. This value may be `null`. |

**See Also**

- getStateCount
- getStateSet

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

- getStateCount
- getStateDrawable

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFocusStateSpecified(): Boolean
```

Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`.

Note: A View uses a Drawable instance as its background and it changes its appearance based on a state. On keyboard devices, it should specify its `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` to make sure the user knows which view is holding the focus.

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
| `r` | [Resources](../android.content.res/Resources.md): Resources used to resolve attribute values. This value cannot be `null`. |
| `parser` | [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md): XML parser from which to inflate this Drawable. This value cannot be `null`. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md): Base set of attribute values. This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: Theme to apply, may be null |

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
| Drawable | This drawable. This value cannot be `null`. |

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
| `state` | [DrawableContainer.DrawableContainerState](../android/graphics/drawable/DrawableContainer.DrawableContainerState.md): This value cannot be `null`. |
