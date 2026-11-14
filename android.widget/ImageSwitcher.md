Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImageSwitcher

```
open class ImageSwitcher : ViewSwitcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [android.view.View](../android.view/View.md) ||||||
| | ↳ | [android.view.ViewGroup](../android.view/ViewGroup.md) |||||
| | | ↳ | [android.widget.FrameLayout](FrameLayout.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.widget.ViewAnimator](ViewAnimator.md) |||
| | | | | ↳ | [android.widget.ViewSwitcher](ViewSwitcher.md) ||
| | | | | | ↳ | [android.widget.ImageSwitcher](ImageSwitcher.md) |
| --- | --- | --- | --- | --- | --- | --- |

ViewSwitcher that switches between two ImageViews when a new image is set on it. The views added to an ImageSwitcher must all be ImageView.

## Summary

Inherited XML attributes From class FrameLayout attr_FrameLayout Determines whether to measure all children or just those in the VISIBLE or INVISIBLE state when measuring. Defaults to false.

May be a boolean value, such as "`true`" or "`false`".

<br />

From class `https://developer.android.com/reference/kotlin/android/view/View.html#` attr_View Whether or not this view is a heading for accessibility purposes.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Whether or not allow clicks on disabled view.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View alpha property of the view, as a value between 0 (completely transparent) and 1 (completely opaque).

May be a floating point value, such as "`1.2`".

<br />

attr_View A drawable to use as the background. This can be either a reference to a full drawable resource (such as a PNG image, 9-patch, XML state list description, etc), or a solid color such as "#ff000000" (black).

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

<br />

attr_View Defines whether this view reacts to click events.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View

Whether the View's Outline should be used to clip the contents of the View.

Only a single non-rectangular clip can be applied on a View at any time. Circular clips from a android.view.ViewAnimationUtils#createCircularReveal(View,int,int,float,float) circular reveal animation take priority over Outline clipping, and child Outline clipping takes priority over Outline clipping done by a parent.

Note that this flag will only be respected if the View's Outline returns true from canClip.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Defines text that briefly describes content of the view. This property is used primarily for accessibility. Since some views do not have textual representation this attribute can be used for providing such.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

<br />

attr_View Defines the quality of translucent drawing caches. This property is used only when the drawing cache is enabled and translucent. The default value is auto. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

Must be one of the following constant values.
Constant Value Description auto 0 Lets the framework decide what quality level should be used for the drawing cache. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. high 2 High quality. When set to high quality, the drawing cache uses a higher color depth but uses more memory. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11. low 1 Low quality. When set to low quality, the drawing cache uses a lower color depth, thus losing precision in rendering gradients, but uses less memory. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

<br />

attr_View When this attribute is set to true, the view gets its drawable state (focused, pressed, etc.) from its direct parent rather than from itself.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Defines whether to fade out scrollbars when they are not in use.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Defines the length of the fading edges.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Specifies whether to filter touches when the view's window is obscured by another visible window. When set to true, the view will not receive touches whenever a toast, dialog or other window appears above the view's window. Refer to the `https://developer.android.com/reference/kotlin/android/view/View.html#` security documentation for more details.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Boolean internal attribute to adjust view layout based on system windows such as the status bar. If true, adjusts the padding of this view to leave space for the system windows. Will only take effect if this view is in a non-embedded activity.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Controls whether a view can take focus. By default, this is "auto" which lets the framework determine whether a user can move focus to a view. By setting this attribute to true the view is allowed to take focus. By setting it to "false" the view will not take focus. This value does not impact the behavior of directly calling android.view.View#requestFocus, which will always request focus regardless of this view. It only impacts where focus navigation will try to move focus.

May be a boolean value, such as "`true`" or "`false`".

Must be one of the following constant values.
Constant Value Description auto 10

<br />

attr_View Boolean that controls whether a view can take focus while in touch mode. If this is true for a view, that view can gain focus when clicked on, and can keep focus if another view is clicked on that doesn't have this attribute set to true.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Whether this view is a default-focus view. Only one view per keyboard navigation cluster can have this attribute set to true. See setFocusedByDefault.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Boolean that controls whether a view should have haptic feedback enabled for events such as long presses.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Supply an identifier name for this view, to later retrieve it with findViewById or findViewById. This must be a resource reference; typically you set this using the `@+` syntax to create a new ID resources. For example: `android:id="@+id/my_id"` which allows you to later retrieve the view with `findViewById(R.id.my_id)`.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Set this if the view will serve as a scrolling container, meaning that it can be resized to shrink its overall window so that there will be space for an input method. If not set, the default value will be true if "scrollbars" has the vertical scrollbar set, else it will be false.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Controls whether the view's window should keep the screen on while visible.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Whether this view is a root of a keyboard navigation cluster. See setKeyboardNavigationCluster.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Specifies the type of layer backing this view. The default value is none. Refer to setLayerType for more information.

Must be one of the following constant values.
Constant Value Description hardware 2 Use a hardware layer. Refer to setLayerType for more information. none 0 Don't use a layer. software 1 Use a software layer. Refer to setLayerType for more information.

<br />

attr_View Defines the direction of layout drawing. This typically is associated with writing direction of the language script used. The possible values are "ltr" for Left-to-Right, "rtl" for Right-to-Left, "locale", and "inherit" from parent view. If there is nothing to inherit, "locale" is used. "locale" falls back to "en-US". "ltr" is the direction used in "en-US". The default for this attribute is "inherit".

Must be one of the following constant values.
Constant Value Description inherit 2 Inherit from parent. locale 3 Locale. ltr 0 Left-to-Right. rtl 1 Right-to-Left.

<br />

attr_View Defines whether this view reacts to long click events.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Defines the minimum height of the view. It is not guaranteed the view will be able to achieve this minimum height (for example, if its parent layout constrains it with less available height).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Defines the minimum width of the view. It is not guaranteed the view will be able to achieve this minimum width (for example, if its parent layout constrains it with less available width).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Defines the next keyboard navigation cluster. If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_DOWN:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_LEFT:kotlin.Int`. If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_RIGHT:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Defines the next view to give focus to when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_UP:kotlin.Int` If the reference refers to a view that does not exist or is part of a hierarchy that is invisible, a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will result when the reference is accessed.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Name of the method in this View's context to invoke when the view is clicked. This name must correspond to a public method that takes exactly one parameter of type View. For instance, if you specify `android:onClick="sayHello"`, you must declare a `public void sayHello(View v)` method of your context (typically, your Activity).
attr_View Sets the color of the ambient shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final ambient shadow is a function of the shadow caster height, the alpha channel of the outlineAmbientShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#ambientShadowAlpha:kotlin.Int` theme attribute.

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

<br />

attr_View Sets the color of the spot shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final spot shadow is a function of the shadow caster height, the alpha channel of the outlineSpotShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#spotShadowAlpha:kotlin.Int` theme attribute.

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

<br />

attr_View Sets the padding, in pixels, of all four edges. Padding is defined as space between the edges of the view and the view's content. This value will take precedence over any of the edge-specific values (paddingLeft, paddingTop, paddingRight, paddingBottom, paddingHorizontal and paddingVertical), but will not override paddingStart or paddingEnd, if set. A view's size will include its padding. If a `https://developer.android.com/reference/kotlin/android/R.attr.html#background:kotlin.Int` is provided, the padding will initially be set to that (0 if the drawable does not have padding). Explicitly setting a padding value will override the corresponding padding found in the background.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Sets the padding, in pixels, of the bottom edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Sets the padding, in pixels, of the end edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Sets the padding, in pixels, of the left and right edges; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`. This value will take precedence over paddingLeft and paddingRight, but not paddingStart or paddingEnd (if set).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Sets the padding, in pixels, of the left edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Sets the padding, in pixels, of the right edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Sets the padding, in pixels, of the start edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Sets the padding, in pixels, of the top edge; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Sets the padding, in pixels, of the top and bottom edges; see `https://developer.android.com/reference/kotlin/android/R.attr.html#padding:kotlin.Int`. This value will take precedence over paddingTop and paddingBottom, if set.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Defines which edges should be faded on scrolling.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |
Constant Value Description horizontal 1000 Fades horizontal edges only. none 0 No edge is faded. vertical 2000 Fades vertical edges only.

<br />

attr_View rotation of the view, in degrees.

May be a floating point value, such as "`1.2`".

<br />

attr_View rotation of the view around the x axis, in degrees.

May be a floating point value, such as "`1.2`".

<br />

attr_View rotation of the view around the y axis, in degrees.

May be a floating point value, such as "`1.2`".

<br />

attr_View If false, no state will be saved for this view when it is being frozen. The default is true, allowing the view to be saved (however it also must have an ID assigned to it for its state to be saved). Setting this to false only disables the state for this view, not for its children which may still be saved.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View scale of the view in the x direction.

May be a floating point value, such as "`1.2`".

<br />

attr_View scale of the view in the y direction.

May be a floating point value, such as "`1.2`".

<br />

attr_View The initial horizontal scroll offset, in pixels.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View The initial vertical scroll offset, in pixels.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Defines whether the horizontal scrollbar track should always be drawn.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Defines whether the vertical scrollbar track should always be drawn.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Defines the delay in milliseconds that a scrollbar waits before fade out.

May be an integer value, such as "`100`".

<br />

attr_View Defines the delay in milliseconds that a scrollbar takes to fade out.

May be an integer value, such as "`100`".

<br />

attr_View Sets the width of vertical scrollbars and height of horizontal scrollbars.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Controls the scrollbar style and position. The scrollbars can be overlaid or inset. When inset, they add to the padding of the view. And the scrollbars can be drawn inside the padding area or on the edge of the view. For example, if a view has a background drawable and you want to draw the scrollbars inside the padding specified by the drawable, you can use insideOverlay or insideInset. If you want them to appear at the edge of the view, ignoring the padding, then you can use outsideOverlay or outsideInset.

Must be one of the following constant values.
Constant Value Description insideInset 1000000 Inside the padding and inset. insideOverlay 0 Inside the padding and overlaid. outsideInset 3000000 Edge of the view and inset. outsideOverlay 2000000 Edge of the view and overlaid.

<br />

attr_View Defines the horizontal scrollbar thumb drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Defines the vertical scrollbar thumb drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Defines the horizontal scrollbar track drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Defines the vertical scrollbar track drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Defines which scrollbars should be displayed on scrolling or not.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |
Constant Value Description horizontal 100 Displays horizontal scrollbar only. none 0 No scrollbar is displayed. vertical 200 Displays vertical scrollbar only.

<br />

attr_View Boolean that controls whether a view should have sound effects enabled for events such as clicking and touching.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_View Sets the state-based animator for the View.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View Supply a tag for this view containing a String, to be retrieved later with android.view.View#getTag or searched for with findViewWithTag. It is generally preferable to use IDs (through the android:id attribute) instead of tags because they are faster and allow for compile-time type checking.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

<br />

attr_View Defines the alignment of the text.

May be an integer value, such as "`100`".

Must be one of the following constant values.
Constant Value Description center 4 Center the paragraph, for example: ALIGN_CENTER. gravity 1 Default for the root view. The gravity determines the alignment, ALIGN_NORMAL, ALIGN_CENTER, or ALIGN_OPPOSITE, which are relative to each paragraph's text direction. inherit 0 Default. textEnd 3 Align to the end of the paragraph, for example: ALIGN_OPPOSITE. textStart 2 Align to the start of the paragraph, for example: ALIGN_NORMAL. viewEnd 6 Align to the end of the view, which is ALIGN_RIGHT if the view's resolved layoutDirection is LTR, and ALIGN_LEFT otherwise. viewStart 5 Align to the start of the view, which is ALIGN_LEFT if the view's resolved layoutDirection is LTR, and ALIGN_RIGHT otherwise.

<br />

attr_View Defines the direction of the text.

May be an integer value, such as "`100`".

Must be one of the following constant values.
Constant Value Description anyRtl 2 The paragraph direction is RTL if it contains any strong RTL character, otherwise it is LTR if it contains any strong LTR characters. If there are neither, the paragraph direction is the view's resolved layout direction. firstStrong 1 Default for the root view. The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is the view's resolved layout direction. firstStrongLtr 6 The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is LTR. firstStrongRtl 7 The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is RTL. inherit 0 Default. locale 5 The paragraph direction is coming from the system Locale. ltr 3 The paragraph direction is left to right. rtl 4 The paragraph direction is right to left.

<br />

attr_View Specifies a theme override for a view. When a theme override is set, the view will be inflated using a `https://developer.android.com/reference/kotlin/android/content/Context.html#` themed with the specified resource. During XML inflation, any child views under the view with a theme override will inherit the themed context.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_View x location of the pivot point around which the view will rotate and scale. This xml attribute sets the pivotX property of the View.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View y location of the pivot point around which the view will rotate and scale. This xml attribute sets the pivotY property of the View.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Names a View such that it can be identified for Transitions. Names should be unique in the View hierarchy.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

<br />

attr_View translation in x of the view. This value is added post-layout to the left property of the view, which is set by its layout.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View translation in y of the view. This value is added post-layout to the top property of the view, which is set by its layout.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View translation in z of the view. This value is added to its elevation.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

attr_View Controls the initial visibility of the view.

Must be one of the following constant values.
Constant Value Description gone 2 Completely hidden, as if the view had not been added. invisible 1 Not displayed, but taken into account during layout (space is left for it). visible 0 Visible on screen; the default value.

<br />

From class ViewAnimator attr_ViewAnimator Defines whether to animate the current View when the ViewAnimation is first displayed.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_ViewAnimator Identifier for the animation to use when a view is shown.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_ViewAnimator Identifier for the animation to use when a view is hidden.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

From class `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` attr_ViewGroup Sets whether this ViewGroup's drawable states also include its children's drawable states. This is used, for example, to make a group appear to be focused when its child EditText or button is focused.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_ViewGroup Defines whether the ViewGroup should always draw its children using their drawing cache or not. The default value is true. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_ViewGroup Defines whether changes in layout (caused by adding and removing items) should cause a LayoutTransition to run. When this flag is set to true, a default LayoutTransition object will be set on the ViewGroup container and default animations will run when these layout changes occur.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_ViewGroup Defines whether layout animations should create a drawing cache for their children. Enabling the animation cache consumes more memory and requires a longer initialization but provides better performance. The animation cache is enabled by default.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_ViewGroup Defines whether a child is limited to draw inside of its bounds or not. This is useful with animations that scale the size of the children to more than 100% for instance. In such a case, this property should be set to false to allow the children to draw outside of their bounds. The default value of this property is true.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_ViewGroup Defines whether the ViewGroup will clip its children and resize (but not clip) any EdgeEffect to its padding, if padding is not zero. This property is set to true by default.

May be a boolean value, such as "`true`" or "`false`".

<br />

attr_ViewGroup Defines the relationship between the ViewGroup and its descendants when looking for a View to take focus.

Must be one of the following constant values.
Constant Value Description afterDescendants 1 The ViewGroup will get focus only if none of its descendants want it. beforeDescendants 0 The ViewGroup will get focus before any of its descendants. blocksDescendants 2 The ViewGroup will block its descendants from receiving focus.

<br />

attr_ViewGroup Defines the layout animation to use the first time the ViewGroup is laid out. Layout animations can also be started manually after the first layout.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

attr_ViewGroup Defines the layout mode of this ViewGroup.

Must be one of the following constant values.
Constant Value Description clipBounds 0 Use the children's clip bounds when laying out this container. opticalBounds 1 Use the children's optical bounds when laying out this container.

<br />

attr_ViewGroup Defines the persistence of the drawing cache. The drawing cache might be enabled by a ViewGroup for all its children in specific situations (for instance during a scrolling.) This property lets you persist the cache in memory after its initial usage. Persisting the cache consumes more memory but may prevent frequent garbage collection if the cache is created over and over again. By default the persistence is set to scrolling. Deprecated: The view drawing cache was largely made obsolete with the introduction of hardware-accelerated rendering in API 11.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |
Constant Value Description all 3 The drawing cache is always persisted. animation 1 The drawing cache is persisted after a layout animation. none 0 The drawing cache is not persisted after use. scrolling 2 The drawing cache is persisted after a scroll.

<br />

attr_ViewGroup Sets whether this ViewGroup should split MotionEvents to separate child views during touch event dispatch. If false (default prior to HONEYCOMB), touch events will be dispatched to the child view where the first pointer went down until the last pointer goes up. If true (default for HONEYCOMB and later), touch events may be dispatched to multiple children. MotionEvents for each pointer will be dispatched to the child view where the initial ACTION_DOWN event happened. See setMotionEventSplittingEnabled for more information.

May be a boolean value, such as "`true`" or "`false`".

<br />

Inherited constants From class `https://developer.android.com/reference/kotlin/android/view/View.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_DATA_SENSITIVE_AUTO:kotlin.Int`

Automatically determine whether the view should only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true.

Accessibility interactions from services without `isAccessibilityTool` set to true are disallowed for any of the following conditions:
- this view sets getFilterTouchesWhenObscured.
- any parent of this view returns true from isAccessibilityDataSensitive.

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_DATA_SENSITIVE_NO:kotlin.Int`

Allow interactions from all `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s, regardless of their isAccessibilityTool property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_DATA_SENSITIVE_YES:kotlin.Int`

Only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int`

Live region mode specifying that accessibility services should immediately notify users of changes to this view. For example, a screen reader may interrupt ongoing speech to immediately announce these changes.

Use with setAccessibilityLiveRegion.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int`

Live region mode specifying that accessibility services should not automatically announce changes to this view. This is the default live region mode for most views.

Use with setAccessibilityLiveRegion.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int`

Live region mode specifying that accessibility services should notify users of changes to this view.

Use with setAccessibilityLiveRegion.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int`

Flag requesting you to add views that are marked as not important for autofill (see setImportantForAutofill) to a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String`

Hint indicating that this view can be autofilled with a credit card expiration date.

It should be used when the credit card expiration date is represented by just one view; if it is represented by more than one (for example, one view for the month and another view for the year), then each of these views should use the hint specific for the unit (`https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String`).

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE}`).

When annotating a view with this hint, it's recommended to use a date autofill value to avoid ambiguity when the autofill service provides a value for it. To understand why a value can be ambiguous, consider "April of 2020", which could be represented as either of the following options:

- `"04/2020"`
- `"4/2020"`
- `"2020/04"`
- `"2020/4"`
- `"April/2020"`
- `"Apr/2020"`

You define a date autofill value for the view by overriding the following methods:

1. getAutofillType to return `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_DATE:kotlin.Int`.
2. getAutofillValue to return a forDate.
3. autofill to expect a data autofillvalue.

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`

Hint indicating that this view can be autofilled with a credit card expiration day.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String`

Hint indicating that this view can be autofilled with a credit card expiration month.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH}`).

When annotating a view with this hint, it's recommended to use a text autofill value whose value is the numerical representation of the month, starting on `1` to avoid ambiguity when the autofill service provides a value for it. To understand why a value can be ambiguous, consider "January", which could be represented as either of

- `"1"`: recommended way.
- `"0"`: if following the `https://developer.android.com/reference/kotlin/java/util/Calendar.html#MONTH:kotlin.Int` convention.
- `"January"`: full name, in English.
- `"jan"`: abbreviated name, in English.
- `"Janeiro"`: full name, in another language.

Another recommended approach is to use a date autofill value - see `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String` for more details.

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String`

Hint indicating that this view can be autofilled with a credit card expiration year.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String`

Hint indicating that this view can be autofilled with a credit card number.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_NUMBER}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String`

Hint indicating that this view can be autofilled with a credit card security code.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_EMAIL_ADDRESS:kotlin.String`

Hint indicating that this view can be autofilled with an email address.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_EMAIL_ADDRESS}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_NAME:kotlin.String`

Hint indicating that this view can be autofilled with a user's real name.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_NAME}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_PASSWORD:kotlin.String`

Hint indicating that this view can be autofilled with a password.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_PASSWORD}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_PHONE:kotlin.String`

Hint indicating that this view can be autofilled with a phone number.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_PHONE}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_POSTAL_ADDRESS:kotlin.String`

Hint indicating that this view can be autofilled with a postal address.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_POSTAL_ADDRESS}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_POSTAL_CODE:kotlin.String`

Hint indicating that this view can be autofilled with a postal code.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_POSTAL_CODE}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_USERNAME:kotlin.String`

Hint indicating that this view can be autofilled with a username.

Can be used with either setAutofillHints or [`android:autofillHint`](../android.view/View.md) (in which case the value should be `{@value #AUTOFILL_HINT_USERNAME}`).

See setAutofillHints for more info about autofill hints.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_DATE:kotlin.Int`

Autofill type for a field that contains a date, which is represented by a long representing the number of milliseconds since the standard base time known as "the epoch", namely January 1, 1970, 00:00:00 GMT (see getTime.

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` instances for autofilling a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be obtained through forDate, and the values passed to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be fetched through getDateValue.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_LIST:kotlin.Int`

Autofill type for a selection list field, which is filled by an `int` representing the element index inside the list (starting at `0`).

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` instances for autofilling a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be obtained through forList, and the value passed to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be fetched through getListValue.

The available options in the selection list are typically provided by getAutofillOptions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_NONE:kotlin.Int`

Autofill type for views that cannot be autofilled.

Typically used when the view is read-only; for example, a text label.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_TEXT:kotlin.Int`

Autofill type for a text field, which is filled by a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#`.

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` instances for autofilling a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be obtained through forText, and the value passed to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be fetched through getTextValue.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_TOGGLE:kotlin.Int`

Autofill type for a togglable field, which is filled by a `boolean`.

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` instances for autofilling a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be obtained through forToggle, and the value passed to autofill a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be fetched through getToggleValue.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#CONTENT_SENSITIVITY_AUTO:kotlin.Int`

Content sensitivity is determined by the framework. The framework uses a heuristic to determine if this view displays sensitive content. Autofill hints i.e. getAutofillHints are used in the heuristic to determine if this view should be considered as a sensitive view.

`https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_USERNAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_PASSWORD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String` are considered sensitive hints by the framework, and the list may include more hints in the future.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_SECURE:kotlin.Int` to the window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#CONTENT_SENSITIVITY_NOT_SENSITIVE:kotlin.Int`

The view doesn't display sensitive content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#CONTENT_SENSITIVITY_SENSITIVE:kotlin.Int`

The view displays sensitive content.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_SECURE:kotlin.Int` to the window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_ACCESSIBILITY_ACTION:kotlin.Int`

Flag indicating that the drag was initiated with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.html#ACTION_DRAG_START:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`. When startDragAndDrop is called, this is used by the system to perform a drag without animations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL:kotlin.Int`

Flag indicating that a drag can cross window boundaries. When startDragAndDrop is called with this flag set, all visible applications with targetSdkVersion \>= `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` will be able to participate in the drag operation and receive the dragged content.

Global drags require a valid non-null `https://developer.android.com/reference/kotlin/android/content/ClipData.html#`.

If this is the only flag set, then the drag recipient will only have access to text data and intents contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object. Access to URIs contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` is determined by other DRAG_FLAG_GLOBAL_\* flags

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_PERSISTABLE_URI_PERMISSION:kotlin.Int`

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`, the URI permission grant can be persisted across device reboots until explicitly revoked with revokeUriPermission Context.revokeUriPermission}.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_PREFIX_URI_PERMISSION:kotlin.Int`

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`, the URI permission grant applies to any URI that is a prefix match against the original granted URI.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_SAME_APPLICATION:kotlin.Int`

Flag indicating that a drag can cross window boundaries (within the same application). When startDragAndDrop is called with this flag set, only visible windows belonging to the same application (ie. share the same UID) with targetSdkVersion \>= `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` will be able to participate in the drag operation and receive the dragged content. If both DRAG_FLAG_GLOBAL_SAME_APPLICATION and DRAG_FLAG_GLOBAL are set, then DRAG_FLAG_GLOBAL_SAME_APPLICATION takes precedence and the drag will only go to visible windows from the same application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_URI_READ:kotlin.Int`

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL:kotlin.Int`, the drag recipient will be able to request read access to the content URI(s) contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL_URI_WRITE:kotlin.Int`

When this flag is used with `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_GLOBAL:kotlin.Int`, the drag recipient will be able to request write access to the content URI(s) contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_HIDE_CALLING_TASK_ON_DRAG_START:kotlin.Int`

Flag indicating that this drag will result in the caller activity's task to be hidden for the duration of the drag, which means that the source activity will not receive drag events for the current drag gesture. Only the current `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#` may use this flag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_OPAQUE:kotlin.Int`

Flag indicating that the drag shadow will be opaque. When startDragAndDrop is called with this flag set, the drag shadow will be opaque, otherwise, it will be semitransparent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAG_FLAG_START_INTENT_SENDER_ON_UNHANDLED_DRAG:kotlin.Int`

Flag indicating that an unhandled drag should be delegated to the system to be started if no visible window wishes to handle the drop. When using this flag, the caller must provide ClipData with an Item that contains an immutable IntentSender to an activity to be launched (not a broadcast, service, etc). See setIntentSender. The system can decide to launch the intent or not based on factors like the current screen size or windowing mode. If the system does not launch the intent, it will be canceled via the normal drag and drop flow.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAWING_CACHE_QUALITY_AUTO:kotlin.Int`

Enables automatic quality mode for the drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAWING_CACHE_QUALITY_HIGH:kotlin.Int`

Enables high quality mode for the drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#DRAWING_CACHE_QUALITY_LOW:kotlin.Int`

Enables low quality mode for the drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int`

Find find views that contain the specified content description.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FIND_VIEWS_WITH_TEXT:kotlin.Int`

Find views that render the specified text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSABLE:kotlin.Int`

This view wants keystrokes.

Use with setFocusable and [`android:focusable`.](../android.view/View.md)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSABLES_ALL:kotlin.Int`

View flag indicating whether addFocusables should add all focusable Views regardless if they are focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSABLES_TOUCH_MODE:kotlin.Int`

View flag indicating whether addFocusables should add only Views focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSABLE_AUTO:kotlin.Int`

This view determines focusability automatically. This is the default.

Use with setFocusable and [`android:focusable`.](../android.view/View.md)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_BACKWARD:kotlin.Int`

Use with focusSearch. Move focus to the previous selectable item.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_DOWN:kotlin.Int`

Use with focusSearch. Move focus down.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_FORWARD:kotlin.Int`

Use with focusSearch. Move focus to the next selectable item.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_LEFT:kotlin.Int`

Use with focusSearch. Move focus to the left.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_RIGHT:kotlin.Int`

Use with focusSearch. Move focus to the right.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_UP:kotlin.Int`

Use with focusSearch. Move focus up.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#GONE:kotlin.Int`

This view is invisible, and it doesn't take any space for layout purposes. Use with setVisibility and [`android:visibility`.](../android.view/View.md)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#HAPTIC_FEEDBACK_ENABLED:kotlin.Int`

View flag indicating whether this view should have haptic feedback enabled for events such as long presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int`

Automatically determine whether a view is important for accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int`

The view is not important for accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`

The view is not important for accessibility, nor are any of its descendant views.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int`

The view is important for accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`

Automatically determine whether a view is important for autofill.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`

The view is not important for autofill, but its children (if any) will be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`

The view is not important for autofill, and its children (if any) will not be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int`

The view is important for autofill, and its children (if any) will be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`

The view is important for autofill, but its children (if any) will not be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int`

Automatically determine whether a view is important for content capture.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int`

The view is not important for content capture, but its children (if any) will be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_CONTENT_CAPTURE_NO_EXCLUDE_DESCENDANTS:kotlin.Int`

The view is not important for content capture, and its children (if any) will not be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int`

The view is important for content capture, and its children (if any) will be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_CONTENT_CAPTURE_YES_EXCLUDE_DESCENDANTS:kotlin.Int`

The view is important for content capture, but its children (if any) will not be traversed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`

This view is invisible, but it still takes up space for layout purposes. Use with setVisibility and [`android:visibility`.](../android.view/View.md)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#KEEP_SCREEN_ON:kotlin.Int`

View flag indicating that the screen should remain on while the window containing this view is visible to the user. This effectively takes care of automatically setting the WindowManager's `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_KEEP_SCREEN_ON:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int`

Indicates that the view has a hardware layer. A hardware layer is backed by a hardware specific texture (generally Frame Buffer Objects or FBO on OpenGL hardware) and causes the view to be rendered using Android's hardware rendering pipeline, but only if hardware acceleration is turned on for the view hierarchy. When hardware acceleration is turned off, hardware layers behave exactly as `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_SOFTWARE:kotlin.Int`.

A hardware layer is useful to apply a specific color filter and/or blending mode and/or translucency to a view and all its children.

A hardware layer can be used to cache a complex view tree into a texture and reduce the complexity of drawing operations. For instance, when animating a complex view tree with a translation, a hardware layer can be used to render the view tree only once.

A hardware layer can also be used to increase the rendering quality when rotation transformations are applied on a view. It can also be used to prevent potential clipping issues when applying 3D transforms on a view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_NONE:kotlin.Int`

Indicates that the view does not have a layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_SOFTWARE:kotlin.Int`

Indicates that the view has a software layer. A software layer is backed by a bitmap and causes the view to be rendered using Android's software rendering pipeline, even if hardware acceleration is enabled.

Software layers have various usages:

When the application is not using hardware acceleration, a software layer is useful to apply a specific color filter and/or blending mode and/or translucency to a view and all its children.

When the application is using hardware acceleration, a software layer is useful to render drawing primitives not supported by the hardware accelerated pipeline. It can also be used to cache a complex view tree into a texture and reduce the complexity of drawing operations. For instance, when animating a complex view tree with a translation, a software layer can be used to render the view tree only once.

Software layers should be avoided when the affected view tree updates often. Every update will require to re-render the software layer, which can potentially be slow (particularly when hardware acceleration is turned on since the layer will have to be uploaded into a hardware texture after every update.)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_INHERIT:kotlin.Int`

Horizontal layout direction of this view is inherited from its parent. Use with setLayoutDirection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LOCALE:kotlin.Int`

Horizontal layout direction of this view is from deduced from the default language script for the locale. Use with setLayoutDirection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int`

Horizontal layout direction of this view is from Left to Right. Use with setLayoutDirection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int`

Horizontal layout direction of this view is from Right to Left. Use with setLayoutDirection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_HEIGHT_STATE_SHIFT:kotlin.Int`

Bit shift of `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_STATE_MASK:kotlin.Int` to get to the height bits for functions that combine both width and height into a single int, such as getMeasuredState and the childState argument of resolveSizeAndState.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_SIZE_MASK:kotlin.Int`

Bits of getMeasuredWidthAndState and getMeasuredWidthAndState that provide the actual measured size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_STATE_MASK:kotlin.Int`

Bits of getMeasuredWidthAndState and getMeasuredWidthAndState that provide the additional state bits.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_STATE_TOO_SMALL:kotlin.Int`

Bit of getMeasuredWidthAndState and getMeasuredWidthAndState that indicates the measured size is smaller that the space the view would like to have.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#NOT_FOCUSABLE:kotlin.Int`

This view does not want keystrokes.

Use with setFocusable and [`android:focusable`.](../android.view/View.md)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int`

Used to mark a View that has no ID.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_ALWAYS:kotlin.Int`

Always allow a user to over-scroll this view, provided it is a view that can scroll.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int`

Allow a user to over-scroll this view only if the content is large enough to meaningfully scroll, provided it is a view that can scroll.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_NEVER:kotlin.Int`

Never allow a user to over-scroll this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#POINTER_CAPTURE_MODE_ABSOLUTE:kotlin.Int`

A pointer capture mode in which touchpads report absolute finger locations.

In this capture mode, no attempt is made to recognize gestures from touchpad input. Instead, the absolute location of each touch on the pad is reported directly to the View, in the same way that other touches on devices with `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int` are reported.

Events will be delivered with the source `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TOUCHPAD:kotlin.Int`. The absolute position of each touch will be available through getX and getY, and their relative movements through `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_RELATIVE_X:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_RELATIVE_Y:kotlin.Int`. If the touchpad supports them, touch dimension information may be available through the `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_PRESSURE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_TOUCH_MAJOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_TOUCH_MINOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_TOOL_MAJOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_TOOL_MINOR:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_ORIENTATION:kotlin.Int` axes.

Events from mice are always reported in the same way regardless of capture mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int`

A pointer capture mode in which touchpad gestures are recognized and reported like mouse movements.

In this capture mode, the following gestures made on a captured touchpad will be recognized and reported:

- Pointer movement gestures (such as moving a single finger on the pad) will be reported like mouse movements, with the `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_MOVE:kotlin.Int` action and their relative position changes available through android.view.MotionEvent#getX and android.view.MotionEvent#getY.
- Scrolling gestures (such as two-finger swipes) will be reported like scroll wheel movements on a mouse, with the `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_SCROLL:kotlin.Int` action and the scroll amounts available through the `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_VSCROLL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#AXIS_HSCROLL:kotlin.Int` axes.

Motion values are proportional to the physical motion of the gesturing finger(s), and the physical movement in mm can be found using the resolution reported by getResolution for the relevant axis.

These events will be reported with `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_MOUSE_RELATIVE:kotlin.Int`.

Events from mice are always reported in the same way regardless of capture mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#POINTER_CAPTURE_MODE_UNCAPTURED:kotlin.Int`

A "pointer capture mode" in which the pointer is not captured.

Passing this to requestPointerCapture is equivalent to calling releasePointerCapture.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int`

Represents that the user interaction that is requesting a rectangle on screen is doing so because the View has input/keyboard focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int`

Represents that the user interaction that is requesting a rectangle on screen is doing so only to scroll the View on screen, and the rectangle is not associated with a text cursor or keyboard focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int`

Represents that the user interaction that is requesting a rectangle on screen is doing so because the View contains a text cursor (caret).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED:kotlin.Int`

Represents that the user interaction that is requesting a rectangle on screen is doing so via the original requestRectangleOnScreen or requestRectangleOnScreen APIs that do not define the source. RECTANGLE_ON_SCREEN_REQUEST_SOURCE_UNDEFINED should be reserved for backward compatibility and should only be provided from calls to the original API.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#REQUESTED_FRAME_RATE_CATEGORY_DEFAULT:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#REQUESTED_FRAME_RATE_CATEGORY_HIGH:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#REQUESTED_FRAME_RATE_CATEGORY_LOW:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#REQUESTED_FRAME_RATE_CATEGORY_NORMAL:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE:kotlin.Float`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCREEN_STATE_OFF:kotlin.Int`

Indicates that the screen has changed state and is now off.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCREEN_STATE_ON:kotlin.Int`

Indicates that the screen has changed state and is now on.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBARS_INSIDE_INSET:kotlin.Int`

The scrollbar style to display the scrollbars inside the padded area, increasing the padding of the view. The scrollbars will not overlap the content area of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBARS_INSIDE_OVERLAY:kotlin.Int`

The scrollbar style to display the scrollbars inside the content area, without increasing the padding. The scrollbars will be overlaid with translucency on the view's content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBARS_OUTSIDE_INSET:kotlin.Int`

The scrollbar style to display the scrollbars at the edge of the view, increasing the padding of the view. The scrollbars will only overlap the background, if any.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBARS_OUTSIDE_OVERLAY:kotlin.Int`

The scrollbar style to display the scrollbars at the edge of the view, without increasing the padding. The scrollbars will be overlaid with translucency.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBAR_POSITION_DEFAULT:kotlin.Int`

Position the scroll bar at the default position as determined by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBAR_POSITION_LEFT:kotlin.Int`

Position the scroll bar along the left edge.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBAR_POSITION_RIGHT:kotlin.Int`

Position the scroll bar along the right edge.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_AXIS_HORIZONTAL:kotlin.Int`

Indicates scrolling along the horizontal axis.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_AXIS_NONE:kotlin.Int`

Indicates no axis of view scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_AXIS_VERTICAL:kotlin.Int`

Indicates scrolling along the vertical axis.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_AUTO:kotlin.Int`

The content of this view will be considered for scroll capture if scrolling is possible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int`

Explicitly exclude this view as a potential scroll capture target. The system will not consider it. Mutually exclusive with `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int`, which this flag takes precedence over.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_EXCLUDE_DESCENDANTS:kotlin.Int`

Explicitly exclude all children of this view as potential scroll capture targets. This view is unaffected. Note: Excluded children are not considered, regardless of `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int`

Explicitly include this view as a potential scroll capture target. When locating a scroll capture target, this view will be prioritized before others without this flag. Mutually exclusive with `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int`, which takes precedence.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_INDICATOR_BOTTOM:kotlin.Int`

Scroll indicator direction for the bottom edge of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_INDICATOR_END:kotlin.Int`

Scroll indicator direction for the ending edge of the view.

Resolved according to the view's layout direction, see getLayoutDirection for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_INDICATOR_LEFT:kotlin.Int`

Scroll indicator direction for the left edge of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_INDICATOR_RIGHT:kotlin.Int`

Scroll indicator direction for the right edge of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_INDICATOR_START:kotlin.Int`

Scroll indicator direction for the starting edge of the view.

Resolved according to the view's layout direction, see getLayoutDirection for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_INDICATOR_TOP:kotlin.Int`

Scroll indicator direction for the top edge of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SOUND_EFFECTS_ENABLED:kotlin.Int`

View flag indicating whether this view should have sound effects enabled for events such as clicking and touching.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#STATUS_BAR_HIDDEN:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#STATUS_BAR_VISIBLE:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`

Flag for setSystemUiVisibility: View has requested to go into the normal fullscreen mode so that its content can take over the screen while still allowing the user to interact with the application.

This has the same visual effect as `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_FULLSCREEN:kotlin.Int`, meaning that non-critical screen decorations (such as the status bar) will be hidden while the user is in the View's window, focusing the experience on that content. Unlike the window flag, if you are using ActionBar in overlay mode with `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, then enabling this flag will also hide the action bar.

This approach to going fullscreen is best used over the window flag when it is a transient state -- that is, the application does this at certain points in its user interaction where it wants to allow the user to focus on content, but not as a continuous state. For situations where the application would like to simply stay full screen the entire time (such as a game that wants to take over the screen), the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_FULLSCREEN:kotlin.Int` is usually a better approach. The state set here will be removed by the system in various situations (such as the user moving to another application) like the other system UI states.

When using this flag, the application should provide some easy facility for the user to go out of it. A common example would be in an e-book reader, where tapping on the screen brings back whatever screen and UI decorations that had been hidden while the user was immersed in reading the book.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`

Flag for setSystemUiVisibility: View has requested that the system navigation be temporarily hidden.

This is an even less obtrusive state than that called for by `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int`; on devices that draw essential navigation controls (Home, Back, and the like) on screen, `SYSTEM_UI_FLAG_HIDE_NAVIGATION` will cause those to disappear. This is useful (in conjunction with the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_LAYOUT_IN_SCREEN:kotlin.Int` window flags) for displaying content using every last pixel on the display.

There is a limitation: because navigation controls are so important, the least user interaction will cause them to reappear immediately. When this happens, both this flag and `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` will be cleared automatically, so that both elements reappear at the same time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_IMMERSIVE:kotlin.Int`

Flag for setSystemUiVisibility: View would like to remain interactive when hiding the navigation bar with `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. If this flag is not set, `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` will be force cleared by the system on any user interaction.

Since this flag is a modifier for `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, it only has an effect when used in combination with that flag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int`

Flag for setSystemUiVisibility: View would like to remain interactive when hiding the status bar with `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and/or hiding the navigation bar with `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. Use this flag to create an immersive experience while also hiding the system bars. If this flag is not set, `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` will be force cleared by the system on any user interaction, and `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` will be force-cleared by the system if the user swipes from the top of the screen.

When system bars are hidden in immersive mode, they can be revealed temporarily with system gestures, such as swiping from the top of the screen. These transient system bars will overlay app's content, may have some degree of transparency, and will automatically hide after a short timeout.

Since this flag is a modifier for `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, it only has an effect when used in combination with one or both of those flags.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int`

Flag for setSystemUiVisibility: View would like its window to be laid out as if it has requested `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`, even if it currently hasn't. This allows it to avoid artifacts when switching in and out of that mode, at the expense that some of its user interface may be covered by screen decorations when they are shown. You can perform layout of your inner UI elements to account for non-fullscreen system UI through the fitSystemWindows method.

Note: on displays that have a `https://developer.android.com/reference/kotlin/android/view/DisplayCutout.html#`, the window may still be placed differently than if `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` was set, if the window's `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#layoutInDisplayCutoutMode:kotlin.Int` is `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#LAYOUT_IN_DISPLAY_CUTOUT_MODE_DEFAULT:kotlin.Int`. To avoid this, use either of the other modes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int`

Flag for setSystemUiVisibility: View would like its window to be laid out as if it has requested `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`, even if it currently hasn't. This allows it to avoid artifacts when switching in and out of that mode, at the expense that some of its user interface may be covered by screen decorations when they are shown. You can perform layout of your inner UI elements to account for the navigation system UI through the fitSystemWindows method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int`

Flag for setSystemUiVisibility: When using other layout flags, we would like a stable view of the content insets given to fitSystemWindows. This means that the insets seen there will always represent the worst case that the application can expect as a continuous state. In the stock Android UI this is the space for the system bar, nav bar, and status bar, but not more transient elements such as an input method. The stable layout your UI sees is based on the system UI modes you can switch to. That is, if you specify `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` then you will get a stable layout for changes of the `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` mode; if you specify `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int`, then you can transition to `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int` with a stable layout. (Note that you should avoid using `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int` by itself.) If you have set the window flag `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_FULLSCREEN:kotlin.Int` to hide the status bar (instead of using `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`), then a hidden status bar will be considered a "stable" state for purposes here. This allows your UI to continually hide the status bar, while still using the system UI flags to hide the action bar while still retaining a stable layout. Note that changing the window fullscreen flag will never provide a stable layout for a clean transition.

If you are using ActionBar in overlay mode with `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, this flag will also impact the insets it adds to those given to the application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LIGHT_NAVIGATION_BAR:kotlin.Int`

Flag for setSystemUiVisibility: Requests the navigation bar to draw in a mode that is compatible with light navigation bar backgrounds.

For this to take effect, the window must request `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` but not `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_TRANSLUCENT_NAVIGATION:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LIGHT_STATUS_BAR:kotlin.Int`

Flag for setSystemUiVisibility: Requests the status bar to draw in a mode that is compatible with light status bar backgrounds.

For this to take effect, the window must request `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS:kotlin.Int` but not `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_TRANSLUCENT_STATUS:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int`

Flag for setSystemUiVisibility: View has requested the system UI to enter an unobtrusive "low profile" mode.

This is for use in games, book readers, video players, or any other "immersive" application where the usual system chrome is deemed too distracting.

In low profile mode, the status bar and/or navigation icons may dim.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_VISIBLE:kotlin.Int`

Special constant for setSystemUiVisibility: View has requested the system UI (status bar) to be visible (the default).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_LAYOUT_FLAGS:kotlin.Int`

Flags that can impact the layout in relation to system UI.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_ALIGNMENT_CENTER:kotlin.Int`

Center the paragraph, e.g. ALIGN_CENTER. Use with setTextAlignment

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_ALIGNMENT_GRAVITY:kotlin.Int`

Default for the root view. The gravity determines the text alignment, ALIGN_NORMAL, ALIGN_CENTER, or ALIGN_OPPOSITE, which are relative to each paragraph's text direction. Use with setTextAlignment

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_ALIGNMENT_INHERIT:kotlin.Int`

Default text alignment. The text alignment of this View is inherited from its parent. Use with setTextAlignment

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_ALIGNMENT_TEXT_END:kotlin.Int`

Align to the end of the paragraph, e.g. ALIGN_OPPOSITE. Use with setTextAlignment

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_ALIGNMENT_TEXT_START:kotlin.Int`

Align to the start of the paragraph, e.g. ALIGN_NORMAL. Use with setTextAlignment

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_ALIGNMENT_VIEW_END:kotlin.Int`

Align to the end of the view, which is ALIGN_RIGHT if the view's resolved layoutDirection is LTR, and ALIGN_LEFT otherwise. Use with setTextAlignment

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_ALIGNMENT_VIEW_START:kotlin.Int`

Align to the start of the view, which is ALIGN_LEFT if the view's resolved layoutDirection is LTR, and ALIGN_RIGHT otherwise. Use with setTextAlignment

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_ANY_RTL:kotlin.Int`

Text direction is using "any-RTL" algorithm. The paragraph direction is RTL if it contains any strong RTL character, otherwise it is LTR if it contains any strong LTR characters. If there are neither, the paragraph direction is the view's resolved layout direction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_FIRST_STRONG:kotlin.Int`

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is the view's resolved layout direction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_FIRST_STRONG_LTR:kotlin.Int`

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is LTR.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_FIRST_STRONG_RTL:kotlin.Int`

Text direction is using "first strong algorithm". The first strong directional character determines the paragraph direction. If there is no strong directional character, the paragraph direction is RTL.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_INHERIT:kotlin.Int`

Text direction is inherited through `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_LOCALE:kotlin.Int`

Text direction is coming from the system Locale.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_LTR:kotlin.Int`

Text direction is forced to LTR.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#TEXT_DIRECTION_RTL:kotlin.Int`

Text direction is forced to RTL.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#VIEW_LOG_TAG:kotlin.String`

The logging tag used by this class with android.util.Log.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int`

This view is visible. Use with setVisibility and [`android:visibility`.](../android.view/View.md)

<br />

From class `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#CLIP_TO_PADDING_MASK:kotlin.Int`

We clip to padding when FLAG_CLIP_TO_PADDING and FLAG_PADDING_NOT_NULL are set at the same time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#FOCUS_AFTER_DESCENDANTS:kotlin.Int`

This view will get focus only if none of its descendants want it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#FOCUS_BEFORE_DESCENDANTS:kotlin.Int`

This view will get focus before any of its descendants.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#FOCUS_BLOCK_DESCENDANTS:kotlin.Int`

This view will block any of its descendants from getting focus, even if they are focusable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int`

This constant is a setLayoutMode. Clip bounds are the raw values of getLeft, getTop, getRight and getBottom.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#LAYOUT_MODE_OPTICAL_BOUNDS:kotlin.Int`

This constant is a setLayoutMode. Optical bounds describe where a widget appears to be. They sit inside the clip bounds which need to cover a larger area to allow other effects, such as shadows and glows, to be drawn.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#PERSISTENT_ALL_CACHES:kotlin.Int`

Used to indicate that all drawing caches should be kept in memory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#PERSISTENT_ANIMATION_CACHE:kotlin.Int`

Used to indicate that the animation drawing cache should be kept in memory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#PERSISTENT_NO_CACHE:kotlin.Int`

Used to indicate that no drawing cache should be kept in memory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#PERSISTENT_SCROLLING_CACHE:kotlin.Int`

Used to indicate that the scrolling drawing cache should be kept in memory.

<br />

| Public constructors ||
|---|---|
| ImageSwitcher Creates a new empty ImageSwitcher. |
| ImageSwitcher Creates a new empty ImageSwitcher for the given context and with the specified set attributes. |

| Public methods ||
|---|---|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getAccessibilityClassName Return the class name of this object to be used for accessibility purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImageDrawable Sets a new drawable on the ImageSwitcher. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImageResource Sets a new image on the ImageSwitcher with the given resource id. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImageURI Sets a new image on the ImageSwitcher with the given Uri. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addChildrenForAccessibility

Adds the children of this View relevant for accessibility to the given list as output. Since some Views are not important for accessibility the added child views are not necessarily direct children of this view, rather they are the first level of descendants important for accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addExtraDataToAccessibilityNodeInfo

Adds extra data to an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#` based on an explicit request for the additional data.

This method only needs overloading if the node is marked as having extra data available.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addFocusables

Adds any focusable views that are descendants of this view (possibly including this view if it is focusable itself) to views. This method adds all focusable views regardless if we are in touch mode or only views focusable in touch mode if we are in touch mode or only views that can take accessibility focus if accessibility is enabled depending on the focusable mode parameter.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addKeyboardNavigationClusters

Adds any keyboard navigation cluster roots that are descendants of this view (possibly including this view if it is a cluster root itself) to views.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` addStatesFromChildren

Returns whether this ViewGroup's drawable states also include its children's drawable states. This is used, for example, to make a group appear to be focused when its child EditText or button is focused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addTouchables

Add any touchable views that are descendants of this view (possibly including this view if it is touchable itself) to views.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addView

Adds a child view. If no layout parameters are already set on the child, the default parameters for this ViewGroup are set on the child.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addView

Adds a child view with the specified layout parameters.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addView

Adds a child view. If no layout parameters are already set on the child, the default parameters for this ViewGroup are set on the child.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addView

Adds a child view with the specified layout parameters.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addView

Adds a child view with this ViewGroup's default layout parameters and the specified width and height.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` addViewInLayout

Adds a view during layout. This is useful if in your onLayout() method, you need to add more views (as does the list view for example). If index is negative, it means put it at the end of the list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` addViewInLayout

Adds a view during layout. This is useful if in your onLayout() method, you need to add more views (as does the list view for example). If index is negative, it means put it at the end of the list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` attachLayoutAnimationParameters

Subclasses should override this method to set layout animation parameters on the supplied child.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` attachViewToParent

Attaches a view to this view group. Attaching a view assigns this group as the parent, sets the layout parameters and puts the view in the list of children so that it can be retrieved by calling getChildAt.

This method is intended to be lightweight and makes no assumptions about whether the parent or child should be redrawn. Proper use of this method will include also making any appropriate #requestLayout() or invalidate calls. For example, callers can post a `https://developer.android.com/reference/kotlin/java/lang/Runnable.html#` which performs a #requestLayout() on the next frame, after all detach/attach calls are finished, causing layout to be run prior to redrawing the view hierarchy.

This method should be called only for views which were detached from their parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` bringChildToFront

Change the z order of the child so it's on top of all other children. This ordering change may affect layout, if this container uses an order-dependent layout scheme (e.g., LinearLayout). Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int` this method should be followed by calls to requestLayout and invalidate on this parent to force the parent to redraw with the new child ordering.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` canAnimate

Indicates whether the view group has the ability to animate its children after the first layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` childDrawableStateChanged

If addStatesFromChildren is true, refreshes this group's drawable state (to include the states from its children).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` childHasTransientStateChanged

Called when a child view has changed whether or not it is tracking transient state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` cleanupLayoutState

Prevents the specified child to be laid out during the next layout pass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` clearChildFocus

Called when a child of this parent is giving up focus

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` clearDisappearingChildren

Removes any pending animations for views that have been removed. Call this if you don't want animations for exiting views to stack up.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` clearFocus

Called when this view wants to give up focus. If focus is cleared onFocusChanged is called.

**Note:** When not in touch-mode, the framework will try to give focus to the first focusable View from the top after focus is cleared. Hence, if this View is the first from the top that can take focus, then all callbacks related to clearing focus will be invoked after which the framework will give focus to this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` debug

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` detachAllViewsFromParent

Detaches all views from the parent. Detaching a view should be followed either by a call to attachViewToParent or a call to removeDetachedView. Detachment should only be temporary; reattachment or removal should happen within the same drawing cycle as detachment. When a view is detached, its parent is null and cannot be retrieved by a call to getChildAt.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` detachViewFromParent

Detaches a view from its parent. Detaching a view should be followed either by a call to attachViewToParent or a call to removeDetachedView. Detachment should only be temporary; reattachment or removal should happen within the same drawing cycle as detachment. When a view is detached, its parent is null and cannot be retrieved by a call to getChildAt.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` detachViewFromParent

Detaches a view from its parent. Detaching a view should be followed either by a call to attachViewToParent or a call to removeDetachedView. Detachment should only be temporary; reattachment or removal should happen within the same drawing cycle as detachment. When a view is detached, its parent is null and cannot be retrieved by a call to getChildAt.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` detachViewsFromParent

Detaches a range of views from their parents. Detaching a view should be followed either by a call to attachViewToParent or a call to removeDetachedView. Detachment should only be temporary; reattachment or removal should happen within the same drawing cycle as detachment. When a view is detached, its parent is null and cannot be retrieved by a call to getChildAt.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#!` dispatchApplyWindowInsets

Request to apply the given window insets to this view or another view in its subtree.

This method should be called by clients wishing to apply insets corresponding to areas obscured by window decorations or overlays. This can include the status and navigation bars, action bars, input methods and more. New inset categories may be added in the future. The method returns the insets provided minus any that were applied by this view or its children.

Clients wishing to provide custom behavior should override the onApplyWindowInsets method or alternatively provide a `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener.html#` via the setOnApplyWindowInsetsListener method.

This method replaces the older fitSystemWindows method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchCapturedPointerEvent

Pass a captured pointer event down to the focused view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchConfigurationChanged

Dispatch a notification about a resource configuration change down the view hierarchy. ViewGroups should override to route to their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchCreateViewTranslationRequest

Dispatch to collect the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest.html#`s for translation purpose by traversing the hierarchy when the app requests ui translation. Typically, this method should only be overridden by subclasses that provide a view hierarchy (such as `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`). Other classes should override onCreateViewTranslationRequest for normal view or override onVirtualViewTranslationResponses for view contains virtual children. When requested to start the ui translation, the system will call this method to traverse the view hierarchy to collect `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest.html#`s and create a `https://developer.android.com/reference/kotlin/android/view/translation/Translator.html#` to translate the requests. All the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest.html#`s must be added when the traversal is done.

The default implementation calls onCreateViewTranslationRequest for normal view or calls onVirtualViewTranslationResponses for view contains virtual children to build `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest.html#` if the view should be translated. The view is marked as having setHasTransientState so that recycling of views doesn't prevent the system from attaching the response to it. Therefore, if overriding this method, you should set or reset the transient state.
The implementation calls dispatchCreateViewTranslationRequest for all the child views.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchDisplayHint

Dispatch a hint about whether this view is displayed. For instance, when a View moves out of the screen, it might receives a display hint indicating the view is not displayed. Applications should not *rely* on this hint as there is no guarantee that they will receive one.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchDragEvent

Detects if this View is enabled and has a drag event listener. If both are true, then it calls the drag event listener with the `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#` it received. If the drag event listener returns `true`, then dispatchDragEvent() returns `true`.

For all other cases, the method calls the onDragEvent drag event handler method and returns its result.

This ensures that a drag event is always consumed, even if the View does not have a drag event listener. However, if the View has a listener and the listener returns true, then onDragEvent() is not called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchDraw

Called by draw to draw the child views. This may be overridden by derived classes to gain control just before its children are drawn (but after its own view has been drawn).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchDrawableHotspotChanged

Dispatches drawable hotspot changes to child views that meet at least one of the following criteria:

- Returns `false` from both isClickable and isLongClickable
- Requests duplication of parent state via setDuplicateParentStateEnabled

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchFinishTemporaryDetach

Dispatch onFinishTemporaryDetach to this View and its direct children if this is a container View. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchFreezeSelfOnly

Perform dispatching of a saveHierarchyState freeze()} to only this view, not to its children. For use when overriding dispatchSaveInstanceState dispatchFreeze()} to allow subclasses to freeze their own state but not the state of their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchGenericFocusedEvent

Dispatch a generic motion event to the currently focused view.

Do not call this method directly. Call dispatchGenericMotionEvent instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchGenericPointerEvent

Dispatch a generic motion event to the view under the first pointer.

Do not call this method directly. Call dispatchGenericMotionEvent instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchHoverEvent

Dispatch a hover event.

Do not call this method directly. Call dispatchGenericMotionEvent instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchKeyEvent

Dispatch a key event to the next view on the focus path. This path runs from the top of the view tree down to the currently focused view. If this view has focus, it will dispatch to itself. Otherwise it will dispatch the next node down the focus path. This method also fires any key listeners.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchKeyEventPreIme

Dispatch a key event before it is processed by any input method associated with the view hierarchy. This can be used to intercept key events in special situations before the IME consumes them; a typical example would be handling the BACK key to update the application's UI instead of allowing the IME to see it and close itself.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchKeyShortcutEvent

Dispatches a key shortcut event.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchPointerCaptureChanged

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchProvideAutofillStructure

Dispatches creation of a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#`s for autofill purposes down the hierarchy, when an Assist structure is being created as part of an autofill request.

The default implementation does the following:

- Sets the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` in the structure.
- Calls onProvideAutofillStructure.
- Calls onProvideAutofillVirtualStructure.

Typically, this method should only be overridden by subclasses that provide a view hierarchy (such as `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`) - other classes should override onProvideAutofillStructure or onProvideAutofillVirtualStructure instead.

When overridden, it must:

- Either call `super.dispatchProvideAutofillStructure(structure, flags)` or explicitly set the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` in the structure (for example, by calling `structure.setAutofillId(getAutofillId())`).
- Decide how to handle the `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` flag - when set, all views in the structure should be considered important for autofill, regardless of what isImportantForAutofill returns. We encourage you to respect this flag to provide a better user experience - this flag is typically used when an user explicitly requested autofill. If the flag is not set, then only views marked as important for autofill should be included in the structure - skipping non-important views optimizes the overall autofill performance.

This implementation adds in all child views of the view group, in addition to calling the default `https://developer.android.com/reference/kotlin/android/view/View.html#` implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchProvideStructure

Dispatch creation of `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` down the hierarchy. This implementation adds in all child views of the view group, in addition to calling the default View implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchRestoreInstanceState

Called by restoreHierarchyState to retrieve the state for this view and its children. May be overridden to modify how restoring happens to a view's children; for example, some views may want to not store state for their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchSaveInstanceState

Called by saveHierarchyState to store the state for this view and its children. May be overridden to modify how freezing happens to a view's children; for example, some views may want to not store state for their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchScrollCaptureSearch

Handle the scroll capture search request by checking this view if applicable, then to each child view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchSetActivated

Dispatch setActivated to all of this View's children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchSetPressed

Dispatch setPressed to all of this View's children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchSetSelected

Dispatch setSelected to all of this View's children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchStartTemporaryDetach

Dispatch onStartTemporaryDetach to this View and its direct children if this is a container View. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchSystemUiVisibilityChanged

Dispatch callbacks to setOnSystemUiVisibilityChangeListener down the view hierarchy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchThawSelfOnly

Perform dispatching of a restoreHierarchyState to only this view, not to its children. For use when overriding dispatchRestoreInstanceState to allow subclasses to thaw their own state but not the state of their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchTouchEvent

Pass the touch screen motion event down to the target view, or this view if it is the target.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchTrackballEvent

Pass a trackball motion event down to the focused view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchUnhandledMove

This method is the last chance for the focused view and its ancestors to respond to an arrow key. This is called when the focused view did not consume the key internally, nor could the view system find a new view in the requested direction to give focus to.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchVisibilityChanged

Dispatch a view visibility change down the view hierarchy. ViewGroups should override to route to their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchWindowFocusChanged

Called when the window containing this view gains or loses window focus. ViewGroups should override to route to their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchWindowInsetsAnimationEnd

Dispatches onEnd when Window Insets animation ends.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchWindowInsetsAnimationPrepare

Dispatches onPrepare when Window Insets animation is being prepared.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#` dispatchWindowInsetsAnimationProgress

Dispatches onProgress when Window Insets animation makes progress.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds.html#` dispatchWindowInsetsAnimationStart

Dispatches onStart when Window Insets animation is started.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchWindowSystemUiVisiblityChanged

Dispatch callbacks to onWindowSystemUiVisibilityChanged down the view hierarchy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` dispatchWindowVisibilityChanged

Dispatch a window visibility change down the view hierarchy. ViewGroups should override to route to their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` drawChild

Draw one child of this View Group. This method is responsible for getting the canvas in the right state. This includes clipping, translating so that the child's scrolled origin is at 0, 0, and applying any animation transformations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` drawableStateChanged

This function is called whenever the state of the view changes in such a way that it impacts the state of drawables being shown.

If the View has a StateListAnimator, it will also be called to run necessary state change animations.

Be sure to call through to the superclass when overriding this function. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` endViewTransition

This method should always be called following an earlier call to startViewTransition. The given View is finally removed from its parent and will no longer be displayed. Note that this method does not perform the functionality of removing a view from its parent; it just discontinues the display of a View that has previously been removed.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` findFocus

Find the view in the hierarchy rooted at this view that currently has focus.

<br />

`https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#?` findOnBackInvokedDispatcherForChild

Walk up the View hierarchy to find the nearest `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` findViewsWithText

Finds the Views that contain given text. The containment is case insensitive. The search is performed by either the text that the View renders or the content description that describes the view for accessibility purposes and the view does not render or both. Clients can specify how the search is to be performed via passing the `https://developer.android.com/reference/kotlin/android/view/View.html#FIND_VIEWS_WITH_TEXT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View.html#FIND_VIEWS_WITH_CONTENT_DESCRIPTION:kotlin.Int` flags.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` focusSearch

Find the nearest view in the specified direction that wants to take focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` focusableViewAvailable

Tells the parent that a new focusable view has become available. This is to handle transitions from the case where there are no focusable views to the case where the first focusable view appears.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` gatherTransparentRegion

This is used by the ViewRoot to perform an optimization when the view hierarchy contains one or several SurfaceView. SurfaceView is always considered transparent, but its children are not, therefore all View objects remove themselves from the global transparent region (passed as a parameter to this function).

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` getChildAt

Returns the view at the specified position in the group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getChildCount

Returns the number of children in the group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getChildDrawingOrder

Converts drawing order position to container position.

Children are not necessarily drawn in the order in which they appear in the container. ViewGroups can enable a custom ordering via setChildrenDrawingOrderEnabled. This method returns the container position of a child that appears in the given position in the current drawing order.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getChildDrawingOrder

Converts drawing order position to container position. Override this if you want to change the drawing order of children. By default, it returns drawingPosition.

NOTE: In order for this method to be called, you must enable child ordering first by calling setChildrenDrawingOrderEnabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getChildMeasureSpec

Does the hard part of measureChildren: figuring out the MeasureSpec to pass to a particular child. This method figures out the right MeasureSpec for one dimension (height or width) of one child view. The goal is to combine information from our MeasureSpec with the LayoutParams of the child to get the best possible results. For example, if the this view knows its size (because its MeasureSpec has a mode of EXACTLY), and the child has indicated in its LayoutParams that it wants to be the same size as the parent, the parent should ask the child to layout given an exact size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getChildStaticTransformation

Sets `t` to be the static transformation of the child, if set, returning a boolean to indicate whether a static transform was set. The default implementation simply returns `false`; subclasses may override this method for different behavior. setStaticTransformationsEnabled must be set to true for this method to be called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getChildVisibleRect

Compute the visible part of a rectangular region defined in terms of a child view's coordinates.

Returns the clipped visible part of the rectangle `r`, defined in the `child`'s local coordinate system. `r` is modified by this method to contain the result, expressed in the global (root) coordinate system.

The resulting rectangle is always axis aligned. If a rotation is applied to a node in the View hierarchy, the result is the axis-aligned bounding box of the visible rectangle.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getClipChildren

Returns whether this group's children are clipped to their bounds before drawing. The default value is true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getClipToPadding

Returns whether this ViewGroup will clip its children to its padding, and resize (but not clip) any EdgeEffect to the padded region, if padding is present.

By default, children are clipped to the padding of their parent Viewgroup. This clipping behavior is only enabled if padding is non-zero.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getDescendantFocusability

Gets the descendant focusability of this view group. The descendant focusability defines the relationship between this view group and its descendants when looking for a view to take focus in requestFocus.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` getFocusedChild

Returns the focused child of this view, if any. The child may have focus or contain focus.

<br />

`https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController.html#!` getLayoutAnimation

Returns the layout animation controller used to animate the group's children.

<br />

`https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener.html#!` getLayoutAnimationListener

Returns the animation listener to which layout animation events are sent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getLayoutMode

Returns the basis of alignment during layout operations on this ViewGroup: either `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#LAYOUT_MODE_OPTICAL_BOUNDS:kotlin.Int`.

If no layoutMode was explicitly set, either programmatically or in an XML resource, the method returns the layoutMode of the view's parent ViewGroup if such a parent exists, otherwise the method returns a default value of `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.html#!` getLayoutTransition

Gets the LayoutTransition object for this ViewGroup. If the LayoutTransition object is not null, changes in layout which occur because of children being added to or removed from the ViewGroup will be animated according to the animations defined in that LayoutTransition object. By default, the transition object is null (so layout changes are not animated).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getNestedScrollAxes

Return the current axes of nested scrolling for this ViewGroup.

A ViewGroup returning something other than `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_AXIS_NONE:kotlin.Int` is currently acting as a nested scrolling parent for one or more descendant views in the hierarchy.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewGroupOverlay.html#!` getOverlay

Returns the ViewGroupOverlay for this view group, creating it if it does not yet exist. In addition to `https://developer.android.com/reference/kotlin/android/view/ViewOverlay.html#`'s support for drawables, `https://developer.android.com/reference/kotlin/android/view/ViewGroupOverlay.html#` allows views to be added to the overlay. These views, like overlay drawables, are visual-only; they do not receive input events and should not be used as anything other than a temporary representation of a view in a parent container, such as might be used by an animation effect.

Note: Overlays do not currently work correctly with `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` or `https://developer.android.com/reference/kotlin/android/view/TextureView.html#`; contents in overlays for these types of views may not display correctly.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getPersistentDrawingCache

Returns an integer indicating what types of drawing caches are kept in memory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getTouchscreenBlocksFocus

Check whether this ViewGroup should ignore focus requests for itself and its children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasFocus

Returns true if this view has or contains focus

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasTransientState

Indicates whether the view is currently tracking transient state that the app should not need to concern itself with saving and restoring, but that the framework should take special note to preserve when possible.

A view with transient state cannot be trivially rebound from an external data source, such as an adapter binding item views in a list. This may be because the view is performing an animation, tracking user selection of content, or similar.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` indexOfChild

Returns the position in the group of the specified child view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` invalidateChild

Don't call or override this method. It is used for the implementation of the view hierarchy.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewParent.html#!` invalidateChildInParent

Don't call or override this method. It is used for the implementation of the view hierarchy. This implementation returns null if this ViewGroup does not have a parent, if this ViewGroup is already fully invalidated or if the dirty rectangle does not intersect with this ViewGroup's bounds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isAlwaysDrawnWithCacheEnabled

Indicates whether this ViewGroup will always try to draw its children using their drawing cache. By default this property is enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isAnimationCacheEnabled

Indicates whether the children's drawing cache is used during a layout animation. By default, the drawing cache is enabled but this will prevent nested layout animations from working. To nest animations, you must disable the cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isChildrenDrawingOrderEnabled

Indicates whether the ViewGroup is drawing its children in the order defined by getChildDrawingOrder.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isChildrenDrawnWithCacheEnabled

Indicates whether the ViewGroup is currently drawing its children using their drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isLayoutSuppressed

Returns whether layout calls on this container are currently being suppressed, due to an earlier call to suppressLayout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isMotionEventSplittingEnabled

Returns true if MotionEvents dispatched to this ViewGroup can be split to multiple children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isTransitionGroup

Returns true if this ViewGroup should be considered as a single entity for removal when executing an Activity transition. If this is false, child elements will move individually during the transition.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` jumpDrawablesToCurrentState

Call jumpToCurrentState on all Drawable objects associated with this view.

Also calls jumpToCurrentState if there is a StateListAnimator attached to this view. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` layout

Assign a size and position to a view and all of its descendants

This is the second phase of the layout mechanism. (The first is measuring). In this phase, each parent calls layout on all of its children to position them. This is typically done using the child measurements that were stored in the measure pass().

Derived classes should not override this method. Derived classes with children should override onLayout. In that method, they should call layout on each of their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` measureChild

Ask one of the children of this view to measure itself, taking into account both the MeasureSpec requirements for this view and its padding. The heavy lifting is done in getChildMeasureSpec.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` measureChildWithMargins

Ask one of the children of this view to measure itself, taking into account both the MeasureSpec requirements for this view and its padding and margins. The child must have MarginLayoutParams The heavy lifting is done in getChildMeasureSpec.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` measureChildren

Ask all of the children of this view to measure themselves, taking into account both the MeasureSpec requirements for this view and its padding. We skip children that are in the GONE state The heavy lifting is done in getChildMeasureSpec.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` notifySubtreeAccessibilityStateChanged

Notifies a view parent that the accessibility state of one of its descendants has changed and that the structure of the subtree is different.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` offsetDescendantRectToMyCoords

Offset a rectangle that is in a descendant's coordinate space into our coordinate space.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` offsetRectIntoDescendantCoords

Offset a rectangle that is in our coordinate space into an ancestor's coordinate space.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onAttachedToWindow

This is called when the view is attached to a window. At this point it has a Surface and will start drawing. Note that this function is guaranteed to be called before onDraw, however it may be called any time before the first onDraw -- including before or after onMeasure. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` onCreateDrawableState

Generate the new `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` state for this view. This is called by the view system when the cached Drawable state is determined to be invalid. To retrieve the current state, you should use getDrawableState.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onDescendantInvalidated

The target View has been invalidated, or has had a drawing property changed that requires the hierarchy to re-render. This method is called by the View hierarchy to signal ancestors that a View either needs to re-record its drawing commands, or drawing properties have changed. This is how Views schedule a drawing traversal. This signal is generally only dispatched for attached Views, since only they need to draw. If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onDetachedFromWindow

This is called when the view is detached from a window. At this point it no longer has a surface for drawing. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onInterceptHoverEvent

Implement this method to intercept hover events before they are handled by child views.

This method is called before dispatching a hover event to a child of the view group or to the view group's own onHoverEvent to allow the view group a chance to intercept the hover event. This method can also be used to watch all pointer motions that occur within the bounds of the view group even when the pointer is hovering over a child of the view group rather than over the view group itself.

The view group can prevent its children from receiving hover events by implementing this method and returning `true` to indicate that it would like to intercept hover events. The view group must continuously return `true` from onInterceptHoverEvent for as long as it wishes to continue intercepting hover events from its children.

Interception preserves the invariant that at most one view can be hovered at a time by transferring hover focus from the currently hovered child to the view group or vice-versa as needed.

If this method returns `true` and a child is already hovered, then the child view will first receive a hover exit event and then the view group itself will receive a hover enter event in onHoverEvent. Likewise, if this method had previously returned `true` to intercept hover events and instead returns `false` while the pointer is hovering within the bounds of one of a child, then the view group will first receive a hover exit event in onHoverEvent and then the hovered child will receive a hover enter event.

The default implementation handles mouse hover on the scroll bars.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onInterceptTouchEvent

Implement this method to intercept all touch screen motion events. This allows you to watch events as they are dispatched to your children, and take ownership of the current gesture at any point.

Using this function takes some care, as it has a fairly complicated interaction with onTouchEvent, and using it requires implementing that method as well as this one in the correct way. Events will be received in the following order:

1. You will receive the down event here.
2. The down event will be handled either by a child of this view group, or given to your own onTouchEvent() method to handle; this means you should implement onTouchEvent() to return true, so you will continue to see the rest of the gesture (instead of looking for a parent view to handle it). Also, by returning true from onTouchEvent(), you will not receive any following events in onInterceptTouchEvent() and all touch processing must happen in onTouchEvent() like normal.
3. For as long as you return false from this function, each following event (up to and including the final up) will be delivered first here and then to the target's onTouchEvent().
4. If you return true from here, you will not receive any following events: the target view will receive the same event but with the action `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_CANCEL:kotlin.Int`, and all further events will be delivered to your onTouchEvent() method and no longer appear here.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onNestedFling

Request a fling from a nested scroll.

This method signifies that a nested scrolling child has detected suitable conditions for a fling. Generally this means that a touch scroll has ended with a `https://developer.android.com/reference/kotlin/android/view/VelocityTracker.html#` in the direction of scrolling that meets or exceeds the getScaledMinimumFlingVelocity along a scrollable axis.

If a nested scrolling child view would normally fling but it is at the edge of its own content, it can use this method to delegate the fling to its nested scrolling parent instead. The parent may optionally consume the fling or observe a child fling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onNestedPreFling

React to a nested fling before the target view consumes it.

This method siginfies that a nested scrolling child has detected a fling with the given velocity along each axis. Generally this means that a touch scroll has ended with a `https://developer.android.com/reference/kotlin/android/view/VelocityTracker.html#` in the direction of scrolling that meets or exceeds the getScaledMinimumFlingVelocity along a scrollable axis.

If a nested scrolling parent is consuming motion as part of a onNestedPreScroll, it may be appropriate for it to also consume the pre-fling to complete that same motion. By returning `true` from this method, the parent indicates that the child should not fling its own internal content as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onNestedPrePerformAccessibilityAction

React to an accessibility action delegated by a target descendant view before the target processes it.

This method may be called by a target descendant view if the target wishes to give a view in its parent chain a chance to react to the event before normal processing occurs. Most commonly this will be a scroll event such as `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#ACTION_SCROLL_FORWARD:kotlin.Int`. A ViewParent that supports acting as a nested scrolling parent should override this method and act accordingly to implement scrolling via accesibility systems.

Subclasses should always call `super.onNestedPrePerformAccessibilityAction`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onNestedPreScroll

React to a nested scroll in progress before the target view consumes a portion of the scroll.

When working with nested scrolling often the parent view may want an opportunity to consume the scroll before the nested scrolling child does. An example of this is a drawer that contains a scrollable list. The user will want to be able to scroll the list fully into view before the list itself begins scrolling.

`onNestedPreScroll` is called when a nested scrolling child invokes dispatchNestedPreScroll. The implementation should report how any pixels of the scroll reported by dx, dy were consumed in the `consumed` array. Index 0 corresponds to dx and index 1 corresponds to dy. This parameter will never be null. Initial values for consumed\[0\] and consumed\[1\] will always be 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onNestedScroll

React to a nested scroll in progress.

This method will be called when the ViewParent's current nested scrolling child view dispatches a nested scroll event. To receive calls to this method the ViewParent must have previously returned `true` for a call to onStartNestedScroll.

Both the consumed and unconsumed portions of the scroll distance are reported to the ViewParent. An implementation may choose to use the consumed portion to match or chase scroll position of multiple child elements, for example. The unconsumed portion may be used to allow continuous dragging of multiple scrolling or draggable elements, such as scrolling a list within a vertical drawer where the drawer begins dragging once the edge of inner scrolling content is reached.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onNestedScrollAccepted

React to the successful claiming of a nested scroll operation.

This method will be called after onStartNestedScroll returns true. It offers an opportunity for the view and its superclasses to perform initial configuration for the nested scroll. Implementations of this method should always call their superclass's implementation of this method if one is present.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onRequestFocusInDescendants

Look for a descendant to call android.view.View#requestFocus on. Called by requestFocus when it wants to request focus within its children. Override this to customize how your `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` requests focus within its children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onRequestSendAccessibilityEvent

Called when a child has requested sending an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#` and gives an opportunity to its parent to augment the event.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its onRequestSendAccessibilityEvent is responsible for handling this call.

<br />

`https://developer.android.com/reference/kotlin/android/view/PointerIcon.html#!` onResolvePointerIcon

Resolve the pointer icon that should be used for specified pointer in the motion event. The default implementation will resolve the pointer icon to one set using setPointerIcon for mouse devices. Subclasses may override this to customize the icon for the given pointer. For example, to always show the PointerIcon.TYPE_HANDWRITING icon for a stylus pointer, the event can be resolved in the following way: `
`

 @Override
 public PointerIcon onResolvePointerIcon(MotionEvent event, int pointerIndex) {
 final int toolType = event.getToolType(pointerIndex);
 if (!event.isFromSource(InputDevice.SOURCE_MOUSE)
 && event.isFromSource(InputDevice.SOURCE_STYLUS)
 && (toolType == MotionEvent.TOOL_TYPE_STYLUS
 || toolType == MotionEvent.TOOL_TYPE_ERASER)) {
| --- | --- |
 // Show this pointer icon only if this pointer is a stylus.
 return PointerIcon.getSystemIcon(mContext, PointerIcon.TYPE_HANDWRITING);
 }
 // Use the default logic for determining the pointer icon for other non-stylus pointers,
 // like for the mouse cursor.
 return super.onResolvePointerIcon(event, pointerIndex);
 }
 
`
`

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onStartNestedScroll

React to a descendant view initiating a nestable scroll operation, claiming the nested scroll operation if appropriate.

This method will be called in response to a descendant view invoking startNestedScroll. Each parent up the view hierarchy will be given an opportunity to respond and claim the nested scrolling operation by returning `true`.

This method may be overridden by ViewParent implementations to indicate when the view is willing to support a nested scrolling operation that is about to begin. If it returns true, this ViewParent will become the target view's nested scrolling parent for the duration of the scroll operation in progress. When the nested scroll is finished this ViewParent will receive a call to onStopNestedScroll.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onStopNestedScroll

React to a nested scroll operation ending.

Perform cleanup after a nested scrolling operation. This method will be called when a nested scroll stops, for example when a nested touch scroll ends with a `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_UP:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_CANCEL:kotlin.Int` event. Implementations of this method should always call their superclass's implementation of this method if one is present.

The default implementation of onStopNestedScroll calls stopNestedScroll to halt any recursive nested scrolling in progress.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onViewAdded

Called when a new child is added to this ViewGroup. Overrides should always call super.onViewAdded.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onViewRemoved

Called when a child view is removed from this ViewGroup. Overrides should always call super.onViewRemoved.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` propagateRequestedFrameRate

You can set the preferred frame rate for a ViewGroup and its children using a positive number or by specifying the preferred frame rate category using constants, including REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, REQUESTED_FRAME_RATE_CATEGORY_HIGH. Keep in mind that the preferred frame rate affects the frame rate for the next frame, so use this method carefully. It's important to note that the preference is valid as long as the ViewGroup or any of its children is invalidated. To undo the frame rate propagation, call the API with REQUESTED_FRAME_RATE_CATEGORY_DEFAULT.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` recomputeViewAttributes

Tell view hierarchy that the global view attributes need to be re-evaluated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeAllViews

Call this method to remove all child views from the ViewGroup.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeAllViewsInLayout

Called by a ViewGroup subclass to remove child views from itself, when it must first know its size on screen before it can calculate how many child views it will render. An example is a Gallery or a ListView, which may "have" 50 children, but actually only render the number of children that can currently fit inside the object on screen. Do not call this method unless you are extending ViewGroup and understand the view measuring and layout pipeline.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeDetachedView

Finishes the removal of a detached view. This method will dispatch the detached from window event and notify the hierarchy change listener.

This method is intended to be lightweight and makes no assumptions about whether the parent or child should be redrawn. Proper use of this method will include also making any appropriate #requestLayout() or invalidate calls. For example, callers can post a `https://developer.android.com/reference/kotlin/java/lang/Runnable.html#` which performs a #requestLayout() on the next frame, after all detach/remove calls are finished, causing layout to be run prior to redrawing the view hierarchy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeView

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeViewAt

Removes the view at the specified position in the group.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeViewInLayout

Removes a view during layout. This is useful if in your onLayout() method, you need to remove more views.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeViews

Removes the specified range of views from the group.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeViewsInLayout

Removes a range of views during layout. This is useful if in your onLayout() method, you need to remove more views.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestChildFocus

Called when a child of this parent wants focus

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestChildRectangleOnScreen

Called when a child of this group wants a particular rectangle to be positioned onto the screen. `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`s overriding this can trust that:

- `child` will be a direct child of this group
- `rectangle` will be in the child's content coordinates

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`s overriding this should uphold the contract:

- nothing will change if the rectangle is already visible
- the view port will be scrolled only just enough to make the rectangle visible

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestChildRectangleOnScreen

Called when a child of this group wants a particular rectangle to be positioned onto the screen. `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`s overriding this can trust that:

- `child` will be a direct child of this group
- `rectangle` will be in the child's content coordinates

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`s overriding this should uphold the contract:

- nothing will change if the rectangle is already visible
- the view port will be scrolled only just enough to make the rectangle visible

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestDisallowInterceptTouchEvent

Called when a child does not want this parent and its ancestors to intercept touch events with onInterceptTouchEvent.

This parent should pass this call onto its parents. This parent must obey this request for the duration of the touch (that is, only clear the flag after this parent has received an up or a cancel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestFocus

Call this to try to give focus to a specific view or to one of its descendants and give it hints about the direction and a specific rectangle that the focus is coming from. The rectangle can help give larger views a finer grained hint about where focus is coming from, and therefore, where to show selection, or forward focus change internally. A view will not actually take focus if it is not focusable (isFocusable returns false), or if it is focusable and it is not focusable in touch mode (isFocusableInTouchMode) while the device is in touch mode. A View will not take focus if it is not visible. A View will not take focus if one of its parents has getDescendantFocusability equal to `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#FOCUS_BLOCK_DESCENDANTS:kotlin.Int`. See also focusSearch, which is what you call to say that you have focus, and you want your parent to look for the next one. You may wish to override this method if your custom `https://developer.android.com/reference/kotlin/android/view/View.html#` has an internal `https://developer.android.com/reference/kotlin/android/view/View.html#` that it wishes to forward the request to. Looks for a view to give focus to respecting the setting specified by getDescendantFocusability. Uses onRequestFocusInDescendants to find focus within the children of this group when appropriate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestSendAccessibilityEvent

Called by a child to request from its parent to send an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#`. The child has already populated a record for itself in the event and is delegating to its parent to send the event. The parent can optionally add a record for itself.

Note: An accessibility event is fired by an individual view which populates the event with a record for its state and requests from its parent to perform the sending. The parent can optionally add a record for itself before dispatching the request to its parent. A parent can also choose not to respect the request for sending the event. The accessibility event is sent by the topmost view in the view tree.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestTransparentRegion

Called when a child wants the view hierarchy to gather and report transparent regions to the window compositor. Views that "punch" holes in the view hierarchy, such as SurfaceView can use this API to improve performance of the system. When no such a view is present in the hierarchy, this optimization in unnecessary and might slightly reduce the view hierarchy performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` restoreDefaultFocus

Gives focus to the default-focus view in the view hierarchy that has this view as a root. If the default-focus view cannot be found, falls back to calling requestFocus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` scheduleLayoutAnimation

Schedules the layout animation to be played after the next layout pass of this view group. This can be used to restart the layout animation when the content of the view group changes or when the activity is paused and resumed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAddStatesFromChildren

Sets whether this ViewGroup's drawable states also include its children's drawable states. This is used, for example, to make a group appear to be focused when its child EditText or button is focused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAlwaysDrawnWithCacheEnabled

Indicates whether this ViewGroup will always try to draw its children using their drawing cache. This property can be set to true when the cache rendering is slightly different from the children's normal rendering. Renderings can be different, for instance, when the cache's quality is set to low. When this property is disabled, the ViewGroup will use the drawing cache of its children only when asked to. It's usually the task of subclasses to tell ViewGroup when to start using the drawing cache and when to stop using it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAnimationCacheEnabled

Enables or disables the children's drawing cache during a layout animation. By default, the drawing cache is enabled but this will prevent nested layout animations from working. To nest animations, you must disable the cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setChildrenDrawingCacheEnabled

Enables or disables the drawing cache for each child of this view group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setChildrenDrawingOrderEnabled

Tells the ViewGroup whether to draw its children in the order defined by the method getChildDrawingOrder.

Note that getZ reordering, done by dispatchDraw, will override custom child ordering done via this method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setChildrenDrawnWithCacheEnabled

Tells the ViewGroup to draw its children using their drawing cache. This property is ignored when isAlwaysDrawnWithCacheEnabled is true. A child's drawing cache will be used only if it has been enabled. Subclasses should call this method to start and stop using the drawing cache when they perform performance sensitive operations, like scrolling or animating.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setClipChildren

By default, children are clipped to their bounds before drawing. This allows view groups to override this behavior for animations, etc.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setClipToPadding

Sets whether this ViewGroup will clip its children to its padding and resize (but not clip) any EdgeEffect to the padded region, if padding is present.

By default, children are clipped to the padding of their parent ViewGroup. This clipping behavior is only enabled if padding is non-zero.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setDescendantFocusability

Set the descendant focusability of this view group. This defines the relationship between this view group and its descendants when looking for a view to take focus in requestFocus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLayoutAnimation

Sets the layout animation controller used to animate the group's children after the first layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLayoutAnimationListener

Specifies the animation listener to which layout animation events must be sent. Only onAnimationStart and onAnimationEnd are invoked.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLayoutMode

Sets the basis of alignment during the layout of this ViewGroup. Valid values are either `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#LAYOUT_MODE_CLIP_BOUNDS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#LAYOUT_MODE_OPTICAL_BOUNDS:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLayoutTransition

Sets the LayoutTransition object for this ViewGroup. If the LayoutTransition object is not null, changes in layout which occur because of children being added to or removed from the ViewGroup will be animated according to the animations defined in that LayoutTransition object. By default, the transition object is null (so layout changes are not animated).

Replacing a non-null transition will cause that previous transition to be canceled, if it is currently running, to restore this container to its correct post-transition state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setMotionEventSplittingEnabled

Enable or disable the splitting of MotionEvents to multiple children during touch event dispatch. This behavior is enabled by default for applications that target an SDK version of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or newer.

When this option is enabled MotionEvents may be split and dispatched to different child views depending on where each pointer initially went down. This allows for user interactions such as scrolling two panes of content independently, chording of buttons, and performing independent gestures on different pieces of content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnHierarchyChangeListener

Register a callback to be invoked when a child is added to or removed from this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPersistentDrawingCache

Indicates what types of drawing caches should be kept in memory after they have been created.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setRequestedFrameRate

You can set the preferred frame rate for a ViewGroup using a positive number or by specifying the preferred frame rate category using constants, including REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, REQUESTED_FRAME_RATE_CATEGORY_HIGH. Keep in mind that the preferred frame rate affects the frame rate for the next frame, so use this method carefully. It's important to note that the preference is valid as long as the ViewGroup is invalidated. Please also be aware that the requested frame rate will not propagate to child views.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setStaticTransformationsEnabled

When this property is set to true, this ViewGroup supports static transformations on children; this causes getChildStaticTransformation to be invoked when a child is drawn. Any subclass overriding getChildStaticTransformation should set this property to true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTouchscreenBlocksFocus

Set whether this ViewGroup should ignore focus requests for itself and its children. If this option is enabled and the ViewGroup or a descendant currently has focus, focus will proceed forward.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTransitionGroup

Changes whether or not this ViewGroup should be treated as a single entity during Activity Transitions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setWindowInsetsAnimationCallback

Sets a `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback.html#` to be notified about animations of windows that cause insets.

The callback's getDispatchMode will affect whether animation callbacks are dispatched to the children of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` showContextMenuForChild

Shows the context menu for the specified view or its ancestors.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, addView) then it should override this and show the context menu.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` showContextMenuForChild

Shows the context menu for the specified view or its ancestors anchored to the specified view-relative coordinate.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, addView) then it should override this and show the context menu.

If a subclass overrides this method it should also override showContextMenuForChild.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode.html#!` startActionModeForChild

Start an action mode for the specified view with the default type `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#TYPE_PRIMARY:kotlin.Int`.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, addView) then it should override this and start the action mode.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode.html#!` startActionModeForChild

Start an action mode of a specific type for the specified view.

In most cases, a subclass does not need to override this. However, if the subclass is added directly to the window manager (for example, addView) then it should override this and start the action mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startLayoutAnimation

Runs the layout animation. Calling this method triggers a relayout of this view group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startViewTransition

This method tells the ViewGroup that the given View object, which should have this ViewGroup as its parent, should be kept around (re-displayed when the ViewGroup draws its children) even if it is removed from its parent. This allows animations, such as those used by `https://developer.android.com/reference/kotlin/android/app/Fragment.html#` and `https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.html#` to animate the removal of views. A call to this method should always be accompanied by a later call to endViewTransition, such as after an animation on the View has finished, so that the View finally gets removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` suppressLayout

Tells this ViewGroup to suppress all layout() calls until layout suppression is disabled with a later call to suppressLayout(false). When layout suppression is disabled, a requestLayout() call is sent if layout() was attempted while layout was being suppressed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` updateViewLayout

<br />

From class `https://developer.android.com/reference/kotlin/android/view/View.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addFocusables

Add any focusable views that are descendants of this view (possibly including this view if it is focusable itself) to views. If we are in touch mode, only add views that are also focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addOnAttachStateChangeListener

Add a listener for attach state changes. This listener will be called whenever this view is attached or detached from a window. Remove the listener using removeOnAttachStateChangeListener.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addOnLayoutChangeListener

Add a listener that will be called when the bounds of the view change due to layout processing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addOnUnhandledKeyEventListener

Adds a listener which will receive unhandled `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`s. This must be called on the UI thread.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator.html#!` animate

This method returns a ViewPropertyAnimator object, which can be used to animate specific properties on this View.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` announceForAccessibility

Convenience method for sending a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_ANNOUNCEMENT:kotlin.Int` `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#` to suggest that an accessibility service announce the specified text to its users.

Note: The event generated with this API carries no semantic meaning, and accessibility services may choose to ignore it. Apps that accurately supply accessibility with the semantics of their UI should not need to specify what exactly is announced.

In general, do not attempt to generate announcements as confirmation message for simple actions like a button press. Label your controls concisely and precisely instead.

To convey significant UI changes like window changes, use setTitle and setAccessibilityPaneTitle.

Use setAccessibilityLiveRegion to inform the user of changes to critical views within the user interface. These should still be used sparingly as they may generate announcements every time a View is updated.

Use setStateDescription to convey state changes to views within the user interface. While a live region may send different types of events generated by the view, state description will send `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` events of type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int`.

For notifying users about errors, such as in a login screen with text that displays an "incorrect password" notification, set setError and dispatch an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` event with a change type of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int`, instead. Some widgets may expose methods that convey error states to accessibility automatically, such as setError, which manages these accessibility semantics and event dispatch for callers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` autofill

Automatically fills the content of the virtual children within this view.

Views with virtual children support the Autofill Framework mainly by:

- Providing the metadata defining what the virtual children mean and how they can be autofilled.
- Implementing the methods that autofill the virtual children.

onProvideAutofillVirtualStructure is responsible for the former, this method is responsible for the latter - see autofill and onProvideAutofillVirtualStructure for more info about autofill.

If a child value is updated asynchronously, the next call to notifyValueChanged must happen **after** the value was changed to the autofilled value. If not, the child will not be considered autofilled.

**Note:** To indicate that a virtual view was autofilled, `?android:attr/autofilledHighlight` should be drawn over it until the data changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` autofill

Automatically fills the content of this view with the `value`.

Views support the Autofill Framework mainly by:

- Providing the metadata defining what the view means and how it can be autofilled.
- Implementing the methods that autofill the view.

onProvideAutofillStructure is responsible for the former, this method is responsible for latter.

This method does nothing by default, but when overridden it typically:

1. Checks if the provided value matches the expected type (which is defined by getAutofillType).
2. Checks if the view is editable - if it isn't, it should return right away.
3. Call the proper getter method on `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` to fetch the actual value.
4. Pass the actual value to the equivalent setter in the view.

For example, a text-field view could implement the method this way:

```kotlin
@Override
  public void autofill(AutofillValue value) {
    if (!value.isText() || !this.isEditable()) {
       return;
    }
    CharSequence text = value.getTextValue();
    if (text != null) {
      this.setText(text);
    }
  }
  
```

If the value is updated asynchronously, the next call to notifyValueChanged must happen **after** the value was changed to the autofilled value. If not, the view will not be considered autofilled.

**Note:** After this method is called, the value returned by getAutofillValue must be equal to the `value` passed to it, otherwise the view will not be highlighted as autofilled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` awakenScrollBars

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a default delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by isHorizontalScrollBarEnabled and isVerticalScrollBarEnabled. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls invalidate; in that case the caller should not call invalidate.

This method should be invoked every time a subclass directly updates the scroll parameters.

This method is automatically invoked by scrollBy and scrollTo.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` awakenScrollBars

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a fixed delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by isHorizontalScrollBarEnabled and isVerticalScrollBarEnabled. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls invalidate; in that case the caller should not call invalidate.

This method should be invoked every time a subclass directly updates the scroll parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` awakenScrollBars

Trigger the scrollbars to draw. When invoked this method starts an animation to fade the scrollbars out after a fixed delay. If a subclass provides animated scrolling, the start delay should equal the duration of the scrolling animation.

The animation starts only if at least one of the scrollbars is enabled, as specified by isHorizontalScrollBarEnabled and isVerticalScrollBarEnabled. When the animation is started, this method returns true, and false otherwise. If the animation is started, this method calls invalidate if the invalidate parameter is set to true; in that case the caller should not call invalidate.

This method should be invoked every time a subclass directly updates the scroll parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` bringToFront

Change the view's z order in the tree, so it's on top of other sibling views. This ordering change may affect layout, if the parent container uses an order-dependent layout scheme (e.g., LinearLayout). Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int` this method should be followed by calls to requestLayout and invalidate on the view's parent to force the parent to redraw with the new child ordering.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` buildDrawingCache

Calling this method is equivalent to calling `buildDrawingCache(false)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` buildDrawingCache

Forces the drawing cache to be built if the drawing cache is invalid.

If you call buildDrawingCache manually without calling setDrawingCacheEnabled, you should cleanup the cache by calling destroyDrawingCache afterwards.

Note about auto scaling in compatibility mode: When auto scaling is not enabled, this method will create a bitmap of the same size as this view. Because this bitmap will be drawn scaled by the parent ViewGroup, the result on screen might show scaling artifacts. To avoid such artifacts, you should call this method by setting the auto scaling to true. Doing so, however, will generate a bitmap of a different size than the view. This implies that your application must be able to handle this size.

You should avoid calling this method when hardware acceleration is enabled. If you do not need the drawing cache bitmap, calling this method will increase memory usage and cause the view to be rendered in software once, thus negatively impacting performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` buildLayer

Forces this view's layer to be created and this view to be rendered into its layer. If this view's layer type is set to `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_NONE:kotlin.Int`, invoking this method will have no effect. This method can for instance be used to render a view into its layer before starting an animation. If this view is complex, rendering into the layer before starting the animation will avoid skipping frames.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` callOnClick

Directly call any attached OnClickListener. Unlike performClick, this only calls the listener, and does not do any associated clicking actions like reporting an accessibility event.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` canResolveLayoutDirection

Check if layout direction resolution can be done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` canResolveTextAlignment

Check if text alignment resolution can be done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` canResolveTextDirection

Check if text direction resolution can be done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` canScrollHorizontally

Check if this view can be scrolled horizontally in a certain direction.

This is without regard to whether the view is enabled or not, or if it will scroll in response to user input or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` canScrollVertically

Check if this view can be scrolled vertically in a certain direction.

This is without regard to whether the view is enabled or not, or if it will scroll in response to user input or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` cancelDragAndDrop

Cancels an ongoing drag and drop operation.

A `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#` object with getAction value of `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#ACTION_DRAG_ENDED:kotlin.Int` and getResult value of `false` will be sent to every View that received `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#ACTION_DRAG_STARTED:kotlin.Int` even if they are not currently visible.

This method can be called on any View in the same window as the View on which startDragAndDrop was called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` cancelLongPress

Cancels a pending long press. Your subclass can use this if you want the context menu to come up if the user presses and holds at the same place, but you don't want it to come up if they press and then move around enough to cause scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` cancelPendingInputEvents

Cancel any deferred high-level input events that were previously posted to the event queue.

Many views post high-level events such as click handlers to the event queue to run deferred in order to preserve a desired user experience - clearing visible pressed states before executing, etc. This method will abort any events of this nature that are currently in flight.

Custom views that generate their own high-level deferred input events should override onCancelPendingInputEvents and remove those pending events from the queue.

This will also cancel pending input events for any child views.

Note that this may not be sufficient as a debouncing strategy for clicks in all cases. This will not impact newer events posted after this call that may occur as a result of lower-level input events still waiting in the queue. If you are trying to prevent double-submitted events for the duration of some sort of asynchronous transaction you should also take other steps to protect against unexpected double inputs e.g. calling setEnabled and re-enabling the view when the transaction completes, tracking already submitted transaction IDs, etc.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` checkInputConnectionProxy

Called by the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` when a view who is not the current input connection target is trying to make a call on the manager. The default implementation returns false; you can override this to return true for certain views if you are performing InputConnection proxying to them.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` clearAnimation

Cancels any animations for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` clearPendingCredentialRequest

Clears the request and callback previously set through setPendingCredentialRequest. Once this API is invoked, there will be no request fired to `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` on future view focus events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` clearViewTranslationCallback

Clear the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback.html#` from this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` combineMeasuredStates

Merge two states as returned by getMeasuredState.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` computeHorizontalScrollExtent

Compute the horizontal extent of the horizontal scrollbar's thumb within the horizontal range. This value is used to compute the length of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by computeHorizontalScrollRange and computeHorizontalScrollOffset.

The default extent is the drawing width of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` computeHorizontalScrollOffset

Compute the horizontal offset of the horizontal scrollbar's thumb within the horizontal range. This value is used to compute the position of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by computeHorizontalScrollRange and computeHorizontalScrollExtent.

The default offset is the scroll offset of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` computeHorizontalScrollRange

Compute the horizontal range that the horizontal scrollbar represents.

The range is expressed in arbitrary units that must be the same as the units used by computeHorizontalScrollExtent and computeHorizontalScrollOffset.

The default range is the drawing width of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` computeScroll

Called by a parent to request that a child update its values for mScrollX and mScrollY if necessary. This will typically be done if the child is animating a scroll using a Scroller object.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#!` computeSystemWindowInsets

Compute insets that should be consumed by this view and the ones that should propagate to those under it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` computeVerticalScrollExtent

Compute the vertical extent of the vertical scrollbar's thumb within the vertical range. This value is used to compute the length of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by computeVerticalScrollRange and computeVerticalScrollOffset.

The default extent is the drawing height of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` computeVerticalScrollOffset

Compute the vertical offset of the vertical scrollbar's thumb within the horizontal range. This value is used to compute the position of the thumb within the scrollbar's track.

The range is expressed in arbitrary units that must be the same as the units used by computeVerticalScrollRange and computeVerticalScrollExtent.

The default offset is the scroll offset of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` computeVerticalScrollRange

Compute the vertical range that the vertical scrollbar represents.

The range is expressed in arbitrary units that must be the same as the units used by computeVerticalScrollExtent and computeVerticalScrollOffset.

<br />

`https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#!` createAccessibilityNodeInfo

Returns an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#` representing this view from the point of view of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This method is responsible for obtaining an accessibility node info from a pool of reusable instances and calling onInitializeAccessibilityNodeInfo on this view to initialize the former.

Note: The client is responsible for recycling the obtained instance by calling recycle to minimize object creation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` createContextMenu

Show the context menu for this view. It is not safe to hold on to the menu after returning from this method. You should normally not overload this method. Overload onCreateContextMenu or define an `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#` to add items to the context menu.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` destroyDrawingCache

Frees the resources used by the drawing cache. If you call buildDrawingCache manually without calling setDrawingCacheEnabled, you should cleanup the cache with this method afterwards.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchGenericMotionEvent

Dispatch a generic motion event.

Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view. Hover events are handled specially and are delivered to onHoverEvent first.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchNestedFling

Dispatch a fling to a nested scrolling parent.

This method should be used to indicate that a nested scrolling child has detected suitable conditions for a fling. Generally this means that a touch scroll has ended with a `https://developer.android.com/reference/kotlin/android/view/VelocityTracker.html#` in the direction of scrolling that meets or exceeds the getScaledMinimumFlingVelocity along a scrollable axis.

If a nested scrolling child view would normally fling but it is at the edge of its own content, it can use this method to delegate the fling to its nested scrolling parent instead. The parent may optionally consume the fling or observe a child fling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchNestedPreFling

Dispatch a fling to a nested scrolling parent before it is processed by this view.

Nested pre-fling events are to nested fling events what touch intercept is to touch and what nested pre-scroll is to nested scroll. `dispatchNestedPreFling` offsets an opportunity for the parent view in a nested fling to fully consume the fling before the child view consumes it. If this method returns `true`, a nested parent view consumed the fling and this view should not scroll as a result.

For a better user experience, only one view in a nested scrolling chain should consume the fling at a time. If a parent view consumed the fling this method will return false. Custom view implementations should account for this in two ways:

- If a custom view is paged and needs to settle to a fixed page-point, do not call `dispatchNestedPreFling`; consume the fling and settle to a valid position regardless.
- If a nested parent does consume the fling, this view should not scroll at all, even to settle back to a valid idle position.

Views should also not offer fling velocities to nested parent views along an axis where scrolling is not currently supported; a ScrollView should not offer a horizontal fling velocity to its parents since scrolling along that axis is not permitted and carrying velocity along that motion does not make sense.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchNestedPrePerformAccessibilityAction

Report an accessibility action to this view's parents for delegated processing.

Implementations of performAccessibilityAction may internally call this method to delegate an accessibility action to a supporting parent. If the parent returns true from its onNestedPrePerformAccessibilityAction method this method will return true to signify that the action was consumed.

This method is useful for implementing nested scrolling child views. If isNestedScrollingEnabled returns true and the action is a scrolling action a custom view implementation may invoke this method to allow a parent to consume the scroll first. If this method returns true the custom view should skip its own scrolling behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchNestedPreScroll

Dispatch one step of a nested scroll in progress before this view consumes any portion of it.

Nested pre-scroll events are to nested scroll events what touch intercept is to touch. `dispatchNestedPreScroll` offers an opportunity for the parent view in a nested scrolling operation to consume some or all of the scroll operation before the child view consumes it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchNestedScroll

Dispatch one step of a nested scroll in progress.

Implementations of views that support nested scrolling should call this to report info about a scroll in progress to the current nested scrolling parent. If a nested scroll is not currently in progress or nested scrolling is not isNestedScrollingEnabled for this view this method does nothing.

Compatible View implementations should also call dispatchNestedPreScroll before consuming a component of the scroll event themselves.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` dispatchPopulateAccessibilityEvent

Dispatches an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#` to the `https://developer.android.com/reference/kotlin/android/view/View.html#` to add the text content of the view and its children.

**Note:** This method should only be used with event.setText(). Avoid mutating other event state in this method. In general, put UI metadata in the node for services to easily query.

- If you are modifying other event properties, you may be eliminating semantics accessibility services may want. Instead, send a separate event using sendAccessibilityEvent and override onInitializeAccessibilityEvent.
- If you are checking for type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_STATE_CHANGED:kotlin.Int` to generate window/title announcements, you may be causing disruptive announcements (or making no announcements at all). Instead, follow the practices described in announceForAccessibility. **Note:** this does not suggest calling announceForAccessibility(), but using the suggestions listed in its documentation.
- If you are making changes based on the state of accessibility, such as checking for an event type to trigger a UI update, while well-intentioned, you are creating brittle, less well-maintained code that works for some users but not others. Instead, leverage existing code for equitable experiences and less technical debt. See isEnabled for an example.

Note that the event text is populated in a separate dispatch path (onPopulateAccessibilityEvent) since we add to the event not only the text of the source but also the text of all its descendants.

A typical implementation will call onPopulateAccessibilityEvent on this view and then call the dispatchPopulateAccessibilityEvent on each child or the first child that is visible. Override this method if custom population of the event text content is required.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its dispatchPopulateAccessibilityEvent is responsible for handling this call.

If this view sets isAccessibilityDataSensitive then this view should only append sensitive information to an event that also sets isAccessibilityDataSensitive.

*Note:* Accessibility events of certain types are not dispatched for populating the event text via this method. For details refer to `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` draw

Manually render this view (and all of its children) to the given Canvas. The view must have already done a full layout before this function is called. When implementing a view, implement onDraw instead of overriding this method. If you do need to override this method, call the superclass version. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` drawableHotspotChanged

This function is called whenever the view hotspot changes and needs to be propagated to drawables or child views managed by the view.

Dispatching to child views is handled by dispatchDrawableHotspotChanged.

Be sure to call through to the superclass when overriding this function. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#?` findOnBackInvokedDispatcher

Walk up the View hierarchy to find the nearest `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#`.

<br />

`T` findViewById

Finds the first descendant view with the given ID, the view itself if the ID matches getId, or `null` if the ID is invalid (\< 0) or there is no matching view in the hierarchy.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

<br />

`T` findViewWithTag

Look for a child view with the given tag. If this view has the given tag, return this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` fitSystemWindows

Called by the view hierarchy when the content insets for a window have changed, to allow it to adjust its content to fit within those windows. The content insets tell you the space that the status bar, input method, and other system windows infringe on the application's window.

You do not normally need to deal with this function, since the default window decoration given to applications takes care of applying it to the content of the window. If you use `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int` this will not be the case, and your content can be placed under those system elements. You can then use this method within your view hierarchy if you have parts of your UI which you would like to ensure are not being covered.

The default implementation of this method simply applies the content insets to the view's padding, consuming that content (modifying the insets to be 0), and returning true. This behavior is off by default, but can be enabled through setFitsSystemWindows.

This function's traversal down the hierarchy is depth-first. The same content insets object is propagated down the hierarchy, so any changes made to it will be seen by all following views (including potentially ones above in the hierarchy since this is a depth-first traversal). The first view that returns true will abort the entire traversal.

The default implementation works well for a situation where it is used with a container that covers the entire window, allowing it to apply the appropriate insets to its content on all edges. If you need a more complicated layout (such as two different views fitting system windows, one on the top of the window, and one on the bottom), you can override the method and handle the insets however you would like. Note that the insets provided by the framework are always relative to the far edges of the window, not accounting for the location of the called view within that window. (In fact when this method is called you do not yet know where the layout will place the view, as it is done before layout happens.)

Note: unlike many View methods, there is no dispatch phase to this call. If you are overriding it in a ViewGroup and want to allow the call to continue to your children, you must be sure to call the super implementation.

Here is a sample layout that makes use of fitting system windows to have controls for a video view placed inside of the window decorations that it hides and shows. This can be used with code like the second sample (video player) shown in setSystemUiVisibility.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` focusSearch

Find the nearest view in the specified direction that can take focus. This does not actually give focus to that view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` forceHasOverlappingRendering

Sets the behavior for overlapping rendering for this view (see hasOverlappingRendering for more details on this behavior). Calling this method is an alternative to overriding hasOverlappingRendering in a subclass, providing the value which is then used internally. That is, when forceHasOverlappingRendering is called, the value of hasOverlappingRendering is ignored and the value passed into this method is used instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` forceLayout

Forces this view to be laid out during the next layout pass. This method does not call requestLayout() or forceLayout() on the parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` generateDisplayHash

Called to generate a `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHash.html#` for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` generateViewId

Generate a value suitable for use in setId. This value will not collide with ID values generated at build time by aapt for R.id.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#!` getAccessibilityDelegate

Returns the delegate for implementing accessibility support via composition. For more details see `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getAccessibilityLiveRegion

Gets the live region mode for this View.

<br />

`https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider.html#!` getAccessibilityNodeProvider

Gets the provider for managing a virtual view hierarchy rooted at this View and reported to `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s that explore the window content.

If this method returns an instance, this instance is responsible for managing `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#`s describing the virtual sub-tree rooted at this View including the one representing the View itself. Similarly the returned instance is responsible for performing accessibility actions on any virtual view or the root view itself.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its getAccessibilityNodeProvider is responsible for handling this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` getAccessibilityPaneTitle

Get the title of the pane for purposes of accessibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getAccessibilityTraversalAfter

Gets the id of a view after which this one is visited in accessibility traversal.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getAccessibilityTraversalBefore

Gets the id of a view before which this one is visited in accessibility traversal.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` getAllowedHandwritingDelegatePackageName

Returns the allowed package for delegate editor views for which this view may act as a handwriting delegator, as set by setAllowedHandwritingDelegatePackage. If setAllowedHandwritingDelegatePackage has not been called, or called with `null` argument, this will return `null`, meaning that this delegator view may only be used to initiate handwriting mode for a delegate editor view from the same package as this delegator view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` getAllowedHandwritingDelegatorPackageName

Returns the allowed package for views which may act as a handwriting delegator for this delegate editor view, as set by setAllowedHandwritingDelegatorPackage. If setAllowedHandwritingDelegatorPackage has not been called, or called with `null` argument, this will return `null`, meaning that only views from the same package as this delegator editor view may act as a handwriting delegator.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getAlpha

The opacity of the view. This is a value from 0 to 1, where 0 means the view is completely transparent and 1 means the view is completely opaque.

By default this is 1.0f.

<br />

`https://developer.android.com/reference/kotlin/android/view/animation/Animation.html#!` getAnimation

Get the animation currently associated with this view.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#?` getAnimationMatrix

Return the current transformation matrix of the view. This is used in animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`. Returns `null` when there is no transformation provided by setAnimationMatrix. Application developers should use transformation methods like setRotation, setScaleX, setScaleX, setTranslationX} and setTranslationY (float)}} instead.

<br />

`https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` getApplicationWindowToken

Retrieve a unique token identifying the top-level "real" window of the window that this view is attached to. That is, this is like getWindowToken, except if the window this view in is a panel window (attached to another containing window), then the token of the containing window is returned instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` getAttributeResolutionStack

Returns the ordered list of resource ID that are considered when resolving attribute values for this `https://developer.android.com/reference/kotlin/android/view/View.html#`. The list will include layout resource ID if the View is inflated from XML. It will also include a set of explicit styles if specified in XML using `style="..."`. Finally, it will include the default styles resolved from the theme.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` getAttributeSourceResourceMap

Returns the mapping of attribute resource ID to source resource ID where the attribute value was set. Source resource ID can either be a layout resource ID, if the value was set in XML within the View tag, or a style resource ID, if the attribute was set in a style. The source resource value will be one of the resource IDs from getAttributeSourceResourceMap.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` getAutofillHints

Gets the hints that help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how to autofill the view with the user's data.

See setAutofillHints for more info about these hints.

<br />

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#!` getAutofillId

Gets the unique, logical identifier of this view in the activity, for autofill purposes.

The autofill id is created on demand, unless it is explicitly set by setAutofillId.

See setAutofillId for more info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getAutofillType

Describes the autofill type of this view, so an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` can create the proper `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` when autofilling the view.

By default returns `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_NONE:kotlin.Int`, but views should override it to properly support the Autofill Framework.

<br />

`https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#?` getAutofillValue

Gets the `https://developer.android.com/reference/kotlin/android/view/View.html#`'s current autofill value.

By default returns `null`, but subclasses should override it and return an appropriate value to properly support the Autofill Framework.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` getBackground

Gets the background drawable

<br />

`https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?` getBackgroundTintBlendMode

Return the blending mode used to apply the tint to the background drawable, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?` getBackgroundTintList

Return the tint applied to the background drawable, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?` getBackgroundTintMode

Return the blending mode used to apply the tint to the background drawable, if specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getBaseline

Return the offset of the widget's text baseline from the widget's top boundary. If this widget does not support baseline alignment, this method returns -1.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getBottom

Bottom position of this view relative to its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getBottomFadingEdgeStrength

Returns the strength, or intensity, of the bottom faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getBottomPaddingOffset

Amount by which to extend the bottom fading region. Called only when isPaddingOffsetRequired returns true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getCameraDistance

Gets the distance along the Z axis from the camera to this view.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!` getClipBounds

Returns a copy of the current setClipBounds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getClipBounds

Populates an output rectangle with the clip bounds of the view, returning `true` if successful or `false` if the view's clip bounds are `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getClipToOutline

Returns whether the Outline should be used to clip the contents of the View.

Note that this flag will only be respected if the View's Outline returns true from canClip.

<br />

`https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession.html#?` getContentCaptureSession

Gets the session used to notify content capture events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` getContentDescription

Returns the `https://developer.android.com/reference/kotlin/android/view/View.html#`'s content description.

**Note:** Do not override this method, as it will have no effect on the content description presented to accessibility services. You must call setContentDescription to modify the content description.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getContentSensitivity

Gets content sensitivity mode to determine whether this view displays sensitive content.

See setContentSensitivity and isContentSensitive for more info about this mode.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` getContext

Returns the context the view is running in, through which it can access the current theme, resources, etc.

<br />

`https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#!` getContextMenuInfo

Views should implement this if they have extra information to associate with the context menu. The return result is supplied as a parameter to the onCreateContextMenu callback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getDefaultFocusHighlightEnabled

Returns whether this View should use a default focus highlight when it gets focused but doesn't have `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` defined in its background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getDefaultSize

Utility to return a default size. Uses the supplied size if the MeasureSpec imposed no constraints. Will get larger if allowed by the MeasureSpec.

<br />

`https://developer.android.com/reference/kotlin/android/view/Display.html#!` getDisplay

Gets the logical display to which the view's window has been attached.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` getDrawableState

Return an array of resource IDs of the drawable states representing the current state of the view.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!` getDrawingCache

Calling this method is equivalent to calling `getDrawingCache(false)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!` getDrawingCache

Returns the bitmap in which this view drawing is cached. The returned bitmap is null when caching is disabled. If caching is enabled and the cache is not ready, this method will create it. Calling draw will not draw from the cache when the cache is enabled. To benefit from the cache, you must request the drawing cache by calling this method and draw it on screen if the returned bitmap is not null.

Note about auto scaling in compatibility mode: When auto scaling is not enabled, this method will create a bitmap of the same size as this view. Because this bitmap will be drawn scaled by the parent ViewGroup, the result on screen might show scaling artifacts. To avoid such artifacts, you should call this method by setting the auto scaling to true. Doing so, however, will generate a bitmap of a different size than the view. This implies that your application must be able to handle this size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getDrawingCacheBackgroundColor

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getDrawingCacheQuality

Returns the quality of the drawing cache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` getDrawingRect

Return the visible drawing bounds of your view. Fills in the output rectangle with the values from getScrollX(), getScrollY(), getWidth(), and getHeight(). These bounds do not account for any transformation properties currently set on the view, such as setScaleX or setRotation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` getDrawingTime

Return the time at which the drawing of the view hierarchy started.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getElevation

The base elevation of this view relative to its parent, in pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getExplicitStyle

Returns the resource ID for the style specified using `style="..."` in the `https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#`'s backing XML element or `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int` otherwise if not specified or otherwise not applicable.

Each `https://developer.android.com/reference/kotlin/android/view/View.html#` can have an explicit style specified in the layout file. This style is used first during the `https://developer.android.com/reference/kotlin/android/view/View.html#` attribute resolution, then if an attribute is not defined there the resource system looks at default style and theme as fallbacks.

**Note:** this method will only return actual values if the view attribute debugging is enabled in Android developer options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getFilterTouchesWhenObscured

Gets whether the framework should discard touches when the view's window is obscured by another visible window at the touched location. Refer to the `https://developer.android.com/reference/kotlin/android/view/View.html#` security documentation for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getFitsSystemWindows

Check for state of setFitsSystemWindows. If this method returns `true`, the default implementation of fitSystemWindows will be executed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getFocusable

Returns the focusable setting for this view.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!>!` getFocusables

Find and return all focusable views that are descendants of this view, possibly including this view if it is focusable itself.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` getFocusedRect

When a view has focus and the user navigates away from it, the next view is searched for starting from the rectangle filled in by this method. By default, the rectangle is the getDrawingRect) of the view. However, if your view maintains some idea of internal selection, such as a cursor, or a selected row or column, you should override this method and fill in a more specific rectangle.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` getForeground

Returns the drawable used as the foreground of this View. The foreground drawable, if non-null, is always drawn on top of the view's content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getForegroundGravity

Describes how the foreground is positioned.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?` getForegroundTintBlendMode

Return the blending mode used to apply the tint to the foreground drawable, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?` getForegroundTintList

Return the tint applied to the foreground drawable, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?` getForegroundTintMode

Return the blending mode used to apply the tint to the foreground drawable, if specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getFrameContentVelocity

Get the current velocity of the View. The value should always be greater than or equal to 0. Note that this is only valid till the next drawn frame.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getGlobalVisibleRect

Sets `r` to the coordinates of the non-clipped area of this view in the coordinate space of the view's root view.

See getGlobalVisibleRect for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getGlobalVisibleRect

Sets `r` to the coordinates of the non-clipped area of this view in the coordinate space of the view's root view. Sets `globalOffset` to the offset of the view's x and y coordinates from the coordinate space origin, which is the top left corner of the root view irrespective of screen decorations and system UI elements.

To convert `r` to coordinates relative to the top left corner of this view (without taking view rotations into account), offset `r` by the inverse values of `globalOffset`---`r.offset(-globalOffset.x, -globalOffset.y)`---which is equivalent to calling getLocalVisibleRect.

**Note:** Do not use this method to determine the size of a window in multi-window mode; use getCurrentWindowMetrics.

<br />

`https://developer.android.com/reference/kotlin/android/os/Handler.html#!` getHandler

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getHandwritingBoundsOffsetBottom

Return the amount of offset applied to the bottom edge of this view's handwriting bounds, in the unit of pixel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getHandwritingBoundsOffsetLeft

Return the amount of offset applied to the left edge of this view's handwriting bounds, in the unit of pixel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getHandwritingBoundsOffsetRight

Return the amount of offset applied to the right edge of this view's handwriting bounds, in the unit of pixel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getHandwritingBoundsOffsetTop

Return the amount of offset applied to the top edge of this view's handwriting bounds, in the unit of pixel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getHandwritingDelegateFlags

Returns flags configuring the handwriting delegation behavior for this delegate editor view, as set by setHandwritingDelegateFlags.

<br />

`https://developer.android.com/reference/kotlin/java/lang/Runnable.html#?` getHandwritingDelegatorCallback

Returns the callback set by setHandwritingDelegatorCallback which should be called when a stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#` occurs within this view's bounds. The callback should only be called from the UI thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getHasOverlappingRendering

Returns the value for overlapping rendering that is used internally. This is either the value passed into forceHasOverlappingRendering, if called, or the return value of hasOverlappingRendering, otherwise.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getHeight

Return the height of your view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` getHitRect

Hit rectangle in parent's coordinates

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getHorizontalFadingEdgeLength

Returns the size of the horizontal faded edges used to indicate that more content in this view is visible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getHorizontalScrollbarHeight

Returns the height of the horizontal scrollbar.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` getHorizontalScrollbarThumbDrawable

Returns the currently configured Drawable for the thumb of the horizontal scroll bar if it exists, null otherwise.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` getHorizontalScrollbarTrackDrawable

Returns the currently configured Drawable for the track of the horizontal scroll bar if it exists, null otherwise.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getId

Returns this view's identifier.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getImportantForAccessibility

Gets the mode for determining whether this View is important for accessibility. A view is important for accessibility if it fires accessibility events and if it is reported to accessibility services that query the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getImportantForAutofill

Gets the mode for determining whether this view is important for autofill.

See setImportantForAutofill and isImportantForAutofill for more info about this mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getImportantForContentCapture

Gets the mode for determining whether this view is important for content capture.

See setImportantForContentCapture and isImportantForContentCapture for more info about this mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getKeepScreenOn

Returns whether the screen should remain on, corresponding to the current value of `https://developer.android.com/reference/kotlin/android/view/View.html#KEEP_SCREEN_ON:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState.html#!` getKeyDispatcherState

Return the global `https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState.html#` for this view's window. Returns null if the view is not currently attached to the window. Normally you will not need to use this directly, but just use the standard high-level event callbacks like onKeyDown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getLabelFor

Gets the id of a view for which this view serves as a label for accessibility purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getLayerType

Indicates what type of layer is currently associated with this view. By default a view does not have a layer, and the layer type is `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_NONE:kotlin.Int`. Refer to the documentation of setLayerType for more information on the different types of layers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getLayoutDirection

Returns the resolved layout direction for this view.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#!` getLayoutParams

Get the LayoutParams associated with this view. All views should have layout parameters. These supply parameters to the *parent* of this view specifying how it should be arranged. There are many subclasses of ViewGroup.LayoutParams, and these correspond to the different subclasses of ViewGroup that are responsible for arranging their children. This method may return null if this View is not attached to a parent ViewGroup or setLayoutParams was not invoked successfully. When a View is attached to a parent ViewGroup, this method must not return null.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getLeft

Left position of this view relative to its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getLeftFadingEdgeStrength

Returns the strength, or intensity, of the left faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getLeftPaddingOffset

Amount by which to extend the left fading region. Called only when isPaddingOffsetRequired returns true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getLocalVisibleRect

Sets `r` to the coordinates of the non-clipped area of this view relative to the top left corner of the view.

If the view is clipped on the left or top, the left and top coordinates are offset from 0 by the clipped amount. For example, if the view is off screen 50px on the left and 30px at the top, the left and top coordinates are 50 and 30 respectively.

If the view is clipped on the right or bottom, the right and bottom coordinates are reduced by the clipped amount. For example, if the view is off screen 40px on the right and 20px at the bottom, the right coordinate is the view width - 40, and the bottom coordinate is the view height - 20.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` getLocationInSurface

Gets the coordinates of this view in the coordinate space of the `https://developer.android.com/reference/kotlin/android/view/Surface.html#` that contains the view.

In multiple-screen scenarios, if the surface spans multiple screens, the coordinate space of the surface also spans multiple screens.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` getLocationInWindow

Gets the coordinates of this view in the coordinate space of the window that contains the view, irrespective of system decorations.

In multi-window mode, the origin of the coordinate space is the top left corner of the window that contains the view. In full screen mode, the origin is the top left corner of the device screen.

In multiple-screen scenarios, if the app spans multiple screens, the coordinate space also spans multiple screens. But if the app is restricted to a single screen, the coordinate space includes only the screen on which the app is running.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` getLocationOnScreen

Gets the coordinates of this view in the coordinate space of the device screen, irrespective of system decorations and whether the system is in multi-window mode.

In multi-window mode, the coordinate space encompasses the entire device screen, ignoring the bounds of the app window. For example, if the view is in the bottom portion of a horizontal split screen, the top edge of the screen---not the top edge of the window---is the origin from which the y-coordinate is calculated.

In multiple-screen scenarios, the coordinate space can span screens. For example, if the app is spanning both screens of a dual-screen device and the view is located on the right-hand screen, the x-coordinate is calculated from the left edge of the left-hand screen to the left edge of the view. When the app is restricted to a single screen in a multiple-screen environment, the coordinate space includes only the screen on which the app is running.

After the method returns, the argument array contains the x and y coordinates of the view relative to the view's left and top edges, respectively.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#!` getMatrix

The transform matrix of this view, which is calculated based on the current rotation, scale, and pivot properties.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getMeasuredHeight

Like getMeasuredHeightAndState, but only returns the raw height component (that is the result is masked by `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_SIZE_MASK:kotlin.Int`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getMeasuredHeightAndState

Return the full height measurement information for this view as computed by the most recent call to measure. This result is a bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_STATE_TOO_SMALL:kotlin.Int`. This should be used during measurement and layout calculations only. Use getHeight to see how high a view is after layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getMeasuredState

Return only the state bits of getMeasuredWidthAndState and getMeasuredHeightAndState, combined into one integer. The width component is in the regular bits `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_STATE_MASK:kotlin.Int` and the height component is at the shifted bits `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_HEIGHT_STATE_SHIFT:kotlin.Int`\>\>`https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_STATE_MASK:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getMeasuredWidth

Like getMeasuredWidthAndState, but only returns the raw width component (that is the result is masked by `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_SIZE_MASK:kotlin.Int`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getMeasuredWidthAndState

Return the full width measurement information for this view as computed by the most recent call to measure. This result is a bit mask as defined by `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_SIZE_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_STATE_TOO_SMALL:kotlin.Int`. This should be used during measurement and layout calculations only. Use getWidth to see how wide a view is after layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getMinimumHeight

Returns the minimum height of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getMinimumWidth

Returns the minimum width of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getNextClusterForwardId

Gets the id of the root of the next keyboard navigation cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getNextFocusDownId

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_DOWN:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getNextFocusForwardId

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_FORWARD:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getNextFocusLeftId

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_LEFT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getNextFocusRightId

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_RIGHT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getNextFocusUpId

Gets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_UP:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.OnFocusChangeListener.html#!` getOnFocusChangeListener

Returns the focus-change callback registered for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getOutlineAmbientShadowColor

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#!` getOutlineProvider

Returns the current `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#` of the view, which generates the Outline that defines the shape of the shadow it casts, and enables outline clipping.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getOutlineSpotShadowColor

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getOverScrollMode

Returns the over-scroll mode for this view. The result will be one of `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_ALWAYS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int` (allow over-scrolling only if the view content is larger than the container), or `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_NEVER:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getPaddingBottom

Returns the bottom padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getPaddingEnd

Returns the end padding of this view depending on its resolved layout direction. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getPaddingLeft

Returns the left padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getPaddingRight

Returns the right padding of this view. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getPaddingStart

Returns the start padding of this view depending on its resolved layout direction. If there are inset and enabled scrollbars, this value may include the space required to display the scrollbars as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getPaddingTop

Returns the top padding of this view.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewParent.html#!` getParent

Gets the parent of this view. Note that the parent is a ViewParent and not necessarily a View.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewParent.html#!` getParentForAccessibility

Gets the parent for accessibility purposes. Note that the parent for accessibility is not necessary the immediate parent. It is the first predecessor that is important for accessibility.

<br />

`https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#!, https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException.html#!>?` getPendingCredentialCallback

Returns the callback that has previously been set up on this view through the setPendingCredentialRequest API. If the return value is null, that means no callback, or request, has been set on the view and no `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` flow will be invoked when this view is focused. Traditioanl autofill flows will still work, and autofillable content will still be returned through the autofill )} API.

See setPendingCredentialRequest for more info.

<br />

`https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#?` getPendingCredentialRequest

Returns the `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#` associated with the view. If the return value is null, that means no request has been set on the view and no `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` flow will be invoked when this view is focused. Traditioanl autofill flows will still work, autofilling content if applicable, from the active `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` on the device.

See setPendingCredentialRequest for more info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getPivotX

The x location of the point around which the view is setRotation and setScaleX.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getPivotY

The y location of the point around which the view is setRotation and setScaleY.

<br />

`https://developer.android.com/reference/kotlin/android/view/PointerIcon.html#!` getPointerIcon

Gets the mouse pointer icon for the current view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>` getPreferKeepClearRects

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` getReceiveContentMimeTypes

Returns the MIME types accepted by performReceiveContent for this view, as configured via setOnReceiveContentListener. By default returns null.

Different features (e.g. pasting from the clipboard, inserting stickers from the soft keyboard, etc) may optionally use this metadata to conditionally alter their behavior. For example, a soft keyboard may choose to hide its UI for inserting GIFs for a particular input field if the MIME types returned here for that field don't include "image/gif" or "image/\*".

Note: Comparisons of MIME types should be performed using utilities such as compareMimeTypes rather than simple string equality, in order to correctly handle patterns such as "text/\*", "image/\*", etc. Note that MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lowercase letters, or use normalizeMimeType to ensure that it is converted to lowercase.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getRequestedFrameRate

Get the current preferred frame rate of the View. The value could be negative when preferred frame rate category is set instead of perferred frame rate. The frame rate category includes REQUESTED_FRAME_RATE_CATEGORY_NO_PREFERENCE, REQUESTED_FRAME_RATE_CATEGORY_LOW, REQUESTED_FRAME_RATE_CATEGORY_NORMAL, and REQUESTED_FRAME_RATE_CATEGORY_HIGH. Note that the frame rate value is valid as long as the View is invalidated. Please also be aware that the requested frame rate will not propagate to child views when this API is used on a ViewGroup.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` getResources

Returns the resources associated with this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getRevealOnFocusHint

Returns this view's preference for reveal behavior when it gains focus.

When this method returns true for a child view requesting focus, ancestor views responding to a focus change in requestChildFocus should make a best effort to make the newly focused child fully visible to the user. When it returns false, ancestor views should preferably not disrupt scroll positioning or other properties affecting visibility to the user as part of the focus change.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getRight

Right position of this view relative to its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getRightFadingEdgeStrength

Returns the strength, or intensity, of the right faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getRightPaddingOffset

Amount by which to extend the right fading region. Called only when isPaddingOffsetRequired returns true.

<br />

`https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.html#?` getRootSurfaceControl

The AttachedSurfaceControl itself is not a View, it is just the interface to the windowing-system object that contains the entire view hierarchy. For the root View of a given hierarchy see getRootView.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` getRootView

Finds the topmost view in the current view hierarchy.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#!` getRootWindowInsets

Provide original WindowInsets that are dispatched to the view hierarchy. The insets are only available if the view is attached.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getRotation

The degrees that the view is rotated around the pivot point.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getRotationX

The degrees that the view is rotated around the horizontal axis through the pivot point.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getRotationY

The degrees that the view is rotated around the vertical axis through the pivot point.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getScaleX

The amount that the view is scaled in x around the pivot point, as a proportion of the view's unscaled width. A value of 1, the default, means that no scaling is applied.

By default, this is 1.0f.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getScaleY

The amount that the view is scaled in y around the pivot point, as a proportion of the view's unscaled height. A value of 1, the default, means that no scaling is applied.

By default, this is 1.0f.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getScrollBarDefaultDelayBeforeFade

Returns the delay before scrollbars fade.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getScrollBarFadeDuration

Returns the scrollbar fade duration.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getScrollBarSize

Returns the scrollbar size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getScrollBarStyle

Returns the current scrollbar style.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getScrollCaptureHint

Returns the current scroll capture hint for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getScrollIndicators

Returns a bitmask representing the enabled scroll indicators.

For example, if the top and left scroll indicators are enabled and all other indicators are disabled, the return value will be `View.SCROLL_INDICATOR_TOP | View.SCROLL_INDICATOR_LEFT`.
| --- | --- |

To check whether the bottom scroll indicator is enabled, use the value of `(getScrollIndicators() & View.SCROLL_INDICATOR_BOTTOM) != 0`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getScrollX

Return the scrolled left position of this view. This is the left edge of the displayed part of your view. You do not need to draw any pixels farther left, since those are outside of the frame of your view on screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getScrollY

Return the scrolled top position of this view. This is the top edge of the displayed part of your view. You do not need to draw any pixels above it, since those are outside of the frame of your view on screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getSolidColor

Override this if your view is known to always be drawn on top of a solid color background, and needs to draw fading edges. Returning a non-zero color enables the view system to optimize the drawing of the fading edges. If you do return a non-zero color, the alpha should be set to 0xFF.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getSourceLayoutResId

A `https://developer.android.com/reference/kotlin/android/view/View.html#` can be inflated from an XML layout. For such Views this method returns the resource ID of the source layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` getStateDescription

Returns the `https://developer.android.com/reference/kotlin/android/view/View.html#`'s state description.

**Note:** Do not override this method, as it will have no effect on the state description presented to accessibility services. You must call setStateDescription to modify the state description.

<br />

`https://developer.android.com/reference/kotlin/android/animation/StateListAnimator.html#!` getStateListAnimator

Returns the current StateListAnimator if exists.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getSuggestedMinimumHeight

Returns the suggested minimum height that the view should use. This returns the maximum of the view's minimum height and the background's minimum height (getMinimumHeight).

When being used in onMeasure, the caller should still ensure the returned height is within the requirements of the parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getSuggestedMinimumWidth

Returns the suggested minimum width that the view should use. This returns the maximum of the view's minimum width and the background's minimum width (getMinimumWidth).

When being used in onMeasure, the caller should still ensure the returned width is within the requirements of the parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` getSupplementalDescription

Returns the `https://developer.android.com/reference/kotlin/android/view/View.html#`'s supplemental description.

A supplemental description provides brief supplemental information for this node, such as the purpose of the node when that purpose is not conveyed within its textual representation. For example, if a dropdown select has a purpose of setting font family, the supplemental description could be "font family". If this node has children, its supplemental description serves as additional information and is not intended to replace any existing information in the subtree. This is different from the getContentDescription in that this description is purely supplemental while a content description may be used to replace a description for a node or its subtree that an assistive technology would otherwise compute based on other properties of the node and its descendants.

**Note:** Do not override this method, as it will have no effect on the supplemental description presented to accessibility services. You must call setSupplementalDescription to modify the supplemental description.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!>` getSystemGestureExclusionRects

Retrieve the list of areas within this view's post-layout coordinate space where the system should not intercept touch or other pointing device gestures.

Do not modify the returned list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getSystemUiVisibility

Returns the last setSystemUiVisibility that this view has requested.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` getTag

Returns this view's tag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` getTag

Returns the tag associated with this view and the specified key.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getTextAlignment

Return the resolved text alignment.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getTextDirection

Return the resolved text direction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` getTooltipText

Returns the view's tooltip text. **Note:** Do not override this method, as it will have no effect on the text displayed in the tooltip. You must call setTooltipText to modify the tooltip text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getTop

Top position of this view relative to its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getTopFadingEdgeStrength

Returns the strength, or intensity, of the top faded edge. The strength is a value between 0.0 (no fade) and 1.0 (full fade). The default implementation returns 0.0 or 1.0 but no value in between. Subclasses should override this method to provide a smoother fade transition when scrolling occurs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getTopPaddingOffset

Amount by which to extend the top fading region. Called only when isPaddingOffsetRequired returns true.

<br />

`https://developer.android.com/reference/kotlin/android/view/TouchDelegate.html#!` getTouchDelegate

Gets the TouchDelegate for this View.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!>!` getTouchables

Find and return all touchable views that are descendants of this view, possibly including this view if it is touchable itself.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getTransitionAlpha

This property is intended only for use by the Fade transition, which animates it to produce a visual translucency that does not side-effect (or get affected by) the real alpha property. This value is composited with the other alpha value (and the AlphaAnimation value, when that is present) to produce a final visual translucency result, which is what is passed into the DisplayList.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` getTransitionName

Returns the name of the View to be used to identify Views in Transitions. Names should be unique in the View hierarchy.

This returns null if the View has not been given a name.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getTranslationX

The horizontal location of this view relative to its getLeft position. This position is post-layout, in addition to wherever the object's layout placed it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getTranslationY

The vertical location of this view relative to its getTop position. This position is post-layout, in addition to wherever the object's layout placed it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getTranslationZ

The depth location of this view relative to its getElevation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` getUniqueDrawingId

Get the identifier used for this view by the drawing system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getVerticalFadingEdgeLength

Returns the size of the vertical faded edges used to indicate that more content in this view is visible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getVerticalScrollbarPosition

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` getVerticalScrollbarThumbDrawable

Returns the currently configured Drawable for the thumb of the vertical scroll bar if it exists, null otherwise.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` getVerticalScrollbarTrackDrawable

Returns the currently configured Drawable for the track of the vertical scroll bar if it exists, null otherwise.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getVerticalScrollbarWidth

Returns the width of the vertical scrollbar.

<br />

`https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse.html#?` getViewTranslationResponse

Returns the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse.html#` associated with this view. The response will be set when the translation is done then onViewTranslationResponse is called. The `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback.html#` can use to get `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse.html#` to display the translated information.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.html#!` getViewTreeObserver

Returns the ViewTreeObserver for this view's hierarchy. The view tree observer can be used to get notifications when global events, like layout, happen. The returned ViewTreeObserver observer is not guaranteed to remain valid for the lifetime of this View. If the caller of this method keeps a long-lived reference to ViewTreeObserver, it should always check for the return value of isAlive.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getVisibility

Returns the visibility status for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getWidth

Return the width of your view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getWindowAttachCount

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowId.html#!` getWindowId

Retrieve the `https://developer.android.com/reference/kotlin/android/view/WindowId.html#` for the window this view is currently attached to.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.html#?` getWindowInsetsController

Retrieves the single `https://developer.android.com/reference/kotlin/android/view/WindowInsetsController.html#` of the window this view is attached to.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getWindowSystemUiVisibility

Returns the current system UI visibility that is currently set for the entire window. This is the combination of the setSystemUiVisibility values supplied by all of the views in the window.

<br />

`https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` getWindowToken

Retrieve a unique token identifying the window this view is attached to.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getWindowVisibility

