Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RippleDrawable

```
open class RippleDrawable : LayerDrawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) |||
| | ↳ | [android.graphics.drawable.LayerDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable) ||
| | | ↳ | [android.graphics.drawable.RippleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#) |
| --- | --- | --- | --- |

Drawable that shows a ripple effect in response to state changes. The anchoring position of the ripple for a given state may be specified by calling #setHotspot(float,float) with the corresponding state attribute identifier.

A touch feedback drawable may contain multiple child layers, including a special mask layer that is not drawn to the screen. A single layer may be set as the mask from XML by specifying its `android:id` value as `https://developer.android.com/reference/kotlin/android/R.id.html#mask:kotlin.Int`. At run time, a single layer may be set as the mask using `setId(..., android.R.id.mask)` or an existing mask layer may be replaced using `setDrawableByLayerId(android.R.id.mask, ...)`.

```kotlin
<code>&lt;!-- A red ripple masked against an opaque rectangle. --&gt;
  &lt;ripple android:color="#ffff0000"&gt;
    &lt;item android:id="@android:id/mask"
          android:drawable="@android:color/white" /&gt;
  &lt;/ripple&gt;</code>
```

If a mask layer is set, the ripple effect will be masked against that layer before it is drawn over the composite of the remaining child layers.

If no mask layer is set, the ripple effect is masked against the composite of the child layers.

```kotlin
<code>&lt;!-- A green ripple drawn atop a black rectangle. --&gt;
  &lt;ripple android:color="#ff00ff00"&gt;
    &lt;item android:drawable="@android:color/black" /&gt;
  &lt;/ripple&gt;
 
  &lt;!-- A blue ripple drawn atop a drawable resource. --&gt;
  &lt;ripple android:color="#ff0000ff"&gt;
    &lt;item android:drawable="@drawable/my_drawable" /&gt;
  &lt;/ripple&gt;</code>
```

If no child layers or mask is specified and the ripple is set as a View background, the ripple will be drawn atop the first available parent background within the View's hierarchy. In this case, the drawing region may extend outside of the Drawable bounds.

```kotlin
<code>&lt;!-- An unbounded red ripple. --&gt;
  &lt;ripple android:color="#ffff0000" /&gt;</code>
```

## Summary

