Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LayerDrawable

```
open class LayerDrawable : Drawable, Drawable.Callback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](../android/graphics/drawable/Drawable.md) ||
| | ↳ | [android.graphics.drawable.LayerDrawable](../android/graphics/drawable/LayerDrawable.md) |

Known Direct Subclasses [RippleDrawable](../android/graphics/drawable/RippleDrawable.md), [TransitionDrawable](../android/graphics/drawable/TransitionDrawable.md) [RippleDrawable](../android/graphics/drawable/RippleDrawable.md) Drawable that shows a ripple effect in response to state changes.
[TransitionDrawable](../android/graphics/drawable/TransitionDrawable.md) An extension of LayerDrawables that is intended to cross-fade between the first and second layer.

A Drawable that manages an array of other Drawables. These are drawn in array order, so the element with the largest index will be drawn on top.

It can be defined in an XML file with the `<layer-list>` element. Each Drawable in the layer is defined in a nested `<item>`.

For more information, see the guide to [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

## Summary

| XML attributes ||
|---|---|
| [`android:bottom`](../android/graphics/drawable/LayerDrawable.md) | Bottom inset to apply to the layer. |
| [`android:drawable`](../android/graphics/drawable/LayerDrawable.md) | Drawable used to render the layer. |
| [`android:end`](../android/graphics/drawable/LayerDrawable.md) | End inset to apply to the layer. |
| --- | --- |
| [`android:gravity`](../android/graphics/drawable/LayerDrawable.md) | Gravity used to align the layer within its container. |
| [`android:height`](../android/graphics/drawable/LayerDrawable.md) | Height of the layer. |
| [`android:id`](../android/graphics/drawable/LayerDrawable.md) | Identifier of the layer. |
| --- | --- |
| [`android:left`](../android/graphics/drawable/LayerDrawable.md) | Left inset to apply to the layer. |
| [`android:paddingMode`](../android/graphics/drawable/LayerDrawable.md) | Indicates how layer padding should affect the bounds of subsequent layers. |
| [`android:right`](../android/graphics/drawable/LayerDrawable.md) | Right inset to apply to the layer. |
| --- | --- |
| [`android:start`](../android/graphics/drawable/LayerDrawable.md) | Start inset to apply to the layer. |
| [`android:top`](../android/graphics/drawable/LayerDrawable.md) | Top inset to apply to the layer. |
| [`android:width`](../android/graphics/drawable/LayerDrawable.md) | Width of the layer. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#INSET_UNDEFINED:kotlin.Int` Value used for undefined start and end insets. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_NEST:kotlin.Int` Padding mode used to nest each layer inside the padding of the previous layer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_STACK:kotlin.Int` Padding mode used to stack each layer directly atop the previous layer. |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#LayerDrawable(kotlin.Array)(layers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!>)` Creates a new layer drawable with the list of specified layers. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#addLayer(android.graphics.drawable.Drawable)(dr: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!)` Adds a new layer containing the specified `drawable` to the end of the layer list and returns its index. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#applyTheme(android.content.res.Resources.Theme)(t: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#canApplyTheme()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#draw(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)` Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). |
| open [Drawable](../android/graphics/drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#findDrawableByLayerId(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Looks for a layer with the given ID and returns its `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#findIndexByLayerId(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the layer with the specified `id`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getAlpha()()` Gets the current alpha value for the drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getBottomPadding()()` Returns the bottom padding in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getChangingConfigurations()()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| --- | --- |
| open [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getConstantState()()` Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable. |
| open [Drawable](../android/graphics/drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getDrawable(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the drawable for the layer at the specified index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getEndPadding()()` Returns the end padding in pixels. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getHotspotBounds(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Populates `outRect` with the hotspot bounds. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getId(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the ID of the specified layer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getIntrinsicHeight()()` Returns the drawable's intrinsic height. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getIntrinsicWidth()()` Returns the drawable's intrinsic width. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerGravity(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerHeight(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetBottom(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetEnd(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetLeft(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetRight(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetStart(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetTop(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerWidth(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLeftPadding()()` Returns the left padding in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getNumberOfLayers()()` Returns the number of layers contained within this layer drawable. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getOpacity()()` Return the opacity/transparency of this Drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getOutline(android.graphics.Outline)(outline: https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)` Populates `outline` with the first available (non-empty) layer outline. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)(padding: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getRightPadding()()` Returns the right padding in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getStartPadding()()` Returns the start padding in pixels. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getTopPadding()()` Returns the top padding in pixels. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#hasFocusStateSpecified()()` Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Inflate this Drawable from an XML resource optionally styled by a theme. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#invalidateDrawable(android.graphics.drawable.Drawable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)` Called when the drawable needs to be redrawn. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#isAutoMirrored()()` Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#isProjected()()` Whether this drawable requests projection. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#isStateful()()` Indicates whether this drawable will change its appearance based on state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#jumpToCurrentState()()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. |
| open [Drawable](../android/graphics/drawable/Drawable.md) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#mutate()()` Make this drawable mutable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#onLayoutDirectionChanged(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the drawable's resolved layout direction changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable, what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` A Drawable can call this to schedule the next frame of its animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setAlpha(kotlin.Int)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify an alpha value for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setAutoMirrored(kotlin.Boolean)(mirrored: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setColorFilter(android.graphics.ColorFilter)(colorFilter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?)` Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setDither(kotlin.Boolean)(dither: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!)` Sets the drawable for the layer at the specified index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setDrawableByLayerId(kotlin.Int,%20android.graphics.drawable.Drawable)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!)` Replaces the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` for the layer with the given id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setHotspot(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Specifies the hotspot's location within the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setId(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the ID of a layer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerGravity(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, gravity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the gravity used to position or stretch the specified layer within its container. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerHeight(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInset(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies the insets in pixels for the drawable at the specified index. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetBottom(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetEnd(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, e: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetLeft(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, e: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies the relative insets in pixels for the drawable at the specified index. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetRight(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetStart(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInsetTop(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, w: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, h: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets an explicit size for the specified layer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerWidth(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, w: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setOpacity(kotlin.Int)(opacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the opacity of this drawable directly instead of collecting the states from the layers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the absolute padding. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies how layer padding should affect the bounds of subsequent layers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the relative padding. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setTintBlendMode(android.graphics.BlendMode)(blendMode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#!)` Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setTintList(android.content.res.ColorStateList)(tint: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?)` Specifies tint color for this drawable as a color state list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setVisible(kotlin.Boolean,%20kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, restart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is visible. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#unscheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable)(who: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable, what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` A Drawable can call this to unschedule an action previously scheduled with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)`. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#onBoundsChange(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Override this in your subclass to change appearance if you vary based on the bounds. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#onLevelChange(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Override this in your subclass to change appearance if you vary based on level. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#onStateChange(kotlin.IntArray)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Override this in your subclass to change appearance if you recognize the specified state. |
| --- | --- |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter()()`

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

### android:bottom

```
android:bottom
```
Bottom inset to apply to the layer.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:drawable

```
android:drawable
```
Drawable used to render the layer.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:end

```
android:end
```
End inset to apply to the layer. Overrides `left` or `right` depending on layout direction.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:gravity

```
android:gravity
```
Gravity used to align the layer within its container. If no value is specified, the default behavior depends on whether an explicit width or height has been set, If no dimension is set, gravity in that direction defaults to `fill_horizontal` or `fill_vertical`; otherwise, it defaults to `left` or `top`.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---|---|---|
| bottom | 50 | Push object to the bottom of its container, not changing its size. |
| center | 11 | Place the object in the center of its container in both the vertical and horizontal axis, not changing its size. |
| center_horizontal | 1 | Place object in the horizontal center of its container, not changing its size. |
| --- | --- | --- |
| center_vertical | 10 | Place object in the vertical center of its container, not changing its size. |
| clip_horizontal | 8 | Additional option that can be set to have the left and/or right edges of the child clipped to its container's bounds. The clip will be based on the horizontal gravity: a left gravity will clip the right edge, a right gravity will clip the left edge, and neither will clip both edges. |
| clip_vertical | 80 | Additional option that can be set to have the top and/or bottom edges of the child clipped to its container's bounds. The clip will be based on the vertical gravity: a top gravity will clip the bottom edge, a bottom gravity will clip the top edge, and neither will clip both edges. |
| --- | --- | --- |
| end | 800005 | Push object to the end of its container, not changing its size. |
| fill | 77 | Grow the horizontal and vertical size of the object if needed so it completely fills its container. |
| fill_horizontal | 7 | Grow the horizontal size of the object if needed so it completely fills its container. |
| --- | --- | --- |
| fill_vertical | 70 | Grow the vertical size of the object if needed so it completely fills its container. |
| left | 3 | Push object to the left of its container, not changing its size. |
| right | 5 | Push object to the right of its container, not changing its size. |
| --- | --- | --- |
| start | 800003 | Push object to the beginning of its container, not changing its size. |
| top | 30 | Push object to the top of its container, not changing its size. |

### android:height

```
android:height
```
Height of the layer. Defaults to the layer's intrinsic height.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:id

```
android:id
```
Identifier of the layer. This can be used to retrieve the layer from a drawable container.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:left

```
android:left
```
Left inset to apply to the layer.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:paddingMode

```
android:paddingMode
```
Indicates how layer padding should affect the bounds of subsequent layers. The default padding mode value is nest.

Must be one of the following constant values.

| Constant | Value | Description |
|---|---|---|
| nest | 0 | Nest each layer inside the padding of the previous layer. |
| stack | 1 | Stack each layer directly atop the previous layer. |

### android:right

```
android:right
```
Right inset to apply to the layer.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:start

```
android:start
```
Start inset to apply to the layer. Overrides `left` or `right` depending on layout direction.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:top

```
android:top
```
Top inset to apply to the layer.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

### android:width

```
android:width
```
Width of the layer. Defaults to the layer's intrinsic width.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

## Constants

### INSET_UNDEFINED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSET_UNDEFINED: Int
```

Value used for undefined start and end insets.

 Value: -2147483648

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetStart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerInsetEnd(kotlin.Int)`

### PADDING_MODE_NEST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PADDING_MODE_NEST: Int
```

Padding mode used to nest each layer inside the padding of the previous layer.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`

### PADDING_MODE_STACK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PADDING_MODE_STACK: Int
```

Padding mode used to stack each layer directly atop the previous layer.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`

## Public constructors

### LayerDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LayerDrawable(layers: Array<Drawable!>)
```

Creates a new layer drawable with the list of specified layers.

| Parameters ||
|---|---|
| `layers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Drawable](../android/graphics/drawable/Drawable.md)!\>: a list of drawables to use as layers in this new drawable, must be non-null |

## Public methods

### addLayer

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLayer(dr: Drawable!): Int
```

Adds a new layer containing the specified `drawable` to the end of the layer list and returns its index.

| Parameters ||
|---|---|
| `dr` | [Drawable](../android/graphics/drawable/Drawable.md)!: The drawable to add as a new layer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The index of the new layer. |

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|---|---|
| `t` | [Resources.Theme](../android/content/res/Resources.Theme.md): This value cannot be `null`. |

### canApplyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canApplyTheme(): Boolean
```

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun draw(canvas: Canvas): Unit
```

Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter).

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android/graphics/Canvas.md): The canvas to draw into. This value cannot be `null`. |

### findDrawableByLayerId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findDrawableByLayerId(id: Int): Drawable!
```

Looks for a layer with the given ID and returns its `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable`.

If multiple layers are found for the given ID, returns the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` for the matching layer at the highest index.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The layer ID to search for. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!` | The `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` for the highest-indexed layer that has the given ID, or null if not found. |

### findIndexByLayerId

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findIndexByLayerId(id: Int): Int
```

Returns the layer with the specified `id`.

If multiple layers have the same ID, returns the layer with the lowest index.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ID of the layer to return. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The index of the layer with the specified ID. |

### getAlpha

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlpha(): Int
```

Gets the current alpha value for the drawable. 0 means fully transparent, 255 means fully opaque. This method is implemented by Drawable subclasses and the value returned is specific to how that class treats alpha. The default return value is 255 if the class does not override this method to return a value specific to its use of alpha.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 0 and 255 inclusive |

### getBottomPadding

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBottomPadding(): Int
```

Returns the bottom padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the bottom padding in pixels, or -1 if not explicitly specified |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)`

### getChangingConfigurations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChangingConfigurations(): Int
```

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)` or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int` |

### getConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConstantState(): Drawable.ConstantState?
```

Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState?` | The ConstantState associated to that Drawable. This value may be `null`. |

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(index: Int): Drawable!
```

Returns the drawable for the layer at the specified index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the layer, must be in the range `0...getNumberOfLayers()-1`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable!` | The `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` at the specified layer index. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)`

### getEndPadding

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEndPadding(): Int
```

Returns the end padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the end padding in pixels, or -1 if not explicitly specified |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)`

### getHotspotBounds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHotspotBounds(outRect: Rect): Unit
```

Populates `outRect` with the hotspot bounds.

| Parameters ||
|---|---|
| `outRect` | [Rect](../android/graphics/Rect.md): the rect to populate with the hotspot bounds. This value cannot be `null`. |

### getId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(index: Int): Int
```

Returns the ID of the specified layer.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the layer, must be in the range `0...getNumberOfLayers()-1`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The id of the layer or `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` if the layer has no id. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setId(kotlin.Int,%20kotlin.Int)`

### getIntrinsicHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntrinsicHeight(): Int
```

Returns the drawable's intrinsic height.

Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the intrinsic height, or -1 if no intrinsic height |

### getIntrinsicWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntrinsicWidth(): Int
```

Returns the drawable's intrinsic width.

Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the intrinsic width, or -1 if no intrinsic width |

