# BitmapDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BitmapDrawable

Kotlin| [Java](BitmapDrawable.md) 
| --- | --- |

```
open class BitmapDrawable : Drawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](Drawable.md) ||
| | ↳ | [android.graphics.drawable.BitmapDrawable](BitmapDrawable.md) |

A Drawable that wraps a bitmap and can be tiled, stretched, or aligned. You can create a BitmapDrawable from a file path, an input stream, through XML inflation, or from a [android.graphics.Bitmap](../android.graphics/Bitmap.md) object.

It can be defined in an XML file with the`<bitmap>`element. For more information, see the guide to [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

Also see the [android.graphics.Bitmap](../android.graphics/Bitmap.md) class, which handles the management and transformation of raw bitmap graphics, and should be used when drawing to a [android.graphics.Canvas](../android.graphics/Canvas.md).

## Summary

| XML attributes ||
|------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`android:antialias`](BitmapDrawable.md) | Enables or disables antialiasing. |
| [`android:dither`](BitmapDrawable.md) | Enables or disables dithering of the bitmap if the bitmap does not have the same pixel configuration as the screen (for instance: a ARGB 8888 bitmap with an RGB 565 screen). |
| [`android:filter`](BitmapDrawable.md) | Enables or disables bitmap filtering. |
| --- | --- |
| [`android:gravity`](BitmapDrawable.md) | Defines the gravity for the bitmap. |
| [`android:mipMap`](BitmapDrawable.md) | Enables or disables the mipmap hint. |
| [`android:src`](BitmapDrawable.md) | Identifier of the bitmap file. |
| --- | --- |
| [`android:tileMode`](BitmapDrawable.md) | Defines the tile mode. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BitmapDrawable](BitmapDrawable.md))`()` Create an empty drawable, not dealing with density. |
| [BitmapDrawable](BitmapDrawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)!`)` Create an empty drawable, setting initial target density based on the display metrics of the resources. |
| [BitmapDrawable](BitmapDrawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)!`, `bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`)` Create drawable from a bitmap, setting initial target density based on the display metrics of the resources. |
| [BitmapDrawable](BitmapDrawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)!`, `is:` ` [InputStream](../java.io/InputStream.md)!`)` Create a drawable by decoding a bitmap from the given input stream. |
| [BitmapDrawable](BitmapDrawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)!`, `filepath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable by opening a given file path and decoding the bitmap. |
| [BitmapDrawable](BitmapDrawable.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`)` Create drawable from a bitmap, not dealing with density. |
| [BitmapDrawable](BitmapDrawable.md))`(`is:` ` [InputStream](../java.io/InputStream.md)!`)` Create a drawable by decoding a bitmap from the given input stream. |
| [BitmapDrawable](BitmapDrawable.md))`(`filepath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable by opening a given file path and decoding the bitmap. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](BitmapDrawable.md))`(`t:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](BitmapDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](BitmapDrawable.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](BitmapDrawable.md))`()` <br /> |
| [Bitmap](../android.graphics/Bitmap.md)! | [getBitmap](BitmapDrawable.md))`()` Returns the bitmap used by this drawable to render. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](BitmapDrawable.md))`()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| --- | --- |
| open [ColorFilter](../android.graphics/ColorFilter.md)? | [getColorFilter](BitmapDrawable.md))`()` <br /> |
| [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | [getConstantState](BitmapDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGravity](BitmapDrawable.md))`()` Get the gravity used to position/stretch the bitmap within its bounds. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](BitmapDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](BitmapDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](BitmapDrawable.md))`()` <br /> |
| --- | --- |
| open [Insets](../android.graphics/Insets.md) | [getOpticalInsets](BitmapDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](BitmapDrawable.md))`(`outline:` ` [Outline](../android.graphics/Outline.md)`)` Called to get the drawable to populate the Outline that defines its drawing area. |
| [Paint](../android.graphics/Paint.md)! | [getPaint](BitmapDrawable.md))`()` Returns the paint used to render this drawable. |
| --- | --- |
| open [Shader.TileMode](../android/graphics/Shader.TileMode.md)! | [getTileModeX](BitmapDrawable.md))`()` Indicates the repeat behavior of this drawable on the X axis. |
| open [Shader.TileMode](../android/graphics/Shader.TileMode.md)! | [getTileModeY](BitmapDrawable.md))`()` Indicates the repeat behavior of this drawable on the Y axis. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAntiAlias](BitmapDrawable.md))`()` Indicates whether anti-aliasing is enabled for this drawable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](BitmapDrawable.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMipMap](BitmapDrawable.md))`()` Indicates whether the mipmap hint is enabled on this drawable's bitmap. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](BitmapDrawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](BitmapDrawable.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](BitmapDrawable.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](BitmapDrawable.md))`()` <br /> |
| --- | --- |
| open [Drawable](Drawable.md) | [mutate](BitmapDrawable.md))`()` A mutable BitmapDrawable still shares its Bitmap with any other Drawable that comes from the same resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](BitmapDrawable.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAntiAlias](BitmapDrawable.md))`(`aa:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables anti-aliasing for this drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](BitmapDrawable.md))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBitmap](BitmapDrawable.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)?`)` Switch to a new Bitmap object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](BitmapDrawable.md))`(`colorFilter:` ` [ColorFilter](../android.graphics/ColorFilter.md)?`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](BitmapDrawable.md))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](BitmapDrawable.md))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGravity](BitmapDrawable.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the gravity used to position/stretch the bitmap within its bounds. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMipMap](BitmapDrawable.md))`(`mipMap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables the mipmap hint for this drawable's bitmap. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](BitmapDrawable.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)!`)` Set the density scale at which this drawable will be rendered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](BitmapDrawable.md))`(`metrics:` ` [DisplayMetrics](../android.util/DisplayMetrics.md)!`)` Set the density scale at which this drawable will be rendered. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetDensity](BitmapDrawable.md))`(`density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the density at which this drawable will be rendered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTileModeX](BitmapDrawable.md))`(`mode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)!`)` Sets the repeat behavior of this drawable on the X axis. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTileModeXY](BitmapDrawable.md))`(`xmode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)!`, `ymode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)!`)` Sets the repeat behavior of this drawable on both axis. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTileModeY](BitmapDrawable.md))`(`mode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)!`)` Sets the repeat behavior of this drawable on the Y axis. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](BitmapDrawable.md))`(`blendMode:` ` [BlendMode](../android.graphics/BlendMode.md)!`)` Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](BitmapDrawable.md))`(`tint:` ` [ColorStateList](../android.content.res/ColorStateList.md)?`)` <br /> |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](BitmapDrawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](BitmapDrawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](Drawable.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](Drawable.md))`()` <br /> Removes the color filter for this drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [copyBounds](Drawable.md))`()` <br /> Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](Drawable.md)? | [createFromPath](Drawable.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a drawable from file path name. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromStream](Drawable.md))`(`is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`)` <br /> Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` <br /> Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from inside an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns`null`if the tag is not a valid drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [getBounds](Drawable.md))`()` <br /> Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)? | [getCallback](Drawable.md))`()` <br /> Return the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation attached to this Drawable. <br /> | | [Drawable](Drawable.md) | [getCurrent](Drawable.md))`()` <br /> | | [Rect](../android.graphics/Rect.md) | [getDirtyBounds](Drawable.md))`()` <br /> Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](Drawable.md))`(`outRect:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Populates`outRect`with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](Drawable.md))`()` <br /> Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](Drawable.md))`()` <br /> Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](Drawable.md))`()` <br /> Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](Drawable.md))`()` <br /> Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](Drawable.md))`(`padding:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](Drawable.md))`()` <br /> Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_selected](../android/R.attr.md), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](../android.graphics/Region.md)? | [getTransparentRegion](Drawable.md))`()` <br /> Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` <br /> Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](Drawable.md))`()` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](Drawable.md))`()` <br /> Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](../android.graphics/RenderNode.md) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](Drawable.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](Drawable.md))`()` <br /> If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Override this in your subclass to change appearance if you vary based on level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](Drawable.md))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](Drawable.md))`(`cb:` ` [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)?`)` <br /> Bind a [Callback](../android/graphics/drawable/Drawable.Callback.md) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](Drawable.md))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](Drawable.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` <br /> Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](Drawable.md))which constructs a [PorterDuffColorFilter](../android.graphics/PorterDuffColorFilter.md). **Note:** Setting a color filter disables [tint](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](Drawable.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](Drawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_pressed](../android/R.attr.md)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](Drawable.md))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)). To clear the tint, pass`null`to [setTintList(android.content.res.ColorStateList)](Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](Drawable.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](Drawable.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## XML attributes

### android:antialias

```
android:antialias
```
Enables or disables antialiasing. Antialiasing can be used to smooth the edges of a bitmap when rotated. Default value is false.

May be a boolean value, such as "`true`" or "`false`". 

### android:dither

```
android:dither
```
Enables or disables dithering of the bitmap if the bitmap does not have the same pixel configuration as the screen (for instance: a ARGB 8888 bitmap with an RGB 565 screen). Default value is true.

May be a boolean value, such as "`true`" or "`false`". 

### android:filter

```
android:filter
```
Enables or disables bitmap filtering. Filtering is used when the bitmap is shrunk or stretched to smooth its appearance. Default value is true.

May be a boolean value, such as "`true`" or "`false`". 

### android:gravity

```
android:gravity
```
Defines the gravity for the bitmap. The gravity indicates where to position the drawable in its container if the bitmap is smaller than the container.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
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

### android:mipMap

```
android:mipMap
```
Enables or disables the mipmap hint. See [android.graphics.Bitmap#setHasMipMap(boolean)](../android.graphics/Bitmap.md))for more information. Default value is false.

May be a boolean value, such as "`true`" or "`false`". 

### android:src

```
android:src
```
Identifier of the bitmap file. This attribute is mandatory.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:tileMode

```
android:tileMode
```
Defines the tile mode. When the tile mode is enabled, the bitmap is repeated. Gravity is ignored when the tile mode is enabled. Default value is "disabled".

Must be one of the following constant values.

| Constant | Value | Description |
|----------|----------|------------------------------------------------------------------------------------------------------------------------|
| clamp | 0 | Replicates the edge color. |
| disabled | ffffffff | Do not tile the bitmap. This is the default value. |
| mirror | 2 | Repeats the shader's image horizontally and vertically, alternating mirror images so that adjacent images always seam. |
| --- | --- | --- |
| repeat | 1 | Repeats the bitmap in both direction. |

## Public constructors

### BitmapDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitmapDrawable()
```

**Deprecated:** *Use [BitmapDrawable(android.content.res.Resources,android.graphics.Bitmap)](BitmapDrawable.md))instead to specify a bitmap to draw with and ensure the correct density is set.*

Create an empty drawable, not dealing with density. 

### BitmapDrawable

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitmapDrawable(res: Resources!)
```

**Deprecated:** *Use [BitmapDrawable(android.content.res.Resources,android.graphics.Bitmap)](BitmapDrawable.md))instead to specify a bitmap to draw with.*

Create an empty drawable, setting initial target density based on the display metrics of the resources. 

### BitmapDrawable

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitmapDrawable(
    res: Resources!, 
    bitmap: Bitmap!)
```

Create drawable from a bitmap, setting initial target density based on the display metrics of the resources. 

### BitmapDrawable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitmapDrawable(
    res: Resources!, 
    is: InputStream!)
```

Create a drawable by decoding a bitmap from the given input stream. 

### BitmapDrawable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitmapDrawable(
    res: Resources!, 
    filepath: String!)