| XML attributes ||
|---|---|
| [`android:color`](https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#attr_RippleDrawable) | The color to use for ripple effects. |

Inherited XML attributes From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Bottom inset to apply to the layer.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Drawable used to render the layer.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` End inset to apply to the layer. Overrides `left` or `right` depending on layout direction.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Gravity used to align the layer within its container. If no value is specified, the default behavior depends on whether an explicit width or height has been set, If no dimension is set, gravity in that direction defaults to `fill_horizontal` or `fill_vertical`; otherwise, it defaults to `left` or `top`.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |
Constant Value Description bottom 50 Push object to the bottom of its container, not changing its size. center 11 Place the object in the center of its container in both the vertical and horizontal axis, not changing its size. center_horizontal 1 Place object in the horizontal center of its container, not changing its size. center_vertical 10 Place object in the vertical center of its container, not changing its size. clip_horizontal 8 Additional option that can be set to have the left and/or right edges of the child clipped to its container's bounds. The clip will be based on the horizontal gravity: a left gravity will clip the right edge, a right gravity will clip the left edge, and neither will clip both edges. clip_vertical 80 Additional option that can be set to have the top and/or bottom edges of the child clipped to its container's bounds. The clip will be based on the vertical gravity: a top gravity will clip the bottom edge, a bottom gravity will clip the top edge, and neither will clip both edges. end 800005 Push object to the end of its container, not changing its size. fill 77 Grow the horizontal and vertical size of the object if needed so it completely fills its container. fill_horizontal 7 Grow the horizontal size of the object if needed so it completely fills its container. fill_vertical 70 Grow the vertical size of the object if needed so it completely fills its container. left 3 Push object to the left of its container, not changing its size. right 5 Push object to the right of its container, not changing its size. start 800003 Push object to the beginning of its container, not changing its size. top 30 Push object to the top of its container, not changing its size.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Height of the layer. Defaults to the layer's intrinsic height.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Identifier of the layer. This can be used to retrieve the layer from a drawable container.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Left inset to apply to the layer.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Indicates how layer padding should affect the bounds of subsequent layers. The default padding mode value is nest.

Must be one of the following constant values.
Constant Value Description nest 0 Nest each layer inside the padding of the previous layer. stack 1 Stack each layer directly atop the previous layer.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Right inset to apply to the layer.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Start inset to apply to the layer. Overrides `left` or `right` depending on layout direction.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Top inset to apply to the layer.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#attr_LayerDrawable` Width of the layer. Defaults to the layer's intrinsic width.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

<br />

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#RADIUS_AUTO:kotlin.Int` Radius value that specifies the ripple radius should be computed based on the size of the ripple's container. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#INSET_UNDEFINED:kotlin.Int`

Value used for undefined start and end insets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_NEST:kotlin.Int`

Padding mode used to nest each layer inside the padding of the previous layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_STACK:kotlin.Int`

Padding mode used to stack each layer directly atop the previous layer.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#RippleDrawable(android.content.res.ColorStateList,%20android.graphics.drawable.Drawable,%20android.graphics.drawable.Drawable)(color: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#, content: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?, mask: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?)` Creates a new ripple drawable with the specified ripple color and optional content and mask drawables. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#applyTheme(android.content.res.Resources.Theme)(t: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#canApplyTheme()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#draw(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)` Optimized for drawing ripples with a mask layer and optional content. |
| --- | --- |
| open [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#getConstantState()()` Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable. |
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#getDirtyBounds()()` Return the drawable's dirty bounds Rect. |
| open [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#getEffectColor()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#getHotspotBounds(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Populates `outRect` with the hotspot bounds. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#getOpacity()()` Return the opacity/transparency of this Drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#getOutline(android.graphics.Outline)(outline: https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)` Populates `outline` with the first available layer outline, excluding the mask layer. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#getRadius()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#hasFocusStateSpecified()()` Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Inflate this Drawable from an XML resource optionally styled by a theme. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#invalidateSelf()()` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#isProjected()()` Whether this drawable requests projection. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#isStateful()()` Indicates whether this drawable will change its appearance based on state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#jumpToCurrentState()()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#mutate()()` Make this drawable mutable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#setColor(android.content.res.ColorStateList)(color: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)` Sets the ripple color. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#setDrawableByLayerId(kotlin.Int,%20android.graphics.drawable.Drawable)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!)` Replaces the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` for the layer with the given id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#setEffectColor(android.content.res.ColorStateList)(color: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)` Sets the ripple effect color. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#setHotspot(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Specifies the hotspot's location within the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#setPaddingMode(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies how layer padding should affect the bounds of subsequent layers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#setRadius(kotlin.Int)(radius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the radius in pixels of the fully expanded ripple. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#setVisible(kotlin.Boolean,%20kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, restart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is visible. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#onBoundsChange(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Override this in your subclass to change appearance if you vary based on the bounds. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#onStateChange(kotlin.IntArray)(stateSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Override this in your subclass to change appearance if you recognize the specified state. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#addLayer(android.graphics.drawable.Drawable)(dr: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!)`

Adds a new layer containing the specified `drawable` to the end of the layer list and returns its index.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#findDrawableByLayerId(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Looks for a layer with the given ID and returns its `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable`.

If multiple layers are found for the given ID, returns the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` for the matching layer at the highest index.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#findIndexByLayerId(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns the layer with the specified `id`.

If multiple layers have the same ID, returns the layer with the lowest index.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getAlpha()()`

Gets the current alpha value for the drawable. 0 means fully transparent, 255 means fully opaque. This method is implemented by Drawable subclasses and the value returned is specific to how that class treats alpha. The default return value is 255 if the class does not override this method to return a value specific to its use of alpha.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getBottomPadding()()`

Returns the bottom padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getChangingConfigurations()()`

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)` or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getDrawable(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns the drawable for the layer at the specified index.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getEndPadding()()`

Returns the end padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getId(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns the ID of the specified layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getIntrinsicHeight()()`

Returns the drawable's intrinsic height.

Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getIntrinsicWidth()()`

Returns the drawable's intrinsic width.

Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerGravity(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerHeight(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetBottom(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetEnd(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetLeft(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetRight(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetStart(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetTop(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerWidth(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLeftPadding()()`

Returns the left padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getNumberOfLayers()()`

Returns the number of layers contained within this layer drawable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)(padding: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`

Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getRightPadding()()`

Returns the right padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getStartPadding()()`

Returns the start padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getTopPadding()()`

Returns the top padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#invalidateDrawable(android.graphics.drawable.Drawable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)`

Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#isAutoMirrored()()`

Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#onLayoutDirectionChanged(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when the drawable's resolved layout direction changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#onLevelChange(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Override this in your subclass to change appearance if you vary based on level.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable, what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call `https://developer.android.com/reference/kotlin/android/os/Handler.html#postAtTime(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long)` with the parameters (what, who, when) to perform the scheduling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setAlpha(kotlin.Int)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setAutoMirrored(kotlin.Boolean)(mirrored: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setColorFilter(android.graphics.ColorFilter)(colorFilter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?)`

Specify an optional color filter for the drawable.

If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas.

Pass `null` to remove any existing color filter.

**Note:** Setting a non-`null` color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setDither(kotlin.Boolean)(dither: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!)`

Sets the drawable for the layer at the specified index.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setId(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the ID of a layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerGravity(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, gravity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the gravity used to position or stretch the specified layer within its container. Gravity is applied after any layer insets (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInset(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`) or padding (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`).

If gravity is specified as `https://developer.android.com/reference/kotlin/android/view/Gravity.html#NO_GRAVITY:kotlin.Int`, the default behavior depends on whether an explicit width or height has been set (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`), If a dimension is not set, gravity in that direction defaults to `https://developer.android.com/reference/kotlin/android/view/Gravity.html#FILL_HORIZONTAL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/Gravity.html#FILL_VERTICAL:kotlin.Int`; otherwise, gravity in that direction defaults to `https://developer.android.com/reference/kotlin/android/view/Gravity.html#LEFT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/Gravity.html#TOP:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerHeight(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInset(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Specifies the insets in pixels for the drawable at the specified index.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetBottom(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetEnd(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, e: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetLeft(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, e: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Specifies the relative insets in pixels for the drawable at the specified index.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetRight(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetStart(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetTop(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, w: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets an explicit size for the specified layer.

**Note:** Setting an explicit layer size changes the default layer gravity behavior. See `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerGravity(kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerWidth(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, w: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setOpacity(kotlin.Int)(opacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the opacity of this drawable directly instead of collecting the states from the layers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the absolute padding.

If padding in a dimension is specified as `-1`, the resolved padding will use the value computed according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`).

Calling this method clears any relative padding values previously set using `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the relative padding.

If padding in a dimension is specified as `-1`, the resolved padding will use the value computed according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`).

Calling this method clears any absolute padding values previously set using `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setTintBlendMode(android.graphics.BlendMode)(blendMode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#!)`

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setTintList(android.content.res.ColorStateList)(tint: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?)`

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#unscheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable, what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`

A Drawable can call this to unschedule an action previously scheduled with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)`. An implementation can generally simply call `https://developer.android.com/reference/kotlin/android/os/Handler.html#removeCallbacks(java.lang.Runnable,%20kotlin.Any)` with the parameters (what, who) to unschedule the drawable.

<br />

From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter()()`

Removes the color filter for this drawable.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds()()`

Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`

Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String)(pathName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Create a drawable from file path name.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#?, value: https://developer.android.com/reference/kotlin/android/util/TypedValue.html#?, is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Create a drawable from an inputstream, using the given resources and value to determine density information.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#?, value: https://developer.android.com/reference/kotlin/android/util/TypedValue.html#?, is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, opts: https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#?)`

Create a drawable from an inputstream, using the given resources and value to determine density information.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String)(is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Create a drawable from an inputstream

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`

Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)`

Create a drawable from an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`

Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)`

Create a drawable from inside an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds()()`

Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback()()`

Return the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation attached to this Drawable.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getColorFilter()()`

Returns the current color filter, or `null` if none set.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCurrent()()`

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds()()`

Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed).

By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection()()`

Returns the resolved layout direction for this Drawable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel()()`

Retrieve the current level.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumHeight()()`

Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumWidth()()`

Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Insets.html#` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpticalInsets()()`

Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState()()`

Describes the current state, as a union of primitive states, such as `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int`, etc. Some drawables may modify their imagery based on the selected state.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Region.html#?` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getTransparentRegion()()`

Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`

Inflate this Drawable from an XML resource. Does not apply a theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()()`

Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isFilterBitmap()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)(op1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, op2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned.

This is to help in implementing `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long)(what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`

Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback)(cb: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?)`

Bind a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` object to this Drawable. Required for clients that want to support animated drawables.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)(configs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)`

Specify a color and Porter-Duff mode to be the color filter for this drawable.

Convenience for `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` which constructs a `https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#`.

**Note:** Setting a color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setFilterBitmap(kotlin.Boolean)(filter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated.

This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level.

If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()` in order to have itself redrawn, *and* true will be returned from this function.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray)(stateSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \[`https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int`\].

If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()` in order to have itself redrawn, *and* true will be returned from this function.

Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int)(tintColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Specifies tint color for this drawable.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`.

To clear the tint, pass `null` to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode)(tintMode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?)`

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable)(what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`

Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable.

<br />

## XML attributes

### android:color

```
android:color
```
The color to use for ripple effects. This attribute is required.

May be a color value, in the form of "`rgb`", "`argb`", "`rrggbb`", or "`aarrggbb`".

## Constants

### RADIUS_AUTO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RADIUS_AUTO: Int
```

Radius value that specifies the ripple radius should be computed based on the size of the ripple's container.

 Value: -1

## Public constructors

### RippleDrawable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RippleDrawable(
    color: ColorStateList, 
    content: Drawable?, 
    mask: Drawable?)
```

Creates a new ripple drawable with the specified ripple color and optional content and mask drawables.

| Parameters ||
|---|---|
| `color` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#): The ripple color. This value cannot be `null`. |
| `content` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)?: The content drawable, may be `null` |
| `mask` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)?: The mask drawable, may be `null` |
| --- | --- |

## Public methods

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|---|---|
| `t` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#): This value cannot be `null`. |

### canApplyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canApplyTheme(): Boolean
```

### draw

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun draw(canvas: Canvas): Unit
```

Optimized for drawing ripples with a mask layer and optional content.

| Parameters ||
|---|---|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): This value cannot be `null`. |

### getConstantState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConstantState(): Drawable.ConstantState?
```

Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState?` | The ConstantState associated to that Drawable. This value may be `null`. |

### getDirtyBounds

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDirtyBounds(): Rect
```

Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed).

By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | The dirty bounds of this drawable. This value cannot be `null`. |

### getEffectColor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEffectColor(): ColorStateList
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#` | The ripple effect color as a color state list. This value cannot be `null`. |

### getHotspotBounds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHotspotBounds(outRect: Rect): Unit
```

Populates `outRect` with the hotspot bounds.

| Parameters ||
|---|---|
| `outRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): the rect to populate with the hotspot bounds. This value cannot be `null`. |

### getOpacity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpacity(): Int
```

Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`: `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int`.

An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT.

Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)` to perform a standard reduction of two opacities to the appropriate single output.

Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)` or #setColorFilter methods. Some subclasses, such as `https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable`, `https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable`, and `https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable`, do account for the value of `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)`, but the general behavior is dependent upon the implementation of the subclass.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int The opacity class of the Drawable. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int` |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOutline(outline: Outline): Unit
```

Populates `outline` with the first available layer outline, excluding the mask layer.

| Parameters ||
|---|---|
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#): Outline in which to place the first available layer outline. This value cannot be `null`. |

### getRadius

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRadius(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the radius in pixels of the fully expanded ripple if an explicit radius has been set, or `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#RADIUS_AUTO:kotlin.Int` if the radius is computed based on the container size |

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
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |
| `org.xmlpull.v1.XmlPullParserException` | |

### invalidateSelf

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateSelf(): Unit
```

Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable.

### isProjected

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isProjected(): Boolean
```

Whether this drawable requests projection. Indicates that the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#` this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver.

### isStateful

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStateful(): Boolean
```

Indicates whether this drawable will change its appearance based on state. Clients can use this to determine whether it is necessary to calculate their state and call setState.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this drawable changes its appearance based on state, false otherwise. |

### jumpToCurrentState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun jumpToCurrentState(): Unit
```

If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations.

### mutate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mutate(): Drawable
```

Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | This drawable. This value cannot be `null`. |

### setColor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColor(color: ColorStateList): Unit
```

Sets the ripple color.

| Parameters ||
|---|---|
| `color` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#): Ripple color as a color state list. This value cannot be `null`. |

### setDrawableByLayerId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDrawableByLayerId(
    id: Int, 
    drawable: Drawable!
): Boolean
```

Replaces the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` for the layer with the given id.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The layer ID to search for. |
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)!: The replacement `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` was replaced (could return false if the id was not found). |

### setEffectColor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEffectColor(color: ColorStateList): Unit
```

Sets the ripple effect color.

| Parameters ||
|---|---|
| `color` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#): Ripple color as a color state list. This value cannot be `null`. |

### setHotspot

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHotspot(
    x: Float, 
    y: Float
): Unit
```

Specifies the hotspot's location within the drawable.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X coordinate of the center of the hotspot |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y coordinate of the center of the hotspot |

### setHotspotBounds

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHotspotBounds(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the left bound |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the top bound |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the right bound |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the bottom bound |

### setPaddingMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPaddingMode(mode: Int): Unit
```

Specifies how layer padding should affect the bounds of subsequent layers. The default and recommended value for RippleDrawable is `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_STACK:kotlin.Int`.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): padding mode, one of: - `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_NEST:kotlin.Int` to nest each layer inside the padding of the previous layer - `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_STACK:kotlin.Int` to stack each layer directly atop the previous layer |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`

### setRadius

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRadius(radius: Int): Unit
```

Sets the radius in pixels of the fully expanded ripple.

| Parameters ||
|---|---|
| `radius` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): ripple radius in pixels, or `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable#RADIUS_AUTO:kotlin.Int` to compute the radius based on the container size |

### setVisible

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVisible(
    visible: Boolean, 
    restart: Boolean
): Boolean
```

Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations.

| Parameters ||
|---|---|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if visible, false if not. |
| `restart` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): You can supply true here to force the drawable to behave as if it has just become visible, even if it had last been set visible. Used for example to force animations to restart. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean Returns true if the new visibility is different than its previous state. |

## Protected methods

### onBoundsChange

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

Override this in your subclass to change appearance if you vary based on the bounds.

| Parameters ||
|---|---|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): This value cannot be `null`. |

### onStateChange

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
