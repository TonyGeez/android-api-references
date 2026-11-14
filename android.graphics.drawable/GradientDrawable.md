Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GradientDrawable

Kotlin | [Java](https://developer.android.com/reference/android/graphics/drawable/GradientDrawable "View this page in Java") 

```
open class GradientDrawable : Drawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) ||
| | ↳ | [android.graphics.drawable.GradientDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#) |

A Drawable with a color gradient for buttons, backgrounds, etc.

It can be defined in an XML file with the `<shape>` element. For more information, see the guide to [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Orientation](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable.Orientation) Controls how the gradient is oriented relative to the drawable's bounds |

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [`android:angle`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Angle of the gradient, used only with linear gradient. |
| [`android:bottom`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Amount of bottom padding inside the gradient shape. |
| [`android:centerColor`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Optional center color. |
| [`android:centerX`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | X-position of the center point of the gradient within the shape as a fraction of the width. |
| [`android:centerY`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Y-position of the center point of the gradient within the shape as a fraction of the height. |
| [`android:color`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Solid color for the gradient shape. |
| [`android:color`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Color of the gradient shape's stroke. |
| [`android:dashGap`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Gap between dashes in the stroke. |
| [`android:dashWidth`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Length of a dash in the stroke. |
| [`android:endColor`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | End color of the gradient. |
| [`android:gradientRadius`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Radius of the gradient, used only with radial gradient. |
| [`android:height`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Height of the gradient shape. |
| [`android:innerRadius`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Inner radius of the ring. |
| [`android:innerRadiusRatio`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Inner radius of the ring expressed as a ratio of the ring's width. |
| [`android:left`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Amount of left padding inside the gradient shape. |
| [`android:right`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Amount of right padding inside the gradient shape. |
| [`android:shape`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Indicates what shape to fill with a gradient. |
| [`android:startColor`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Start color of the gradient. |
| [`android:thickness`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Thickness of the ring. |
| [`android:thicknessRatio`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Thickness of the ring expressed as a ratio of the ring's width. |
| [`android:top`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Amount of top padding inside the gradient shape. |
| [`android:type`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Type of gradient. |
| [`android:useLevel`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Whether the drawable level value (see android.graphics.drawable.Drawable#getLevel() ) is used to scale the shape. |
| [`android:useLevel`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Whether the drawable level value (see android.graphics.drawable.Drawable#getLevel() ) is used to scale the gradient. |
| [`android:visible`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Indicates whether the drawable should intially be visible. |
| [`android:width`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Width of the gradient shape. |
| [`android:width`](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#attr_GradientDrawable) | Width of the gradient shape's stroke. |

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ARC](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#ARC:kotlin.Int) Shape is an arc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINE:kotlin.Int) Shape is a line |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINEAR_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINEAR_GRADIENT:kotlin.Int) Gradient is linear (default.) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OVAL](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#OVAL:kotlin.Int) Shape is an ellipse |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int) Gradient is circular. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECTANGLE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RECTANGLE:kotlin.Int) Shape is a rectangle, possibly with rounded corners |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RING](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RING:kotlin.Int) Shape is a ring. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SWEEP_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#SWEEP_GRADIENT:kotlin.Int) Gradient is a sweep. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GradientDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#GradientDrawable())`()` <br /> |
| [GradientDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#GradientDrawable(android.graphics.drawable.GradientDrawable.Orientation,%20kotlin.IntArray))`(`orientation:` ` [GradientDrawable.Orientation](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable.Orientation)!`, `colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Create a new gradient drawable given an orientation and an array of colors for the gradient. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#applyTheme(android.content.res.Resources.Theme))`(`t:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)`)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#canApplyTheme())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#draw(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getAlpha())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getChangingConfigurations())`()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| open [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)? | [getColor](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getColor())`()` Returns the color state list used to fill the shape, or `null` if the shape is filled with a gradient or has no fill color. |
| open [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | [getColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getColorFilter())`()` Returns the current color filter, or `null` if none set. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getColors](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getColors())`()` Returns the colors used to draw the gradient, or `null` if the gradient is drawn using a single color or no colors. |
| open [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | [getConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getConstantState())`()` <br /> |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)? | [getCornerRadii](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getCornerRadii())`()` Returns the radii for each of the 4 corners. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCornerRadius](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getCornerRadius())`()` Returns the radius for the corners of the gradient, that was previously set with [setCornerRadius(float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadius(kotlin.Float)). |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGradientCenterX](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientCenterX())`()` Returns the X-position of the center of the gradient as a fraction of the width. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGradientCenterY](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientCenterY())`()` Returns the Y-position of the center of this gradient as a fraction of the height. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGradientRadius](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientRadius())`()` Returns the radius of the gradient in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGradientType](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientType())`()` Returns the type of gradient used by this drawable, one of [LINEAR_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINEAR_GRADIENT:kotlin.Int), [RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int), or [SWEEP_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#SWEEP_GRADIENT:kotlin.Int). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInnerRadius](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getInnerRadius())`()` Return the inner radius of the ring The units of this value are pixels. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInnerRadiusRatio](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getInnerRadiusRatio())`()` Return the inner radius of the ring expressed as a ratio of the ring's width. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getIntrinsicHeight())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getIntrinsicWidth())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getOpacity())`()` <br /> |
| open [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getOpticalInsets](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getOpticalInsets())`()` <br /> |
| open [GradientDrawable.Orientation](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable.Orientation)! | [getOrientation](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getOrientation())`()` Returns the orientation of the gradient defined in this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getPadding(android.graphics.Rect))`(`padding:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getShape())`()` Returns the type of shape used by this drawable, one of [LINE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINE:kotlin.Int), [OVAL](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#OVAL:kotlin.Int), [RECTANGLE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RECTANGLE:kotlin.Int) or [RING](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RING:kotlin.Int). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThickness](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getThickness())`()` Return the thickness of the ring The units of this value are pixels. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getThicknessRatio](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getThicknessRatio())`()` Return the thickness ratio of the ring expressed as a ratio of the ring's width. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getUseLevel())`()` Returns whether this drawable's `level` property will be used to scale the gradient. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#hasFocusStateSpecified())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Inflate this Drawable from an XML resource optionally styled by a theme. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#isStateful())`()` <br /> |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [mutate](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setAlpha(kotlin.Int))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColor](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColor(android.content.res.ColorStateList))`(`colorStateList:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?`)` Changes this drawable to use a single color state list instead of a gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColor](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColor(kotlin.Int))`(`argb:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes this drawable to use a single color instead of a gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColorFilter(android.graphics.ColorFilter))`(`colorFilter:` ` [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?`)` Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColors](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColors(kotlin.IntArray))`(`colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`)` Sets the colors used to draw the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColors](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColors(kotlin.IntArray,%20kotlin.FloatArray))`(`colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`, `offsets:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`)` Sets the colors and offsets used to draw the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCornerRadii](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadii(kotlin.FloatArray))`(`radii:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`)` Specifies radii for each of the 4 corners. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCornerRadius](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadius(kotlin.Float))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the radius for the corners of the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setDither(kotlin.Boolean))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGradientCenter](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientCenter(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the position of the center of the gradient as a fraction of the width and height. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGradientRadius](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientRadius(kotlin.Float))`(`gradientRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the radius of the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGradientType](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientType(kotlin.Int))`(`gradient:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of gradient used by this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInnerRadius](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setInnerRadius(kotlin.Int))`(`innerRadius:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Configure the inner radius of the ring. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInnerRadiusRatio](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setInnerRadiusRatio(kotlin.Float))`(`innerRadiusRatio:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Inner radius of the ring expressed as a ratio of the ring's width. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrientation](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setOrientation(android.graphics.drawable.GradientDrawable.Orientation))`(`orientation:` ` [GradientDrawable.Orientation](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable.Orientation)!`)` Sets the orientation of the gradient defined in this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPadding](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setPadding(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Configure the padding of the gradient shape |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setShape(kotlin.Int))`(`shape:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of shape used to draw the gradient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSize](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setSize(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the size of the shape drawn by this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStroke](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setStroke(kotlin.Int,%20android.content.res.ColorStateList))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colorStateList:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)!`)` Set the stroke width and color state list for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStroke](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setStroke(kotlin.Int,%20android.content.res.ColorStateList,%20kotlin.Float,%20kotlin.Float))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colorStateList:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)!`, `dashWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dashGap:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the stroke width and color state list for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStroke](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setStroke(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the stroke width and color for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStroke](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setStroke(kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dashWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dashGap:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the stroke width and color for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThickness](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setThickness(kotlin.Int))`(`thickness:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Configure the thickness of the ring. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setThicknessRatio](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setThicknessRatio(kotlin.Float))`(`thicknessRatio:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Configure the thickness of the ring expressed as a ratio of the ring's width. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setTintBlendMode(android.graphics.BlendMode))`(`blendMode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)!`)` Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setTintList(android.content.res.ColorStateList))`(`tint:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?`)` Specifies tint color for this drawable as a color state list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setUseLevel(kotlin.Boolean))`(`useLevel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this drawable's `level` property will be used to scale the gradient. |

| Protected methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#onBoundsChange(android.graphics.Rect))`(`r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#onLevelChange(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#onStateChange(kotlin.IntArray))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter())`()` Removes the color filter for this drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds())`()` Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromPath](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable from file path name. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromResourceStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options))`(`res:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?`, `is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#)?`)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [createFromStream](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a drawable from an inputstream <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`)` Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXml](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Create a drawable from an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [createFromXmlInner](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Create a drawable from inside an XML document using an optional [Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds())`()` Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)? | [getCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback())`()` Return the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation attached to this Drawable. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | [getCurrent](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCurrent())`()` <br /> | | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getDirtyBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds())`()` Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getHotspotBounds(android.graphics.Rect))`(`outRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Populates `outRect` with the hotspot bounds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection())`()` Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel())`()` Retrieve the current level. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumHeight())`()` Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumWidth())`()` Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState())`()` Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_selected](https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)? | [getTransparentRegion](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getTransparentRegion())`()` Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet))`(`r:` ` [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)`, `parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf())`()` Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isAutoMirrored())`()` Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See [android.util.LayoutDirection](https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isFilterBitmap())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isProjected())`()` Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#jumpToCurrentState())`()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onLayoutDirectionChanged(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the drawable's resolved layout direction changes. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAutoMirrored(kotlin.Boolean))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See [android.util.LayoutDirection](https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback))`(`cb:` ` [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)?`)` Bind a [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)`)` Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) which constructs a [PorterDuffColorFilter](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#). **Note:** Setting a color filter disables [tint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setFilterBitmap(kotlin.Boolean))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspot(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Specifies the hotspot's location within the drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()) in order to have itself redrawn, *and* true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int), [android.R.attr#state_pressed](https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()) in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)). To clear the tint, pass `null` to [setTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)) overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode))`(`tintMode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)?`)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)) overrides tint. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setVisible(kotlin.Boolean,%20kotlin.Boolean))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable))`(`what:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)`)` Use the current [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

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

### android:useLevel

```
android:useLevel
```
Whether the drawable level value (see [android.graphics.drawable.Drawable#getLevel()](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel())) is used to scale the shape. Scaling behavior depends on the shape type. For "ring", the angle is scaled from 0 to 360. For all other types, there is no effect. The default value is true.

May be a boolean value, such as "`true`" or "`false`". 

### android:useLevel

```
android:useLevel
```
Whether the drawable level value (see [android.graphics.drawable.Drawable#getLevel()](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel())) is used to scale the gradient. Scaling behavior varies based on gradient type. For "linear", adjusts the ending position along the gradient's axis of orientation. For "radial", adjusts the outer radius. For "sweep", adjusts the ending angle. The default value is false.

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
| `t` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#): This value cannot be `null`. |

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
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): The canvas to draw into This value cannot be `null`. |

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

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)) or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either `0` or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) |

### getColor

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColor(): ColorStateList?
```

Returns the color state list used to fill the shape, or `null` if the shape is filled with a gradient or has no fill color.

| Return ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)? | the color state list used to fill this gradient, or `null` |

**See Also**

- [#setColor(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColor(kotlin.Int))
- [#setColor(ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColor(android.content.res.ColorStateList)) 

### getColorFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorFilter(): ColorFilter?
```

Returns the current color filter, or `null` if none set.

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------|
| [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | This value may be `null`. |

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
| [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | The ConstantState associated to that Drawable. This value may be `null`. |

### getCornerRadii

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCornerRadii(): FloatArray?
```

Returns the radii for each of the 4 corners. For each corner, the array contains 2 values, `[X_radius, Y_radius]`. The corners are ordered top-left, top-right, bottom-right, bottom-left.

If the radius was previously set with [setCornerRadius(float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadius(kotlin.Float)), or if the corners are not rounded, this method will return `null`.

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

Returns the radius for the corners of the gradient, that was previously set with [setCornerRadius(float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadius(kotlin.Float)).

If the radius was previously cleared via passing `null` to [setCornerRadii(float[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadii(kotlin.FloatArray)), this method will return 0.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the radius in pixels of the corners of the rectangle shape, or 0 |

**See Also**

- [#setCornerRadius](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadius(kotlin.Float)) 

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

- [#setGradientCenter(float, float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientCenter(kotlin.Float,%20kotlin.Float)) 

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

- [#setGradientCenter(float, float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientCenter(kotlin.Float,%20kotlin.Float)) 

### getGradientRadius

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGradientRadius(): Float
```

Returns the radius of the gradient in pixels. The radius is valid only when the gradient type is set to [RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int).

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the radius of the gradient in pixels |

**See Also**

- [#setGradientRadius(float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientRadius(kotlin.Float)) 

### getGradientType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGradientType(): Int
```

Returns the type of gradient used by this drawable, one of [LINEAR_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINEAR_GRADIENT:kotlin.Int), [RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int), or [SWEEP_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#SWEEP_GRADIENT:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the type of gradient used by this drawable Value is [android.graphics.drawable.GradientDrawable#LINEAR_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINEAR_GRADIENT:kotlin.Int), [android.graphics.drawable.GradientDrawable#RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int), or [android.graphics.drawable.GradientDrawable#SWEEP_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#SWEEP_GRADIENT:kotlin.Int) |

**See Also**

- [#setGradientType(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientType(kotlin.Int)) 

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

- [#setInnerRadius(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setInnerRadius(kotlin.Int)) 

### getInnerRadiusRatio

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInnerRadiusRatio(): Float
```

Return the inner radius of the ring expressed as a ratio of the ring's width. 
**See Also**

- [#setInnerRadiusRatio(float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setInnerRadiusRatio(kotlin.Float)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The opacity class of the Drawable. Value is [android.graphics.PixelFormat#UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int), [android.graphics.PixelFormat#TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int), [android.graphics.PixelFormat#TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int), or [android.graphics.PixelFormat#OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int) |

### getOpticalInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOpticalInsets(): Insets
```

| Return ||
|----------------------------------------------------------------------------------------|------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | This value cannot be `null`. |

### getOrientation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrientation(): GradientDrawable.Orientation!
```

Returns the orientation of the gradient defined in this drawable.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [GradientDrawable.Orientation](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable.Orientation)! | the orientation of the gradient defined in this drawable |

**See Also**

- [#setOrientation(Orientation)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setOrientation(android.graphics.drawable.GradientDrawable.Orientation)) 

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutline(outline: Outline): Unit
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------|
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#): This value cannot be `null`. |

### getPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPadding(padding: Rect): Boolean
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `padding` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this drawable actually has a padding, else false. When false is returned, the padding is always set to 0. |

### getShape

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShape(): Int
```

Returns the type of shape used by this drawable, one of [LINE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINE:kotlin.Int), [OVAL](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#OVAL:kotlin.Int), [RECTANGLE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RECTANGLE:kotlin.Int) or [RING](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RING:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the type of shape used by this drawable Value is [android.graphics.drawable.GradientDrawable#RECTANGLE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RECTANGLE:kotlin.Int), [android.graphics.drawable.GradientDrawable#OVAL](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#OVAL:kotlin.Int), [android.graphics.drawable.GradientDrawable#LINE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINE:kotlin.Int), [android.graphics.drawable.GradientDrawable#RING](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RING:kotlin.Int), or [android.graphics.drawable.GradientDrawable#ARC](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#ARC:kotlin.Int) |

**See Also**

- [#setShape(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setShape(kotlin.Int)) 

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

- [#setThickness(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setThickness(kotlin.Int)) 

### getThicknessRatio

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThicknessRatio(): Float
```

Return the thickness ratio of the ring expressed as a ratio of the ring's width. 
**See Also**

- [#setThicknessRatio(float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setThicknessRatio(kotlin.Float)) 

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

- [#setUseLevel(boolean)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setUseLevel(kotlin.Boolean)) 

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasFocusStateSpecified(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if [android.R.attr#state_focused](https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int) is specified for this drawable. |

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
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): This value cannot be `null`. |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: This value may be `null`. |

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
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | This drawable. This value cannot be `null`. |

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

Changes this drawable to use a single color state list instead of a gradient. Calling this method with a null argument will clear the color and is equivalent to calling [setColor(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColor(kotlin.Int)) with the argument [Color.TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/Color.html#TRANSPARENT:kotlin.Int).

**Note** : changing color will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing the color.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorStateList` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?: The color state list used to fill the shape This value may be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#getColor](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getColor()) 

### setColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColor(argb: Int): Unit
```

Changes this drawable to use a single color instead of a gradient.

**Note** : changing color will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing the color.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `argb` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color used to fill the shape |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setColors(int[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColors(kotlin.IntArray))
- [#getColor](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getColor()) 

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### setColors

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColors(colors: IntArray?): Unit
```

Sets the colors used to draw the gradient.

Each color is specified as an ARGB integer and the array must contain at least 2 colors.

**Note** : changing colors will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing the colors.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: an array containing 2 or more ARGB colors This value may be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setColor(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setColor(kotlin.Int)) 

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

**Note** : changing colors will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing the colors.

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

Specifies radii for each of the 4 corners. For each corner, the array contains 2 values, `[X_radius, Y_radius]`. The corners are ordered top-left, top-right, bottom-right, bottom-left. This property is honored only when the shape is of type [RECTANGLE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RECTANGLE:kotlin.Int).

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `radii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: an array of length \>= 8 containing 4 pairs of X and Y radius for each corner, specified in pixels This value may be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setShape(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setShape(kotlin.Int))
- [#setCornerRadius(float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadius(kotlin.Float)) 

### setCornerRadius

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCornerRadius(radius: Float): Unit
```

Specifies the radius for the corners of the gradient. If this is \> 0, then the drawable is drawn in a round-rectangle, rather than a rectangle. This property is honored only when the shape is of type [RECTANGLE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RECTANGLE:kotlin.Int).

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The radius in pixels of the corners of the rectangle shape |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setCornerRadii(float[])](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setCornerRadii(kotlin.FloatArray))
- [#setShape(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setShape(kotlin.Int)) 

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

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the X-position of the center of the gradient |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the Y-position of the center of the gradient |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setGradientType(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientType(kotlin.Int))
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientCenterX()>
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientCenterY()> 

### setGradientRadius

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGradientRadius(gradientRadius: Float): Unit
```

Sets the radius of the gradient. The radius is honored only when the gradient type is set to [RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int).

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------|
| `gradientRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the radius of the gradient in pixels |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setGradientType(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientType(kotlin.Int))
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getGradientRadius()> 

### setGradientType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGradientType(gradient: Int): Unit
```

Sets the type of gradient used by this drawable.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gradient` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of the gradient: [LINEAR_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINEAR_GRADIENT:kotlin.Int), [RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int) or [SWEEP_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#SWEEP_GRADIENT:kotlin.Int) Value is [android.graphics.drawable.GradientDrawable#LINEAR_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINEAR_GRADIENT:kotlin.Int), [android.graphics.drawable.GradientDrawable#RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int), or [android.graphics.drawable.GradientDrawable#SWEEP_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#SWEEP_GRADIENT:kotlin.Int) |

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

**Note** : changing orientation will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing the orientation.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `orientation` | [GradientDrawable.Orientation](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable.Orientation)!: the desired orientation (angle) of the gradient |

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
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bottom padding of the gradient shape The units of this value are pixels. |

### setShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShape(shape: Int): Unit
```

Sets the type of shape used to draw the gradient.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shape` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired shape for this drawable: [LINE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINE:kotlin.Int), [OVAL](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#OVAL:kotlin.Int), [RECTANGLE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RECTANGLE:kotlin.Int) or [RING](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RING:kotlin.Int) Value is [android.graphics.drawable.GradientDrawable#RECTANGLE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RECTANGLE:kotlin.Int), [android.graphics.drawable.GradientDrawable#OVAL](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#OVAL:kotlin.Int), [android.graphics.drawable.GradientDrawable#LINE](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINE:kotlin.Int), [android.graphics.drawable.GradientDrawable#RING](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RING:kotlin.Int), or [android.graphics.drawable.GradientDrawable#ARC](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#ARC:kotlin.Int) |

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

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the shape used by this drawable |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the shape used by this drawable |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setGradientType(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setGradientType(kotlin.Int)) 

### setStroke

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStroke(
    width: Int, 
    colorStateList: ColorStateList!
): Unit
```

Set the stroke width and color state list for the drawable. If width is zero, then no stroke is drawn.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width in pixels of the stroke |
| `colorStateList` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)!: The color state list of the stroke |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setStroke(int, ColorStateList, float, float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setStroke(kotlin.Int,%20android.content.res.ColorStateList,%20kotlin.Float,%20kotlin.Float)) 

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

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width in pixels of the stroke |
| `colorStateList` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)!: The color state list of the stroke |
| `dashWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The length in pixels of the dashes, set to 0 to disable dashes |
| `dashGap` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The gap in pixels between dashes |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setStroke(int, ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setStroke(kotlin.Int,%20android.content.res.ColorStateList)) 

### setStroke

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStroke(
    width: Int, 
    color: Int
): Unit
```

Set the stroke width and color for the drawable. If width is zero, then no stroke is drawn.

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width in pixels of the stroke |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color of the stroke |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setStroke(int, int, float, float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setStroke(kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float)) 

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

**Note** : changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width in pixels of the stroke |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color of the stroke |
| `dashWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The length in pixels of the dashes, set to 0 to disable dashes |
| `dashGap` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The gap in pixels between dashes |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setStroke(int, int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#setStroke(kotlin.Int,%20kotlin.Int)) 

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

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter))

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)!: This value cannot be `null`. |

### setTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)).

**Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)) or [setColorFilter(int,android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)) overrides tint.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?: This value may be `null`. |

### setUseLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUseLevel(useLevel: Boolean): Unit
```

Sets whether this drawable's `level` property will be used to scale the gradient. If a gradient is not used, this property has no effect.

Scaling behavior varies based on gradient type:

- [LINEAR_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#LINEAR_GRADIENT:kotlin.Int) adjusts the ending position along the gradient's axis of orientation (see [getOrientation()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#getOrientation()))
- [RADIAL_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#RADIAL_GRADIENT:kotlin.Int) adjusts the outer radius
- [SWEEP_GRADIENT](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#SWEEP_GRADIENT:kotlin.Int) adjusts the ending angle
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
 - **Note** : Changing this property will affect all instances of a drawable loaded from a resource. It is recommended to invoke [mutate()](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()) before changing this property.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `useLevel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the gradient should be scaled based on level, `false` otherwise |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable#mutate()>
- [#setLevel(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int))
- [#getLevel()](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel())
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
