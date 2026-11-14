# ColorStateListDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorStateListDrawable

Kotlin| [Java](ColorStateListDrawable.md) 
| --- | --- |

```
open class ColorStateListDrawable : Drawable, Drawable.Callback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](Drawable.md) ||
| | ↳ | [android.graphics.drawable.ColorStateListDrawable](ColorStateListDrawable.md) |

A Drawable that manages a [ColorDrawable](ColorDrawable.md) to make it stateful and backed by a [ColorStateList](../android.content.res/ColorStateList.md).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ColorStateListDrawable](ColorStateListDrawable.md))`()` <br /> |
| [ColorStateListDrawable](ColorStateListDrawable.md))`(`colorStateList:` ` [ColorStateList](../android.content.res/ColorStateList.md)`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](ColorStateListDrawable.md))`(`t:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)`)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](ColorStateListDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAlpha](ColorStateListDrawable.md))`()` Remove the alpha override, reverting to the alpha defined on each color in the [ColorStateList](../android.content.res/ColorStateList.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](ColorStateListDrawable.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](ColorStateListDrawable.md))`()` Gets the current alpha value for the drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](ColorStateListDrawable.md))`()` <br /> |
| --- | --- |
| open [ColorFilter](../android.graphics/ColorFilter.md)? | [getColorFilter](ColorStateListDrawable.md))`()` Returns the current color filter, or`null`if none set. |
| open [ColorStateList](../android.content.res/ColorStateList.md) | [getColorStateList](ColorStateListDrawable.md))`()` Returns the ColorStateList backing this Drawable, or a new ColorStateList of the default ColorDrawable color if one hasn't been defined yet. |
| open [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md) | [getConstantState](ColorStateListDrawable.md))`()` Return a [ConstantState](../android/graphics/drawable/Drawable.ConstantState.md) instance that holds the shared state of this Drawable. |
| --- | --- |
| open [Drawable](Drawable.md) | [getCurrent](ColorStateListDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](ColorStateListDrawable.md))`()` Return the opacity/transparency of this Drawable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](ColorStateListDrawable.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateDrawable](ColorStateListDrawable.md))`(`who:` ` [Drawable](Drawable.md)`)` Called when the drawable needs to be redrawn. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](ColorStateListDrawable.md))`()` <br /> |
| open [Drawable](Drawable.md) | [mutate](ColorStateListDrawable.md))`()` Make this drawable mutable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleDrawable](ColorStateListDrawable.md))`(`who:` ` [Drawable](Drawable.md)`, `what:` ` [Runnable](../java.lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` A Drawable can call this to schedule the next frame of its animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](ColorStateListDrawable.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify an alpha value for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](ColorStateListDrawable.md))`(`colorFilter:` ` [ColorFilter](../android.graphics/ColorFilter.md)?`)` Specify an optional color filter for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorStateList](ColorStateListDrawable.md))`(`colorStateList:` ` [ColorStateList](../android.content.res/ColorStateList.md)`)` Replace this Drawable's ColorStateList. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](ColorStateListDrawable.md))`(`blendMode:` ` [BlendMode](../android.graphics/BlendMode.md)!`)` Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](ColorStateListDrawable.md))`(`tint:` ` [ColorStateList](../android.content.res/ColorStateList.md)?`)` Specifies tint color for this drawable as a color state list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleDrawable](ColorStateListDrawable.md))`(`who:` ` [Drawable](Drawable.md)`, `what:` ` [Runnable](../java.lang/Runnable.md)`)` A Drawable can call this to unschedule an action previously scheduled with [scheduleDrawable](../android/graphics/drawable/Drawable.Callback.md)). |

| Protected methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](ColorStateListDrawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](ColorStateListDrawable.md))`(`state:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](Drawable.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](Drawable.md))`()` <br /> Removes the color filter for this drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [copyBounds](Drawable.md))`()` <br /> Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](Drawable.md)? | [createFromPath](Drawable.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a drawable from file path name. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromStream](Drawable.md))`(`is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`)` <br /> Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` <br /> Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from inside an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns`null`if the tag is not a valid drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [getBounds](Drawable.md))`()` <br /> Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)? | [getCallback](Drawable.md))`()` <br /> Return the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation attached to this Drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [getDirtyBounds](Drawable.md))`()` <br /> Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](Drawable.md))`(`outRect:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Populates`outRect`with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](Drawable.md))`()` <br /> Returns the drawable's intrinsic height. Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](Drawable.md))`()` <br /> Returns the drawable's intrinsic width. Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](Drawable.md))`()` <br /> Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](Drawable.md))`()` <br /> Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](Drawable.md))`()` <br /> Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](Drawable.md))`()` <br /> Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Insets](../android.graphics/Insets.md) | [getOpticalInsets](Drawable.md))`()` <br /> Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](Drawable.md))`(`outline:` ` [Outline](../android.graphics/Outline.md)`)` <br /> Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default [android.view.ViewOutlineProvider](../android.view/ViewOutlineProvider.md) to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](Drawable.md))`(`padding:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](Drawable.md))`()` <br /> Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_selected](../android/R.attr.md), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](../android.graphics/Region.md)? | [getTransparentRegion](Drawable.md))`()` <br /> Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` <br /> Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](Drawable.md))`()` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](Drawable.md))`()` <br /> Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See [android.util.LayoutDirection](../android.util/LayoutDirection.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](Drawable.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](Drawable.md))`()` <br /> Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](../android.graphics/RenderNode.md) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](Drawable.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](Drawable.md))`()` <br /> If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Override this in your subclass to change appearance if you vary based on level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](Drawable.md))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](Drawable.md))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See [android.util.LayoutDirection](../android.util/LayoutDirection.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](Drawable.md))`(`cb:` ` [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)?`)` <br /> Bind a [Callback](../android/graphics/drawable/Drawable.Callback.md) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](Drawable.md))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](Drawable.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` <br /> Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](Drawable.md))which constructs a [PorterDuffColorFilter](../android.graphics/PorterDuffColorFilter.md). **Note:** Setting a color filter disables [tint](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](Drawable.md))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](Drawable.md))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](Drawable.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](Drawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_pressed](../android/R.attr.md)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](Drawable.md))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)). To clear the tint, pass`null`to [setTintList(android.content.res.ColorStateList)](Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](Drawable.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](Drawable.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## Public constructors

### ColorStateListDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorStateListDrawable()
```  

### ColorStateListDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorStateListDrawable(colorStateList: ColorStateList)
```

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `colorStateList` | [ColorStateList](../android.content.res/ColorStateList.md):This value cannot be`null`. |

## Public methods

### applyTheme

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [Resources.Theme](../android/content/res/Resources.Theme.md):This value cannot be`null`. |

### canApplyTheme

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canApplyTheme(): Boolean
```  

### clearAlpha

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearAlpha(): Unit
```

Remove the alpha override, reverting to the alpha defined on each color in the [ColorStateList](../android.content.res/ColorStateList.md). 

### draw

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(canvas: Canvas): Unit
```

Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android.graphics/Canvas.md):This value cannot be`null`. |

### getAlpha

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlpha(): Int
```

Gets the current alpha value for the drawable. 0 means fully transparent, 255 means fully opaque. This method is implemented by Drawable subclasses and the value returned is specific to how that class treats alpha. The default return value is 255 if the class does not override this method to return a value specific to its use of alpha.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 0 and 255 inclusive |

### getChangingConfigurations

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChangingConfigurations(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns a mask of the changing configuration parameters, as defined by [android.content.pm.ActivityInfo](../android.content.pm/ActivityInfo.md). Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android.content.pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android.content.pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android.content.pm/ActivityInfo.md) |

### getColorFilter

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorFilter(): ColorFilter?
```

Returns the current color filter, or`null`if none set.

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------|
| [ColorFilter](../android.graphics/ColorFilter.md)? | This value may be`null`. |

### getColorStateList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorStateList(): ColorStateList
```

Returns the ColorStateList backing this Drawable, or a new ColorStateList of the default ColorDrawable color if one hasn't been defined yet.

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [ColorStateList](../android.content.res/ColorStateList.md) | a ColorStateList This value cannot be`null`. |

### getConstantState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConstantState(): Drawable.ConstantState
```

Return a [ConstantState](../android/graphics/drawable/Drawable.ConstantState.md) instance that holds the shared state of this Drawable.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md) | This value cannot be`null`. |

### getCurrent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrent(): Drawable
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [Drawable](Drawable.md) | This value cannot be`null`. |

### getOpacity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOpacity(): Int
```

Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in [android.graphics.PixelFormat](../android.graphics/PixelFormat.md): [android.graphics.PixelFormat#UNKNOWN](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSLUCENT](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSPARENT](../android.graphics/PixelFormat.md), or [android.graphics.PixelFormat#OPAQUE](../android.graphics/PixelFormat.md).

An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT.

Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method [resolveOpacity](Drawable.md))to perform a standard reduction of two opacities to the appropriate single output.

Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the [setAlpha](Drawable.md))or #setColorFilter methods. Some subclasses, such as [BitmapDrawable](BitmapDrawable.md), [ColorDrawable](ColorDrawable.md), and [GradientDrawable](GradientDrawable.md), do account for the value of [setAlpha](Drawable.md)), but the general behavior is dependent upon the implementation of the subclass.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.PixelFormat#UNKNOWN](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSLUCENT](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSPARENT](../android.graphics/PixelFormat.md), or [android.graphics.PixelFormat#OPAQUE](../android.graphics/PixelFormat.md) |

### hasFocusStateSpecified

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasFocusStateSpecified(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if [android.R.attr#state_focused](../android/R.attr.md) is specified for this drawable. |

### invalidateDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun invalidateDrawable(who: Drawable): Unit
```

Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `who` | [Drawable](Drawable.md):This value cannot be`null`. |

### isStateful

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStateful(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this drawable changes its appearance based on state, false otherwise. |

### mutate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mutate(): Drawable
```

Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [Drawable](Drawable.md) | This value cannot be`null`. |

### scheduleDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scheduleDrawable(
    who: Drawable, 
    what: Runnable, 
    when: Long
): Unit
```

A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call [android.os.Handler#postAtTime(Runnable, Object, long)](../android.os/Handler.md))with the parameters (what, who, when) to perform the scheduling.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `who` | [Drawable](Drawable.md):This value cannot be`null`. |
| `what` | [Runnable](../java.lang/Runnable.md):This value cannot be`null`. |
| `when` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in milliseconds) to run. The timebase is [android.os.SystemClock#uptimeMillis](../android.os/SystemClock.md)) |
| --- | --- |

### setAlpha

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlpha(alpha: Int): Unit
```

Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is between 0 and 255 inclusive |

### setColorFilter

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorFilter(colorFilter: ColorFilter?): Unit
```

Specify an optional color filter for the drawable.

If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas.

Pass`null`to remove any existing color filter.

**Note:** Setting a non-`null`color filter disables [tint](Drawable.md)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| `colorFilter` | [ColorFilter](../android.graphics/ColorFilter.md)?:This value may be`null`. |

### setColorStateList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorStateList(colorStateList: ColorStateList): Unit
```

Replace this Drawable's ColorStateList. It is not copied, so changes will propagate on the next call to[setState(int[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorStateList` | [ColorStateList](../android.content.res/ColorStateList.md):A color state list to attach. This value cannot be`null`. |

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintBlendMode(blendMode: BlendMode!): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](../android.graphics/BlendMode.md).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](../android.graphics/BlendMode.md)!:This value cannot be`null`. |

### setTintList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?:This value may be`null`. |

### unscheduleDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unscheduleDrawable(
    who: Drawable, 
    what: Runnable
): Unit
```

A Drawable can call this to unschedule an action previously scheduled with [scheduleDrawable](../android/graphics/drawable/Drawable.Callback.md)). An implementation can generally simply call [android.os.Handler#removeCallbacks(Runnable, Object)](../android.os/Handler.md))with the parameters (what, who) to unschedule the drawable.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `who` | [Drawable](Drawable.md):This value cannot be`null`. |
| `what` | [Runnable](../java.lang/Runnable.md):This value cannot be`null`. |

## Protected methods

### onBoundsChange

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android.graphics/Rect.md):This value cannot be`null`. |

### onStateChange

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStateChange(state: IntArray): Boolean
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `state` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |
