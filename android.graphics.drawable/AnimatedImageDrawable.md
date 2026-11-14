# AnimatedImageDrawable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatedImageDrawable

Kotlin | [Java](https://developer.android.com/reference/android/graphics/drawable/AnimatedImageDrawable "View this page in Java") 
| --- | --- |

```
open class AnimatedImageDrawable : Drawable, Animatable2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) ||
| | ↳ | [android.graphics.drawable.AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#) |

[Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) for drawing animated images (like GIF).

The framework handles decoding subsequent frames in another thread and updating when necessary. The drawable will only animate while it is being displayed.

Created by android.graphics.ImageDecoder#decodeDrawable. A user needs to call [start](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#start()) to start the animation.

It can also be defined in XML using the `<animated-image>` element.

## Summary

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [`android:autoMirrored`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#attr_AnimatedImageDrawable) | Indicates if the drawable needs to be mirrored when its layout direction is RTL (right-to-left). |
| [`android:autoStart`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#attr_AnimatedImageDrawable) | When true, automatically start animating. |
| [`android:repeatCount`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#attr_AnimatedImageDrawable) | Replace the loop count in the encoded data. |
| --- | --- |
| [`android:src`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#attr_AnimatedImageDrawable) | Identifier of the image file. |

| Constants ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPEAT_INFINITE](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#REPEAT_INFINITE:kotlin.Int) Pass this to [setRepeatCount](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setRepeatCount(kotlin.Int)) to repeat infinitely. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#AnimatedImageDrawable())`()` Create an empty AnimatedImageDrawable. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAnimationCallbacks](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#clearAnimationCallbacks())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#draw(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`)` Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#getAlpha())`()` <br /> |
| --- | --- |
| open [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | [getColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#getColorFilter())`()` Returns the current color filter, or `null` if none set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#getIntrinsicHeight())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#getIntrinsicWidth())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#getOpacity())`()` Return the opacity/transparency of this Drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatCount](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#getRepeatCount())`()` Retrieve the number of times the animation will repeat. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#isAutoMirrored())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#isFilterBitmap())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#isRunning())`()` Return whether the animation is currently running. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#onLayoutDirectionChanged(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#registerAnimationCallback(android.graphics.drawable.Animatable2.AnimationCallback))`(`callback:` ` [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback)`)` Adds a callback to listen to the animation events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setAlpha(kotlin.Int))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify an alpha value for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setAutoMirrored(kotlin.Boolean))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setColorFilter(android.graphics.ColorFilter))`(`colorFilter:` ` [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?`)` Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setFilterBitmap(kotlin.Boolean))`(`filterBitmap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatCount](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setRepeatCount(kotlin.Int))`(`repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify the number of times to repeat the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#start())`()` Start the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#stop())`()` Stop the animation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterAnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#unregisterAnimationCallback(android.graphics.drawable.Animatable2.AnimationCallback))`(`callback:` ` [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback)`)` Removes the specified animation callback. |

| Protected methods ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#onBoundsChange(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) |----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#applyTheme(android.content.res.Resources.Theme))`(`t:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)`)` Applies the specified theme to this Drawable and its children. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#canApplyTheme())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter())`()` Removes the color filter for this drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds())`()` Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromPath](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable from file path name. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`)` Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Create a drawable from an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Create a drawable from inside an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds())`()` Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)? | [getCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback())`()` Return the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation attached to this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getChangingConfigurations())`()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)) or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold. <br /> | | [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | [getConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getConstantState())`()` Return a [ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState) instance that holds the shared state of this Drawable. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [getCurrent](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCurrent())`()` <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getDirtyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds())`()` Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getHotspotBounds(android.graphics.Rect))`(`outRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Populates `outRect` with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection())`()` Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel())`()` Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumHeight())`()` Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumWidth())`()` Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getOpticalInsets](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpticalInsets())`()` Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default [android.view.ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#) to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getPadding(android.graphics.Rect))`(`padding:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState())`()` Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_selected](https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)? | [getTransparentRegion](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getTransparentRegion())`()` Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#hasFocusStateSpecified())`()` Indicates whether this drawable has at least one state spec explicitly specifying [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int). Note: A View uses a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) instance as its background and it changes its appearance based on a state. On keyboard devices, it should specify its [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int) to make sure the user knows which view is holding the focus. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())`()` Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isProjected())`()` Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isStateful())`()` Indicates whether this drawable will change its appearance based on state. Clients can use this to determine whether it is necessary to calculate their state and call setState. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#jumpToCurrentState())`()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [mutate](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#mutate())`()` Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onLevelChange(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Override this in your subclass to change appearance if you vary based on level. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onStateChange(kotlin.IntArray))`(`state:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Override this in your subclass to change appearance if you recognize the specified state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback))`(`cb:` ` [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)?`)` Bind a [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)`)` Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) which constructs a [PorterDuffColorFilter](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#). **Note:** Setting a color filter disables [tint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setDither(kotlin.Boolean))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspot(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()) in order to have itself redrawn, *and* true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_pressed](https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()) in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)). To clear the tint, pass `null` to [setTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)) overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintBlendMode(android.graphics.BlendMode))`(`blendMode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)?`)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList))`(`tint:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?`)` Specifies tint color for this drawable as a color state list. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)) overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode))`(`tintMode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)?`)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)) overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setVisible(kotlin.Boolean,%20kotlin.Boolean))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## XML attributes

### android:autoMirrored

```
android:autoMirrored
```
Indicates if the drawable needs to be mirrored when its layout direction is RTL (right-to-left).

May be a boolean value, such as "`true`" or "`false`". 

### android:autoStart

```
android:autoStart
```
When true, automatically start animating. The default is false, meaning that the animation will not start until start() is called.

May be a boolean value, such as "`true`" or "`false`". 

### android:repeatCount

```
android:repeatCount
```
Replace the loop count in the encoded data. A repeat count of 0 means that the animation will play once, regardless of the number of times specified in the encoded data. Setting this to infinite (-1) will result in the animation repeating as long as it is displayed (once start() is called).

May be an integer value, such as "`100`".

Must be one of the following constant values.

| Constant | Value | Description |
|----------|----------|-------------|
| infinite | ffffffff | |

### android:src

```
android:src
```
Identifier of the image file. This attribute is mandatory. It must be an image file with multiple frames, e.g. gif or webp

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*".

## Constants

### REPEAT_INFINITE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPEAT_INFINITE: Int
```

Pass this to [setRepeatCount](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setRepeatCount(kotlin.Int)) to repeat infinitely.

[Animatable2.AnimationCallback.onAnimationEnd](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback#onAnimationEnd(android.graphics.drawable.Drawable)) will never be called unless there is an error. 

 Value: -1

## Public constructors

### AnimatedImageDrawable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnimatedImageDrawable()
```

Create an empty AnimatedImageDrawable.

## Public methods

### clearAnimationCallbacks

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearAnimationCallbacks(): Unit
```  

### draw

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(canvas: Canvas): Unit
```

Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): This value cannot be `null`. |

### getAlpha

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlpha(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 0 and 255 inclusive |

### getColorFilter

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorFilter(): ColorFilter?
```

Returns the current color filter, or `null` if none set.

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------|
| [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | This value may be `null`. |

### getIntrinsicHeight

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntrinsicHeight(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the intrinsic height, or -1 if no intrinsic height |

### getIntrinsicWidth

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntrinsicWidth(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the intrinsic width, or -1 if no intrinsic width |

### getOpacity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOpacity(): Int
```

Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in [android.graphics.PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#): [android.graphics.PixelFormat#UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int), [android.graphics.PixelFormat#TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int), [android.graphics.PixelFormat#TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int), or [android.graphics.PixelFormat#OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int).

An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT.

Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method [resolveOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)) to perform a standard reduction of two opacities to the appropriate single output.

Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)) or #setColorFilter methods. Some subclasses, such as [BitmapDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable), [ColorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable), and [GradientDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable), do account for the value of [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)), but the general behavior is dependent upon the implementation of the subclass.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.PixelFormat#UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int), [android.graphics.PixelFormat#TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int), [android.graphics.PixelFormat#TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int), or [android.graphics.PixelFormat#OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int) |

### getRepeatCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRepeatCount(): Int
```

Retrieve the number of times the animation will repeat.

By default, the repeat count in the encoded data is respected. If the value is [REPEAT_INFINITE](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#REPEAT_INFINITE:kotlin.Int), the animation will repeat as long as it is displayed. If the value is `0`, it will play once.

Calling [setRepeatCount](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setRepeatCount(kotlin.Int)) will make future calls to this method return the value passed to [setRepeatCount](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#setRepeatCount(kotlin.Int)). 

### inflate

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    r: Resources, 
    parser: XmlPullParser, 
    attrs: AttributeSet, 
    theme: Resources.Theme?
): Unit
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): Resources used to resolve attribute values This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): XML parser from which to inflate this Drawable This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): Base set of attribute values This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: Theme to apply, may be null |

| Exceptions ||
|-----------------------------------------|---|
| `org.xmlpull.v1.XmlPullParserException` | |
| `java.io.IOException` | |

### isAutoMirrored

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAutoMirrored(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Returns true if this Drawable will be automatically mirrored. |

### isFilterBitmap

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFilterBitmap(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether this drawable filters its bitmaps |

### isRunning

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRunning(): Boolean
```

Return whether the animation is currently running.

When this drawable is created, this will return `false`. A client needs to call [start](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#start()) to start the animation.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the animation is running, false otherwise. |

### onLayoutDirectionChanged

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLayoutDirectionChanged(layoutDirection: Int): Boolean
```

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new resolved layout direction Value is [android.view.View#LAYOUT_DIRECTION_LTR](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int), or [android.view.View#LAYOUT_DIRECTION_RTL](https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the layout direction change has caused the appearance of the drawable to change such that it needs to be re-drawn, `false` otherwise |

### registerAnimationCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerAnimationCallback(callback: Animatable2.AnimationCallback): Unit
```

Adds a callback to listen to the animation events.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback): This value cannot be `null`. |

### setAlpha

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlpha(alpha: Int): Unit
```

Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is between 0 and 255 inclusive |

### setAutoMirrored

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAutoMirrored(mirrored: Boolean): Unit
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `mirrored` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if the Drawable should be mirrored, false if not. |

### setColorFilter

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorFilter(colorFilter: ColorFilter?): Unit
```

Specify an optional color filter for the drawable.

If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas.

Pass `null` to remove any existing color filter.

**Note:** Setting a non-`null` color filter disables [tint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)).

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| `colorFilter` | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?: This value may be `null`. |

### setFilterBitmap

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilterBitmap(filterBitmap: Boolean): Unit
```  

### setRepeatCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRepeatCount(repeatCount: Int): Unit
```

Specify the number of times to repeat the animation.

By default, the repeat count in the encoded data is respected. If set to [REPEAT_INFINITE](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#REPEAT_INFINITE:kotlin.Int), the animation will repeat as long as it is displayed. If the value is `0`, the animation will play once.

This call replaces the current repeat count. If the encoded data specified a repeat count of `2` (meaning that [getRepeatCount()](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#getRepeatCount()) returns `2`, the animation will play three times. Calling `setRepeatCount(1)` will result in playing only twice and [getRepeatCount()](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#getRepeatCount()) returning `1`.

If the animation is already playing, the iterations that have already occurred count towards the new count. If the animation has already repeated the appropriate number of times (or more), it will finish its current iteration and then stop.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `repeatCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.graphics.drawable.AnimatedImageDrawable#REPEAT_INFINITE](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#REPEAT_INFINITE:kotlin.Int) or greater |

### start

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Start the animation.

Does nothing if the animation is already running. If the animation is stopped, this will reset it.

When the drawable is drawn, starting the animation, [Animatable2.AnimationCallback.onAnimationStart](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback#onAnimationStart(android.graphics.drawable.Drawable)) will be called. 

### stop

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Stop the animation.

If the animation is stopped, it will continue to display the frame it was displaying when stopped. 

### unregisterAnimationCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterAnimationCallback(callback: Animatable2.AnimationCallback): Boolean
```

Removes the specified animation callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback): This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false` if callback didn't exist in the call back list, or `true` if callback has been removed successfully. |

## Protected methods

### onBoundsChange

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): This value cannot be `null`. |
