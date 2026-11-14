Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GradientDrawable

Kotlin | [Java](GradientDrawable.md) 
| --- | --- |

```
open class GradientDrawable : Drawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](Drawable.md) ||
| | ↳ | [android.graphics.drawable.GradientDrawable](GradientDrawable.md) |

A Drawable with a color gradient for buttons, backgrounds, etc.

It can be defined in an XML file with the `<shape>` element. For more information, see the guide to [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Orientation](../android/graphics/drawable/GradientDrawable.Orientation.md) Controls how the gradient is oriented relative to the drawable's bounds |

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [`android:angle`](GradientDrawable.md) | Angle of the gradient, used only with linear gradient. |
| [`android:bottom`](GradientDrawable.md) | Amount of bottom padding inside the gradient shape. |
| [`android:centerColor`](GradientDrawable.md) | Optional center color. |
| --- | --- |
| [`android:centerX`](GradientDrawable.md) | X-position of the center point of the gradient within the shape as a fraction of the width. |
| [`android:centerY`](GradientDrawable.md) | Y-position of the center point of the gradient within the shape as a fraction of the height. |
| [`android:color`](GradientDrawable.md) | Solid color for the gradient shape. |
| --- | --- |
| [`android:color`](GradientDrawable.md) | Color of the gradient shape's stroke. |
| [`android:dashGap`](GradientDrawable.md) | Gap between dashes in the stroke. |
| [`android:dashWidth`](GradientDrawable.md) | Length of a dash in the stroke. |
| --- | --- |
| [`android:endColor`](GradientDrawable.md) | End color of the gradient. |
| [`android:gradientRadius`](GradientDrawable.md) | Radius of the gradient, used only with radial gradient. |
| [`android:height`](GradientDrawable.md) | Height of the gradient shape. |
| --- | --- |
| [`android:innerRadius`](GradientDrawable.md) | Inner radius of the ring. |
| [`android:innerRadiusRatio`](GradientDrawable.md) | Inner radius of the ring expressed as a ratio of the ring's width. |
| [`android:left`](GradientDrawable.md) | Amount of left padding inside the gradient shape. |
| --- | --- |
| [`android:right`](GradientDrawable.md) | Amount of right padding inside the gradient shape. |
| [`android:shape`](GradientDrawable.md) | Indicates what shape to fill with a gradient. |
| [`android:startColor`](GradientDrawable.md) | Start color of the gradient. |
| --- | --- |
| [`android:thickness`](GradientDrawable.md) | Thickness of the ring. |
| [`android:thicknessRatio`](GradientDrawable.md) | Thickness of the ring expressed as a ratio of the ring's width. |
| [`android:top`](GradientDrawable.md) | Amount of top padding inside the gradient shape. |
| --- | --- |
| [`android:type`](GradientDrawable.md) | Type of gradient. |
| [`android:useLevel`](GradientDrawable.md) | Whether the drawable level value (see android.graphics.drawable.Drawable#getLevel() ) is used to scale the shape. |
| [`android:useLevel`](GradientDrawable.md) | Whether the drawable level value (see android.graphics.drawable.Drawable#getLevel() ) is used to scale the gradient. |
| --- | --- |
| [`android:visible`](GradientDrawable.md) | Indicates whether the drawable should intially be visible. |
| [`android:width`](GradientDrawable.md) | Width of the gradient shape. |
| [`android:width`](GradientDrawable.md) | Width of the gradient shape's stroke. |
| --- | --- |

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ARC](GradientDrawable.md) Shape is an arc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE](GradientDrawable.md) Shape is a line |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINEAR_GRADIENT](GradientDrawable.md) Gradient is linear (default.) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OVAL](GradientDrawable.md) Shape is an ellipse |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RADIAL_GRADIENT](GradientDrawable.md) Gradient is circular. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECTANGLE](GradientDrawable.md) Shape is a rectangle, possibly with rounded corners |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RING](GradientDrawable.md) Shape is a ring. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SWEEP_GRADIENT](GradientDrawable.md) Gradient is a sweep. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GradientDrawable](GradientDrawable.md))`()` <br /> |
| [GradientDrawable](GradientDrawable.md))`(`orientation:` ` [GradientDrawable.Orientation](../android/graphics/drawable/GradientDrawable.Orientation.md)!`, `colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Create a new gradient drawable given an orientation and an array of colors for the gradient. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](GradientDrawable.md))`(`t:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)`)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](GradientDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](GradientDrawable.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](GradientDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](GradientDrawable.md))`()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| open [ColorStateList](../android.content.res/ColorStateList.md)? | [getColor](GradientDrawable.md))`()` Returns the color state list used to fill the shape, or `null` if the shape is filled with a gradient or has no fill color. |
| --- | --- |
| open [ColorFilter](../android.graphics/ColorFilter.md)? | [getColorFilter](GradientDrawable.md))`()` Returns the current color filter, or `null` if none set. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getColors](GradientDrawable.md))`()` Returns the colors used to draw the gradient, or `null` if the gradient is drawn using a single color or no colors. |
| open [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | [getConstantState](GradientDrawable.md))`()` <br /> |
| --- | --- |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)? | [getCornerRadii](GradientDrawable.md))`()` Returns the radii for each of the 4 corners. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCornerRadius](GradientDrawable.md))`()` Returns the radius for the corners of the gradient, that was previously set with [setCornerRadius(float)](GradientDrawable.md)). |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGradientCenterX](GradientDrawable.md))`()` Returns the X-position of the center of the gradient as a fraction of the width. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGradientCenterY](GradientDrawable.md))`()` Returns the Y-position of the center of this gradient as a fraction of the height. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGradientRadius](GradientDrawable.md))`()` Returns the radius of the gradient in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGradientType](GradientDrawable.md))`()` Returns the type of gradient used by this drawable, one of [LINEAR_GRADIENT](GradientDrawable.md), [RADIAL_GRADIENT](GradientDrawable.md), or [SWEEP_GRADIENT](GradientDrawable.md). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInnerRadius](GradientDrawable.md))`()` Return the inner radius of the ring The units of this value are pixels. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInnerRadiusRatio](GradientDrawable.md))`()` Return the inner radius of the ring expressed as a ratio of the ring's width. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](GradientDrawable.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](GradientDrawable.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](GradientDrawable.md))`()` <br /> |
| open [Insets](../android.graphics/Insets.md) | [getOpticalInsets](GradientDrawable.md))`()` <br /> |
| --- | --- |
| open [GradientDrawable.Orientation](../android/graphics/drawable/GradientDrawable.Orientation.md)! | [getOrientation](GradientDrawable.md))`()` Returns the orientation of the gradient defined in this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](GradientDrawable.md))`(`outline:` ` [Outline](../android.graphics/Outline.md)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](GradientDrawable.md))`(`padding:` ` [Rect](../android.graphics/Rect.md)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getShape](GradientDrawable.md))`()` Returns the type of shape used by this drawable, one of [LINE](GradientDrawable.md), [OVAL](GradientDrawable.md), [RECTANGLE](GradientDrawable.md) or [RING](GradientDrawable.md). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThickness](GradientDrawable.md))`()` Return the thickness of the ring The units of this value are pixels. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getThicknessRatio](GradientDrawable.md))`()` Return the thickness ratio of the ring expressed as a ratio of the ring's width. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseLevel](GradientDrawable.md))`()` Returns whether this drawable's `level` property will be used to scale the gradient. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](GradientDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](GradientDrawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Inflate this Drawable from an XML resource optionally styled by a theme. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](GradientDrawable.md))`()` <br /> |
| open [Drawable](Drawable.md) | [mutate](GradientDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](GradientDrawable.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColor](GradientDrawable.md))`(`colorStateList:` ` [ColorStateList](../android.content.res/ColorStateList.md)?`)` Changes this drawable to use a single color state list instead of a gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColor](GradientDrawable.md))`(`argb:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes this drawable to use a single color instead of a gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](GradientDrawable.md))`(`colorFilter:` ` [ColorFilter](../android.graphics/ColorFilter.md)?`)` Specify an optional color filter for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColors](GradientDrawable.md))`(`colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`)` Sets the colors used to draw the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColors](GradientDrawable.md))`(`colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`, `offsets:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`)` Sets the colors and offsets used to draw the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCornerRadii](GradientDrawable.md))`(`radii:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`)` Specifies radii for each of the 4 corners. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCornerRadius](GradientDrawable.md))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the radius for the corners of the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](GradientDrawable.md))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGradientCenter](GradientDrawable.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the position of the center of the gradient as a fraction of the width and height. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGradientRadius](GradientDrawable.md))`(`gradientRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the radius of the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGradientType](GradientDrawable.md))`(`gradient:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of gradient used by this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInnerRadius](GradientDrawable.md))`(`innerRadius:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Configure the inner radius of the ring. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInnerRadiusRatio](GradientDrawable.md))`(`innerRadiusRatio:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Inner radius of the ring expressed as a ratio of the ring's width. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrientation](GradientDrawable.md))`(`orientation:` ` [GradientDrawable.Orientation](../android/graphics/drawable/GradientDrawable.Orientation.md)!`)` Sets the orientation of the gradient defined in this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPadding](GradientDrawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Configure the padding of the gradient shape |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShape](GradientDrawable.md))`(`shape:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of shape used to draw the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSize](GradientDrawable.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the size of the shape drawn by this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStroke](GradientDrawable.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colorStateList:` ` [ColorStateList](../android.content.res/ColorStateList.md)!`)` Set the stroke width and color state list for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStroke](GradientDrawable.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colorStateList:` ` [ColorStateList](../android.content.res/ColorStateList.md)!`, `dashWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dashGap:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the stroke width and color state list for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStroke](GradientDrawable.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the stroke width and color for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStroke](GradientDrawable.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dashWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dashGap:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the stroke width and color for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThickness](GradientDrawable.md))`(`thickness:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Configure the thickness of the ring. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThicknessRatio](GradientDrawable.md))`(`thicknessRatio:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Configure the thickness of the ring expressed as a ratio of the ring's width. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](GradientDrawable.md))`(`blendMode:` ` [BlendMode](../android.graphics/BlendMode.md)!`)` Specifies a tint blending mode for this drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](GradientDrawable.md))`(`tint:` ` [ColorStateList](../android.content.res/ColorStateList.md)?`)` Specifies tint color for this drawable as a color state list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseLevel](GradientDrawable.md))`(`useLevel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this drawable's `level` property will be used to scale the gradient. |

| Protected methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](GradientDrawable.md))`(`r:` ` [Rect](../android.graphics/Rect.md)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](GradientDrawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](GradientDrawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Drawable](Drawable.md) |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](Drawable.md))`()` Removes the color filter for this drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [copyBounds](Drawable.md))`()` Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](Drawable.md)? | [createFromPath](Drawable.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable from file path name. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromStream](Drawable.md))`(`is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`)` Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Create a drawable from an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Create a drawable from inside an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [getBounds](Drawable.md))`()` Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)? | [getCallback](Drawable.md))`()` Return the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation attached to this Drawable. <br /> | | [Drawable](Drawable.md) | [getCurrent](Drawable.md))`()` <br /> | | [Rect](../android.graphics/Rect.md) | [getDirtyBounds](Drawable.md))`()` Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](Drawable.md))`(`outRect:` ` [Rect](../android.graphics/Rect.md)`)` Populates `outRect` with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](Drawable.md))`()` Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](Drawable.md))`()` Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](Drawable.md))`()` Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](Drawable.md))`()` Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](Drawable.md))`()` Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_selected](../android/R.attr.md), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](../android.graphics/Region.md)? | [getTransparentRegion](Drawable.md))`()` Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](Drawable.md))`()` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](Drawable.md))`()` Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See [android.util.LayoutDirection](../android.util/LayoutDirection.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](Drawable.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](Drawable.md))`()` Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](../android.graphics/RenderNode.md) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](Drawable.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](Drawable.md))`()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the drawable's resolved layout direction changes. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](Drawable.md))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](Drawable.md))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See [android.util.LayoutDirection](../android.util/LayoutDirection.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](Drawable.md))`(`cb:` ` [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)?`)` Bind a [Callback](../android/graphics/drawable/Drawable.Callback.md) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](Drawable.md))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](Drawable.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](Drawable.md)) which constructs a [PorterDuffColorFilter](../android.graphics/PorterDuffColorFilter.md). **Note:** Setting a color filter disables [tint](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](Drawable.md))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](Drawable.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md)) in order to have itself redrawn, *and* true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](Drawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_pressed](../android/R.attr.md)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md)) in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](Drawable.md))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)). To clear the tint, pass `null` to [setTintList(android.content.res.ColorStateList)](Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)) overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](Drawable.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)) overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](Drawable.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`)` Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## XML attributes

### android:angle

```
android:angle
```
Angle of the gradient, used only with linear gradient. Must be a multiple of 45 in the range \[0, 315\].

May be a floating point value, such as "`1.2`". 

### android:bottom

```
android:bottom
```
Amount of bottom padding inside the gradient shape.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:centerColor

```
android:centerColor
```
Optional center color. For linear gradients, use centerX or centerY to place the center color.

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:centerX

```
android:centerX
```
X-position of the center point of the gradient within the shape as a fraction of the width. The default value is 0.5.

May be a floating point value, such as "`1.2`".

May be a fractional value, which is a floating point number appended with either % or %p, such as "`14.5%`". The % suffix always means a percentage of the base size; the optional %p suffix provides a size relative to some parent container. 

### android:centerY

```
android:centerY
```
Y-position of the center point of the gradient within the shape as a fraction of the height. The default value is 0.5.

May be a floating point value, such as "`1.2`".

May be a fractional value, which is a floating point number appended with either % or %p, such as "`14.5%`". The % suffix always means a percentage of the base size; the optional %p suffix provides a size relative to some parent container. 

### android:color

```
android:color
```
Solid color for the gradient shape.

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:color

```
android:color
```
Color of the gradient shape's stroke.

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:dashGap

```
android:dashGap
```
Gap between dashes in the stroke.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:dashWidth

```
android:dashWidth
```
Length of a dash in the stroke.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:endColor

```
android:endColor
```
End color of the gradient.

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:gradientRadius

```
android:gradientRadius
```
Radius of the gradient, used only with radial gradient. May be an explicit dimension or a fractional value relative to the shape's minimum dimension.

May be a floating point value, such as "`1.2`".

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

May be a fractional value, which is a floating point number appended with either % or %p, such as "`14.5%`". The % suffix always means a percentage of the base size; the optional %p suffix provides a size relative to some parent container. 

### android:height

```
android:height
```
Height of the gradient shape.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:innerRadius

```
android:innerRadius
```
Inner radius of the ring. When defined, innerRadiusRatio is ignored.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:innerRadiusRatio

```
android:innerRadiusRatio
```
Inner radius of the ring expressed as a ratio of the ring's width. For instance, if innerRadiusRatio=9, then the inner radius equals the ring's width divided by 9. This value is ignored if innerRadius is defined. Default value is 9.

May be a floating point value, such as "`1.2`". 

### android:left

```
android:left
```
Amount of left padding inside the gradient shape.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:right

```
android:right
```
Amount of right padding inside the gradient shape.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:shape

```
android:shape
```
Indicates what shape to fill with a gradient.

Must be one of the following constant values.

| Constant | Value | Description |
|-----------|-------|-------------------------------------------------|
| arc | 4 | ARC shape. |
| line | 2 | Line shape. |
| oval | 1 | Oval shape. |
| --- | --- | --- |
| rectangle | 0 | Rectangle shape, with optional rounder corners. |
| ring | 3 | Ring shape. |

### android:startColor

```
android:startColor
```
Start color of the gradient.

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:thickness

```
android:thickness
```
Thickness of the ring. When defined, thicknessRatio is ignored.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:thicknessRatio

```
android:thicknessRatio
```
Thickness of the ring expressed as a ratio of the ring's width. For instance, if thicknessRatio=3, then the thickness equals the ring's width divided by 3. This value is ignored if innerRadius is defined. Default value is 3.

May be a floating point value, such as "`1.2`". 

### android:top

```
android:top
```
Amount of top padding inside the gradient shape.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:type

```
android:type
```
Type of gradient. The default type is linear.

Must be one of the following constant values.

| Constant | Value | Description |
|----------|-------|---------------------------------------------------------------------------------|
| linear | 0 | Linear gradient extending across the center point. |
| radial | 1 | Radial gradient extending from the center point outward. |
| sweep | 2 | Sweep (or angular) gradient sweeping counter-clockwise around the center point. |
| --- | --- | --- |

### android:useLevel

```
android:useLevel
```
Whether the drawable level value (see [android.graphics.drawable.Drawable#getLevel()](Drawable.md))) is used to scale the shape. Scaling behavior depends on the shape type. For "ring", the angle is scaled from 0 to 360. For all other types, there is no effect. The default value is true.

May be a boolean value, such as "`true`" or "`false`". 

### android:useLevel

```
android:useLevel
```
Whether the drawable level value (see [android.graphics.drawable.Drawable#getLevel()](Drawable.md))) is used to scale the gradient. Scaling behavior varies based on gradient type. For "linear", adjusts the ending position along the gradient's axis of orientation. For "radial", adjusts the outer radius. For "sweep", adjusts the ending angle. The default value is false.

May be a boolean value, such as "`true`" or "`false`". 

### android:visible

```
android:visible
```
Indicates whether the drawable should intially be visible.

May be a boolean value, such as "`true`" or "`false`". 

### android:width

```
android:width
```
Width of the gradient shape.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:width

```
android:width
```
Width of the gradient shape's stroke.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

## Constants

### ARC

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ARC: Int
```

Shape is an arc. 

 Value: 4

### LINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE: Int
```

Shape is a line 

 Value: 2

### LINEAR_GRADIENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINEAR_GRADIENT: Int
```

Gradient is linear (default.) 

 Value: 0

### OVAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVAL: Int
```

Shape is an ellipse 

 Value: 1

### RADIAL_GRADIENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RADIAL_GRADIENT: Int
```

Gradient is circular. 

 Value: 1

### RECTANGLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECTANGLE: Int
```

Shape is a rectangle, possibly with rounded corners 

 Value: 0

### RING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RING: Int
```

Shape is a ring. 

 Value: 3

### SWEEP_GRADIENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SWEEP_GRADIENT: Int
```

Gradient is a sweep. 

 Value: 2

## Public constructors

### GradientDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GradientDrawable()
```  

### GradientDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GradientDrawable(
    orientation: GradientDrawable.Orientation!, 
    colors: IntArray!)
```

Create a new gradient drawable given an orientation and an array of colors for the gradient.

## Public methods

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------|
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

### getColor

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColor(): ColorStateList?
```

Returns the color state list used to fill the shape, or `null` if the shape is filled with a gradient or has no fill color.

| Return ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [ColorStateList](../android.content.res/ColorStateList.md)? | the color state list used to fill this gradient, or `null` |

**See Also**

- [#setColor(int)](GradientDrawable.md))
- [#setColor(ColorStateList)](GradientDrawable.md)) 

### getColorFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorFilter(): ColorFilter?
```

Returns the current color filter, or `null` if none set.

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------|
| [ColorFilter](../android.graphics/ColorFilter.md)? | This value may be `null`. |

### getColors

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColors(): IntArray?
```

Returns the colors used to draw the gradient, or `null` if the gradient is drawn using a single color or no colors.

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | the colors used to draw the gradient, or `null` |

**See Also**

- [#setColors(int[] colors)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColors(kotlin.IntArray)) 

### getConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConstantState(): Drawable.ConstantState?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | The ConstantState associated to that Drawable. This value may be `null`. |

### getCornerRadii

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCornerRadii(): FloatArray?
```

Returns the radii for each of the 4 corners. For each corner, the array contains 2 values, `[X_radius, Y_radius]`. The corners are ordered top-left, top-right, bottom-right, bottom-left.

If the radius was previously set with [setCornerRadius(float)](GradientDrawable.md)), or if the corners are not rounded, this method will return `null`.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)? | an array containing the radii for each of the 4 corners, or `null` |

**See Also**

- [#setCornerRadii(float[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadii(kotlin.FloatArray)) 

### getCornerRadius

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCornerRadius(): Float
```

Returns the radius for the corners of the gradient, that was previously set with [setCornerRadius(float)](GradientDrawable.md)).

If the radius was previously cleared via passing `null` to [setCornerRadii(float[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadii(kotlin.FloatArray)), this method will return 0.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the radius in pixels of the corners of the rectangle shape, or 0 |

**See Also**

- [#setCornerRadius](GradientDrawable.md)) 

### getGradientCenterX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGradientCenterX(): Float
```

Returns the X-position of the center of the gradient as a fraction of the width.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the X-position of the center of the gradient |

**See Also**

- [#setGradientCenter(float, float)](GradientDrawable.md)) 

### getGradientCenterY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGradientCenterY(): Float
```

Returns the Y-position of the center of this gradient as a fraction of the height.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the Y-position of the center of the gradient |

**See Also**

- [#setGradientCenter(float, float)](GradientDrawable.md)) 

### getGradientRadius

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGradientRadius(): Float
```

Returns the radius of the gradient in pixels. The radius is valid only when the gradient type is set to [RADIAL_GRADIENT](GradientDrawable.md).

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the radius of the gradient in pixels |

**See Also**

- [#setGradientRadius(float)](GradientDrawable.md)) 

### getGradientType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGradientType(): Int
```

Returns the type of gradient used by this drawable, one of [LINEAR_GRADIENT](GradientDrawable.md), [RADIAL_GRADIENT](GradientDrawable.md), or [SWEEP_GRADIENT](GradientDrawable.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the type of gradient used by this drawable Value is [android.graphics.drawable.GradientDrawable#LINEAR_GRADIENT](GradientDrawable.md), [android.graphics.drawable.GradientDrawable#RADIAL_GRADIENT](GradientDrawable.md), or [android.graphics.drawable.GradientDrawable#SWEEP_GRADIENT](GradientDrawable.md) |

**See Also**

- [#setGradientType(int)](GradientDrawable.md)) 

### getInnerRadius

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInnerRadius(): Int
```

Return the inner radius of the ring 
The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The units of this value are pixels. {} |

**See Also**

- [#setInnerRadius(int)](GradientDrawable.md)) 

### getInnerRadiusRatio

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInnerRadiusRatio(): Float
```

Return the inner radius of the ring expressed as a ratio of the ring's width. 
**See Also**

- [#setInnerRadiusRatio(float)](GradientDrawable.md)) 

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

### getOpticalInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOpticalInsets(): Insets
```

| Return ||
|----------------------------------------------------------------------------------------|------------------------------|
| [Insets](../android.graphics/Insets.md) | This value cannot be `null`. |

### getOrientation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrientation(): GradientDrawable.Orientation!
```

Returns the orientation of the gradient defined in this drawable.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [GradientDrawable.Orientation](../android/graphics/drawable/GradientDrawable.Orientation.md)! | the orientation of the gradient defined in this drawable |

**See Also**

- [#setOrientation(Orientation)](GradientDrawable.md)) 

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

### getShape

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShape(): Int
```

Returns the type of shape used by this drawable, one of [LINE](GradientDrawable.md), [OVAL](GradientDrawable.md), [RECTANGLE](GradientDrawable.md) or [RING](GradientDrawable.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the type of shape used by this drawable Value is [android.graphics.drawable.GradientDrawable#RECTANGLE](GradientDrawable.md), [android.graphics.drawable.GradientDrawable#OVAL](GradientDrawable.md), [android.graphics.drawable.GradientDrawable#LINE](GradientDrawable.md), [android.graphics.drawable.GradientDrawable#RING](GradientDrawable.md), or [android.graphics.drawable.GradientDrawable#ARC](GradientDrawable.md) |

**See Also**

- [#setShape(int)](GradientDrawable.md)) 

### getThickness

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThickness(): Int
```

Return the thickness of the ring 
The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The units of this value are pixels. {} |

**See Also**

- [#setThickness(int)](GradientDrawable.md)) 

### getThicknessRatio

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThicknessRatio(): Float
```

Return the thickness ratio of the ring expressed as a ratio of the ring's width. 
**See Also**

- [#setThicknessRatio(float)](GradientDrawable.md)) 

### getUseLevel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUseLevel(): Boolean
```

Returns whether this drawable's `level` property will be used to scale the gradient.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the gradient should be scaled based on level, `false` otherwise |

**See Also**

- [#setUseLevel(boolean)](GradientDrawable.md)) 

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

Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Resources](../android.content.res/Resources.md): This value cannot be `null`. |
| `parser` | [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md): This value cannot be `null`. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md): This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: This value may be `null`. |

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

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is between 0 and 255 inclusive |

### setColor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColor(colorStateList: ColorStateList?): Unit
```

Changes this drawable to use a single color state list instead of a gradient. Calling this method with a null argument will clear the color and is equivalent to calling [setColor(int)](GradientDrawable.md)) with the argument [Color.TRANSPARENT](../android.graphics/Color.md).

**Note** : changing color will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing the color.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorStateList` | [ColorStateList](../android.content.res/ColorStateList.md)?: The color state list used to fill the shape This value may be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#getColor](GradientDrawable.md)) 

### setColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColor(argb: Int): Unit
```

Changes this drawable to use a single color instead of a gradient.

**Note** : changing color will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing the color.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `argb` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color used to fill the shape |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setColors(int[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColors(kotlin.IntArray))
- [#getColor](GradientDrawable.md)) 

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorFilter(colorFilter: ColorFilter?): Unit
```

Specify an optional color filter for the drawable.

If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas.

Pass `null` to remove any existing color filter.

**Note:** Setting a non-`null` color filter disables [tint](Drawable.md)).

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| `colorFilter` | [ColorFilter](../android.graphics/ColorFilter.md)?: This value may be `null`. |

### setColors

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColors(colors: IntArray?): Unit
```

Sets the colors used to draw the gradient.

Each color is specified as an ARGB integer and the array must contain at least 2 colors.

**Note** : changing colors will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing the colors.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: an array containing 2 or more ARGB colors This value may be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setColor(int)](GradientDrawable.md)) 

### setColors

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColors(
    colors: IntArray?, 
    offsets: FloatArray?
): Unit
```

Sets the colors and offsets used to draw the gradient.

Each color is specified as an ARGB integer and the array must contain at least 2 colors.

**Note** : changing colors will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing the colors.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: an array containing 2 or more ARGB colors This value may be `null`. |
| `offsets` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: optional array of floating point parameters representing the positions of the colors. Null evenly disperses the colors This value may be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setColors(int[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColors(kotlin.IntArray)) 

### setCornerRadii

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCornerRadii(radii: FloatArray?): Unit
```

Specifies radii for each of the 4 corners. For each corner, the array contains 2 values, `[X_radius, Y_radius]`. The corners are ordered top-left, top-right, bottom-right, bottom-left. This property is honored only when the shape is of type [RECTANGLE](GradientDrawable.md).

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `radii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: an array of length \>= 8 containing 4 pairs of X and Y radius for each corner, specified in pixels This value may be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setShape(int)](GradientDrawable.md))
- [#setCornerRadius(float)](GradientDrawable.md)) 

### setCornerRadius

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCornerRadius(radius: Float): Unit
```

Specifies the radius for the corners of the gradient. If this is \> 0, then the drawable is drawn in a round-rectangle, rather than a rectangle. This property is honored only when the shape is of type [RECTANGLE](GradientDrawable.md).

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The radius in pixels of the corners of the rectangle shape |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setCornerRadii(float[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadii(kotlin.FloatArray))
- [#setShape(int)](GradientDrawable.md)) 

### setDither

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDither(dither: Boolean): Unit
```  

### setGradientCenter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGradientCenter(
    x: Float, 
    y: Float
): Unit
```

Sets the position of the center of the gradient as a fraction of the width and height.

The default value is (0.5, 0.5).

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the X-position of the center of the gradient |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the Y-position of the center of the gradient |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setGradientType(int)](GradientDrawable.md))
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientCenterX()>
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientCenterY()> 

### setGradientRadius

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGradientRadius(gradientRadius: Float): Unit
```

Sets the radius of the gradient. The radius is honored only when the gradient type is set to [RADIAL_GRADIENT](GradientDrawable.md).

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------|
| `gradientRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the radius of the gradient in pixels |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setGradientType(int)](GradientDrawable.md))
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientRadius()> 

### setGradientType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGradientType(gradient: Int): Unit
```

Sets the type of gradient used by this drawable.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gradient` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of the gradient: [LINEAR_GRADIENT](GradientDrawable.md), [RADIAL_GRADIENT](GradientDrawable.md) or [SWEEP_GRADIENT](GradientDrawable.md) Value is [android.graphics.drawable.GradientDrawable#LINEAR_GRADIENT](GradientDrawable.md), [android.graphics.drawable.GradientDrawable#RADIAL_GRADIENT](GradientDrawable.md), or [android.graphics.drawable.GradientDrawable#SWEEP_GRADIENT](GradientDrawable.md) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientType()> 

### setInnerRadius

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInnerRadius(innerRadius: Int): Unit
```

Configure the inner radius of the ring.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------|
| `innerRadius` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The units of this value are pixels. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getInnerRadius()> 

### setInnerRadiusRatio

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInnerRadiusRatio(innerRadiusRatio: Float): Unit
```

Inner radius of the ring expressed as a ratio of the ring's width.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------|
| `innerRadiusRatio` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Value is 0.0f or greater |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getInnerRadiusRatio()> 

### setOrientation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOrientation(orientation: GradientDrawable.Orientation!): Unit
```

Sets the orientation of the gradient defined in this drawable.

**Note** : changing orientation will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing the orientation.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `orientation` | [GradientDrawable.Orientation](../android/graphics/drawable/GradientDrawable.Orientation.md)!: the desired orientation (angle) of the gradient |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getOrientation()> 

### setPadding

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPadding(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Configure the padding of the gradient shape

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Left padding of the gradient shape The units of this value are pixels. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Top padding of the gradient shape The units of this value are pixels. |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Right padding of the gradient shape The units of this value are pixels. |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bottom padding of the gradient shape The units of this value are pixels. |

### setShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShape(shape: Int): Unit
```

Sets the type of shape used to draw the gradient.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shape` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired shape for this drawable: [LINE](GradientDrawable.md), [OVAL](GradientDrawable.md), [RECTANGLE](GradientDrawable.md) or [RING](GradientDrawable.md) Value is [android.graphics.drawable.GradientDrawable#RECTANGLE](GradientDrawable.md), [android.graphics.drawable.GradientDrawable#OVAL](GradientDrawable.md), [android.graphics.drawable.GradientDrawable#LINE](GradientDrawable.md), [android.graphics.drawable.GradientDrawable#RING](GradientDrawable.md), or [android.graphics.drawable.GradientDrawable#ARC](GradientDrawable.md) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()> 

### setSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSize(
    width: Int, 
    height: Int
): Unit
```

Sets the size of the shape drawn by this drawable.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the shape used by this drawable |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the shape used by this drawable |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setGradientType(int)](GradientDrawable.md)) 

### setStroke

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStroke(
    width: Int, 
    colorStateList: ColorStateList!
): Unit
```

Set the stroke width and color state list for the drawable. If width is zero, then no stroke is drawn.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width in pixels of the stroke |
| `colorStateList` | [ColorStateList](../android.content.res/ColorStateList.md)!: The color state list of the stroke |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setStroke(int, ColorStateList, float, float)](GradientDrawable.md)) 

### setStroke

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStroke(
    width: Int, 
    colorStateList: ColorStateList!, 
    dashWidth: Float, 
    dashGap: Float
): Unit
```

Set the stroke width and color state list for the drawable. If width is zero, then no stroke is drawn. This method can also be used to dash the stroke.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width in pixels of the stroke |
| `colorStateList` | [ColorStateList](../android.content.res/ColorStateList.md)!: The color state list of the stroke |
| `dashWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The length in pixels of the dashes, set to 0 to disable dashes |
| --- | --- |
| `dashGap` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The gap in pixels between dashes |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setStroke(int, ColorStateList)](GradientDrawable.md)) 

### setStroke

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStroke(
    width: Int, 
    color: Int
): Unit
```

Set the stroke width and color for the drawable. If width is zero, then no stroke is drawn.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width in pixels of the stroke |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color of the stroke |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setStroke(int, int, float, float)](GradientDrawable.md)) 

### setStroke

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStroke(
    width: Int, 
    color: Int, 
    dashWidth: Float, 
    dashGap: Float
): Unit
```

Set the stroke width and color for the drawable. If width is zero, then no stroke is drawn. This method can also be used to dash the stroke.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width in pixels of the stroke |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color of the stroke |
| `dashWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The length in pixels of the dashes, set to 0 to disable dashes |
| --- | --- |
| `dashGap` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The gap in pixels between dashes |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setStroke(int, int)](GradientDrawable.md)) 

### setThickness

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setThickness(thickness: Int): Unit
```

Configure the thickness of the ring.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `thickness` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The units of this value are pixels. |

### setThicknessRatio

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setThicknessRatio(thicknessRatio: Float): Unit
```

Configure the thickness of the ring expressed as a ratio of the ring's width.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------|
| `thicknessRatio` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Value is 0.0f or greater |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getThicknessRatio()> 

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

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)) overrides tint.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?: This value may be `null`. |

### setUseLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUseLevel(useLevel: Boolean): Unit
```

Sets whether this drawable's `level` property will be used to scale the gradient. If a gradient is not used, this property has no effect.

Scaling behavior varies based on gradient type:

- [LINEAR_GRADIENT](GradientDrawable.md) adjusts the ending position along the gradient's axis of orientation (see [getOrientation()](GradientDrawable.md)))
- [RADIAL_GRADIENT](GradientDrawable.md) adjusts the outer radius
- [SWEEP_GRADIENT](GradientDrawable.md) adjusts the ending angle
 - The default value for this property is `false`.
 - **Note** : This property corresponds to the `android:useLevel` attribute on the inner `<gradient>` tag, NOT the `android:useLevel` attribute on the outer `<shape>` tag. For example, 

  ```kotlin
  <code>&lt;shape ...&gt;
        &lt;gradient
            ...
            android:useLevel="true" /&gt;
    &lt;/shape&gt;
    </code>
  ```
 - **Note** : Changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](GradientDrawable.md)) before changing this property.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `useLevel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the gradient should be scaled based on level, `false` otherwise |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setLevel(int)](Drawable.md))
- [#getLevel()](Drawable.md))
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getUseLevel()>

## Protected methods

### onBoundsChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBoundsChange(r: Rect): Unit
```

| Parameters ||
|----------|------------------------------|
| `bounds` | This value cannot be `null`. |

### onLevelChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onLevelChange(level: Int): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the level change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last level. |

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