Returns the current visibility of the window this view is attached to (either `https://developer.android.com/reference/kotlin/android/view/View.html#GONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` getWindowVisibleDisplayFrame

Retrieve the overall visible display size in which the window this view is attached to has been positioned in. This takes into account screen decorations above the window, for both cases where the window itself is being position inside of them or the window is being placed under then and covered insets are used for the window to position its content inside. In effect, this tells you the available area where content can be placed and remain visible to users.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getX

The visual x position of this view, in pixels. This is equivalent to the setTranslationX property plus the current getLeft property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getY

The visual y position of this view, in pixels. This is equivalent to the setTranslationY property plus the current getTop property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` getZ

The visual z position of this view, in pixels. This is equivalent to the setTranslationZ property plus the current getElevation property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasExplicitFocusable

Returns true if this view is focusable or if it contains a reachable View for which hasExplicitFocusable returns `true`. A "reachable hasExplicitFocusable()" is a view whose parents do not block descendants focus. Only `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` views for which getFocusable would return `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSABLE:kotlin.Int` are considered focusable.

This method preserves the pre-`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` behavior of hasFocusable in that only views explicitly set focusable will cause this method to return true. A view set to `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSABLE_AUTO:kotlin.Int` that resolves to focusable will not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasFocusable

Returns true if this view is focusable or if it contains a reachable View for which hasFocusable returns `true`. A "reachable hasFocusable()" is a view whose parents do not block descendants focus. Only `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` views are considered focusable.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` views that are determined to be focusable through `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSABLE_AUTO:kotlin.Int` will also cause this method to return `true`. Apps that declare a `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#targetSdkVersion:kotlin.Int` of earlier than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` will continue to see this method return `false` for views not explicitly marked as focusable. Use hasExplicitFocusable if you require the pre-`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasNestedScrollingParent

Returns true if this view has a nested scrolling parent.

The presence of a nested scrolling parent indicates that this view has initiated a nested scroll and it was accepted by an ancestor view further up the view hierarchy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasOnClickListeners

Return whether this view has an attached OnClickListener. Returns true if there is a listener, false if there is none.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasOnLongClickListeners

Return whether this view has an attached OnLongClickListener. Returns true if there is a listener, false if there is none.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasOverlappingRendering

Returns whether this View has content which overlaps.

This function, intended to be overridden by specific View types, is an optimization when alpha is set on a view. If rendering overlaps in a view with alpha \< 1, that view is drawn to an offscreen buffer and then composited into place, which can be expensive. If the view has no overlapping rendering, the view can draw each primitive with the appropriate alpha value directly. An example of overlapping rendering is a TextView with a background image, such as a Button. An example of non-overlapping rendering is a TextView with no background, or an ImageView with only the foreground image. The default implementation returns true; subclasses should override if they have cases which can be optimized.

**Note:** The return value of this method is ignored if forceHasOverlappingRendering has been called on this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasPointerCapture

Checks pointer capture status.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` hasWindowFocus

Returns true if this view is in a window that currently has window focus. Note that this is not the same as the view itself having focus.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` inflate

Inflate a view from an XML resource. This convenience method wraps the `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` class, which provides a full range of options for view inflation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` invalidate

Invalidate the whole view. If the view is visible, onDraw will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call postInvalidate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` invalidate

Mark the area defined by dirty as needing to be drawn. If the view is visible, onDraw will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call postInvalidate.

**WARNING:** In API 19 and below, this method may be destructive to `dirty`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` invalidate

Mark the area defined by the rect (l,t,r,b) as needing to be drawn. The coordinates of the dirty rect are relative to the view. If the view is visible, onDraw will be called at some point in the future.

This must be called from a UI thread. To call from a non-UI thread, call postInvalidate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` invalidateDrawable

Invalidates the specified Drawable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` invalidateOutline

Called to rebuild this View's Outline from its `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isAccessibilityDataSensitive

Whether this view should restrict accessibility service access only to services that have the isAccessibilityTool property set to true.

See default behavior provided by `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_DATA_SENSITIVE_AUTO:kotlin.Int`. Otherwise, returns true for `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_DATA_SENSITIVE_YES:kotlin.Int` or false for `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_DATA_SENSITIVE_NO:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isAccessibilityFocused

Returns whether this View is accessibility focused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isAccessibilityHeading

Gets whether this view is a heading for accessibility purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isActivated

Indicates the activation state of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isAttachedToWindow

Returns true if this view is currently attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isAutoHandwritingEnabled

Return whether the View allows automatic handwriting initiation. Returns true if automatic handwriting initiation is enabled, and vice versa.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isClickable

Indicates whether this view reacts to click events or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isContentCaptureSelfReportingEnabled

Returns whether this View automatically reports its lifecycle events and layout bounds to the Content Capture Version 2.

By default, this method returns `true`, which instructs the Android View system to automatically track this view's visibility, position, layout bounds, and structural changes and report them directly to the active `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession.html#`.

Views can override this method to return `false` to disable this automatic monitoring and take full manual control over when and how their properties are reported. This is particularly useful for Views that participate in hybrid hierarchies that can nest Views and Virtual Views bidirectionally. By disabling this behavior, the View itself can choose its own parent id and report the relative bounds to that parent in the Content Capture hierarchy.

#### Important for Content Capture Status and Self Reporting

setImportantForContentCapture can influence whether this View is reported to the Content Capture entirely, e.g. `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_CONTENT_CAPTURE_NO:kotlin.Int` also disables self reporting. However, not being important for Content Capture influences how descendant nodes are reported. If this View were to be set as **NOT** important for Content Capture, its children will skip this View while finding their parent id and relative bounds to that parent. Therefore, if this View needs to still act as a parent to its children in Content Capture hierarchy, but needs to control how itself is reported, overriding this method and returning `false` is recommended.

**Note:** If this method returns `false`, the view is fully responsible for notifying the system about its lifecycle and property updates by calling methods such as notifyNodeAppearedOrChanged and notifyNodeDisappeared on the main thread.
This methods belongs to Content Capture Version 2.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isContentSensitive

Returns whether this view displays sensitive content, based on the value explicitly set by setContentSensitivity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isContextClickable

Indicates whether this view reacts to context clicks or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isCredential

Gets the mode for determining whether this view is a credential.

See setIsCredential.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isDirty

True if this view has changed since the last time being drawn.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isDrawingCacheEnabled

Indicates whether the drawing cache is enabled for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isDuplicateParentStateEnabled

Indicates whether this duplicates its drawable state from its parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isEnabled

Returns the enabled status for this view. The interpretation of the enabled state varies by subclass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isFocusable

Returns whether this View is currently able to take focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isFocusableInTouchMode

When a view is focusable, it may not want to take focus when in touch mode. For example, a button would like focus when the user is navigating via a D-pad so that the user can click on it, but once the user starts touching the screen, the button shouldn't take focus

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isFocused

Returns true if this view has focus

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isFocusedByDefault

Returns whether this View should receive focus when the focus is restored for the view hierarchy containing this view.

Focus gets restored for a view hierarchy when the root of the hierarchy gets added to a window or serves as a target of cluster navigation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isForceDarkAllowed

See setForceDarkAllowed

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isHandwritingDelegate

Returns whether this view has been set as a handwriting delegate by setIsHandwritingDelegate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isHapticFeedbackEnabled

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isHardwareAccelerated

Indicates whether this view is attached to a hardware accelerated window or not.

Even if this method returns true, it does not mean that every call to draw will be made with an hardware accelerated `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#`. For instance, if this view is drawn onto an offscreen `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` and its window is hardware accelerated, isHardwareAccelerated will likely return false, and this method will return true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isHorizontalFadingEdgeEnabled

Indicate whether the horizontal edges are faded when the view is scrolled horizontally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isHorizontalScrollBarEnabled

Indicate whether the horizontal scrollbar should be drawn or not. The scrollbar is not drawn by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isHovered

Returns true if the view is currently hovered.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isImportantForAccessibility

Computes whether this view should be exposed for accessibility. In general, views that are interactive or provide information are exposed while views that serve only as containers are hidden.

If an ancestor of this view has importance `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`, this method returns `false`.

Otherwise, the value is computed according to the view's getImportantForAccessibility value:

1. `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int`, return `false `
2. `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_YES:kotlin.Int`, return `true`
3. `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int`, return `true` if view satisfies any of the following:
 - Is actionable, e.g. isClickable, isLongClickable, isContextClickable, isScreenReaderFocusable, or isFocusable
 - Has an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#`
 - Has an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider.html#`
 - Has an interaction listener, e.g. `https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener.html#`, `https://developer.android.com/reference/kotlin/android/view/View.OnKeyListener.html#`, etc.
 - Is an accessibility live region, e.g. getAccessibilityLiveRegion is not `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int`.
4. Has an accessibility pane title, see setAccessibilityPaneTitle
5. Is an accessibility heading, see setAccessibilityHeading.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isImportantForAutofill

Hints the Android System whether the `https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.ViewNode.html#` associated with this view is considered important for autofill purposes.

Generally speaking, a view is important for autofill if:

1. The view can be autofilled by an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#`.
2. The view contents can help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how other views can be autofilled.
 1. For example, view containers should typically return `false` for performance reasons (since the important info is provided by their children), but if its properties have relevant information (for example, a resource id called `credentials`, it should return `true`. On the other hand, views representing labels or editable fields should typically return `true`, but in some cases they could return `false` (for example, if they're part of a "Captcha" mechanism).
 2. The value returned by this method depends on the value returned by getImportantForAutofill:
 1. if it returns `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`, then it returns `true`
 2. if it returns `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`, then it returns `false`
 3. if it returns `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`, then it uses some simple heuristics that can return `true` in some cases (like a container with a resource id), but `false` in most.
 4. otherwise, it returns `false`.
 3. The behavior of importances depends on Android version:
 1. For `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` and below:
 1. When a view is considered important for autofill:
 1. The view might automatically trigger an autofill request when focused on.
 2. The contents of the view are included in the `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` used in an autofill request.
 2. On the other hand, when a view is considered not important for autofill:
 1. The view never automatically triggers autofill requests, but it can trigger a manual request through requestAutofill.
 2. The contents of the view are not included in the `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` used in an autofill request, unless the request has the `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` flag.
 2. For `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and above:
 1. The system uses importance, along with other view properties and other optimization factors, to determine if a view should trigger autofill on focus.
 2. The contents of `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_YES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` views will be included in the `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` used in an autofill request.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isImportantForContentCapture

Hints the Android System whether this view is considered important for content capture, based on the value explicitly set by setImportantForContentCapture and heuristics when it's `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_CONTENT_CAPTURE_AUTO:kotlin.Int`.

See `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager.html#` for more info about content capture.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isInEditMode

Indicates whether this View is currently in edit mode. A View is usually in edit mode when displayed within a developer tool. For instance, if this View is being drawn by a visual user interface builder, this method should return true. Subclasses should check the return value of this method to provide different behaviors if their normal behavior might interfere with the host environment. For instance: the class spawns a thread in its constructor, the drawing code relies on device-specific features, etc. This method is usually checked in the drawing code of custom widgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isInLayout

Returns whether the view hierarchy is currently undergoing a layout pass. This information is useful to avoid situations such as calling requestLayout during a layout pass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isInTouchMode

Returns the touch mode state associated with this view. Attached views return the touch mode state from the associated window's display. Detached views just return the default touch mode value defined in `com.android.internal.R.bool.config_defaultInTouchMode`. Touch mode is entered once the user begins interacting with the device by touch, and affects various things like whether focus highlight is always visible to the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isKeyboardNavigationCluster

Returns whether this View is a root of a keyboard navigation cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isLaidOut

Returns true if this view has been through at least one layout since it was last attached to or detached from a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isLayoutDirectionResolved

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isLayoutRequested

Indicates whether or not this view's layout will be requested during the next hierarchy layout pass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isLongClickable

Indicates whether this view reacts to long click events or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isNestedScrollingEnabled

Returns true if nested scrolling is enabled for this view.

If nested scrolling is enabled and this View class implementation supports it, this view will act as a nested scrolling child view when applicable, forwarding data about the scroll operation in progress to a compatible and cooperating nested scrolling parent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isOpaque

Indicates whether this View is opaque. An opaque View guarantees that it will draw all the pixels overlapping its bounds using a fully opaque color. Subclasses of View should override this method whenever possible to indicate whether an instance is opaque. Opaque Views are treated in a special way by the View hierarchy, possibly allowing it to perform optimizations during invalidate/draw passes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isPaddingOffsetRequired

If the View draws content inside its padding and enables fading edges, it needs to support padding offsets. Padding offsets are added to the fading edges to extend the length of the fade so that it covers pixels drawn inside the padding. Subclasses of this class should override this method if they need to draw content inside the padding.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isPaddingRelative

Return if the padding has been set through relative values setPaddingRelative or through

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isPivotSet

Returns whether or not a pivot has been set by a call to setPivotX or setPivotY. If no pivot has been set then the pivot will be the center of the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isPreferKeepClear

Retrieve the preference for this view to be kept clear. This is set either by setPreferKeepClear or via the attribute android.R.styleable#View_preferKeepClear.

If this is `true`, the system will ignore the Rects set by setPreferKeepClearRects and try to keep the whole view clear.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isPressed

Indicates whether the view is currently in pressed state. Unless setPressed is explicitly called, only clickable views can enter the pressed state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isSaveEnabled

Indicates whether this view will save its state (that is, whether its onSaveInstanceState method will be called).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isSaveFromParentEnabled

Indicates whether the entire hierarchy under this view will save its state when a state saving traversal occurs from its parent. The default is true; if false, these views will not be saved unless saveHierarchyState is called directly on this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isScreenReaderFocusable

Returns whether the view should be treated as a focusable unit by screen reader accessibility tools.

**Note:** Use androidx.core.view.ViewCompat#setScreenReaderFocusable(android.view.View,boolean) for backwards-compatibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isScrollContainer

Indicates whether this view is one of the set of scrollable containers in its window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isScrollbarFadingEnabled

Returns true if scrollbars will fade when this view is not scrolling

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isSelected

Indicates the selection state of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isShowingLayoutBounds

Returns `true` when the View is attached and the system developer setting to show the layout bounds is enabled or `false` otherwise.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isShown

Returns the visibility of this view and all of its ancestors

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isSoundEffectsEnabled

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isTemporarilyDetached

Tells whether the `https://developer.android.com/reference/kotlin/android/view/View.html#` is in the state between onStartTemporaryDetach and onFinishTemporaryDetach.

This method always returns `true` when called directly or indirectly from onStartTemporaryDetach. The return value when called directly or indirectly from onFinishTemporaryDetach, however, depends on the OS version.

- `true` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`
- `false` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int`} and later

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isTextAlignmentResolved

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isTextDirectionResolved

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isVerticalFadingEdgeEnabled

Indicate whether the vertical edges are faded when the view is scrolled horizontally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isVerticalScrollBarEnabled

Indicate whether the vertical scrollbar should be drawn or not. The scrollbar is not drawn by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isVisibleToUserForAutofill

Computes whether this virtual autofill view is visible to the user.

**Note:** By default it returns `true`, but views providing a virtual hierarchy view must override it.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` keyboardNavigationClusterSearch

Find the nearest keyboard navigation cluster in the specified direction. This does not actually give focus to that cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` measure

This is called to find out how big a view should be. The parent supplies constraint information in the width and height parameters.

The actual measurement work of a view is performed in onMeasure, called by this method. Therefore, only onMeasure can and must be overridden by subclasses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` mergeDrawableStates

Merge your own state values in additionalState into the base state values baseState that were returned by onCreateDrawableState.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` offsetLeftAndRight

Offset this view's horizontal location by the specified amount of pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` offsetTopAndBottom

Offset this view's vertical location by the specified number of pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onAnimationEnd

Invoked by a parent ViewGroup to notify the end of the animation currently associated with this view. If you override this method, always call super.onAnimationEnd();. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onAnimationStart

Invoked by a parent ViewGroup to notify the start of the animation currently associated with this view. If you override this method, always call super.onAnimationStart();. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#!` onApplyWindowInsets

Called when the view should apply `https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#` according to its internal policy.

This method should be overridden by views that wish to apply a policy different from or in addition to the default behavior. Clients that wish to force a view subtree to apply insets should call dispatchApplyWindowInsets.

Clients may supply an `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener.html#` to a view. If one is set it will be called during dispatch instead of this method. The listener may optionally call this method from its own implementation if it wishes to apply the view's default insets policy in addition to its own.

Implementations of this method should either return the insets parameter unchanged or a new `https://developer.android.com/reference/kotlin/android/view/WindowInsets.html#` cloned from the supplied insets with any insets consumed that this view applied itself. This allows new inset types added in future platform versions to pass through existing implementations unchanged without being erroneously consumed.

By default if a view's setFitsSystemWindows property is set then the view will consume the system window insets and apply them as padding for the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onCancelPendingInputEvents

Called as the result of a call to cancelPendingInputEvents on this view or a parent view.

This method is responsible for removing any pending high-level input events that were posted to the event queue to run later. Custom view classes that post their own deferred high-level events via post, postDelayed or `https://developer.android.com/reference/kotlin/android/os/Handler.html#` should override this method, call `super.onCancelPendingInputEvents()` and remove those callbacks as appropriate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onCapturedPointerEvent

Implement this method to handle captured pointer events

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onCheckIsTextEditor

Check whether the called view is a text editor, in which case it would make sense to automatically display a soft input window for it. Subclasses should override this if they implement onCreateInputConnection to return true if a call on that method would return a non-null InputConnection, and they are really a first-class editor that the user would normally start typing on when the go into a window containing your view.

The default implementation always returns false. This does *not* mean that its onCreateInputConnection will not be called or the user can not otherwise perform edits on your view; it is just a hint to the system that this is not the primary purpose of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onConfigurationChanged

Called when the current configuration of the resources being used by the application have changed. You can use this to decide when to reload resources that can changed based on orientation and other configuration characteristics. You only need to use this if you are not relying on the normal `https://developer.android.com/reference/kotlin/android/app/Activity.html#` mechanism of recreating the activity instance upon a configuration change.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onCreateContextMenu

Views should implement this if the view itself is going to add items to the context menu.

<br />

`https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#!` onCreateInputConnection

Create a new InputConnection for an InputMethod to interact with the view. The default implementation returns null, since it doesn't support input methods. You can override this to implement such support. This is only needed for views that take focus and text input.

When implementing this, you probably also want to implement onCheckIsTextEditor to indicate you will return a non-null InputConnection.

Also, take good care to fill in the `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#` object correctly and in its entirety, so that the connected IME can rely on its values. For example, `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#initialSelStart:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#initialSelEnd:kotlin.Int` members must be filled in with the correct cursor position for IMEs to work correctly with your application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onCreateViewTranslationRequest

Collects a `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest.html#` which represents the content to be translated in the view.

The default implementation does nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onCreateVirtualViewTranslationRequests

Collects `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest.html#`s which represents the content to be translated for the virtual views in the host view. This is called if this view returned a virtual view structure from onProvideContentCaptureStructure and the system determined that those virtual views were relevant for translation.

The default implementation does nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onDisplayHint

Gives this view a hint about whether is displayed or not. For instance, when a View moves out of the screen, it might receives a display hint indicating the view is not displayed. Applications should not *rely* on this hint as there is no guarantee that they will receive one.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onDragEvent

Handles drag events sent by the system following a call to startDragAndDrop.

The system calls this method and passes a `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#` object in response to drag and drop events. This method can then call getAction to determine the state of the drag and drop operation.

The default implementation returns `false` unless an `https://developer.android.com/reference/kotlin/android/view/OnReceiveContentListener.html#` has been set for this view (see setOnReceiveContentListener), in which case the default implementation does the following:

- Returns `true` for an `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#ACTION_DRAG_STARTED:kotlin.Int` event
- Calls performReceiveContent for an `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#ACTION_DROP:kotlin.Int` event
- Returns `true` for an `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#ACTION_DROP:kotlin.Int` event if the `OnReceiveContentListener` consumed some or all of the content

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onDraw

Implement this to do your drawing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onDrawForeground

Draw any foreground content for this view.

Foreground content may consist of scroll bars, a setForeground drawable or other view-specific decorations. The foreground is drawn on top of the primary view content.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onDrawScrollBars

Request the drawing of the horizontal and the vertical scrollbar. The scrollbars are painted only if they have been awakened first.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onFilterTouchEventForSecurity

Filter the touch event to apply security policies.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onFinishInflate

Finalize inflating a view from XML. This is called as the last phase of inflation, after all child views have been added.

Even if the subclass overrides onFinishInflate, they should always be sure to call the super method, so that we get called. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onFinishTemporaryDetach

Called after onStartTemporaryDetach when the container is done changing the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onFocusChanged

Called by the view system when the focus state of this view changes. When the focus change event is caused by directional navigation, direction and previouslyFocusedRect provide insight into where the focus is coming from. When overriding, be sure to call up through to the super class so that the standard focus handling will occur. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onGenericMotionEvent

Implement this method to handle generic motion events.

Generic motion events describe joystick movements, hover events from mouse or stylus devices, trackpad touches, scroll wheel movements and other motion events not handled by onTouchEvent or onTrackballEvent. The getSource of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event. The following code example shows how this is done.

Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view.

```kotlin
public boolean onGenericMotionEvent(MotionEvent event) {
      if (event.isFromSource(InputDevice.SOURCE_CLASS_JOYSTICK)) {
          if (event.getAction() == MotionEvent.ACTION_MOVE) {
              // process the joystick movement...
              return true;
          }
      }
      if (event.isFromSource(InputDevice.SOURCE_CLASS_POINTER)) {
          switch (event.getAction()) {
              case MotionEvent.ACTION_HOVER_MOVE:
                  // process the hover movement...
                  return true;
              case MotionEvent.ACTION_SCROLL:
                  // process the scroll wheel movement...
                  return true;
          }
      }
      return super.onGenericMotionEvent(event);
  }
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onHoverChanged

Implement this method to handle hover state changes.

This method is called whenever the hover state changes as a result of a call to setHovered.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onHoverEvent

Implement this method to handle hover events.

This method is called whenever a pointer is hovering into, over, or out of the bounds of a view and the view is not currently being touched. Hover events are represented as pointer events with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_HOVER_ENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_HOVER_MOVE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_HOVER_EXIT:kotlin.Int`.

- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_HOVER_ENTER:kotlin.Int` when the pointer enters the bounds of the view.
- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_HOVER_MOVE:kotlin.Int` when the pointer has already entered the bounds of the view and has moved.
- The view receives a hover event with action `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_HOVER_EXIT:kotlin.Int` when the pointer has exited the bounds of the view or when the pointer is about to go down due to a button click, tap, or similar user action that causes the view to be touched.

The view should implement this method to return true to indicate that it is handling the hover event, such as by changing its drawable state.

The default implementation calls setHovered to update the hovered state of the view when a hover enter or hover exit event is received, if the view is enabled and is clickable. The default implementation also sends hover accessibility events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onInitializeAccessibilityEvent

Initializes an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#` with information about this View which is the event source. In other words, the source of an accessibility event is the view whose state change triggered firing the event.

Example: Setting the password property of an event in addition to properties set by the super implementation:

```kotlin
public void onInitializeAccessibilityEvent(AccessibilityEvent event) {
      super.onInitializeAccessibilityEvent(event);
      event.setPassword(true);
  }
```

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its onInitializeAccessibilityEvent is responsible for handling this call.

**Note:** Always call the super implementation before adding information to the event, in case the default implementation has basic information to add.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onInitializeAccessibilityNodeInfo

Initializes an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#` with information about this view. The base implementation sets:

- setParent,
- setBoundsInParent,
- setBoundsInScreen,
- setPackageName,
- setClassName,
- setContentDescription,
- setEnabled,
- setClickable,
- setFocusable,
- setFocused,
- setLongClickable,
- setSelected,
- setContextClickable

<br />

Subclasses should override this method, call the super implementation, and set additional attributes.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its onInitializeAccessibilityNodeInfo is responsible for handling this call.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onKeyDown

Default implementation of onKeyDown: perform press of the view when `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_DPAD_CENTER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ENTER:kotlin.Int` is released, if the view is enabled and clickable.

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onKeyLongPress

Default implementation of onKeyLongPress: always returns false (doesn't handle the event).

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onKeyMultiple

Default implementation of onKeyMultiple: always returns false (doesn't handle the event).

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onKeyPreIme

Handle a key event before it is processed by any input method associated with the view hierarchy. This can be used to intercept key events in special situations before the IME consumes them; a typical example would be handling the BACK key to update the application's UI instead of allowing the IME to see it and close itself. Due to a bug, this function is not called for BACK key events on Android T and U, when the IME is shown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onKeyShortcut

Called on the focused view when a key shortcut event is not handled. Override this method to implement local key shortcuts for the View. Key shortcuts can also be implemented by setting the setShortcut property of menu items.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onKeyUp

Default implementation of onKeyUp: perform clicking of the view when `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_DPAD_CENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ENTER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_SPACE:kotlin.Int` is released.

Key presses in software keyboards will generally NOT trigger this listener, although some may elect to do so in some situations. Do not rely on this to catch software key presses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onMeasure

Measure the view and its content to determine the measured width and the measured height. This method is invoked by measure and should be overridden by subclasses to provide accurate and efficient measurement of their contents.

**CONTRACT:** When overriding this method, you *must* call setMeasuredDimension to store the measured width and height of this view. Failure to do so will trigger an `IllegalStateException`, thrown by measure. Calling the superclass' onMeasure is a valid use.

The base class implementation of measure defaults to the background size, unless a larger size is allowed by the MeasureSpec. Subclasses should override onMeasure to provide better measurements of their content.

If this method is overridden, it is the subclass's responsibility to make sure the measured height and width are at least the view's minimum height and width (getSuggestedMinimumHeight and getSuggestedMinimumWidth).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onOverScrolled

Called by overScrollBy to respond to the results of an over-scroll operation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onPointerCaptureChange

Called when the window has just acquired or lost pointer capture. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onPopulateAccessibilityEvent

Called from dispatchPopulateAccessibilityEvent giving a chance to this View to populate the accessibility event with its text content.

**Note:** This method should only be used with event.setText(). Avoid mutating other event state in this method. Instead, follow the practices described in dispatchPopulateAccessibilityEvent. In general, put UI metadata in the node for services to easily query, than in transient events.

Example: Adding formatted date string to an accessibility event in addition to the text added by the super implementation:

```kotlin
public void onPopulateAccessibilityEvent(AccessibilityEvent event) {
      super.onPopulateAccessibilityEvent(event);
      final int flags = DateUtils.FORMAT_SHOW_DATE | DateUtils.FORMAT_SHOW_WEEKDAY;
      String selectedDateUtterance = DateUtils.formatDateTime(mContext,
          mCurrentDate.getTimeInMillis(), flags);
      event.getText().add(selectedDateUtterance);
  }
```

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its onPopulateAccessibilityEvent is responsible for handling this call.

**Note:** Always call the super implementation before adding information to the event, in case the default implementation has basic information to add.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onProvideAutofillStructure

Populates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` to fullfil an autofill request.

The structure should contain at least the following properties:

- Autofill id (setAutofillId).
- Autofill type (setAutofillType).
- Autofill value (setAutofillValue).
- Whether the data is sensitive (setDataIsSensitive).

It's also recommended to set the following properties - the more properties the structure has, the higher the chances of an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` properly using the structure:

- Autofill hints (setAutofillHints).
- Autofill options (setAutofillOptions) when the view can only be filled with predefined values (typically used when the autofill type is `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_TYPE_LIST:kotlin.Int`).
- Resource id (setId).
- Class name (setClassName).
- Content description (setContentDescription).
- Visual properties such as visibility (setVisibility), dimensions (setDimens), and opacity (setOpaque).
- For views representing text fields, text properties such as the text itself (setText), text hints (setHint, input type (setInputType),
- For views representing HTML nodes, its web domain (setWebDomain) and HTML properties ((setHtmlInfo).

The default implementation of this method already sets most of these properties based on related `https://developer.android.com/reference/kotlin/android/view/View.html#` methods (for example, the autofill id is set using getAutofillId, the autofill type set using getAutofillType, etc.), and views in the standard Android widgets library also override it to set their relevant properties (for example, TextView already sets the text properties), so it's recommended to only override this method (and call `super.onProvideAutofillStructure()`) when:

- The view contents does not include PII (Personally Identifiable Information), so it can call setDataIsSensitive passing `false`.
- The view can only be autofilled with predefined options, so it can call setAutofillOptions.

**Note:** The `left` and `top` values set in setDimens must be relative to the next isImportantForAutofill predecessor view included in the structure.

Views support the Autofill Framework mainly by:

- Providing the metadata defining what the view means and how it can be autofilled.
- Notifying the Android System when the view value changed by calling notifyValueChanged.
- Implementing the methods that autofill the view.

This method is responsible for the former; autofill is responsible for the latter.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onProvideAutofillVirtualStructure

Populates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` containing virtual children to fullfil an autofill request.

This method should be used when the view manages a virtual structure under this view. For example, a view that draws input fields using draw.

When implementing this method, subclasses must follow the rules below:

- Add virtual children by calling the newChild or asyncNewChild methods, where the `id` is an unique id identifying the children in the virtual structure.
- The children hierarchy can have multiple levels if necessary, but ideally it should exclude intermediate levels that are irrelevant for autofill; that would improve the autofill performance.
- Also implement autofill to autofill the virtual children.
- Set the autofill properties of the child structure as defined by onProvideAutofillStructure, using setAutofillId to set its autofill id.
- Call notifyViewEntered and/or notifyViewExited when the focused virtual child changed.
- Override isVisibleToUserForAutofill to allow the platform to query whether a given virtual view is visible to the user in order to support triggering save when all views of interest go away.
- Call notifyValueChanged when the value of a virtual child changed.
- Call notifyViewVisibilityChanged when the visibility of a virtual child changed.
- Call notifyViewClicked when a virtual child is clicked.
- Call commit when the autofill context of the view structure changed and the current context should be committed (for example, when the user tapped a `SUBMIT` button in an HTML page).
- Call cancel when the autofill context of the view structure changed and the current context should be canceled (for example, when the user tapped a `CANCEL` button in an HTML page).
- Provide ways for users to manually request autofill by calling requestAutofill.
- The `left` and `top` values set in setDimens must be relative to the next isImportantForAutofill predecessor view included in the structure.

Views with virtual children support the Autofill Framework mainly by:

- Providing the metadata defining what the virtual children mean and how they can be autofilled.
- Implementing the methods that autofill the virtual children.

This method is responsible for the former; autofill is responsible for the latter.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onProvideContentCaptureNodeProperties

Populates the properties of this `https://developer.android.com/reference/kotlin/android/view/View.html#` for Content Capture version 2.

This method is called when a view that is eligible for content capture is initially registered and appeared on the screen, or when its properties are explicitly requested to be repopulated. The populated `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties.html#` is subsequently sent to the intelligence service through notifyNodeAppearedOrChanged.

The default implementation of this method computes and sets the most relevant properties, such as the layout bounds relative to the nearest content-capture-important parent, the parent's AutofillId, and the view's content description. Subclasses overriding this method should call the super implementation (`super.onProvideContentCaptureNodeProperties(properties)`) to populate these default properties, and then modify them as appropriate.

**Note for Virtual Views:**Views that host a virtual view structure (such as web pages) must only populate the node properties representing the host view itself and return immediately. They must subsequently report virtual child node events on the main (UI) thread by calling:

- notifyNodeAppearedOrChanged when virtual nodes appear or their properties change
- notifyNodeDisappeared when virtual nodes disappear

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onProvideContentCaptureStructure

Populates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` for content capture.

This method is called after a view that is eligible for content capture (for example, if it isImportantForContentCapture, an intelligence service is enabled for the user, and the activity rendering the view is enabled for content capture) is laid out and is visible. The populated structure is then passed to the service through notifyViewAppeared.

The default implementation of this method sets the most relevant properties based on related `https://developer.android.com/reference/kotlin/android/view/View.html#` methods, and views in the standard Android widgets library also override it to set their relevant properties. Therefore, if overriding this method, it is recommended to call `super.onProvideContentCaptureStructure()`.

**Note:** views that manage a virtual structure under this view must populate just the node representing this view and return right away, then asynchronously report (not necessarily in the UI thread) when the children nodes appear, disappear or have their text changed by calling notifyViewAppeared, notifyViewDisappeared, and notifyViewTextChanged respectively. The structure for a child must be created using newVirtualViewStructure, and the `autofillId` for a child can be obtained either through `childStructure.getAutofillId()` or newAutofillId.

When the virtual view hierarchy represents a web page, you should also:

- Call getContentCaptureConditions to infer content capture events should be generate for that URL.
- Create a new `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession.html#` child for every HTML element that renders a new URL (like an `IFRAME`) and use that session to notify events from that subtree.

**Note:** the following methods of the `structure` will be ignored:

- setChildCount
- addChildCount
- getChildCount
- newChild
- asyncNewChild
- asyncCommit
- setWebDomain
- newHtmlInfoBuilder
- setHtmlInfo
- setDataIsSensitive
- setAlpha
- setElevation
- setTransformation

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onProvideStructure

Called when assist structure is being retrieved from a view as part of onProvideAssistData.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onProvideVirtualStructure

Called when assist structure is being retrieved from a view as part of onProvideAssistData to generate additional virtual structure under this view. The default implementation uses getAccessibilityNodeProvider to try to generate this from the view's virtual accessibility nodes, if any. You can override this for a more optimal implementation providing this data.

<br />

`https://developer.android.com/reference/kotlin/android/view/ContentInfo.html#?` onReceiveContent

Implements the default behavior for receiving content for this type of view. The default view implementation is a no-op (returns the passed-in content without acting on it).

Widgets should override this method to define their default behavior for receiving content. Apps should setOnReceiveContentListener to provide app-specific handling for receiving content.

See setOnReceiveContentListener and performReceiveContent for more info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onRestoreInstanceState

Hook allowing a view to re-apply a representation of its internal state that had previously been generated by onSaveInstanceState. This function will never be called with a null state. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onRtlPropertiesChanged

Called when any RTL property (layout direction or text direction or text alignment) has been changed. Subclasses need to override this method to take care of cached information that depends on the resolved layout direction, or to inform child views that inherit their layout direction. The default implementation does nothing.

<br />

`https://developer.android.com/reference/kotlin/android/os/Parcelable.html#?` onSaveInstanceState

Hook allowing a view to generate a representation of its internal state that can later be used to create a new instance with that same state. This state should only contain information that is not persistent or can not be reconstructed later. For example, you will never store your current position on screen because that will be computed again when a new instance of the view is placed in its view hierarchy.

Some examples of things you may store here: the current cursor position in a text view (but usually not the text itself since that is stored in a content provider or other persistent storage), the currently selected item in a list view. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onScreenStateChanged

This method is called whenever the state of the screen this view is attached to changes. A state change will usually occurs when the screen turns on or off (whether it happens automatically or the user does it manually.)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onScrollCaptureSearch

Called when scroll capture is requested, to search for appropriate content to scroll. If applicable, this view adds itself to the provided list for consideration, subject to the flags set by setScrollCaptureHint.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onScrollChanged

This is called in response to an internal scroll in this view (i.e., the view scrolled its own contents). This is typically as a result of scrollBy or scrollTo having been called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onSetAlpha

Invoked if there is a Transform that involves alpha. Subclass that can draw themselves with the specified alpha should return true, and then respect that alpha when their onDraw() is called. If this returns false then the view may be redirected to draw into an offscreen buffer to fulfill the request, which will look fine, but may be slower than if the subclass handles it internally. The default implementation returns false.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onSizeChanged

This is called during layout when the size of this view has changed. If you were just added to the view hierarchy, you're called with the old values of 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onStartTemporaryDetach

This is called when a container is going to temporarily detach a child, with detachViewFromParent. It will either be followed by onFinishTemporaryDetach or onDetachedFromWindow when the container is done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onTouchEvent

Implement this method to handle pointer events.

This method is called to handle motion events where pointers are down on the view. For example, this could include touchscreen touches, stylus touches, or click-and-drag events from a mouse. However, it is not called for motion events that do not involve pointers being down, such as hover events or mouse scroll wheel movements.

If this method is used to detect click actions, it is recommended that the actions be performed by implementing and calling performClick. This will ensure consistent system behavior, including:

- obeying click sound preferences
- dispatching OnClickListener calls
- handling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#ACTION_CLICK:kotlin.Int` when accessibility features are enabled

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` onTrackballEvent

Implement this method to handle trackball motion events.

The *relative* movement of the trackball since the last event can be retrieve with android.view.MotionEvent#getX and android.view.MotionEvent#getY. These are normalized so that a movement of 1 corresponds to the user pressing one DPAD key (so they will often be fractional values, representing the more fine-grained movement information available from a trackball).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onViewTranslationResponse

Called when the content from onCreateViewTranslationRequest had been translated by the TranslationService. The `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse.html#` should be saved here so that the `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse.html#` can be used to display the translation when the system calls onShowTranslation.

The default implementation will set the ViewTranslationResponse that can be get from getViewTranslationResponse.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onVirtualViewTranslationResponses

Called when the content from onCreateVirtualViewTranslationRequests had been translated by the TranslationService.

The default implementation does nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onVisibilityAggregated

Called when the user-visibility of this View is potentially affected by a change to this view itself, an ancestor view or the window this view is attached to. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onVisibilityChanged

Called when the visibility of the view or an ancestor of the view has changed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onWindowFocusChanged

Called when the window containing this view gains or loses focus. Note that this is separate from view focus: to receive key events, both your view and its window must have focus. If a window is displayed on top of yours that takes input focus, then your own window will lose focus but the view focus will remain unchanged.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onWindowSystemUiVisibilityChanged

Override to find out when the window's requested system UI visibility has changed, that is the value returned by getWindowSystemUiVisibility. This is different from the callbacks received through setOnSystemUiVisibilityChangeListener in that this is only telling you about the local request of the window, not the actual values applied by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onWindowVisibilityChanged

Called when the window containing has change its visibility (between `https://developer.android.com/reference/kotlin/android/view/View.html#GONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int`). Note that this tells you whether or not your window is being made visible to the window manager; this does *not* tell you whether or not your window is obscured by other windows on the screen, even if it is itself visible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` overScrollBy

Scroll the view with standard behavior for scrolling beyond the normal content boundaries. Views that call this method should override onOverScrolled to respond to the results of an over-scroll operation. Views can use this method to handle any touch or fling-based scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performAccessibilityAction

Performs the specified accessibility action on the view. For possible accessibility actions look at `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#`.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its performAccessibilityAction is responsible for handling this call.

The default implementation will delegate `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#ACTION_SCROLL_BACKWARD:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#ACTION_SCROLL_FORWARD:kotlin.Int` to nested scrolling parents if isNestedScrollingEnabled on this view.

**Note:** Avoid setting accessibility focus with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#ACTION_ACCESSIBILITY_FOCUS:kotlin.Int`. This is intended to be controlled by screen readers. Apps changing focus can confuse screen readers, so the resulting behavior can vary by device and screen reader version.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performClick

Call this view's OnClickListener, if it is defined. Performs all normal actions associated with clicking: reporting accessibility event, playing a sound, etc.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performContextClick

Call this view's OnContextClickListener, if it is defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performContextClick

Call this view's OnContextClickListener, if it is defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performHapticFeedback

Like performHapticFeedback, but takes a `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#`.

Using a `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#` allows you to make more elaborate haptic feedback requests, including setting the usage type for the requested feedback.

Specifying the usage type for your feedback allows the system to understand the context of the feedback better, and tune the haptic accordingly. When not specifying the usage type for the feedback request, or when using the other performHapticFeedback APIs, the system will do a best guess of the vibration usage based on the constant.

See `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#` to learn more about vibration usages. The usage provided for this API must be of `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_CLASS_FEEDBACK:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_UNKNOWN:kotlin.Int`. Otherwise, the haptic feedback will not be played. If `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_UNKNOWN:kotlin.Int` is used, the system will do a best guess of the vibration usage based on the constant.

Note that, if you will be calling this API repeatedly and your `https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.html#` does not change across these repeated calls, it is recommended that you create, cache, and reuse the request object to avoid the costs of repeated object creation and garbage collection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performHapticFeedback

BZZZTT!!1!

Provide haptic feedback to the user for this view.

The framework will provide haptic feedback for some built in actions, such as long presses, but you may wish to provide feedback for your own widget.

The feedback will only be performed if isHapticFeedbackEnabled is true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performHapticFeedback

BZZZTT!!1!

Like performHapticFeedback, with additional options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performLongClick

Calls this view's OnLongClickListener, if it is defined. Invokes the context menu if the OnLongClickListener did not consume the event.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` performLongClick

Calls this view's OnLongClickListener, if it is defined. Invokes the context menu if the OnLongClickListener did not consume the event, anchoring it to an (x,y) coordinate.

<br />

`https://developer.android.com/reference/kotlin/android/view/ContentInfo.html#?` performReceiveContent

Receives the given content. If no listener is set, invokes onReceiveContent. If a listener is setOnReceiveContentListener, invokes the listener instead; if the listener returns a non-null result, invokes onReceiveContent to handle it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` playSoundEffect

Play a sound effect for this view.

The framework will play sound effects for some built in actions, such as clicking, but you may wish to play these effects in your widget, for instance, for internal navigation.

The sound effect will only be played if sound effects are enabled by the user, and isSoundEffectsEnabled is true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` post

Causes the Runnable to be added to the message queue. The runnable will be run on the user interface thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` postDelayed

Causes the Runnable to be added to the message queue, to be run after the specified amount of time elapses. The runnable will be run on the user interface thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` postInvalidate

Cause an invalidate to happen on a subsequent cycle through the event loop. Use this to invalidate the View from a non-UI thread.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` postInvalidate

Cause an invalidate of the specified area to happen on a subsequent cycle through the event loop. Use this to invalidate the View from a non-UI thread.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` postInvalidateDelayed

Cause an invalidate to happen on a subsequent cycle through the event loop. Waits for the specified amount of time.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` postInvalidateDelayed

Cause an invalidate of the specified area to happen on a subsequent cycle through the event loop. Waits for the specified amount of time.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` postInvalidateOnAnimation

Cause an invalidate to happen on the next animation time step, typically the next display frame.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` postInvalidateOnAnimation

Cause an invalidate of the specified area to happen on the next animation time step, typically the next display frame.

This method can be invoked from outside of the UI thread only when this View is attached to a window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` postOnAnimation

Causes the Runnable to execute on the next animation time step. The runnable will be run on the user interface thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` postOnAnimationDelayed

Causes the Runnable to execute on the next animation time step, after the specified amount of time elapses. The runnable will be run on the user interface thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` refreshDrawableState

Call this to force a view to update its drawable state. This will cause drawableStateChanged to be called on this view. Views that are interested in the new state should call getDrawableState.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` registerCalledFromWrongThreadListener

Registers a listener that is notified when a View API is called from the wrong thread.

Most View APIs should only be called on the UI thread, and will throw a `CalledFromWrongThreadException` if they are called from the wrong thread. View APIs that throw `CalledFromWrongThreadException` will not notify registered listeners.

For certain APIs, if they are called on the wrong thread then an exception may not be thrown, subject to App Compatibility settings. Instead, applications may be notified when a call to such an API is made from the wrong thread by registering a `https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener.html#` using this method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` releasePointerCapture

Releases the pointer capture.

If the window does not have pointer capture, this call will do nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` removeCallbacks

Removes the specified Runnable from the message queue.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeOnAttachStateChangeListener

Remove a listener for attach state changes. The listener will receive no further notification of window attach/detach events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeOnLayoutChangeListener

Remove a listener for layout changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeOnUnhandledKeyEventListener

Removes a listener which will receive unhandled `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`s. This must be called on the UI thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` reportAppJankStats

Called from apps when they want to report jank stats to the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestApplyInsets

Ask that a new dispatch of onApplyWindowInsets be performed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestFitSystemWindows

Ask that a new dispatch of fitSystemWindows be performed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestFocus

Call this to try to give focus to a specific view or to one of its descendants. A view will not actually take focus if it is not focusable (isFocusable returns false), or if it can't be focused due to other conditions (not focusable in touch mode (isFocusableInTouchMode) while the device is in touch mode, not visible, not enabled, or has no size). See also focusSearch, which is what you call to say that you have focus, and you want your parent to look for the next one. This is equivalent to calling requestFocus with arguments `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_DOWN:kotlin.Int` and `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestFocus

Call this to try to give focus to a specific view or to one of its descendants and give it a hint about what direction focus is heading. A view will not actually take focus if it is not focusable (isFocusable returns false), or if it is focusable and it is not focusable in touch mode (isFocusableInTouchMode) while the device is in touch mode. See also focusSearch, which is what you call to say that you have focus, and you want your parent to look for the next one. This is equivalent to calling requestFocus with `null` set for the previously focused rectangle.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestFocusFromTouch

Call this to try to give focus to a specific view or to one of its descendants. This is a special variant of requestFocus that will allow views that are not focusable in touch mode to request focus when they are touched.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestLayout

Call this when something has changed which has invalidated the layout of this view. This will schedule a layout pass of the view tree. This should not be called while the view hierarchy is currently in a layout pass (isInLayout. If layout is happening, the request may be honored at the end of the current layout pass (and then layout will run again) or after the current frame is drawn and the next layout occurs.

Subclasses which override this method should call the superclass method to handle possible request-during-layout errors correctly.
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestPointerCapture

Requests pointer capture in relative mode.

Equivalent to calling requestPointerCapture with `https://developer.android.com/reference/kotlin/android/view/View.html#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestPointerCapture

Requests pointer capture in the specified mode.

When the window has pointer capture, the mouse pointer icon will disappear and will not change its position. Enabling pointer capture will change the behavior of input devices in the following ways:

- Events from a mouse will be delivered with the source `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_MOUSE_RELATIVE:kotlin.Int`, and relative position changes will be available through android.view.MotionEvent#getX and android.view.MotionEvent#getY.
- Events from a touchpad (also known as a trackpad) will be delivered according to the chosen pointer capture mode. See `https://developer.android.com/reference/kotlin/android/view/View.html#POINTER_CAPTURE_MODE_RELATIVE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View.html#POINTER_CAPTURE_MODE_ABSOLUTE:kotlin.Int` for details.
- Events from other types of devices, such as touchscreens, will not be affected.

Pointer ballistics curves and the user's pointer speed settings will not be applied in this mode.

When pointer capture changes, connected mouse and touchpad devices may be reconfigured, and their properties (such as their sources or motion ranges) may change. Use an `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.InputDeviceListener.html#` to be notified when a device changes (which may happen after enabling or disabling pointer capture), and use getDevice to get the updated `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#`.

Events captured through pointer capture will be dispatched to onCapturedPointer if an `https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener.html#` is set, and otherwise to onCapturedPointerEvent.

If the window already has pointer capture in the same mode, this call does nothing. If it already has pointer capture in a different mode, it will transition to the new mode.

The capture may be released through releasePointerCapture, or will be lost automatically when the window loses focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestRectangleOnScreen

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestRectangleOnScreen

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

When `immediate` is set to true, scrolling will not be animated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` requestRectangleOnScreen

Request that a rectangle of this view be visible on the screen, scrolling if necessary just enough.

A View should call this if it maintains some notion of which part of its content is interesting. For example, a text editing view should call this when its cursor moves.

The Rectangle passed into this method should be in the View's content coordinate space. It should not be affected by which part of the View is currently visible or its scroll position.

When `immediate` is set to true, scrolling will not be animated.

The `source` parameter is used to differentiate behaviors of certain system features, like focus-following with display magnification, based on user preferences and the source of requests to show content on-screen. Callers are encouraged to provide one of the following request sources, when applicable, instead of using requestRectangleOnScreen or requestRectangleOnScreen:

1. `https://developer.android.com/reference/kotlin/android/view/View.html#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_SCROLL_ONLY:kotlin.Int`
2. `https://developer.android.com/reference/kotlin/android/view/View.html#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_TEXT_CURSOR:kotlin.Int`
3. `https://developer.android.com/reference/kotlin/android/view/View.html#RECTANGLE_ON_SCREEN_REQUEST_SOURCE_INPUT_FOCUS:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestUnbufferedDispatch

Request unbuffered dispatch of the given stream of MotionEvents to this View. Until this View receives a corresponding `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_UP:kotlin.Int`, ask that the input system not batch `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s but instead deliver them as soon as they're available. This method should only be called for touch events.

This API is not intended for most applications. Buffered dispatch provides many of benefits, and just requesting unbuffered dispatch on most MotionEvent streams will not improve your input latency. Side effects include: increased latency, jittery scrolls and inability to take advantage of system resampling. Talk to your input professional to see if requestUnbufferedDispatch is right for you.
To receive unbuffered events for arbitrary input device source classes, use requestUnbufferedDispatch,

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` requestUnbufferedDispatch

Request unbuffered dispatch of the given event source class to this view. This is similar to requestUnbufferedDispatch, but does not automatically terminate, and allows the specification of arbitrary input source classes.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, calling this method will not result in any behavioral changes when this View is not attached to a window.

<br />

`T` requireViewById

Finds the first descendant view with the given ID, the view itself if the ID matches getId, or throws an IllegalArgumentException if the ID is invalid or there is no matching view in the hierarchy.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` resetPivot

Clears any pivot previously set by a call to setPivotX or setPivotY. After calling this isPivotSet will be false and the pivot used for rotation will return to default of being centered on the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` resolveSize

Version of resolveSizeAndState returning only the `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_SIZE_MASK:kotlin.Int` bits of the result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` resolveSizeAndState

Utility to reconcile a desired size and state, with constraints imposed by a MeasureSpec. Will take the desired size, unless a different size is imposed by the constraints. The returned value is a compound integer, with the resolved size in the `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_SIZE_MASK:kotlin.Int` bits and optionally the bit `https://developer.android.com/reference/kotlin/android/view/View.html#MEASURED_STATE_TOO_SMALL:kotlin.Int` set if the resulting size is smaller than the size the view wants to be.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` restoreHierarchyState

Restore this view hierarchy's frozen state from the given container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` saveAttributeDataForStyleable

Stores debugging information about attributes. This should be called in a constructor by every custom `https://developer.android.com/reference/kotlin/android/view/View.html#` that uses a custom styleable. If the custom view does not call it, then the custom attributes used by this view will not be visible in layout inspection tools.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` saveHierarchyState

Store this view hierarchy's frozen state into the given container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` scheduleDrawable

Schedules an action on a drawable to occur at a specified time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` scrollBy

Move the scrolled position of your view. This will cause a call to onScrollChanged and the view will be invalidated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` scrollTo

Set the scrolled position of your view. This will cause a call to onScrollChanged and the view will be invalidated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendAccessibilityEvent

Sends an accessibility event of the given type. If accessibility is not enabled this method has no effect. The default implementation calls onInitializeAccessibilityEvent first to populate information about the event source (this View), then calls dispatchPopulateAccessibilityEvent to populate the text content of the event source including its descendants, then for events type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_SCROLLED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` with subtype `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int`, throttle the events, and last calls requestSendAccessibilityEvent on its parent to request sending of the event to interested parties.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its sendAccessibilityEvent is responsible for handling this call.

If this view uses `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider.html#` to provide virtual view hierarchy rooted at this view, this method should not be called to send events from virtual children because it will populate the events with wrong information and the events should be throttled per child instead at the virtual root level. To send events from virtual children, call requestSendAccessibilityEvent on the view's parent to request sending of the event to interested parties.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendAccessibilityEventUnchecked

This method behaves exactly as sendAccessibilityEvent but takes as an argument an empty `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#` and does not perform a check whether accessibility is enabled.

If an `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#` has been specified via calling setAccessibilityDelegate its sendAccessibilityEventUnchecked is responsible for handling this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAccessibilityDataSensitive

Specifies whether this view should only allow interactions from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`s with the isAccessibilityTool property set to true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAccessibilityDelegate

Sets a delegate for implementing accessibility support via composition (as opposed to inheritance). For more details, see `https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#`.

**Note:** On platform versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, delegate methods on views in the `android.widget.*` package are called *before* host methods. This prevents certain properties such as class name from being modified by overriding onInitializeAccessibilityNodeInfo, as any changes will be overwritten by the host class.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, delegate methods are called *after* host methods, which all properties to be modified without being overwritten by the host class.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAccessibilityHeading

Set if view is a heading for a section of content for accessibility purposes.

Users of some accessibility services can choose to navigate between headings instead of between paragraphs, words, etc. Apps that provide headings on sections of text can help the text navigation experience.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityHeading(android.view.View,boolean) for backwards-compatibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAccessibilityLiveRegion

Sets the live region mode for this view. This indicates to accessibility services whether they should automatically notify the user about changes to the view's content description or text, or to the content descriptions or text of the view's children (where applicable).

Different priority levels are available:

- `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int`: Indicates that updates to the region should be presented to the user. Suitable in most cases for prominent updates within app content that don't require the user's immediate attention.
- `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int`: Indicates that updates to the region have the highest priority and should be presented to the user immediately. This may result in disruptive notifications from an accessibility service, which may potentially interrupt other feedback or user actions, so it should generally be used only for critical, time-sensitive information.
- `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int`: Disables change announcements (the default for most views).

Examples:

- Selecting an option in a dropdown menu updates a panel below with the updated content. This panel may be marked as a live region with `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int` to notify users of the change. A screen reader may queue changes as announcements that don't disrupt ongoing speech.
- An emergency alert may be marked with `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_ASSERTIVE:kotlin.Int` to immediately inform users of the emergency.

For error notifications, like an "incorrect password" warning in a login screen, views should send a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` `AccessibilityEvent` with a content change type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int` and set setError. Custom widgets should provide error-setting methods that support accessibility. For example, use setError instead of explicitly sending events.

Don't use live regions for frequently-updating UI elements (e.g., progress bars), as this can overwhelm the user with feedback from accessibility services. If necessary, use setMinDurationBetweenContentChanges to throttle feedback and reduce disruptions.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityLiveRegion(android.view.View,int) for backwards-compatibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAccessibilityPaneTitle

Visually distinct portion of a window with window-like semantics are considered panes for accessibility purposes. One example is the content view of a large fragment that is replaced. In order for accessibility services to understand a pane's window-like behavior, panes should have descriptive titles. Views with pane titles produce `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_STATE_CHANGED:kotlin.Int`s when they appear, disappear, or change title.

When transitioning from one Activity to another, instead of using `setAccessibilityPaneTitle()`, set a descriptive title for its window by using `android:label` for the matching Activity entry in your application's manifest or updating the title at runtime with setTitle.

**Note:** Use androidx.core.view.ViewCompat#setAccessibilityPaneTitle(android.view.View,java.lang.CharSequence) for backwards-compatibility.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAccessibilityTraversalAfter

Sets the id of a view that screen readers are requested to visit before this view.

For example, if view B should be visited after A, with B.setAccessibilityTraversalAfter(A), then this requests that screen readers visit and traverse view A before visiting view B.

**Note:** Views are visited in the order determined by the screen reader. Avoid explicitly manipulating focus order, as this may result in inconsistent user experiences between apps. Instead, use other semantics, such as restructuring the view hierarchy layout, to communicate order.

Setting this view to be after a view that is not important for accessibility, or if this view is not important for accessibility, means this method will have no effect if the service is not aware of unimportant views.

To avoid a risk of loops, set clear relationships between views. For example, if focus order should be B -\> A, and B.setAccessibilityTraversalBefore(A), then also call A.setAccessibilityTraversalAfter(B).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAccessibilityTraversalBefore

Sets the id of a view that screen readers are requested to visit after this view.

For example, if view B should be visited before view A, with B.setAccessibilityTraversalBefore(A), this requests that screen readers visit and traverse view B before visiting view A.

**Note:** Views are visited in the order determined by the screen reader. Avoid explicitly manipulating focus order, as this may result in inconsistent user experiences between apps. Instead, use other semantics, such as restructuring the view hierarchy layout, to communicate order.

Setting this view to be after a view that is not important for accessibility, or if this view is not important for accessibility, means this method will have no effect if the service is not aware of unimportant views.

To avoid a risk of loops, set clear relationships between views. For example, if focus order should be B -\> A, and B.setAccessibilityTraversalBefore(A), then also call A.setAccessibilityTraversalAfter(B).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setActivated

Changes the activated state of this view. A view can be activated or not. Note that activation is not the same as selection. Selection is a transient property, representing the view (hierarchy) the user is currently interacting with. Activation is a longer-term state that the user can move views in and out of. For example, in a list view with single or multiple selection enabled, the views in the current selection set are activated. (Um, yeah, we are deeply sorry about the terminology here.) The activated state is propagated down to children of the view it is set on.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAllowClickWhenDisabled

Enables or disables click events for this view when disabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAllowedHandwritingDelegatePackage

Specifies that this view may act as a handwriting initiation delegator for a delegate editor view from the specified package. If this method is not called, delegators may only be used to initiate handwriting mode for a delegate editor view from the same package as the delegator view. This method allows specifying a different trusted package which may contain a delegate editor view linked to this delegator view.

This method has no effect unless setHandwritingDelegatorCallback is also called to configure this view to act as a handwriting delegator.

If this method is called on the delegator view, then setAllowedHandwritingDelegatorPackage should also be called on the delegate editor view.

For example, to configure a delegator view in package 1:

```kotlin
delegatorView.setHandwritingDelegatorCallback(callback);
  delegatorView.setAllowedHandwritingDelegatePackage(package2);
```
Then to configure the corresponding delegate editor view in package 2:

```kotlin
delegateEditorView.setIsHandwritingDelegate(true);
  delegateEditorView.setAllowedHandwritingDelegatorPackage(package1);
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAllowedHandwritingDelegatorPackage

Specifies that a view from the specified package may act as a handwriting delegator for this delegate editor view. If this method is not called, only views from the same package as this delegate editor view may act as a handwriting delegator. This method allows specifying a different trusted package which may contain a delegator view linked to this delegate editor view.

This method has no effect unless setIsHandwritingDelegate is also called to configure this view to act as a handwriting delegate.

If this method is called on the delegate editor view, then setAllowedHandwritingDelegatePackage should also be called on the delegator view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAlpha

Sets the opacity of the view to a value from 0 to 1, where 0 means the view is completely transparent and 1 means the view is completely opaque.

**Note:** setting alpha to a translucent value (0 \< alpha \< 1) can have significant performance implications, especially for large views. It is best to use the alpha property sparingly and transiently, as in the case of fading animations.

For a view with a frequently changing alpha, such as during a fading animation, it is strongly recommended for performance reasons to either override hasOverlappingRendering to return `false` if appropriate, or setting a setLayerType on the view for the duration of the animation. On versions `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` and below, the default path for rendering an unlayered View with alpha could add multiple milliseconds of rendering cost, even for simple or small views. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int` is automatically applied to the view at the rendering level.

If this view overrides onSetAlpha to return true, then this view is responsible for applying the opacity itself.

On versions `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` and below, note that if the view is backed by a setLayerType and is associated with a setLayerPaint, setting an alpha value less than 1.0 will supersede the alpha of the layer paint.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, setting a translucent alpha value will clip a View to its bounds, unless the View returns `false` from hasOverlappingRendering.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAnimation

Sets the next animation to play for this view. If you want the animation to play immediately, use startAnimation instead. This method provides allows fine-grained control over the start time and invalidation, but you must make sure that 1) the animation has a start time set, and 2) the view's parent (which controls animations on its children) will be invalidated when the animation is supposed to start.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAnimationMatrix

Changes the transformation matrix on the view. This is used in animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`. When the animation finishes, the matrix should be cleared by calling this method with `null` as the matrix parameter. Application developers should use transformation methods like setRotation, setScaleX, setScaleX, setTranslationX} and setTranslationY (float)}} instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAutoHandwritingEnabled

Set whether this view enables automatic handwriting initiation. For a view with an active `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#`, if auto handwriting is enabled then stylus movement within its view boundary will automatically trigger the handwriting mode. Check startStylusHandwriting for more details about handwriting mode. If the View wants to initiate handwriting mode by itself, it can set this field to `false` and call startStylusHandwriting when there is stylus movement detected. Note that this attribute has no effect on the View's children. For example, if a `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` disables auto handwriting but its children set auto handwriting to true, auto handwriting will still work for the children, and vice versa.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAutofillHints

Sets the hints that help an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` determine how to autofill the view with the user's data.

Typically, there is only one way to autofill a view, but there could be more than one. For example, if the application accepts either an username or email address to identify an user.

These hints are not validated by the Android System, but passed "as is" to the service. Hence, they can have any value, but it's recommended to use the `AUTOFILL_HINT_` constants such as: `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_USERNAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_PASSWORD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_EMAIL_ADDRESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_NAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_PHONE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_POSTAL_ADDRESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_POSTAL_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_NUMBER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_SECURITY_CODE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_DAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_MONTH:kotlin.String` or `https://developer.android.com/reference/kotlin/android/view/View.html#AUTOFILL_HINT_CREDIT_CARD_EXPIRATION_YEAR:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAutofillId

Sets the unique, logical identifier of this view in the activity, for autofill purposes.

The autofill id is created on demand, and this method should only be called when a view is reused after dispatchProvideAutofillStructure is called, as that method creates a snapshot of the view that is passed along to the autofill service.

This method is typically used when view subtrees are recycled to represent different content\* ---in this case, the autofill id can be saved before the view content is swapped out, and restored later when it's swapped back in. For example:

```kotlin
EditText reusableView = ...;
  ViewGroup parentView = ...;
  AutofillManager afm = ...;
 
  // Swap out the view and change its contents
  AutofillId oldId = reusableView.getAutofillId();
  CharSequence oldText = reusableView.getText();
  parentView.removeView(reusableView);
  AutofillId newId = afm.getNextAutofillId();
  reusableView.setText("New I am");
  reusableView.setAutofillId(newId);
  parentView.addView(reusableView);
 
  // Later, swap the old content back in
  parentView.removeView(reusableView);
  reusableView.setAutofillId(oldId);
  reusableView.setText(oldText);
  parentView.addView(reusableView);
  
```

NOTE: If this view is a descendant of an AdapterView, the system may reset its autofill id when this view is recycled. If the autofill ids need to be stable, they should be set again in getView.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBackdropRenderEffect

Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` to apply to the backdrop contents of this View. This will apply a visual effect to the result of the backdrop contents of this View before it is drawn. For example if createBlurEffect is provided, the previous content behind this View will be blurred before this View is drawn.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBackground

Set the background to a given Drawable, or remove the background. If the background has padding, this View's padding is set to the background's padding. However, when a background is removed, this View's padding isn't touched. If setting the padding is desired, please use setPadding.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBackgroundColor

Sets the background color for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBackgroundDrawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBackgroundResource

Set the background to a given resource. The resource should refer to a Drawable object or 0 to remove the background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBackgroundTintBlendMode

Specifies the blending mode used to apply the tint specified by setBackgroundTintList} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBackgroundTintList

Applies a tint to the background drawable. Does not modify the current tint mode, which is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#` by default.

Subsequent calls to setBackground will automatically mutate the drawable and apply the specified tint and tint mode using setTintList.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBackgroundTintMode

Specifies the blending mode used to apply the tint specified by setBackgroundTintList} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setBottom

Sets the bottom position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setCameraDistance

Sets the distance along the Z axis (orthogonal to the X/Y plane on which views are drawn) from the camera to this view. The camera's distance affects 3D transformations, for instance rotations around the X and Y axis. If the rotationX or rotationY properties are changed and this view is large (more than half the size of the screen), it is recommended to always use a camera distance that's greater than the height (X axis rotation) or the width (Y axis rotation) of this view.

The distance of the camera from the view plane can have an affect on the perspective distortion of the view when it is rotated around the x or y axis. For example, a large distance will result in a large viewing angle, and there will not be much perspective distortion of the view as it rotates. A short distance may cause much more perspective distortion upon rotation, and can also result in some drawing artifacts if the rotated view ends up partially behind the camera (which is why the recommendation is to use a distance at least as far as the size of the view, if the view is to be rotated.)

The distance is expressed in "depth pixels." The default distance depends on the screen density. For instance, on a medium density display, the default distance is 1280. On a high density display, the default distance is 1920.

If you want to specify a distance that leads to visually consistent results across various densities, use the following formula:

```kotlin
float scale = context.getResources().getDisplayMetrics().density;
  view.setCameraDistance(distance * scale);
  
```

The density scale factor of a high density display is 1.5, and 1920 = 1280 \* 1.5.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setClickable

Enables or disables click events for this view. When a view is clickable it will change its state to "pressed" on every click. Subclasses should set the view clickable to visually react to user's clicks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setClipBounds

Sets a rectangular area on this view to which the view will be clipped when it is drawn. Setting the value to null will remove the clip bounds and the view will draw normally, using its full bounds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setClipToOutline

Sets whether the View's Outline should be used to clip the contents of the View.

Only a single non-rectangular clip can be applied on a View at any time. Circular clips from a createCircularReveal animation take priority over Outline clipping, and child Outline clipping takes priority over Outline clipping done by a parent.

Note that this flag will only be respected if the View's Outline returns true from canClip.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setContentCaptureSession

Sets the (optional) `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession.html#` associated with this view.

This method should be called when you need to associate a `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext.html#` to the content capture events associated with this view or its view hierarchy (if it's a `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`).

For example, if your activity is associated with a web domain, first you would need to set the context for the main DOM:

```kotlin
ContentCaptureSession mainSession = rootView.getContentCaptureSession();
    mainSession.setContentCaptureContext(ContentCaptureContext.forLocusId(Uri.parse(myUrl));
  
```

Then if the page had an `IFRAME`, you would create a new session for it:

```kotlin
ContentCaptureSession iframeSession = mainSession.createContentCaptureSession(
        ContentCaptureContext.forLocusId(Uri.parse(iframeUrl)));
    iframeView.setContentCaptureSession(iframeSession);
  
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setContentDescription

Sets the `https://developer.android.com/reference/kotlin/android/view/View.html#`'s content description.

A content description briefly describes the view and is primarily used for accessibility support to determine how a view should be presented to the user. In the case of a view with no textual representation, such as ImageButton, a useful content description explains what the view does. For example, an image button with a phone icon that is used to place a call may use "Call" as its content description. An image of a floppy disk that is used to save a file may use "Save".

This should omit role or state. Role refers to the kind of user-interface element the View is, such as a Button or Checkbox. State refers to a frequently changing property of the View, such as an On/Off state of a button or the audio level of a volume slider.

Content description updates are not frequent, and are used when the semantic content - not the state - of the element changes. For example, a Play button might change to a Pause button during music playback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setContentSensitivity

Sets content sensitivity mode to determine whether this view displays sensitive content (e.g. username, password etc.). The system will improve user privacy i.e. hide content drawn by a sensitive view from screen sharing and recording.

The window hosting a sensitive view will be marked as secure during an active media projection session. This would be equivalent to applying `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_SECURE:kotlin.Int` to the window.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setContextClickable

Enables or disables context clicking for this view. This event can launch the listener.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setDefaultFocusHighlightEnabled

Sets whether this View should use a default focus highlight when it gets focused but doesn't have `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` defined in its background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setDrawingCacheBackgroundColor

Setting a solid background color for the drawing cache's bitmaps will improve performance and memory usage. Note, though that this should only be used if this view will always be drawn on top of a solid color.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setDrawingCacheEnabled

Enables or disables the drawing cache. When the drawing cache is enabled, the next call to getDrawingCache or buildDrawingCache will draw the view in a bitmap. Calling draw will not draw from the cache when the cache is enabled. To benefit from the cache, you must request the drawing cache by calling getDrawingCache and draw it on screen if the returned bitmap is not null.

Enabling the drawing cache is similar to setLayerType when hardware acceleration is turned off. When hardware acceleration is turned on, enabling the drawing cache has no effect on rendering because the system uses a different mechanism for acceleration which ignores the flag. If you want to use a Bitmap for the view, even when hardware acceleration is enabled, see setLayerType for information on how to enable software and hardware layers.

This API can be used to manually generate a bitmap copy of this view, by setting the flag to `true` and calling getDrawingCache.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setDrawingCacheQuality

Set the drawing cache quality of this view. This value is used only when the drawing cache is enabled

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setDuplicateParentStateEnabled

Enables or disables the duplication of the parent's state into this view. When duplication is enabled, this view gets its drawable state from its parent rather than from its own internal properties.

Note: in the current implementation, setting this property to true after the view was added to a ViewGroup might have no effect at all. This property should always be used from XML or set to true before adding this view to a ViewGroup.

Note: if this view's parent addStateFromChildren property is enabled and this property is enabled, an exception will be thrown.

Note: if the child view uses and updates additional states which are unknown to the parent, these states should not be affected by this method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setElevation

Sets the base elevation of this view, in pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setEnabled

Set the enabled state of this view. The interpretation of the enabled state varies by subclass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFadingEdgeLength

Set the size of the faded edge used to indicate that more content in this view is available. Will not change whether the fading edge is enabled; use setVerticalFadingEdgeEnabled or setHorizontalFadingEdgeEnabled to enable the fading edge for the vertical or horizontal fading edges.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFilterTouchesWhenObscured

Sets whether the framework should discard touches when the view's window is obscured by another visible window at the touched location. Refer to the `https://developer.android.com/reference/kotlin/android/view/View.html#` security documentation for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFitsSystemWindows

Sets whether or not this view should account for system screen decorations such as the status bar and inset its content; that is, controlling whether the default implementation of fitSystemWindows will be executed. See that method for more details.

Note that if you are providing your own implementation of fitSystemWindows, then there is no need to set this flag to true -- your implementation will be overriding the default implementation that checks this flag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFocusable

Set whether this view can receive the focus.

Setting this to false will also ensure that this view is not focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFocusable

Sets whether this view can receive focus.

Setting this to `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSABLE_AUTO:kotlin.Int` tells the framework to determine focusability automatically based on the view's interactivity. This is the default.

Setting this to NOT_FOCUSABLE will ensure that this view is also not focusable in touch mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFocusableInTouchMode

Set whether this view can receive focus while in touch mode. Setting this to true will also ensure that this view is focusable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFocusedByDefault

Sets whether this View should receive focus when the focus is restored for the view hierarchy containing this view.

Focus gets restored for a view hierarchy when the root of the hierarchy gets added to a window or serves as a target of cluster navigation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setForceDarkAllowed

Sets whether or not to allow force dark to apply to this view. Setting this to false will disable the auto-dark feature on everything this view draws, including any descendants. Setting this to true will allow this view to be automatically made dark, however a value of 'true' will not override any 'false' value in its parent chain nor will it prevent any 'false' in any of its children. The default behavior of force dark is also influenced by the Theme's `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_isLightTheme:kotlin.Int` attribute. If a theme is isLightTheme="false", then force dark is globally disabled for that theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setForeground

Supply a Drawable that is to be rendered on top of all of the content in the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setForegroundGravity

Describes how the foreground is positioned. Defaults to START and TOP.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setForegroundTintBlendMode

Specifies the blending mode used to apply the tint specified by setForegroundTintList} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setForegroundTintList

Applies a tint to the foreground drawable. Does not modify the current tint mode, which is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#` by default.

Subsequent calls to setForeground will automatically mutate the drawable and apply the specified tint and tint mode using setTintList.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setForegroundTintMode

Specifies the blending mode used to apply the tint specified by setForegroundTintList} to the background drawable. The default mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFrameContentVelocity

Set the current velocity of the View, we only track positive value. We will use the velocity information to adjust the frame rate when applicable. For example, we could potentially lower the frame rate when the velocity of a fling gesture becomes slower. Note that this is only valid till the next drawn frame.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHandwritingBoundsOffsets

Set the amount of offset applied to this view's stylus handwriting bounds. A positive offset will offset the edge outwards.The base handwriting bounds of a view is its visible bounds. The handwriting bounds offsets are applied to the base handwriting bounds to determine the final handwriting bounds.

This method is mainly used to enlarge the view's handwriting bounds for a better user experience.

Note that when the view is clipped (e.g. the view is in a ScrollView), the offsets are applied after the view's handwriting bounds is clipped.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHandwritingDelegateFlags

Sets flags configuring the handwriting delegation behavior for this delegate editor view.

This method has no effect unless setIsHandwritingDelegate is also called to configure this view to act as a handwriting delegate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHandwritingDelegatorCallback

Sets a callback which should be called when a stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#` occurs within this view's bounds. The callback will be called from the UI thread.

Setting a callback allows this view to act as a handwriting delegator, so that handwriting mode for a delegate editor view can be initiated by stylus movement on this delegator view. The callback implementation is expected to show and focus the delegate editor view. If a view which returns `true` for isHandwritingDelegate creates an input connection while the same stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#` sequence is ongoing, handwriting mode will be initiated for that view.

A common use case is a custom view which looks like a text editor but does not actually support text editing itself, and clicking on the custom view causes an EditText to be shown. To support handwriting initiation in this case, this method can be called on the custom view to configure it as a delegator. The EditText should call setIsHandwritingDelegate to set it as a delegate. The `callback` implementation is typically the same as the click listener implementation which shows the EditText.

If `null` is passed, this view will no longer act as a handwriting initiation delegator.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHapticFeedbackEnabled

Set whether this view should have haptic feedback for events such as long presses.

You may wish to disable haptic feedback if your view already controls its own haptic feedback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHasTransientState

Set whether this view is currently tracking transient state that the framework should attempt to preserve when possible. This flag is reference counted, so every call to setHasTransientState(true) should be paired with a later call to setHasTransientState(false).

A view with transient state cannot be trivially rebound from an external data source, such as an adapter binding item views in a list. This may be because the view is performing an animation, tracking user selection of content, or similar.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHorizontalFadingEdgeEnabled

Define whether the horizontal edges should be faded when this view is scrolled horizontally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHorizontalScrollBarEnabled

Define whether the horizontal scrollbar should be drawn or not. The scrollbar is not drawn by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHorizontalScrollbarThumbDrawable

Defines the horizontal thumb drawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHorizontalScrollbarTrackDrawable

Defines the horizontal track drawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setHovered

Sets whether the view is currently hovered.

Calling this method also changes the drawable state of the view. This enables the view to react to hover by using different drawable resources to change its appearance.

The onHoverChanged method is called when the hovered state changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setId

Sets the identifier for this view. The identifier does not have to be unique in this view's hierarchy. The identifier should be a positive number.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setImportantForAccessibility

Sets how to determine whether this view is important for accessibility which is if it fires accessibility events and if it is reported to accessibility services that query the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setImportantForAutofill

Sets the mode for determining whether this view is considered important for autofill.

The platform determines the importance for autofill automatically but you can use this method to customize the behavior. For example:

1. When the view contents is irrelevant for autofill (for example, a text field used in a "Captcha" challenge), it should be `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int`.
2. When both the view and its children are irrelevant for autofill (for example, the root view of an activity containing a spreadhseet editor), it should be `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int`.
3. When the view content is relevant for autofill but its children aren't (for example, a credit card expiration date represented by a custom view that overrides the proper autofill methods and has 2 children representing the month and year), it should be `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_YES_EXCLUDE_DESCENDANTS:kotlin.Int`.

**Note:** Setting the mode as `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_AUTOFILL_NO_EXCLUDE_DESCENDANTS:kotlin.Int` does not guarantee the view (and its children) will not be used for autofill purpose; for example, when the user explicitly makes an autofill request, all views are included in the ViewStructure, and starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` the system uses other factors along with importance to determine the autofill behavior. See isImportantForAutofill for more details about how the View's importance for autofill is used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setImportantForContentCapture

Sets the mode for determining whether this view is considered important for content capture.

The platform determines the importance for autofill automatically but you can use this method to customize the behavior. Typically, a view that provides text should be marked as `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_CONTENT_CAPTURE_YES:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setIsCredential

Sets whether this view is a credential for Credential Manager purposes.

See isCredential.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setIsHandwritingDelegate

Sets this view to be a handwriting delegate. If a delegate view creates an input connection while a stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#` sequence from a delegator view is ongoing, handwriting mode will be initiated for the delegate view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setKeepScreenOn

Controls whether the screen should remain on, modifying the value of `https://developer.android.com/reference/kotlin/android/view/View.html#KEEP_SCREEN_ON:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setKeyboardNavigationCluster

Set whether this view is a root of a keyboard navigation cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLabelFor

Sets the id of a view for which this view serves as a label for accessibility purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLayerPaint

Updates the `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` object used with the current layer (used only if the current layer type is not set to `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_NONE:kotlin.Int`). Changed properties of the Paint provided to setLayerType will be used the next time the View is redrawn, but setLayerPaint must be called to ensure that the view gets redrawn immediately.

A layer is associated with an optional `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` instance that controls how the layer is composed on screen. The following properties of the paint are taken into account when composing the layer:

- getAlpha
- getXfermode
- getColorFilter

If this view has an alpha value set to \< 1.0 by calling setAlpha, the alpha value of the layer's paint is superseded by this view's alpha value.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLayerType

Specifies the type of layer backing this view. The layer can be `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_SOFTWARE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int`.

A layer is associated with an optional `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` instance that controls how the layer is composed on screen. The following properties of the paint are taken into account when composing the layer:

- getAlpha
- getXfermode
- getColorFilter

If this view has an alpha value set to \< 1.0 by calling setAlpha, the alpha value of the layer's paint is superseded by this view's alpha value.

Refer to the documentation of `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_SOFTWARE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int` for more information on when and how to use layers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLayoutDirection

Set the layout direction for this view. This will propagate a reset of layout direction resolution to the view's children and resolve layout direction for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLayoutParams

Set the layout parameters associated with this view. These supply parameters to the *parent* of this view specifying how it should be arranged. There are many subclasses of ViewGroup.LayoutParams, and these correspond to the different subclasses of ViewGroup that are responsible for arranging their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLeft

Sets the left position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLeftTopRightBottom

Assign a size and position to this view. This method is meant to be used in animations only as it applies this position and size for the view only temporary and it can be changed back at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setLongClickable

Enables or disables long click events for this view. When a view is long clickable it reacts to the user holding down the button for a longer duration than a tap. This event can either launch the listener or a context menu.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setMeasuredDimension

This method must be called by onMeasure to store the measured width and measured height. Failing to do so will trigger an exception at measurement time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setMinimumHeight

Sets the minimum height of the view. It is not guaranteed the view will be able to achieve this minimum height (for example, if its parent layout constrains it with less available height).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setMinimumWidth

Sets the minimum width of the view. It is not guaranteed the view will be able to achieve this minimum width (for example, if its parent layout constrains it with less available width).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setNestedScrollingEnabled

Enable or disable nested scrolling for this view.

If this property is set to true the view will be permitted to initiate nested scrolling operations with a compatible parent view in the current hierarchy. If this view does not implement nested scrolling this will have no effect. Disabling nested scrolling while a nested scroll is in progress has the effect of stopNestedScroll the nested scroll.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setNextClusterForwardId

Sets the id of the view to use as the root of the next keyboard navigation cluster.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setNextFocusDownId

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_DOWN:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setNextFocusForwardId

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_FORWARD:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setNextFocusLeftId

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_LEFT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setNextFocusRightId

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_RIGHT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setNextFocusUpId

Sets the id of the view to use when the next focus is `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_UP:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnApplyWindowInsetsListener

Set an `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener.html#` to take over the policy for applying window insets to this view. The listener's onApplyWindowInsets method will be called instead of the view's onApplyWindowInsets method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnCapturedPointerListener

Set a listener to receive callbacks when the pointer capture state of a view changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnClickListener

Register a callback to be invoked when this view is clicked. If this view is not clickable, it becomes clickable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnContextClickListener

Register a callback to be invoked when this view is context clicked. If the view is not context clickable, it becomes context clickable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnCreateContextMenuListener

Register a callback to be invoked when the context menu for this view is being built. If this view is not long clickable, it becomes long clickable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnDragListener

Register a drag event listener callback object for this View. The parameter is an implementation of `https://developer.android.com/reference/kotlin/android/view/View.OnDragListener.html#`. To send a drag event to a View, the system calls the onDrag method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnFocusChangeListener

Register a callback to be invoked when focus of this view changed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnGenericMotionListener

Register a callback to be invoked when a generic motion event is sent to this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnHoverListener

Register a callback to be invoked when a hover event is sent to this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnKeyListener

Register a callback to be invoked when a hardware key is pressed in this view. Key presses in software input methods will generally not trigger the methods of this listener.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnLongClickListener

Register a callback to be invoked when this view is clicked and held. If this view is not long clickable, it becomes long clickable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnReceiveContentListener

Sets the listener to be performReceiveContent to handle insertion of content into this view.

Depending on the type of view, this listener may be invoked for different scenarios. For example, for an editable TextView, this listener will be invoked for the following scenarios:

1. Paste from the clipboard (e.g. "Paste" or "Paste as plain text" action in the insertion/selection menu)
2. Content insertion from the keyboard (from commitContent)
3. Drag and drop (drop events from onDragEvent)
4. Autofill
5. Selection replacement via `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROCESS_TEXT:kotlin.String`

When setting a listener, clients must also declare the accepted MIME types. The listener will still be invoked even if the MIME type of the content is not one of the declared MIME types (e.g. if the user pastes content whose type is not one of the declared MIME types). In that case, the listener may reject the content (defer to the default platform behavior) or execute some other fallback logic (e.g. show an appropriate message to the user). The declared MIME types serve as a hint to allow different features to optionally alter their behavior. For example, a soft keyboard may optionally choose to hide its UI for inserting GIFs for a particular input field if the MIME types set here for that field don't include "image/gif" or "image/\*".

Note: MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lowercase letters, or use normalizeMimeType to ensure that it is converted to lowercase.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnScrollChangeListener

Register a callback to be invoked when the scroll X or Y positions of this view change.

**Note:** Some views handle scrolling independently from View and may have their own separate listeners for scroll-type events. For example, ListView allows clients to register an setOnScrollListener to listen for changes in list scroll position.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnSystemUiVisibilityChangeListener

Set a listener to receive callbacks when the visibility of the system bar changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOnTouchListener

Register a callback to be invoked when a touch event is sent to this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOutlineAmbientShadowColor

Sets the color of the ambient shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final ambient shadow is a function of the shadow caster height, the alpha channel of the outlineAmbientShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#ambientShadowAlpha:kotlin.Int` theme attribute.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOutlineProvider

Sets the `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#` of the view, which generates the Outline that defines the shape of the shadow it casts, and enables outline clipping.

The default ViewOutlineProvider, `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#BACKGROUND:android.view.ViewOutlineProvider`, queries the Outline from the View's background drawable, via getOutline. Changing the outline provider with this method allows this behavior to be overridden.

If the ViewOutlineProvider is null, if querying it for an outline returns false, or if the produced Outline is isEmpty, shadows will not be cast.

Only outlines that return true from canClip may be used for clipping.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOutlineSpotShadowColor

Sets the color of the spot shadow that is drawn when the view has a positive Z or elevation value.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different views with different colors.

The opacity of the final spot shadow is a function of the shadow caster height, the alpha channel of the outlineSpotShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#spotShadowAlpha:kotlin.Int` theme attribute.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOverScrollMode

Set the over-scroll mode for this view. Valid over-scroll modes are `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_ALWAYS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_IF_CONTENT_SCROLLS:kotlin.Int` (allow over-scrolling only if the view content is larger than the container), or `https://developer.android.com/reference/kotlin/android/view/View.html#OVER_SCROLL_NEVER:kotlin.Int`. Setting the over-scroll mode of a view will have an effect only if the view is capable of scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPadding

Sets the padding. The view may add on the space required to display the scrollbars, depending on the style and visibility of the scrollbars. So the values returned from getPaddingLeft, getPaddingTop, getPaddingRight and getPaddingBottom may be different from the values set in this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPaddingRelative

Sets the relative padding. The view may add on the space required to display the scrollbars, depending on the style and visibility of the scrollbars. So the values returned from getPaddingStart, getPaddingTop, getPaddingEnd and getPaddingBottom may be different from the values set in this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPendingCredentialRequest

Sets a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` request to retrieve credentials, when the user focuses on this given view. When this view is focused, the given `request` will be fired to `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#`, which will fetch content from all `https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService.html#` services on the device, and then display credential options to the user on a relevant UI (dropdown, keyboard suggestions etc.). When the user selects a credential, the final `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#` will be propagated to the given `callback`. Developers are expected to handle the response programmatically and perform a relevant action, e.g. signing in the user.

For details on how to build a Credential Manager request, please see `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#`.

This API should be called at any point before the user focuses on the view, e.g. during `onCreate` of an Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPivotX

Sets the x location of the point around which the view is setRotation and setScaleX. By default, the pivot point is centered on the object. Setting this property disables this behavior and causes the view to use only the explicitly set pivotX and pivotY values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPivotY

Sets the y location of the point around which the view is setRotation and setScaleY. By default, the pivot point is centered on the object. Setting this property disables this behavior and causes the view to use only the explicitly set pivotX and pivotY values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPointerIcon

Set the pointer icon to be used for a mouse pointer in the current view. Passing `null` will restore the pointer icon to its default value. Note that setting the pointer icon using this method will only set it for events coming from a mouse device (i.e. with source `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_MOUSE:kotlin.Int`). To resolve the pointer icon for other device types like styluses, override onResolvePointerIcon.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPreferKeepClear

Set a preference to keep the bounds of this view clear from floating windows above this view's window. This informs the system that the view is considered a vital area for the user and that ideally it should not be covered. Setting this is only appropriate for UI where the user would likely take action to uncover it.

The system will try to respect this preference, but when not possible will ignore it.

Note: This is independent from setPreferKeepClearRects. If both are set, both will be taken into account.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPreferKeepClearRects

Set a preference to keep the provided rects clear from floating windows above this view's window. This informs the system that these rects are considered vital areas for the user and that ideally they should not be covered. Setting this is only appropriate for UI where the user would likely take action to uncover it.

The system will try to respect this preference, but when not possible will ignore it.

Note: This is independent from setPreferKeepClear. If both are set, both will be taken into account.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setPressed

Sets the pressed state for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setRenderEffect

Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect.html#` to apply to this View. This will apply a visual effect to the results of the View before it is drawn. For example if createBlurEffect is provided, the contents will be drawn in a separate layer, then this layer will be blurred when this View is drawn.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setRevealOnFocusHint

Sets this view's preference for reveal behavior when it gains focus.

When set to true, this is a signal to ancestor views in the hierarchy that this view would prefer to be brought fully into view when it gains focus. For example, a text field that a user is meant to type into. Other views such as scrolling containers may prefer to opt-out of this behavior.

The default value for views is true, though subclasses may change this based on their preferred behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setRight

Sets the right position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setRotation

Sets the degrees that the view is rotated around the pivot point. Increasing values result in clockwise rotation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setRotationX

Sets the degrees that the view is rotated around the horizontal axis through the pivot point. Increasing values result in clockwise rotation from the viewpoint of looking down the x axis. When rotating large views, it is recommended to adjust the camera distance accordingly. Refer to setCameraDistance for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setRotationY

Sets the degrees that the view is rotated around the vertical axis through the pivot point. Increasing values result in counter-clockwise rotation from the viewpoint of looking down the y axis. When rotating large views, it is recommended to adjust the camera distance accordingly. Refer to setCameraDistance for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setSaveEnabled

Controls whether the saving of this view's state is enabled (that is, whether its onSaveInstanceState method will be called). Note that even if freezing is enabled, the view still must have an id assigned to it (via setId) for its state to be saved. This flag can only disable the saving of this view; any child views may still have their state saved.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setSaveFromParentEnabled

Controls whether the entire hierarchy under this view will save its state when a state saving traversal occurs from its parent. The default is true; if false, these views will not be saved unless saveHierarchyState is called directly on this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScaleX

Sets the amount that the view is scaled in x around the pivot point, as a proportion of the view's unscaled width. A value of 1 means that no scaling is applied.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScaleY

Sets the amount that the view is scaled in Y around the pivot point, as a proportion of the view's unscaled width. A value of 1 means that no scaling is applied.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScreenReaderFocusable

Sets whether this View should be a focusable element for screen readers and include non-focusable Views from its subtree when providing feedback.

Note: this is similar to using [`android:focusable`, but does not impact input focus behavior.](../android.view/View.md)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollBarDefaultDelayBeforeFade

Define the delay before scrollbars fade.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollBarFadeDuration

Define the scrollbar fade duration.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollBarSize

Define the scrollbar size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollBarStyle

Specify the style of the scrollbars. The scrollbars can be overlaid or inset. When inset, they add to the padding of the view. And the scrollbars can be drawn inside the padding area or on the edge of the view. For example, if a view has a background drawable and you want to draw the scrollbars inside the padding specified by the drawable, you can use SCROLLBARS_INSIDE_OVERLAY or SCROLLBARS_INSIDE_INSET. If you want them to appear at the edge of the view, ignoring the padding, then you can use SCROLLBARS_OUTSIDE_OVERLAY or SCROLLBARS_OUTSIDE_INSET.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollCaptureCallback

Sets the callback to receive scroll capture requests. This component is the adapter between the scroll capture API and application UI code. If no callback is set, the system may provide an implementation. Any value provided here will take precedence over a system version.

This view will be ignored when `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int` is set in its setScrollCaptureHint, regardless whether a callback has been set.

It is recommended to set the scroll capture hint `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int` when setting a custom callback to help ensure it is selected as the target.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollCaptureHint

Sets the scroll capture hint for this View. These flags affect the search for a potential scroll capture targets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollContainer

Change whether this view is one of the set of scrollable containers in its window. This will be used to determine whether the window can resize or must pan when a soft input area is open -- scrollable containers allow the window to use resize mode since the container will appropriately shrink.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollIndicators

Sets the state of all scroll indicators.

See setScrollIndicators for usage information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollIndicators

Sets the state of the scroll indicators specified by the mask. To change all scroll indicators at once, see setScrollIndicators.

When a scroll indicator is enabled, it will be displayed if the view can scroll in the direction of the indicator.

Multiple indicator types may be enabled or disabled by passing the logical OR of the desired types. If multiple types are specified, they will all be set to the same enabled state.

For example, to enable the top scroll indicatorExample: `setScrollIndicators`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollX

Set the horizontal scrolled position of your view. This will cause a call to onScrollChanged and the view will be invalidated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollY

Set the vertical scrolled position of your view. This will cause a call to onScrollChanged and the view will be invalidated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setScrollbarFadingEnabled

Define whether scrollbars will fade when the view is not scrolling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setSelected

Changes the selection state of this view. A view can be selected or not. Note that selection is not the same as focus. Views are typically selected in the context of an AdapterView like ListView or GridView; the selected view is the view that is highlighted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setSoundEffectsEnabled

Set whether this view should have sound effects enabled for events such as clicking and touching.

You may wish to disable sound effects for a view if you already play sounds, for instance, a dial key that plays dtmf tones.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setStateDescription

Sets the `https://developer.android.com/reference/kotlin/android/view/View.html#`'s state description.

A state description briefly describes the states of the view and is primarily used for accessibility support to determine how the states of a view should be presented to the user. It is a supplement to the boolean states (for example, checked/unchecked) and it is used for customized state description (for example, "wifi, connected, three bars"). State description changes frequently while content description should change less often. State description should be localized. For android widgets which have default state descriptions, app developers can call this method to override the state descriptions. Setting state description to null restores the default behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setStateListAnimator

Attaches the provided StateListAnimator to this View.

Any previously attached StateListAnimator will be detached.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setSupplementalDescription

Sets the `https://developer.android.com/reference/kotlin/android/view/View.html#`'s supplemental description.

A supplemental description provides brief supplemental information for this node, such as the purpose of the node when that purpose is not conveyed within its textual representation. For example, if a dropdown select has a purpose of setting font family, the supplemental description could be "font family". If this node has children, its supplemental description serves as additional information and is not intended to replace any existing information in the subtree. This is different from the setContentDescription in that this description is purely supplemental while a content description may be used to replace a description for a node or its subtree that an assistive technology would otherwise compute based on other properties of the node and its descendants.

This should omit role or state. Role refers to the kind of user-interface element the View is, such as a Button or Checkbox. State refers to a frequently changing property of the View, such as an On/Off state of a button or the audio level of a volume slider.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setSystemGestureExclusionRects

Sets a list of areas within this view's post-layout coordinate space where the system should not intercept touch or other pointing device gestures. *This method should be called by onLayout or onDraw.*

Use this to tell the system which specific sub-areas of a view need to receive gesture input in order to function correctly in the presence of global system gestures that may conflict. For example, if the system wishes to capture swipe-in-from-screen-edge gestures to provide system-level navigation functionality, a view such as a navigation drawer container can mark the left (or starting) edge of itself as requiring gesture capture priority using this API. The system may then choose to relax its own gesture recognition to allow the app to consume the user's gesture. It is not necessary for an app to register exclusion rects for broadly spanning regions such as the entirety of a `ScrollView` or for simple press and release click targets such as `Button`. Mark an exclusion rect when interacting with a view requires a precision touch gesture in a small area in either the X or Y dimension, such as an edge swipe or dragging a `SeekBar` thumb.

Note: the system will put a limit of `200dp` on the vertical extent of the exclusions it takes into account. The limit does not apply while the navigation bar is `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int` hidden, nor to the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setSystemUiVisibility

Request that the visibility of the status bar or other screen/window decorations be changed.

This method is used to put the over device UI into temporary modes where the user's attention is focused more on the application content, by dimming or hiding surrounding system affordances. This is typically used in conjunction with `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int`, allowing the applications content to be placed behind the action bar (and with these flags other system affordances) so that smooth transitions between hiding and showing them can be done.

Two representative examples of the use of system UI visibility is implementing a content browsing application (like a magazine reader) and a video playing application.

The first code shows a typical implementation of a View in a content browsing application. In this implementation, the application goes into a content-oriented mode by hiding the status bar and action bar, and putting the navigation elements into lights out mode. The user can then interact with content while in this mode. Such an application should provide an easy way for the user to toggle out of the mode (such as to check information in the status bar or access notifications). In the implementation here, this is done simply by tapping on the content.

This second code sample shows a typical implementation of a View in a video playing application. In this situation, while the video is playing the application would like to go into a complete full-screen mode, to use as much of the display as possible for the video. When in this state the user can not interact with the application; the system intercepts touching on the screen to pop the UI out of full screen mode. See fitSystemWindows for a sample layout that goes with this code.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTag

Sets a tag associated with this view and a key. A tag can be used to mark a view in its hierarchy and does not have to be unique within the hierarchy. Tags can also be used to store data within a view without resorting to another data structure. The specified key should be an id declared in the resources of the application to ensure it is unique (see the [ID resource type](https://developer.android.com/guide/topics/resources/more-resources.html#Id)). Keys identified as belonging to the Android framework or not associated with any package will cause an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` to be thrown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTag

Sets the tag associated with this view. A tag can be used to mark a view in its hierarchy and does not have to be unique within the hierarchy. Tags can also be used to store data within a view without resorting to another data structure.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTextAlignment

Set the text alignment.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTextDirection

Set the text direction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTooltipText

Sets the tooltip text which will be displayed in a small popup next to the view.

The tooltip will be displayed:

- On long click, unless it is handled otherwise (by OnLongClickListener or a context menu).
- On hover, after a brief delay since the pointer has stopped moving

**Note:** Do not override this method, as it will have no effect on the text displayed in the tooltip.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTop

Sets the top position of this view relative to its parent. This method is meant to be called by the layout system and should not generally be called otherwise, because the property may be changed at any time by the layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTouchDelegate

Sets the TouchDelegate for this View.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTransitionAlpha

This property is intended only for use by the Fade transition, which animates it to produce a visual translucency that does not side-effect (or get affected by) the real alpha property. This value is composited with the other alpha value (and the AlphaAnimation value, when that is present) to produce a final visual translucency result, which is what is passed into the DisplayList.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTransitionName

Sets the name of the View to be used to identify Views in Transitions. Names should be unique in the View hierarchy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTransitionVisibility

Changes the visibility of this View without triggering any other changes. This should only be used by animation frameworks, such as `https://developer.android.com/reference/kotlin/android/transition/Transition.html#`, where visibility changes should not adjust focus or trigger a new layout. Application developers should use setVisibility instead to ensure that the hierarchy is correctly updated.

Only call this method when a temporary visibility must be applied during an animation and the original visibility value is guaranteed to be reset after the animation completes. Use setVisibility in all other cases.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTranslationX

Sets the horizontal location of this view relative to its getLeft position. This effectively positions the object post-layout, in addition to wherever the object's layout placed it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTranslationY

Sets the vertical location of this view relative to its getTop position. This effectively positions the object post-layout, in addition to wherever the object's layout placed it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTranslationZ

Sets the depth location of this view relative to its getElevation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setVerticalFadingEdgeEnabled

Define whether the vertical edges should be faded when this view is scrolled vertically.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setVerticalScrollBarEnabled

Define whether the vertical scrollbar should be drawn or not. The scrollbar is not drawn by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setVerticalScrollbarPosition

Set the position of the vertical scroll bar. Should be one of `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBAR_POSITION_DEFAULT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBAR_POSITION_LEFT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#SCROLLBAR_POSITION_RIGHT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setVerticalScrollbarThumbDrawable

Defines the vertical scrollbar thumb drawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setVerticalScrollbarTrackDrawable

Defines the vertical scrollbar track drawable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setViewTranslationCallback

Sets a `https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback.html#` that is used to display/hide the translated information. Developers can provide the customized implementation for show/hide translated information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setVisibility

Set the visibility state of this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setWillNotCacheDrawing

When a View's drawing cache is enabled, drawing is redirected to an offscreen bitmap. Some views, like an ImageView, must be able to bypass this mechanism if they already draw a single bitmap, to avoid unnecessary usage of the memory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setWillNotDraw

If this view doesn't do any drawing on its own, set this flag to allow further optimizations. By default, this flag is not set on View, but could be set on some View subclasses such as ViewGroup. Typically, if you override onDraw you should clear this flag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setX

Sets the visual x position of this view, in pixels. This is equivalent to setting the setTranslationX property to be the difference between the x value passed in and the current getLeft property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setY

Sets the visual y position of this view, in pixels. This is equivalent to setting the setTranslationY property to be the difference between the y value passed in and the current getTop property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setZ

Sets the visual z position of this view, in pixels. This is equivalent to setting the setTranslationZ property to be the difference between the z value passed in and the current getElevation property.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` showContextMenu

Shows the context menu for this view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` showContextMenu

Shows the context menu for this view anchored to the specified view-relative coordinate.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode.html#!` startActionMode

Start an action mode with the default type `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#TYPE_PRIMARY:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode.html#!` startActionMode

Start an action mode with the given type.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startAnimation

Start the specified animation now.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` startDrag

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` startDragAndDrop

Starts a drag and drop operation. When your application calls this method, it passes a `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder.html#` object to the system. The system calls this object's onProvideShadowMetrics to get metrics for the drag shadow, and then calls the object's onDrawShadow to draw the drag shadow itself.

Once the system has the drag shadow, it begins the drag and drop operation by sending drag events to all the View objects in your application that are currently visible. It does this either by calling the View object's drag listener (an implementation of onDrag or by calling the View object's onDragEvent method. Both are passed a `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#` object that has a getAction value of `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#ACTION_DRAG_STARTED:kotlin.Int`.

Your application can invoke startDragAndDrop on any attached View object. The View object does not need to be the one used in `https://developer.android.com/reference/kotlin/android/view/View.DragShadowBuilder.html#`, nor does it need to be related to the View the user selected for dragging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` startNestedScroll

Begin a nestable scroll operation along the given axes.

A view starting a nested scroll promises to abide by the following contract:

The view will call startNestedScroll upon initiating a scroll operation. In the case of a touch scroll this corresponds to the initial `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_DOWN:kotlin.Int`. In the case of touch scrolling the nested scroll will be terminated automatically in the same manner as requestDisallowInterceptTouchEvent. In the event of programmatic scrolling the caller must explicitly call stopNestedScroll to indicate the end of the nested scroll.

If `startNestedScroll` returns true, a cooperative parent was found. If it returns false the caller may ignore the rest of this contract until the next scroll. Calling startNestedScroll while a nested scroll is already in progress will return true.

At each incremental step of the scroll the caller should invoke dispatchNestedPreScroll once it has calculated the requested scrolling delta. If it returns true the nested scrolling parent at least partially consumed the scroll and the caller should adjust the amount it scrolls by.

After applying the remainder of the scroll delta the caller should invoke dispatchNestedScroll, passing both the delta consumed and the delta unconsumed. A nested scrolling parent may treat these values differently. See onNestedScroll.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` stopNestedScroll

Stop a nested scroll in progress.

Calling this method when a nested scroll is not currently in progress is harmless.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` toString

Returns a string representation of the object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` transformMatrixToGlobal

Modifies the input matrix such that it maps view-local coordinates to on-screen coordinates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` transformMatrixToLocal

Modifies the input matrix such that it maps on-screen coordinates to view-local coordinates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` unregisterCalledFromWrongThreadListener

Unregisters a listener that was previously registered with registerCalledFromWrongThreadListener.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` unscheduleDrawable

Unschedule any events associated with the given Drawable. This can be used when selecting a new Drawable into a view, so that the previous one is completely unscheduled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` unscheduleDrawable

Cancels a scheduled action on a drawable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` updateDragShadow

Updates the drag shadow for the ongoing drag and drop operation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` verifyDrawable

If your view subclass is displaying its own Drawable objects, it should override this function and return true for any Drawable it is displaying. This allows animations for those drawables to be scheduled.

Be sure to call through to the super class when overriding this function. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` willNotCacheDrawing

Returns whether or not this View can cache its drawing or not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` willNotDraw

Returns whether or not this View draws on its own.

<br />

From class ViewSwitcher `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` addView

Adds a child view with the specified layout parameters.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` getNextView

Returns the next view to be displayed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` reset

Reset the ViewSwitcher to hide all of the existing views and to make it think that the first time animation has not yet played.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setFactory

Sets the factory used to create the two views between which the ViewSwitcher will flip. Instead of using a factory, you can call #addView(android.view.View,int,android.view.ViewGroup.LayoutParams) twice.

<br />

From class FrameLayout `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` checkLayoutParams

<br />

`https://developer.android.com/reference/kotlin/android/widget/FrameLayout.LayoutParams!` generateDefaultLayoutParams

Returns a set of layout parameters with a width of `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int`, and a height of `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/widget/FrameLayout.LayoutParams!` generateLayoutParams

Returns a new set of layout parameters based on the supplied attributes set.

<br />

`https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#!` generateLayoutParams

Returns a safe set of layout parameters based on the supplied layout params. When a ViewGroup is passed a View whose layout params do not pass the test of checkLayoutParams, this method is invoked. This method should return a new set of layout params suitable for this ViewGroup, possibly by copying the appropriate attributes from the specified set of layout params.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getConsiderGoneChildrenWhenMeasuring

Determines whether all children, or just those in the VISIBLE or INVISIBLE state, are considered when measuring.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getMeasureAllChildren

Determines whether all children, or just those in the VISIBLE or INVISIBLE state, are considered when measuring.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onLayout

Called from layout when this view should assign a size and position to each of its children. Derived classes with children should override this method and call layout on each of their children.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` onMeasure

Measure the view and its content to determine the measured width and the measured height. This method is invoked by measure and should be overridden by subclasses to provide accurate and efficient measurement of their contents.

**CONTRACT:** When overriding this method, you *must* call setMeasuredDimension to store the measured width and height of this view. Failure to do so will trigger an `IllegalStateException`, thrown by measure. Calling the superclass' onMeasure is a valid use.

The base class implementation of measure defaults to the background size, unless a larger size is allowed by the MeasureSpec. Subclasses should override onMeasure to provide better measurements of their content.

If this method is overridden, it is the subclass's responsibility to make sure the measured height and width are at least the view's minimum height and width (getSuggestedMinimumHeight and getSuggestedMinimumWidth).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setForegroundGravity

Describes how the foreground is positioned. Defaults to START and TOP.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setMeasureAllChildren

Sets whether to consider all children, or just those in the VISIBLE or INVISIBLE state, when measuring. Defaults to false.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` shouldDelayChildPressedState

Return true if the pressed state should be delayed for children or descendants of this ViewGroup. Generally, this should be done for containers that can scroll, such as a List. This prevents the pressed state from appearing when the user is actually trying to scroll the content. The default implementation returns true for compatibility reasons. Subclasses that do not scroll should generally override this method and return false.

<br />

From class ViewAnimator `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getAnimateFirstView

Returns whether the current View should be animated the first time the ViewAnimator is displayed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getBaseline

Return the offset of the widget's text baseline from the widget's top boundary. If this widget does not support baseline alignment, this method returns -1.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#!` getCurrentView

Returns the View corresponding to the currently displayed child.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getDisplayedChild

Returns the index of the currently displayed child view.

<br />

`https://developer.android.com/reference/kotlin/android/view/animation/Animation.html#!` getInAnimation

Returns the current animation used to animate a View that enters the screen.

<br />

`https://developer.android.com/reference/kotlin/android/view/animation/Animation.html#!` getOutAnimation

Returns the current animation used to animate a View that exits the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeAllViews

Call this method to remove all child views from the ViewGroup.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeView

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeViewAt

Removes the view at the specified position in the group.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeViewInLayout

Removes a view during layout. This is useful if in your onLayout() method, you need to remove more views.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeViews

Removes the specified range of views from the group.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeViewsInLayout

Removes a range of views during layout. This is useful if in your onLayout() method, you need to remove more views.

**Note:** do not invoke this method from draw, onDraw, dispatchDraw or any related method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setAnimateFirstView

Indicates whether the current View should be animated the first time the ViewAnimator is displayed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setDisplayedChild

Sets which child view will be displayed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setInAnimation

Specifies the animation used to animate a View that enters the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setInAnimation

Specifies the animation used to animate a View that enters the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOutAnimation

Specifies the animation used to animate a View that exit the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOutAnimation

Specifies the animation used to animate a View that exit the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` showNext

Manually shows the next child.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` showPrevious

Manually shows the previous child.

<br />

Inherited properties From class `https://developer.android.com/reference/kotlin/android/view/View.html#` `https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#ALPHA:android.util.Property`

A Property wrapper around the `alpha` functionality handled by the setAlpha and getAlpha methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#EMPTY_STATE_SET:kotlin.IntArray`

Indicates the view has no states set. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#ENABLED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled, focused and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled, focused, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#ENABLED_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled and has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled, focused and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#ENABLED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#ENABLED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#ENABLED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is enabled and that its window has focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is focused and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is focused, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is focused. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view has the focus and that its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_ENABLED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled, focused and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_ENABLED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled, focused, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_ENABLED_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled and focused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_ENABLED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled, focused and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_ENABLED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_ENABLED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_ENABLED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed and enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_ENABLED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, enabled and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_FOCUSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, focused and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_FOCUSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, focused, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed and focused.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_FOCUSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, focused and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed and selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed, selected and its window has the focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#PRESSED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is pressed and its window has the focus.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#ROTATION:android.util.Property`

A Property wrapper around the `rotation` functionality handled by the setRotation and getRotation methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#ROTATION_X:android.util.Property`

A Property wrapper around the `rotationX` functionality handled by the setRotationX and getRotationX methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#ROTATION_Y:android.util.Property`

A Property wrapper around the `rotationY` functionality handled by the setRotationY and getRotationY methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#SCALE_X:android.util.Property`

A Property wrapper around the `scaleX` functionality handled by the setScaleX and getScaleX methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#SCALE_Y:android.util.Property`

A Property wrapper around the `scaleY` functionality handled by the setScaleY and getScaleY methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#SELECTED_STATE_SET:kotlin.IntArray`

Indicates the view is selected. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#SELECTED_WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view is selected and that its window has the focus.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#TRANSLATION_X:android.util.Property`

A Property wrapper around the `translationX` functionality handled by the setTranslationX and getTranslationX methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#TRANSLATION_Y:android.util.Property`

A Property wrapper around the `translationY` functionality handled by the setTranslationY and getTranslationY methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#TRANSLATION_Z:android.util.Property`

A Property wrapper around the `translationZ` functionality handled by the setTranslationZ and getTranslationZ methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/view/View.html#WINDOW_FOCUSED_STATE_SET:kotlin.IntArray`

Indicates the view's window has focus. States are used with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to change the drawing of the view depending on its state.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#X:android.util.Property`

A Property wrapper around the `x` functionality handled by the setX and getX methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#Y:android.util.Property`

A Property wrapper around the `y` functionality handled by the setY and getY methods.

<br />

`https://developer.android.com/reference/kotlin/android/util/Property.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>!` `https://developer.android.com/reference/kotlin/android/view/View.html#Z:android.util.Property`

A Property wrapper around the `z` functionality handled by the setZ and getZ methods.

<br />

## Public constructors

### ImageSwitcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSwitcher(context: Context!)
```

Creates a new empty ImageSwitcher.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: the application's environment |

### ImageSwitcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSwitcher(
    context: Context!, 
    attrs: AttributeSet!)
```

Creates a new empty ImageSwitcher for the given context and with the specified set attributes.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: the application environment |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: a collection of attributes |

## Public methods

### getAccessibilityClassName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibilityClassName(): CharSequence!
```

Return the class name of this object to be used for accessibility purposes. Subclasses should only override this if they are implementing something that should be seen as a completely new class of view when used by accessibility, unrelated to the class it is deriving from. This is used to fill in setClassName.

### setImageDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImageDrawable(drawable: Drawable!): Unit
```

Sets a new drawable on the ImageSwitcher. This will set that drawable on the next ImageView in the switcher and will then switch to that view.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md)!: the drawable to be set or `null` to clear the content |

**See Also**

- setImageDrawable

### setImageResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImageResource(resid: Int): Unit
```

Sets a new image on the ImageSwitcher with the given resource id. This will set that image resource on the next ImageView in the switcher and will then switch to that view.

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a Drawable resource id |

**See Also**

- setImageResource

### setImageURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImageURI(uri: Uri!): Unit
```

Sets a new image on the ImageSwitcher with the given Uri. This will set that image on the next ImageView in the switcher and will then switch to that view.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md)!: the Uri of an image |

**See Also**

- setImageURI