### getLayerGravity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerGravity(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the gravity used to position or stretch the specified layer within its container |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerGravity(kotlin.Int,%20kotlin.Int)`

### getLayerHeight

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerHeight(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the drawable to adjust |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the explicit height of the layer, or -1 if not specified |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### getLayerInsetBottom

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerInsetBottom(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of pixels to inset from the bottom bound |

### getLayerInsetEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerInsetEnd(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of pixels to inset from the end bound |

### getLayerInsetLeft

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerInsetLeft(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of pixels to inset from the left bound |

### getLayerInsetRight

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerInsetRight(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of pixels to inset from the right bound |

### getLayerInsetStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerInsetStart(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of pixels to inset from the start bound, or `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#INSET_UNDEFINED:kotlin.Int` if not specified |

### getLayerInsetTop

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerInsetTop(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of pixels to inset from the top bound |

### getLayerWidth

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayerWidth(index: Int): Int
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the drawable to adjust |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the explicit width of the layer, or -1 if not specified |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### getLeftPadding

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLeftPadding(): Int
```

Returns the left padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the left padding in pixels, or -1 if not explicitly specified |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)`

### getNumberOfLayers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNumberOfLayers(): Int
```

Returns the number of layers contained within this layer drawable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of layers. |

### getOpacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Populates `outline` with the first available (non-empty) layer outline.

| Parameters ||
|---|---|
| `outline` | [Outline](../android/graphics/Outline.md): Outline in which to place the first available layer outline. This value cannot be `null`. |

### getPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPadding(padding: Rect): Boolean
```

Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset).

| Parameters ||
|---|---|
| `padding` | [Rect](../android/graphics/Rect.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this drawable actually has a padding, else false. When false is returned, the padding is always set to 0. |

### getPaddingMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPaddingMode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current padding mode |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`

### getRightPadding

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRightPadding(): Int
```

Returns the right padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the right padding in pixels, or -1 if not explicitly specified |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)`

### getStartPadding

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStartPadding(): Int
```

Returns the start padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the start padding in pixels, or -1 if not explicitly specified |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)`

### getTopPadding

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTopPadding(): Int
```

Returns the top padding in pixels.

A return value of `-1` means there is no explicit padding set for this dimension. As a result, the value for this dimension returned by `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)` will be computed from the child layers according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the top padding in pixels, or -1 if not explicitly specified |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPadding(android.graphics.Rect)`

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
| `r` | [Resources](../android/content/res/Resources.md): This value cannot be `null`. |
| `parser` | [XmlPullParser](../org/xmlpull/v1/XmlPullParser.md): This value cannot be `null`. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md): This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |
| `org.xmlpull.v1.XmlPullParserException` | |

### invalidateDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateDrawable(who: Drawable): Unit
```

Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears).

| Parameters ||
|---|---|
| `who` | [Drawable](../android/graphics/drawable/Drawable.md): This value cannot be `null`. |

### isAutoMirrored

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAutoMirrored(): Boolean
```

Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean Returns true if this Drawable will be automatically mirrored. |

### isProjected

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isProjected(): Boolean
```

Whether this drawable requests projection. Indicates that the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#` this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver.

### isStateful

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStateful(): Boolean
```

Indicates whether this drawable will change its appearance based on state. Clients can use this to determine whether it is necessary to calculate their state and call setState.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this drawable changes its appearance based on state, false otherwise. |

### jumpToCurrentState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun jumpToCurrentState(): Unit
```

If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations.

### mutate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mutate(): Drawable
```

Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | This drawable. This value cannot be `null`. |

### onLayoutDirectionChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onLayoutDirectionChanged(layoutDirection: Int): Boolean
```

Called when the drawable's resolved layout direction changes.

| Parameters ||
|---|---|
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the layout direction change has caused the appearance of the drawable to change such that it needs to be re-drawn, `false` otherwise |

### scheduleDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scheduleDrawable(
    who: Drawable, 
    what: Runnable, 
    when: Long
): Unit
```

A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call `https://developer.android.com/reference/kotlin/android/os/Handler.html#postAtTime(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long)` with the parameters (what, who, when) to perform the scheduling.

| Parameters ||
|---|---|
| `who` | [Drawable](../android/graphics/drawable/Drawable.md): This value cannot be `null`. |
| `what` | [Runnable](../java/lang/Runnable.md): This value cannot be `null`. |
| `when` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in milliseconds) to run. The timebase is `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` |
| --- | --- |

### setAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAlpha(alpha: Int): Unit
```

Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque.

| Parameters ||
|---|---|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is between 0 and 255 inclusive |

### setAutoMirrored

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutoMirrored(mirrored: Boolean): Unit
```

Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`.

| Parameters ||
|---|---|
| `mirrored` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if the Drawable should be mirrored, false if not. |

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorFilter(colorFilter: ColorFilter?): Unit
```

Specify an optional color filter for the drawable.

If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas.

Pass `null` to remove any existing color filter.

**Note:** Setting a non-`null` color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`.

| Parameters ||
|---|---|
| `colorFilter` | [ColorFilter](../android/graphics/ColorFilter.md)?: The color filter to apply, or `null` to remove the existing color filter |

### setDither

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDither(dither: Boolean): Unit
```

Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component.

### setDrawable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDrawable(
    index: Int, 
    drawable: Drawable!
): Unit
```

Sets the drawable for the layer at the specified index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the layer to modify, must be in the range `0...getNumberOfLayers()-1`. |
| `drawable` | [Drawable](../android/graphics/drawable/Drawable.md)!: The drawable to set for the layer. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getDrawable(kotlin.Int)`

### setDrawableByLayerId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `drawable` | [Drawable](../android/graphics/drawable/Drawable.md)!: The replacement `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` was replaced (could return false if the id was not found). |

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

### setId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setId(
    index: Int, 
    id: Int
): Unit
```

Sets the ID of a layer.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the layer to modify, must be in the range `0...getNumberOfLayers()-1`. |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id to assign to the layer. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getId(kotlin.Int)`

### setLayerGravity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerGravity(
    index: Int, 
    gravity: Int
): Unit
```

Sets the gravity used to position or stretch the specified layer within its container. Gravity is applied after any layer insets (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerInset(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`) or padding (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`).

If gravity is specified as `https://developer.android.com/reference/kotlin/android/view/Gravity.html#NO_GRAVITY:kotlin.Int`, the default behavior depends on whether an explicit width or height has been set (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`), If a dimension is not set, gravity in that direction defaults to `https://developer.android.com/reference/kotlin/android/view/Gravity.html#FILL_HORIZONTAL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/Gravity.html#FILL_VERTICAL:kotlin.Int`; otherwise, gravity in that direction defaults to `https://developer.android.com/reference/kotlin/android/view/Gravity.html#LEFT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/Gravity.html#TOP:kotlin.Int`.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the drawable to adjust |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the gravity to set for the layer |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerGravity(kotlin.Int)`

### setLayerHeight

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerHeight(
    index: Int, 
    h: Int
): Unit
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): height in pixels, or -1 to use the intrinsic height |

### setLayerInset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerInset(
    index: Int, 
    l: Int, 
    t: Int, 
    r: Int, 
    b: Int
): Unit
```

Specifies the insets in pixels for the drawable at the specified index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the drawable to adjust |
| `l` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to add to the left bound |
| `t` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to add to the top bound |
| --- | --- |
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to subtract from the right bound |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to subtract from the bottom bound |

### setLayerInsetBottom

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerInsetBottom(
    index: Int, 
    b: Int
): Unit
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the bottom bound |

### setLayerInsetEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerInsetEnd(
    index: Int, 
    e: Int
): Unit
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `e` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the end bound, or `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#INSET_UNDEFINED:kotlin.Int` if not specified |

### setLayerInsetLeft

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerInsetLeft(
    index: Int, 
    l: Int
): Unit
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `l` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the left bound |

### setLayerInsetRelative

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerInsetRelative(
    index: Int, 
    s: Int, 
    t: Int, 
    e: Int, 
    b: Int
): Unit
```

Specifies the relative insets in pixels for the drawable at the specified index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `s` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the start bound |
| `t` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the top bound |
| --- | --- |
| `e` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the end bound |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the bottom bound |

### setLayerInsetRight

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerInsetRight(
    index: Int, 
    r: Int
): Unit
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the right bound |

### setLayerInsetStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerInsetStart(
    index: Int, 
    s: Int
): Unit
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `s` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the start bound |

### setLayerInsetTop

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerInsetTop(
    index: Int, 
    t: Int
): Unit
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `t` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pixels to inset from the top bound |

### setLayerSize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerSize(
    index: Int, 
    w: Int, 
    h: Int
): Unit
```

Sets an explicit size for the specified layer.

**Note:** Setting an explicit layer size changes the default layer gravity behavior. See `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setLayerGravity(kotlin.Int,%20kotlin.Int)` for more information.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): width in pixels, or -1 to use the intrinsic width |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): height in pixels, or -1 to use the intrinsic height |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerWidth(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getLayerHeight(kotlin.Int)`

### setLayerWidth

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLayerWidth(
    index: Int, 
    w: Int
): Unit
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the layer to adjust |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): width in pixels, or -1 to use the intrinsic width |

### setOpacity

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOpacity(opacity: Int): Unit
```

Sets the opacity of this drawable directly instead of collecting the states from the layers.

| Parameters ||
|---|---|
| `opacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The opacity to use, or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int` for the default behavior |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int`

### setPadding

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPadding(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets the absolute padding.

If padding in a dimension is specified as `-1`, the resolved padding will use the value computed according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`).

Calling this method clears any relative padding values previously set using `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the left padding in pixels, or -1 to use computed padding |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the top padding in pixels, or -1 to use computed padding |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the right padding in pixels, or -1 to use computed padding |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bottom padding in pixels, or -1 to use computed padding |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingRelative(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### setPaddingMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPaddingMode(mode: Int): Unit
```

Specifies how layer padding should affect the bounds of subsequent layers. The default value is `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_NEST:kotlin.Int`.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): padding mode, one of: - `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_NEST:kotlin.Int` to nest each layer inside the padding of the previous layer - `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#PADDING_MODE_STACK:kotlin.Int` to stack each layer directly atop the previous layer |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#getPaddingMode()`

### setPaddingRelative

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPaddingRelative(
    start: Int, 
    top: Int, 
    end: Int, 
    bottom: Int
): Unit
```

Sets the relative padding.

If padding in a dimension is specified as `-1`, the resolved padding will use the value computed according to the padding mode (see `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPaddingMode(kotlin.Int)`).

Calling this method clears any absolute padding values previously set using `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start padding in pixels, or -1 to use computed padding |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the top padding in pixels, or -1 to use computed padding |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end padding in pixels, or -1 to use computed padding |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bottom padding in pixels, or -1 to use computed padding |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintBlendMode(blendMode: BlendMode!): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)`

| Parameters ||
|---|---|
| `blendMode` | [BlendMode](../android/graphics/BlendMode.md)!: This value cannot be `null`. |

### setTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint.

| Parameters ||
|---|---|
| `tint` | [ColorStateList](../android/content/res/ColorStateList.md)?: Color state list to use for tinting this drawable, or `null` to clear the tint |

### setVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### unscheduleDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unscheduleDrawable(
    who: Drawable, 
    what: Runnable
): Unit
```

A Drawable can call this to unschedule an action previously scheduled with `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)`. An implementation can generally simply call `https://developer.android.com/reference/kotlin/android/os/Handler.html#removeCallbacks(java.lang.Runnable,%20kotlin.Any)` with the parameters (what, who) to unschedule the drawable.

| Parameters ||
|---|---|
| `who` | [Drawable](../android/graphics/drawable/Drawable.md): This value cannot be `null`. |
| `what` | [Runnable](../java/lang/Runnable.md): This value cannot be `null`. |

## Protected methods

### onBoundsChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

Override this in your subclass to change appearance if you vary based on the bounds.

| Parameters ||
|---|---|
| `bounds` | [Rect](../android/graphics/Rect.md): This value cannot be `null`. |

### onLevelChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onLevelChange(level: Int): Boolean
```

Override this in your subclass to change appearance if you vary based on level.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the level change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last level. |

### onStateChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onStateChange(state: IntArray): Boolean
```

Override this in your subclass to change appearance if you recognize the specified state.

| Parameters ||
|---|---|
| `state` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |
