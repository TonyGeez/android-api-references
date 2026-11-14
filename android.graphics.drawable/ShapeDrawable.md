# ShapeDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ShapeDrawable

Kotlin | [Java](ShapeDrawable.md) 
| --- | --- |

```
open class ShapeDrawable : Drawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](Drawable.md) ||
| | ↳ | [android.graphics.drawable.ShapeDrawable](ShapeDrawable.md) |

| Known Direct Subclasses [PaintDrawable](PaintDrawable.md) |---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [PaintDrawable](PaintDrawable.md) | Drawable that draws its bounds in the given paint, with optional rounded corners. | |
| --- | --- | --- | --- | --- | --- | --- |

A Drawable object that draws primitive shapes. A ShapeDrawable takes a [android.graphics.drawable.shapes.Shape](../android.graphics.drawable.shapes/Shape.md) object and manages its presence on the screen. If no Shape is given, then the ShapeDrawable will default to a [android.graphics.drawable.shapes.RectShape](../android.graphics.drawable.shapes/RectShape.md).

This object can be defined in an XML file with the `<shape>` element.
|
| ### Developer Guides
|
| For more information about how to use ShapeDrawable, read the [Canvas and Drawables](https://developer.android.com/guide/topics/graphics/2d-graphics.html#shape-drawable) document. For more information about defining a ShapeDrawable in XML, read the [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html#Shape) document.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ShaderFactory](../android/graphics/drawable/ShapeDrawable.ShaderFactory.md) Base class defines a factory object that is called each time the drawable is resized (has a new width or height). |

| XML attributes ||
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [`android:bottom`](ShapeDrawable.md) | Bottom padding. |
| [`android:color`](ShapeDrawable.md) | Defines the color of the shape. |
| [`android:height`](ShapeDrawable.md) | Defines the height of the shape. |
| --- | --- |
| [`android:left`](ShapeDrawable.md) | Left padding. |
| [`android:right`](ShapeDrawable.md) | Right padding. |
| [`android:top`](ShapeDrawable.md) | Top padding. |
| --- | --- |
| [`android:width`](ShapeDrawable.md) | Defines the width of the shape. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ShapeDrawable](ShapeDrawable.md))`()` ShapeDrawable constructor. |
| [ShapeDrawable](ShapeDrawable.md))`(`s:` ` [Shape](../android.graphics.drawable.shapes/Shape.md)!`)` Creates a ShapeDrawable with a specified Shape. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](ShapeDrawable.md))`(`t:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](ShapeDrawable.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](ShapeDrawable.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](ShapeDrawable.md))`()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| open [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | [getConstantState](ShapeDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](ShapeDrawable.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](ShapeDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](ShapeDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](ShapeDrawable.md))`(`outline:` ` [Outline](../android.graphics/Outline.md)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](ShapeDrawable.md))`(`padding:` ` [Rect](../android.graphics/Rect.md)`)` <br /> |
| open [Paint](../android.graphics/Paint.md)! | [getPaint](ShapeDrawable.md))`()` Returns the Paint used to draw the shape. |
| open [ShapeDrawable.ShaderFactory](../android/graphics/drawable/ShapeDrawable.ShaderFactory.md)! | [getShaderFactory](ShapeDrawable.md))`()` Returns the ShaderFactory used by this ShapeDrawable for requesting a [android.graphics.Shader](../android.graphics/Shader.md). |
| --- | --- |
| open [Shape](../android.graphics.drawable.shapes/Shape.md)! | [getShape](ShapeDrawable.md))`()` Returns the Shape of this ShapeDrawable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](ShapeDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](ShapeDrawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](ShapeDrawable.md))`()` <br /> |
| open [Drawable](Drawable.md) | [mutate](ShapeDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](ShapeDrawable.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the alpha level for this drawable \[0. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](ShapeDrawable.md))`(`colorFilter:` ` [ColorFilter](../android.graphics/ColorFilter.md)?`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](ShapeDrawable.md))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntrinsicHeight](ShapeDrawable.md))`(`height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the intrinsic (default) height for this shape. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntrinsicWidth](ShapeDrawable.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the intrinsic (default) width for this shape. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPadding](ShapeDrawable.md))`(`padding:` ` [Rect](../android.graphics/Rect.md)!`)` Sets padding for this shape, defined by a Rect object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPadding](ShapeDrawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets padding for the shape. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShaderFactory](ShapeDrawable.md))`(`fact:` ` [ShapeDrawable.ShaderFactory](../android/graphics/drawable/ShapeDrawable.ShaderFactory.md)!`)` Sets a ShaderFactory to which requests for a [android.graphics.Shader](../android.graphics/Shader.md) object will be made. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShape](ShapeDrawable.md))`(`s:` ` [Shape](../android.graphics.drawable.shapes/Shape.md)!`)` Sets the Shape of this ShapeDrawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](ShapeDrawable.md))`(`blendMode:` ` [BlendMode](../android.graphics/BlendMode.md)!`)` Specifies a tint blending mode for this drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](ShapeDrawable.md))`(`tint:` ` [ColorStateList](../android.content.res/ColorStateList.md)?`)` <br /> |

| Protected methods ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inflateTag](ShapeDrawable.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `r:` ` [Resources](../android.content.res/Resources.md)!`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` Subclasses override this to parse custom subelements. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](ShapeDrawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDraw](ShapeDrawable.md))`(`shape:` ` [Shape](../android.graphics.drawable.shapes/Shape.md)!`, `canvas:` ` [Canvas](../android.graphics/Canvas.md)!`, `paint:` ` [Paint](../android.graphics/Paint.md)!`)` Called from the drawable's draw() method after the canvas has been set to draw the shape at (0,0). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](ShapeDrawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](Drawable.md) |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](Drawable.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](Drawable.md))`()` Removes the color filter for this drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [copyBounds](Drawable.md))`()` Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](Drawable.md)? | [createFromPath](Drawable.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable from file path name. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromStream](Drawable.md))`(`is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`)` Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Create a drawable from an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Create a drawable from inside an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [getBounds](Drawable.md))`()` Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)? | [getCallback](Drawable.md))`()` Return the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation attached to this Drawable. <br /> | | [ColorFilter](../android.graphics/ColorFilter.md)? | [getColorFilter](Drawable.md))`()` Returns the current color filter, or `null` if none set. <br /> | | [Drawable](Drawable.md) | [getCurrent](Drawable.md))`()` <br /> | | [Rect](../android.graphics/Rect.md) | [getDirtyBounds](Drawable.md))`()` Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](Drawable.md))`(`outRect:` ` [Rect](../android.graphics/Rect.md)`)` Populates `outRect` with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](Drawable.md))`()` Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](Drawable.md))`()` Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](Drawable.md))`()` Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](Drawable.md))`()` Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Insets](../android.graphics/Insets.md) | [getOpticalInsets](Drawable.md))`()` Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](Drawable.md))`()` Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_selected](../android/R.attr.md), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](../android.graphics/Region.md)? | [getTransparentRegion](Drawable.md))`()` Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](Drawable.md))`()` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](Drawable.md))`()` Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See [android.util.LayoutDirection](../android.util/LayoutDirection.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](Drawable.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](Drawable.md))`()` Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](../android.graphics/RenderNode.md) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](Drawable.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](Drawable.md))`()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Override this in your subclass to change appearance if you vary based on level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](Drawable.md))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](Drawable.md))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See [android.util.LayoutDirection](../android.util/LayoutDirection.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](Drawable.md))`(`cb:` ` [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)?`)` Bind a [Callback](../android/graphics/drawable/Drawable.Callback.md) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](Drawable.md))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](Drawable.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](Drawable.md)) which constructs a [PorterDuffColorFilter](../android.graphics/PorterDuffColorFilter.md). **Note:** Setting a color filter disables [tint](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](Drawable.md))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](Drawable.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md)) in order to have itself redrawn, *and* true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](Drawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_pressed](../android/R.attr.md)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md)) in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](Drawable.md))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)). To clear the tint, pass `null` to [setTintList(android.content.res.ColorStateList)](Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)) overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](Drawable.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)) overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](Drawable.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`)` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## XML attributes

### android:bottom

```
android:bottom
```
Bottom padding.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:color

```
android:color
```
Defines the color of the shape.

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:height

```
android:height
```
Defines the height of the shape.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:left

```
android:left
```
Left padding.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:right

```
android:right
```
Right padding.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:top

```
android:top
```
Top padding.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:width

```
android:width
```
Defines the width of the shape.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

## Public constructors

### ShapeDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ShapeDrawable()
```

ShapeDrawable constructor. 

### ShapeDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ShapeDrawable(s: Shape!)
```

Creates a ShapeDrawable with a specified Shape.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [Shape](../android.graphics.drawable.shapes/Shape.md)!: the Shape that this ShapeDrawable should be |

## Public methods

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyTheme(t: Resources.Theme): Unit
```

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [Resources.Theme](../android/content/res/Resources.Theme.md): the theme to apply This value cannot be `null`. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(canvas: Canvas): Unit
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android.graphics/Canvas.md): The canvas to draw into This value cannot be `null`. |

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

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](Drawable.md)) or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either `0` or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android.content.pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android.content.pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android.content.pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android.content.pm/ActivityInfo.md) |

### getConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConstantState(): Drawable.ConstantState?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | The ConstantState associated to that Drawable. This value may be `null`. |

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
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The opacity class of the Drawable. Value is [android.graphics.PixelFormat#UNKNOWN](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSLUCENT](../android.graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSPARENT](../android.graphics/PixelFormat.md), or [android.graphics.PixelFormat#OPAQUE](../android.graphics/PixelFormat.md) |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutline(outline: Outline): Unit
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------|
| `outline` | [Outline](../android.graphics/Outline.md): This value cannot be `null`. |

### getPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPadding(padding: Rect): Boolean
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `padding` | [Rect](../android.graphics/Rect.md): This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this drawable actually has a padding, else false. When false is returned, the padding is always set to 0. |

### getPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPaint(): Paint!
```

Returns the Paint used to draw the shape. 

### getShaderFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShaderFactory(): ShapeDrawable.ShaderFactory!
```

Returns the ShaderFactory used by this ShapeDrawable for requesting a [android.graphics.Shader](../android.graphics/Shader.md). 

### getShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShape(): Shape!
```

Returns the Shape of this ShapeDrawable. 

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasFocusStateSpecified(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if [android.R.attr#state_focused](../android/R.attr.md) is specified for this drawable. |

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
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Resources](../android.content.res/Resources.md): Resources used to resolve attribute values This value cannot be `null`. |
| `parser` | [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md): XML parser from which to inflate this Drawable This value cannot be `null`. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md): Base set of attribute values This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: Theme to apply, may be null |

| Exceptions ||
|-----------------------------------------|---|
| `org.xmlpull.v1.XmlPullParserException` | |
| `java.io.IOException` | |

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
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| [Drawable](Drawable.md) | This drawable. This value cannot be `null`. |

### setAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlpha(alpha: Int): Unit
```

Set the alpha level for this drawable \[0..255\]. Note that this drawable also has a color in its paint, which has an alpha as well. These two values are automatically combined during drawing. Thus if the color's alpha is 75% (i.e. 192) and the drawable's alpha is 50% (i.e. 128), then the combined alpha that will be used during drawing will be 37.5% (i.e. 96).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is between 0 and 255 inclusive |

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorFilter(colorFilter: ColorFilter?): Unit
```

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorFilter` | [ColorFilter](../android.graphics/ColorFilter.md)?: The color filter to apply, or `null` to remove the existing color filter |

### setDither

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDither(dither: Boolean): Unit
```  

### setIntrinsicHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntrinsicHeight(height: Int): Unit
```

Sets the intrinsic (default) height for this shape.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the intrinsic height (in pixels) |

### setIntrinsicWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntrinsicWidth(width: Int): Unit
```

Sets the intrinsic (default) width for this shape.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the intrinsic width (in pixels) |

### setPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPadding(padding: Rect!): Unit
```

Sets padding for this shape, defined by a Rect object. Define the padding in the Rect object as: left, top, right, bottom. 

### setPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPadding(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets padding for the shape.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): padding for the left side (in pixels) |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): padding for the top (in pixels) |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): padding for the right side (in pixels) |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): padding for the bottom (in pixels) |

### setShaderFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShaderFactory(fact: ShapeDrawable.ShaderFactory!): Unit
```

Sets a ShaderFactory to which requests for a [android.graphics.Shader](../android.graphics/Shader.md) object will be made.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fact` | [ShapeDrawable.ShaderFactory](../android/graphics/drawable/ShapeDrawable.ShaderFactory.md)!: an instance of your ShaderFactory implementation |

### setShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShape(s: Shape!): Unit
```

Sets the Shape of this ShapeDrawable. 

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintBlendMode(blendMode: BlendMode!): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](../android.graphics/BlendMode.md).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](../android.graphics/BlendMode.md)!: This value cannot be `null`. |

### setTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintList(tint: ColorStateList?): Unit
```

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?: Color state list to use for tinting this drawable, or `null` to clear the tint |

## Protected methods

### inflateTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun inflateTag(
    name: String!, 
    r: Resources!, 
    parser: XmlPullParser!, 
    attrs: AttributeSet!
): Boolean
```

Subclasses override this to parse custom subelements. If you handle it, return true, else return *super.inflateTag(...)*. 

### onBoundsChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android.graphics/Rect.md): This value cannot be `null`. |

### onDraw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onDraw(
    shape: Shape!, 
    canvas: Canvas!, 
    paint: Paint!
): Unit
```

Called from the drawable's draw() method after the canvas has been set to draw the shape at (0,0). Subclasses can override for special effects such as multiple layers, stroking, etc. 

### onStateChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStateChange(stateSet: IntArray): Boolean
```

| Parameters ||
|---------|------------------------------|
| `state` | This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |
