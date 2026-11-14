# NinePatchDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NinePatchDrawable

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/NinePatchDrawable "View this page in Java") 
| --- | --- |

```
open class NinePatchDrawable : Drawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) ||
| | ↳ | [android.graphics.drawable.NinePatchDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#) |

A resizeable bitmap, with stretchable areas that you define. This type of image is defined in a .png file with a special format.
|
| ### Developer Guides
|
| For more information about how to use a NinePatchDrawable, read the [Canvas and Drawables](https://developer.android.com/guide/topics/graphics/2d-graphics.html#nine-patch) developer guide. For information about creating a NinePatch image file using the draw9patch tool, see the [Draw 9-patch](https://developer.android.com/guide/developing/tools/draw9patch.html) tool guide.

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NinePatchDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#NinePatchDrawable(android.content.res.Resources,%20android.graphics.Bitmap,%20kotlin.ByteArray,%20android.graphics.Rect,%20kotlin.String))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)!`, `bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`, `chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `padding:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create drawable from raw nine-patch data, setting initial target density based on the display metrics of the resources. |
| [NinePatchDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#NinePatchDrawable(android.content.res.Resources,%20android.graphics.NinePatch))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `patch:` ` [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch.html#)`)` Create drawable from existing nine-patch, setting initial target density based on the display metrics of the resources. |
| [NinePatchDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#NinePatchDrawable(android.graphics.Bitmap,%20kotlin.ByteArray,%20android.graphics.Rect,%20kotlin.String))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`, `chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `padding:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create drawable from raw nine-patch data, not dealing with density. |
| [NinePatchDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#NinePatchDrawable(android.graphics.NinePatch))`(`patch:` ` [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch.html#)`)` Create drawable from existing nine-patch, not dealing with density. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#applyTheme(android.content.res.Resources.Theme))`(`t:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)`)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#canApplyTheme())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#draw(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getAlpha())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getChangingConfigurations())`()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| open [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | [getConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getConstantState())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getIntrinsicHeight())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getIntrinsicWidth())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getOpacity())`()` <br /> |
| --- | --- |
| open [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getOpticalInsets](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getOpticalInsets())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` Called to get the drawable to populate the Outline that defines its drawing area. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getPadding(android.graphics.Rect))`(`padding:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. |
| --- | --- |
| open [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#) | [getPaint](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getPaint())`()` <br /> |
| open [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)? | [getTransparentRegion](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#getTransparentRegion())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#hasFocusStateSpecified())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#isAutoMirrored())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#isFilterBitmap())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#isStateful())`()` <br /> |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [mutate](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#mutate())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setAlpha(kotlin.Int))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setAutoMirrored(kotlin.Boolean))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setColorFilter(android.graphics.ColorFilter))`(`colorFilter:` ` [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?`)` Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setDither(kotlin.Boolean))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setFilterBitmap(kotlin.Boolean))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setTargetDensity(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`)` Set the density scale at which this drawable will be rendered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setTargetDensity(android.util.DisplayMetrics))`(`metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)`)` Set the density scale at which this drawable will be rendered. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setTargetDensity(kotlin.Int))`(`density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the density at which this drawable will be rendered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setTintBlendMode(android.graphics.BlendMode))`(`blendMode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)?`)` Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#setTintList(android.content.res.ColorStateList))`(`tint:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?`)` Specifies tint color for this drawable as a color state list. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#onStateChange(kotlin.IntArray))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter())`()` <br /> Removes the color filter for this drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds())`()` <br /> Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromPath](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a drawable from file path name. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`)` <br /> Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Create a drawable from an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` <br /> Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Create a drawable from inside an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns`null`if the tag is not a valid drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds())`()` <br /> Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)? | [getCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback())`()` <br /> Return the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation attached to this Drawable. <br /> | | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | [getColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getColorFilter())`()` <br /> Returns the current color filter, or`null`if none set. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [getCurrent](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCurrent())`()` <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getDirtyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds())`()` <br /> Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getHotspotBounds(android.graphics.Rect))`(`outRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Populates`outRect`with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection())`()` <br /> Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel())`()` <br /> Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumHeight())`()` <br /> Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumWidth())`()` <br /> Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState())`()` <br /> Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_selected](https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` <br /> Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())`()` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isProjected())`()` <br /> Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#jumpToCurrentState())`()` <br /> If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onBoundsChange(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Override this in your subclass to change appearance if you vary based on the bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onLayoutDirectionChanged(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onLevelChange(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Override this in your subclass to change appearance if you vary based on level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback))`(`cb:` ` [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)?`)` <br /> Bind a [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)`)` <br /> Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))which constructs a [PorterDuffColorFilter](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#). **Note:** Setting a color filter disables [tint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspot(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())in order to have itself redrawn,*and*true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_pressed](https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())in order to have itself redrawn,*and*true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)). To clear the tint, pass`null`to [setTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode))`(`tintMode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)?`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setVisible(kotlin.Boolean,%20kotlin.Boolean))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` <br /> Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

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
| `res` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?:This value may be`null`. |
| `patch` | [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch.html#):This value cannot be`null`. |

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

**Deprecated:** *Use [NinePatchDrawable(android.content.res.Resources,android.graphics.NinePatch)](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable#NinePatchDrawable(android.content.res.Resources,%20android.graphics.NinePatch))to ensure that the drawable has correctly set its target density.*

Create drawable from existing nine-patch, not dealing with density.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `patch` | [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch.html#):This value cannot be`null`. |

## Public methods

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#):This value cannot be`null`. |

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
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#):The canvas to draw into This value cannot be`null`. |

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

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int))or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) |

### getConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConstantState(): Drawable.ConstantState?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | The ConstantState associated to that Drawable. This value may be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The opacity class of the Drawable. Value is [android.graphics.PixelFormat#UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int), [android.graphics.PixelFormat#TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int), [android.graphics.PixelFormat#TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int), or [android.graphics.PixelFormat#OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int) |

### getOpticalInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOpticalInsets(): Insets
```

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | This value cannot be`null`. |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutline(outline: Outline): Unit
```

Called to get the drawable to populate the Outline that defines its drawing area.

This method is called by the default [android.view.ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#) to define the outline of the View.

The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#):This value cannot be`null`. |

### getPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPadding(padding: Rect): Boolean
```

Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `padding` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):This value cannot be`null`. |

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
| [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#) | This value cannot be`null`. |

### getTransparentRegion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransparentRegion(): Region?
```

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)? | Returns null if the Drawables has no transparent region to report, else a Region holding the parts of the Drawable's bounds that are transparent. |

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasFocusStateSpecified(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int) is specified for this drawable. |

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
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#):Resources used to resolve attribute values This value cannot be`null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#):XML parser from which to inflate this Drawable This value cannot be`null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#):Base set of attribute values This value cannot be`null`. |
| --- | --- |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?:Theme to apply, may be null |

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
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | This drawable. This value cannot be`null`. |

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

**Note:** Setting a non-`null`color filter disables [tint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| `colorFilter` | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?:This value may be`null`. |

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
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#):The Canvas from which the density scale must be obtained. This value cannot be`null`. |

**See Also**

- [android.graphics.Bitmap#setDensity(int)](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#setDensity(kotlin.Int))
- [android.graphics.Bitmap#getDensity()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#getDensity()) 

### setTargetDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetDensity(metrics: DisplayMetrics): Unit
```

Set the density scale at which this drawable will be rendered.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#):The DisplayMetrics indicating the density scale for this drawable. This value cannot be`null`. |

**See Also**

- [android.graphics.Bitmap#setDensity(int)](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#setDensity(kotlin.Int))
- [android.graphics.Bitmap#getDensity()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#getDensity()) 

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

- [android.graphics.Bitmap#setDensity(int)](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#setDensity(kotlin.Int))
- [android.graphics.Bitmap#getDensity()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#getDensity()) 

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintBlendMode(blendMode: BlendMode?): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)?:This value may be`null`. |

### setTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))overrides tint.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?:This value may be`null`. |

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