```

Create a drawable by opening a given file path and decoding the bitmap. 

### BitmapDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitmapDrawable(bitmap: Bitmap!)
```

**Deprecated:** *Use [BitmapDrawable(android.content.res.Resources,android.graphics.Bitmap)](BitmapDrawable.md))to ensure that the drawable has correctly set its target density.*

Create drawable from a bitmap, not dealing with density. 

### BitmapDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitmapDrawable(is: InputStream!)
```

**Deprecated:** *Use [BitmapDrawable(android.content.res.Resources,java.io.InputStream)](BitmapDrawable.md))to ensure that the drawable has correctly set its target density.*

Create a drawable by decoding a bitmap from the given input stream. 

### BitmapDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitmapDrawable(filepath: String!)
```

**Deprecated:** *Use [BitmapDrawable(android.content.res.Resources,java.lang.String)](BitmapDrawable.md))to ensure that the drawable has correctly set its target density.*

Create a drawable by opening a given file path and decoding the bitmap.

## Public methods

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyTheme(t: Resources.Theme): Unit
```

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [Resources.Theme](../android/content/res/Resources.Theme.md):the theme to apply This value cannot be`null`. |

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

### getBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBitmap(): Bitmap!
```

Returns the bitmap used by this drawable to render. May be null. 

### getChangingConfigurations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChangingConfigurations(): Int
```

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](Drawable.md))or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android.content.pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android.content.pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android.content.pm/ActivityInfo.md) |

### getColorFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorFilter(): ColorFilter?
```

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [ColorFilter](../android.graphics/ColorFilter.md)? | the current color filter, or`null`if none set |

### getConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConstantState(): Drawable.ConstantState?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | The ConstantState associated to that Drawable. This value may be`null`. |

### getGravity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGravity(): Int
```

Get the gravity used to position/stretch the bitmap within its bounds. See android.view.Gravity

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the gravity applied to the bitmap |

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

### getPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPaint(): Paint!
```

Returns the paint used to render this drawable. 

### getTileModeX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTileModeX(): Shader.TileMode!
```

Indicates the repeat behavior of this drawable on the X axis.

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Shader.TileMode](../android/graphics/Shader.TileMode.md)! | [android.graphics.Shader.TileMode#CLAMP](../android/graphics/Shader.TileMode.md) if the bitmap does not repeat, [android.graphics.Shader.TileMode#REPEAT](../android/graphics/Shader.TileMode.md) or [android.graphics.Shader.TileMode#MIRROR](../android/graphics/Shader.TileMode.md) otherwise. |

### getTileModeY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTileModeY(): Shader.TileMode!
```

Indicates the repeat behavior of this drawable on the Y axis.

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Shader.TileMode](../android/graphics/Shader.TileMode.md)! | [android.graphics.Shader.TileMode#CLAMP](../android/graphics/Shader.TileMode.md) if the bitmap does not repeat, [android.graphics.Shader.TileMode#REPEAT](../android/graphics/Shader.TileMode.md) or [android.graphics.Shader.TileMode#MIRROR](../android/graphics/Shader.TileMode.md) otherwise. |

### hasAntiAlias

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasAntiAlias(): Boolean
```

Indicates whether anti-aliasing is enabled for this drawable.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if anti-aliasing is enabled, false otherwise. |

**See Also**

- [#setAntiAlias(boolean)](BitmapDrawable.md)) 

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasFocusStateSpecified(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if [android.R.attr#state_focused](../android/R.attr.md) is specified for this drawable. |

### hasMipMap

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMipMap(): Boolean
```

Indicates whether the mipmap hint is enabled on this drawable's bitmap.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the mipmap hint is set, false otherwise. If the bitmap is null, this method always returns false. |

**See Also**

- [#setMipMap(boolean)](BitmapDrawable.md)) 

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
fun isAutoMirrored(): Boolean
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

A mutable BitmapDrawable still shares its Bitmap with any other Drawable that comes from the same resource.

| Return ||
|-----------------------------------------------------------------------------------------------|----------------|
| [Drawable](Drawable.md) | This drawable. |

### setAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlpha(alpha: Int): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is between 0 and 255 inclusive |

### setAntiAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAntiAlias(aa: Boolean): Unit
```

Enables or disables anti-aliasing for this drawable. Anti-aliasing affects the edges of the bitmap only so it applies only when the drawable is rotated.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `aa` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the bitmap should be anti-aliased, false otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable#hasAntiAlias()> 

### setAutoMirrored

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAutoMirrored(mirrored: Boolean): Unit
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `mirrored` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true if the Drawable should be mirrored, false if not. |

### setBitmap

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBitmap(bitmap: Bitmap?): Unit
```

Switch to a new Bitmap object.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)?:This value may be`null`. |

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorFilter(colorFilter: ColorFilter?): Unit
```

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorFilter` | [ColorFilter](../android.graphics/ColorFilter.md)?:The color filter to apply, or`null`to remove the existing color filter |

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

### setGravity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGravity(gravity: Int): Unit
```

Set the gravity used to position/stretch the bitmap within its bounds. See android.view.Gravity

| Parameters ||
|-----------|----------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the gravity |

### setMipMap

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMipMap(mipMap: Boolean): Unit
```

Enables or disables the mipmap hint for this drawable's bitmap. See [Bitmap.setHasMipMap(boolean)](../android.graphics/Bitmap.md))for more information. If the bitmap is null calling this method has no effect.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `mipMap` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the bitmap should use mipmaps, false otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable#hasMipMap()> 

### setTargetDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetDensity(canvas: Canvas!): Unit
```

Set the density scale at which this drawable will be rendered. This method assumes the drawable will be rendered at the same density as the specified canvas.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android.graphics/Canvas.md)!:The Canvas from which the density scale must be obtained. |

**See Also**

- [android.graphics.Bitmap#setDensity(int)](../android.graphics/Bitmap.md))
- [android.graphics.Bitmap#getDensity()](../android.graphics/Bitmap.md)) 

### setTargetDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetDensity(metrics: DisplayMetrics!): Unit
```

Set the density scale at which this drawable will be rendered.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metrics` | [DisplayMetrics](../android.util/DisplayMetrics.md)!:The DisplayMetrics indicating the density scale for this drawable. |

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

### setTileModeX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTileModeX(mode: Shader.TileMode!): Unit
```

Sets the repeat behavior of this drawable on the X axis. By default, the drawable does not repeat its bitmap. Using [android.graphics.Shader.TileMode#REPEAT](../android/graphics/Shader.TileMode.md) or [android.graphics.Shader.TileMode#MIRROR](../android/graphics/Shader.TileMode.md) the bitmap can be repeated (or tiled) if the bitmap is smaller than this drawable.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md)!:The repeat mode for this drawable. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable#setTileModeY(android.graphics.Shader.TileMode)>
- [#setTileModeXY(android.graphics.Shader.TileMode, android.graphics.Shader.TileMode)](BitmapDrawable.md)) 

### setTileModeXY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTileModeXY(
    xmode: Shader.TileMode!, 
    ymode: Shader.TileMode!
): Unit
```

Sets the repeat behavior of this drawable on both axis. By default, the drawable does not repeat its bitmap. Using [android.graphics.Shader.TileMode#REPEAT](../android/graphics/Shader.TileMode.md) or [android.graphics.Shader.TileMode#MIRROR](../android/graphics/Shader.TileMode.md) the bitmap can be repeated (or tiled) if the bitmap is smaller than this drawable.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `xmode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md)!:The X repeat mode for this drawable. |
| `ymode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md)!:The Y repeat mode for this drawable. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable#setTileModeX(android.graphics.Shader.TileMode)>
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable#setTileModeY(android.graphics.Shader.TileMode)> 

### setTileModeY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTileModeY(mode: Shader.TileMode!): Unit
```

Sets the repeat behavior of this drawable on the Y axis. By default, the drawable does not repeat its bitmap. Using [android.graphics.Shader.TileMode#REPEAT](../android/graphics/Shader.TileMode.md) or [android.graphics.Shader.TileMode#MIRROR](../android/graphics/Shader.TileMode.md) the bitmap can be repeated (or tiled) if the bitmap is smaller than this drawable.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md)!:The repeat mode for this drawable. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable#setTileModeX(android.graphics.Shader.TileMode)>
- [#setTileModeXY(android.graphics.Shader.TileMode, android.graphics.Shader.TileMode)](BitmapDrawable.md)) 

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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintList(tint: ColorStateList?): Unit
```

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?:Color state list to use for tinting this drawable, or`null`to clear the tint |

## Protected methods

### onBoundsChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android.graphics/Rect.md):This value cannot be`null`. |

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
