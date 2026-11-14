# NinePatchDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NinePatchDrawable

Kotlin| [Java](NinePatchDrawable.md) 
| --- | --- |

```
open class NinePatchDrawable : Drawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](Drawable.md) ||
| | ↳ | [android.graphics.drawable.NinePatchDrawable](NinePatchDrawable.md) |

A resizeable bitmap, with stretchable areas that you define. This type of image is defined in a .png file with a special format.
|
| ### Developer Guides
|
| For more information about how to use a NinePatchDrawable, read the [Canvas and Drawables](https://developer.android.com/guide/topics/graphics/2d-graphics.html#nine-patch) developer guide. For information about creating a NinePatch image file using the draw9patch tool, see the [Draw 9-patch](https://developer.android.com/guide/developing/tools/draw9patch.html) tool guide.

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NinePatchDrawable](NinePatchDrawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)!`, `bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`, `chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `padding:` ` [Rect](../android.graphics/Rect.md)!`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create drawable from raw nine-patch data, setting initial target density based on the display metrics of the resources. |
| [NinePatchDrawable](NinePatchDrawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `patch:` ` [NinePatch](../android.graphics/NinePatch.md)`)` Create drawable from existing nine-patch, setting initial target density based on the display metrics of the resources. |
| [NinePatchDrawable](NinePatchDrawable.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`, `chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `padding:` ` [Rect](../android.graphics/Rect.md)!`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create drawable from raw nine-patch data, not dealing with density. |
| [NinePatchDrawable](NinePatchDrawable.md))`(`patch:` ` [NinePatch](../android.graphics/NinePatch.md)`)` Create drawable from existing nine-patch, not dealing with density. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](NinePatchDrawable.md))`(`t:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)`)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](NinePatchDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](NinePatchDrawable.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](NinePatchDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](NinePatchDrawable.md))`()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| open [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | [getConstantState](NinePatchDrawable.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](NinePatchDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](NinePatchDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](NinePatchDrawable.md))`()` <br /> |
| --- | --- |
| open [Insets](../android.graphics/Insets.md) | [getOpticalInsets](NinePatchDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](NinePatchDrawable.md))`(`outline:` ` [Outline](../android.graphics/Outline.md)`)` Called to get the drawable to populate the Outline that defines its drawing area. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](NinePatchDrawable.md))`(`padding:` ` [Rect](../android.graphics/Rect.md)`)` Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. |
| --- | --- |
| open [Paint](../android.graphics/Paint.md) | [getPaint](NinePatchDrawable.md))`()` <br /> |
| open [Region](../android.graphics/Region.md)? | [getTransparentRegion](NinePatchDrawable.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](NinePatchDrawable.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](NinePatchDrawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](NinePatchDrawable.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](NinePatchDrawable.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](NinePatchDrawable.md))`()` <br /> |
| open [Drawable](Drawable.md) | [mutate](NinePatchDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](NinePatchDrawable.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](NinePatchDrawable.md))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](NinePatchDrawable.md))`(`colorFilter:` ` [ColorFilter](../android.graphics/ColorFilter.md)?`)` Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](NinePatchDrawable.md))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](NinePatchDrawable.md))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](NinePatchDrawable.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` Set the density scale at which this drawable will be rendered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](NinePatchDrawable.md))`(`metrics:` ` [DisplayMetrics](../android.util/DisplayMetrics.md)`)` Set the density scale at which this drawable will be rendered. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](NinePatchDrawable.md))`(`density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the density at which this drawable will be rendered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](NinePatchDrawable.md))`(`blendMode:` ` [BlendMode](../android.graphics/BlendMode.md)?`)` Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](NinePatchDrawable.md))`(`tint:` ` [ColorStateList](../android.content.res/ColorStateList.md)?`)` Specifies tint color for this drawable as a color state list. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](NinePatchDrawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](Drawable.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](Drawable.md))`()` <br /> Removes the color filter for this drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [copyBounds](Drawable.md))`()` <br /> Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](Drawable.md)? | [createFromPath](Drawable.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a drawable from file path name. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromStream](Drawable.md))`(`is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`)` <br /> Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` <br /> Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from inside an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns`null`if the tag is not a valid drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [getBounds](Drawable.md))`()` <br /> Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)? | [getCallback](Drawable.md))`()` <br /> Return the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation attached to this Drawable. <br /> | | [ColorFilter](../android.graphics/ColorFilter.md)? | [getColorFilter](Drawable.md))`()` <br /> Returns the current color filter, or`null`if none set. <br /> | | [Drawable](Drawable.md) | [getCurrent](Drawable.md))`()` <br /> | | [Rect](../android.graphics/Rect.md) | [getDirtyBounds](Drawable.md))`()` <br /> Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](Drawable.md))`(`outRect:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Populates`outRect`with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](Drawable.md))`()` <br /> Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](Drawable.md))`()` <br /> Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](Drawable.md))`()` <br /> Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](Drawable.md))`()` <br /> Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](Drawable.md))`()` <br /> Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_selected](../android/R.attr.md), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` <br /> Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](Drawable.md))`()` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](Drawable.md))`()` <br /> Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](../android.graphics/RenderNode.md) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](Drawable.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](Drawable.md))`()` <br /> If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Override this in your subclass to change appearance if you vary based on the bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Override this in your subclass to change appearance if you vary based on level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](Drawable.md))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](Drawable.md))`(`cb:` ` [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)?`)` <br /> Bind a [Callback](../android/graphics/drawable/Drawable.Callback.md) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](Drawable.md))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](Drawable.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` <br /> Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](Drawable.md))which constructs a [PorterDuffColorFilter](../android.graphics/PorterDuffColorFilter.md). **Note:** Setting a color filter disables [tint](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](Drawable.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](Drawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_pressed](../android/R.attr.md)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](Drawable.md))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)). To clear the tint, pass`null`to [setTintList(android.content.res.ColorStateList)](Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](Drawable.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](Drawable.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## Public constructors

### NinePatchDrawable

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NinePatchDrawable(
    res: Resources!, 
    bitmap: Bitmap!, 
    chunk: ByteArray!, 
    padding: Rect!, 
    srcName: String!)
```

Create drawable from raw nine-patch data, setting initial target density based on the display metrics of the resources. 

### NinePatchDrawable

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NinePatchDrawable(
    res: Resources?, 
    patch: NinePatch)
```

Create drawable from existing nine-patch, setting initial target density based on the display metrics of the resources.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `res` | [Resources](../android.content.res/Resources.md)?:This value may be`null`. |
| `patch` | [NinePatch](../android.graphics/NinePatch.md):This value cannot be`null`. |

### NinePatchDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NinePatchDrawable(
    bitmap: Bitmap!, 
    chunk: ByteArray!, 
    padding: Rect!, 
    srcName: String!)
```

**Deprecated:** *Use[NinePatchDrawable(android.content.res.Resources,android.graphics.Bitmap,byte[],android.graphics.Rect,java.lang.String)](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#NinePatchDrawable(android.content.res.Resources,%20android.graphics.Bitmap,%20kotlin.ByteArray,%20android.graphics.Rect,%20kotlin.String))to ensure that the drawable has correctly set its target density.*

Create drawable from raw nine-patch data, not dealing with density. 

### NinePatchDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NinePatchDrawable(patch: NinePatch)
```

**Deprecated:** *Use [NinePatchDrawable(android.content.res.Resources,android.graphics.NinePatch)](NinePatchDrawable.md))to ensure that the drawable has correctly set its target density.*

Create drawable from existing nine-patch, not dealing with density.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `patch` | [NinePatch](../android.graphics/NinePatch.md):This value cannot be`null`. |

## Public methods

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [Resources.Theme](../android/content/res/Resources.Theme.md):This value cannot be`null`. |

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

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android.graphics/Canvas.md):The canvas to draw into This value cannot be`null`. |

### getAlpha

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlpha(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 0 and 255 inclusive |

### getChangingConfigurations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChangingConfigurations(): Int
```

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](Drawable.md))or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android.content.pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android.content.pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android.content.pm/ActivityInfo.md) |

### getConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConstantState(): Drawable.ConstantState?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | The ConstantState associated to that Drawable. This value may be`null`. |

### getIntrinsicHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntrinsicHeight(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the intrinsic height, or -1 if no intrinsic height |

### getIntrinsicWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntrinsicWidth(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the intrinsic width, or -1 if no intrinsic width |

### getOpacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOpacity(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The opacity class of the Drawable. Value is [android.graphics.PixelFormat#UNKNOWN](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSLUCENT](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSPARENT](../android.graphics/PixelFormat.md), or [android.graphics.PixelFormat#OPAQUE](../android.graphics/PixelFormat.md) |

### getOpticalInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOpticalInsets(): Insets
```

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Insets](../android.graphics/Insets.md) | This value cannot be`null`. |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutline(outline: Outline): Unit
```

Called to get the drawable to populate the Outline that defines its drawing area.

This method is called by the default [android.view.ViewOutlineProvider](../android.view/ViewOutlineProvider.md) to define the outline of the View.

The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `outline` | [Outline](../android.graphics/Outline.md):This value cannot be`null`. |

### getPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPadding(padding: Rect): Boolean
```

Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `padding` | [Rect](../android.graphics/Rect.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this drawable actually has a padding, else false. When false is returned, the padding is always set to 0. |

### getPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPaint(): Paint
```

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------|
| [Paint](../android.graphics/Paint.md) | This value cannot be`null`. |

### getTransparentRegion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransparentRegion(): Region?
```

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Region](../android.graphics/Region.md)? | Returns null if the Drawables has no transparent region to report, else a Region holding the parts of the Drawable's bounds that are transparent. |

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasFocusStateSpecified(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if [android.R.attr#state_focused](../android/R.attr.md) is specified for this drawable. |

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

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Resources](../android.content.res/Resources.md):Resources used to resolve attribute values This value cannot be`null`. |
| `parser` | [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md):XML parser from which to inflate this Drawable This value cannot be`null`. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md):Base set of attribute values This value cannot be`null`. |
| --- | --- |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?:Theme to apply, may be null |

| Exceptions ||
|-----------------------------------------|---|
| `org.xmlpull.v1.XmlPullParserException` | |
| `java.io.IOException` | |

### isAutoMirrored

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAutoMirrored(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Returns true if this Drawable will be automatically mirrored. |

### isFilterBitmap

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFilterBitmap(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether this drawable filters its bitmaps |

### isStateful

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStateful(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this drawable changes its appearance based on state, false otherwise. |

### mutate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mutate(): Drawable
```

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------|
| [Drawable](Drawable.md) | This drawable. This value cannot be`null`. |

### setAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlpha(alpha: Int): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is between 0 and 255 inclusive |

### setAutoMirrored

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAutoMirrored(mirrored: Boolean): Unit
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `mirrored` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true if the Drawable should be mirrored, false if not. |

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### setDither

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDither(dither: Boolean): Unit
```  

### setFilterBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilterBitmap(filter: Boolean): Unit
```  

### setTargetDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetDensity(canvas: Canvas): Unit
```

Set the density scale at which this drawable will be rendered. This method assumes the drawable will be rendered at the same density as the specified canvas.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android.graphics/Canvas.md):The Canvas from which the density scale must be obtained. This value cannot be`null`. |

**See Also**

- [android.graphics.Bitmap#setDensity(int)](../android.graphics/Bitmap.md))
- [android.graphics.Bitmap#getDensity()](../android.graphics/Bitmap.md)) 

### setTargetDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetDensity(metrics: DisplayMetrics): Unit
```

Set the density scale at which this drawable will be rendered.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metrics` | [DisplayMetrics](../android.util/DisplayMetrics.md):The DisplayMetrics indicating the density scale for this drawable. This value cannot be`null`. |

**See Also**

- [android.graphics.Bitmap#setDensity(int)](../android.graphics/Bitmap.md))
- [android.graphics.Bitmap#getDensity()](../android.graphics/Bitmap.md)) 

### setTargetDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetDensity(density: Int): Unit
```

Set the density at which this drawable will be rendered.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The density scale for this drawable. |

**See Also**

- [android.graphics.Bitmap#setDensity(int)](../android.graphics/Bitmap.md))
- [android.graphics.Bitmap#getDensity()](../android.graphics/Bitmap.md)) 

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintBlendMode(blendMode: BlendMode?): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](../android.graphics/BlendMode.md).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](../android.graphics/BlendMode.md)?:This value may be`null`. |

### setTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?:This value may be`null`. |

## Protected methods

### onStateChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStateChange(stateSet: IntArray): Boolean
```

| Parameters ||
|---------|-----------------------------|
| `state` | This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |
