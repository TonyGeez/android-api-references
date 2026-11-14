# ColorStateListDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorStateListDrawable

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/ColorStateListDrawable "View this page in Java") 
| --- | --- |

```
open class ColorStateListDrawable : Drawable, Drawable.Callback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) ||
| | ↳ | [android.graphics.drawable.ColorStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#) |

A Drawable that manages a [ColorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable) to make it stateful and backed by a [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ColorStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#ColorStateListDrawable())`()` <br /> |
| [ColorStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#ColorStateListDrawable(android.content.res.ColorStateList))`(`colorStateList:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#applyTheme(android.content.res.Resources.Theme))`(`t:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)`)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#canApplyTheme())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#clearAlpha())`()` Remove the alpha override, reverting to the alpha defined on each color in the [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#draw(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`)` Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#getAlpha())`()` Gets the current alpha value for the drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#getChangingConfigurations())`()` <br /> |
| --- | --- |
| open [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | [getColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#getColorFilter())`()` Returns the current color filter, or`null`if none set. |
| open [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#) | [getColorStateList](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#getColorStateList())`()` Returns the ColorStateList backing this Drawable, or a new ColorStateList of the default ColorDrawable color if one hasn't been defined yet. |
| open [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState) | [getConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#getConstantState())`()` Return a [ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState) instance that holds the shared state of this Drawable. |
| --- | --- |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [getCurrent](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#getCurrent())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#getOpacity())`()` Return the opacity/transparency of this Drawable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#hasFocusStateSpecified())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#invalidateDrawable(android.graphics.drawable.Drawable))`(`who:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)`)` Called when the drawable needs to be redrawn. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#isStateful())`()` <br /> |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [mutate](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#mutate())`()` Make this drawable mutable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long))`(`who:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)`, `what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` A Drawable can call this to schedule the next frame of its animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#setAlpha(kotlin.Int))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify an alpha value for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#setColorFilter(android.graphics.ColorFilter))`(`colorFilter:` ` [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?`)` Specify an optional color filter for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorStateList](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#setColorStateList(android.content.res.ColorStateList))`(`colorStateList:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)`)` Replace this Drawable's ColorStateList. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#setTintBlendMode(android.graphics.BlendMode))`(`blendMode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)!`)` Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#setTintList(android.content.res.ColorStateList))`(`tint:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?`)` Specifies tint color for this drawable as a color state list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#unscheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable))`(`who:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)`, `what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` A Drawable can call this to unschedule an action previously scheduled with [scheduleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)). |

| Protected methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#onBoundsChange(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable#onStateChange(kotlin.IntArray))`(`state:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter())`()` <br /> Removes the color filter for this drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds())`()` <br /> Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromPath](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a drawable from file path name. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`)` <br /> Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Create a drawable from an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` <br /> Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Create a drawable from inside an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns`null`if the tag is not a valid drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds())`()` <br /> Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)? | [getCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback())`()` <br /> Return the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation attached to this Drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getDirtyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds())`()` <br /> Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getHotspotBounds(android.graphics.Rect))`(`outRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Populates`outRect`with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getIntrinsicHeight())`()` <br /> Returns the drawable's intrinsic height. Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getIntrinsicWidth())`()` <br /> Returns the drawable's intrinsic width. Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection())`()` <br /> Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel())`()` <br /> Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumHeight())`()` <br /> Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumWidth())`()` <br /> Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getOpticalInsets](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpticalInsets())`()` <br /> Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` <br /> Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default [android.view.ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#) to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getPadding(android.graphics.Rect))`(`padding:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState())`()` <br /> Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_selected](https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)? | [getTransparentRegion](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getTransparentRegion())`()` <br /> Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` <br /> Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())`()` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isAutoMirrored())`()` <br /> Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See [android.util.LayoutDirection](https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isFilterBitmap())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isProjected())`()` <br /> Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#jumpToCurrentState())`()` <br /> If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onLayoutDirectionChanged(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onLevelChange(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Override this in your subclass to change appearance if you vary based on level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAutoMirrored(kotlin.Boolean))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See [android.util.LayoutDirection](https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback))`(`cb:` ` [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)?`)` <br /> Bind a [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)`)` <br /> Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))which constructs a [PorterDuffColorFilter](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#). **Note:** Setting a color filter disables [tint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setDither(kotlin.Boolean))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setFilterBitmap(kotlin.Boolean))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspot(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())in order to have itself redrawn,*and*true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_pressed](https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())in order to have itself redrawn,*and*true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)). To clear the tint, pass`null`to [setTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode))`(`tintMode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)?`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setVisible(kotlin.Boolean,%20kotlin.Boolean))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

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
| `colorStateList` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#):This value cannot be`null`. |

## Public methods

### applyTheme

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#):This value cannot be`null`. |

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

Remove the alpha override, reverting to the alpha defined on each color in the [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#). 

### draw

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(canvas: Canvas): Unit
```

Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#):This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns a mask of the changing configuration parameters, as defined by [android.content.pm.ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#). Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) |

### getColorFilter

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorFilter(): ColorFilter?
```

Returns the current color filter, or`null`if none set.

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------|
| [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | This value may be`null`. |

### getColorStateList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorStateList(): ColorStateList
```

Returns the ColorStateList backing this Drawable, or a new ColorStateList of the default ColorDrawable color if one hasn't been defined yet.

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#) | a ColorStateList This value cannot be`null`. |

### getConstantState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConstantState(): Drawable.ConstantState
```

Return a [ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState) instance that holds the shared state of this Drawable.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState) | This value cannot be`null`. |

### getCurrent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrent(): Drawable
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | This value cannot be`null`. |

### getOpacity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOpacity(): Int
```

Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in [android.graphics.PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#): [android.graphics.PixelFormat#UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int), [android.graphics.PixelFormat#TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int), [android.graphics.PixelFormat#TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int), or [android.graphics.PixelFormat#OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int).

An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT.

Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method [resolveOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int))to perform a standard reduction of two opacities to the appropriate single output.

Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int))or #setColorFilter methods. Some subclasses, such as [BitmapDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable), [ColorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable), and [GradientDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable), do account for the value of [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)), but the general behavior is dependent upon the implementation of the subclass.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.PixelFormat#UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int), [android.graphics.PixelFormat#TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int), [android.graphics.PixelFormat#TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int), or [android.graphics.PixelFormat#OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int) |

### hasFocusStateSpecified

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasFocusStateSpecified(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int) is specified for this drawable. |

### invalidateDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun invalidateDrawable(who: Drawable): Unit
```

Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `who` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable):This value cannot be`null`. |

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
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | This value cannot be`null`. |

### scheduleDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scheduleDrawable(
    who: Drawable, 
    what: Runnable, 
    when: Long
): Unit
```

A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call [android.os.Handler#postAtTime(Runnable, Object, long)](https://developer.android.com/reference/kotlin/android/os/Handler.html#postAtTime(java.lang.Runnable,%20kotlin.Any,%20kotlin.Long))with the parameters (what, who, when) to perform the scheduling.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `who` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable):This value cannot be`null`. |
| `what` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#):This value cannot be`null`. |
| `when` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in milliseconds) to run. The timebase is [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()) |
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

**Note:** Setting a non-`null`color filter disables [tint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| `colorFilter` | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?:This value may be`null`. |

### setColorStateList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorStateList(colorStateList: ColorStateList): Unit
```

Replace this Drawable's ColorStateList. It is not copied, so changes will propagate on the next call to[setState(int[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorStateList` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#):A color state list to attach. This value cannot be`null`. |

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintBlendMode(blendMode: BlendMode!): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)!:This value cannot be`null`. |

### setTintList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))overrides tint.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?:This value may be`null`. |

### unscheduleDrawable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unscheduleDrawable(
    who: Drawable, 
    what: Runnable
): Unit
```

A Drawable can call this to unschedule an action previously scheduled with [scheduleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)). An implementation can generally simply call [android.os.Handler#removeCallbacks(Runnable, Object)](https://developer.android.com/reference/kotlin/android/os/Handler.html#removeCallbacks(java.lang.Runnable,%20kotlin.Any))with the parameters (what, who) to unschedule the drawable.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `who` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable):This value cannot be`null`. |
| `what` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#):This value cannot be`null`. |

## Protected methods

### onBoundsChange

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):This value cannot be`null`. |

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
