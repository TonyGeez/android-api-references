Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VectorDrawable

```
open class VectorDrawable : Drawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](Drawable.md) ||
| | ↳ | [android.graphics.drawable.VectorDrawable](VectorDrawable.md) |

This lets you create a drawable based on an XML vector graphic.

<br />

**Note:** To optimize for the re-drawing performance, one bitmap cache is created for each VectorDrawable. Therefore, referring to the same VectorDrawable means sharing the same bitmap cache. If these references don't agree upon on the same size, the bitmap will be recreated and redrawn every time size is changed. In other words, if a VectorDrawable is used for different sizes, it is more efficient to create multiple VectorDrawables, one for each size.

<br />

VectorDrawable can be defined in an XML file with the `<vector>` element.

<br />

The vector drawable has the following elements:

<br />

`<vector>`
: Used to define a vector drawable

 `android:name`
 : Defines the name of this vector drawable.

 `android:width`
 : Used to define the intrinsic width of the drawable. This supports all the dimension units, normally specified with dp.

 `android:height`
 : Used to define the intrinsic height of the drawable. This supports all the dimension units, normally specified with dp.

 `android:viewportWidth`
 : Used to define the width of the viewport space. Viewport is basically the virtual canvas where the paths are drawn on.

 `android:viewportHeight`
 : Used to define the height of the viewport space. Viewport is basically the virtual canvas where the paths are drawn on.

 `android:tint`
 : The color to apply to the drawable as a tint. By default, no tint is applied.

 `android:tintMode`
 : The Porter-Duff blending mode for the tint color. Default is src_in.

 `android:autoMirrored`
 : Indicates if the drawable needs to be mirrored when its layout direction is RTL (right-to-left). Default is false.

 `android:alpha`
 : The opacity of this drawable. Default is 1.0.

`<group>`
: Defines a group of paths or subgroups, plus transformation information. The transformations are defined in the same coordinates as the viewport. And the transformations are applied in the order of scale, rotate then translate.

 `android:name`
 : Defines the name of the group.

 `android:rotation`
 : The degrees of rotation of the group. Default is 0.

 `android:pivotX`
 : The X coordinate of the pivot for the scale and rotation of the group. This is defined in the viewport space. Default is 0.

 `android:pivotY`
 : The Y coordinate of the pivot for the scale and rotation of the group. This is defined in the viewport space. Default is 0.

 `android:scaleX`
 : The amount of scale on the X Coordinate. Default is 1.

 `android:scaleY`
 : The amount of scale on the Y coordinate. Default is 1.

 `android:translateX`
 : The amount of translation on the X coordinate. This is defined in the viewport space. Default is 0.

 `android:translateY`
 : The amount of translation on the Y coordinate. This is defined in the viewport space. Default is 0.

`<path>`
: Defines paths to be drawn.

 `android:name`
 : Defines the name of the path.

 `android:pathData`
 : Defines path data using exactly same format as "d" attribute in the SVG's path data. This is defined in the viewport space.

 `android:fillColor`
 : Specifies the color used to fill the path. May be a color or, for SDK 24+, a color state list or a gradient color (See `https://developer.android.com/reference/kotlin/android/R.styleable.html#GradientColor:kotlin.IntArray` and `https://developer.android.com/reference/kotlin/android/R.styleable.html#GradientColorItem:kotlin.IntArray`). If this property is animated, any value set by the animation will override the original value. No path fill is drawn if this property is not specified.

 `android:strokeColor`
 : Specifies the color used to draw the path outline. May be a color or, for SDK 24+, a color state list or a gradient color (See `https://developer.android.com/reference/kotlin/android/R.styleable.html#GradientColor:kotlin.IntArray` and `https://developer.android.com/reference/kotlin/android/R.styleable.html#GradientColorItem:kotlin.IntArray`). If this property is animated, any value set by the animation will override the original value. No path outline is drawn if this property is not specified.

 `android:strokeWidth`
 : The width a path stroke. Default is 0.

 `android:strokeAlpha`
 : The opacity of a path stroke. Default is 1.

 `android:fillAlpha`
 : The opacity to fill the path with. Default is 1.

 `android:trimPathStart`
 : The fraction of the path to trim from the start, in the range from 0 to 1. Default is 0.

 `android:trimPathEnd`
 : The fraction of the path to trim from the end, in the range from 0 to 1. Default is 1.

 `android:trimPathOffset`
 : Shift trim region (allows showed region to include the start and end), in the range from 0 to 1. Default is 0.

 `android:strokeLineCap`
 : Sets the linecap for a stroked path: butt, round, square. Default is butt.

 `android:strokeLineJoin`
 : Sets the lineJoin for a stroked path: miter,round,bevel. Default is miter.

 `android:strokeMiterLimit`
 : Sets the Miter limit for a stroked path. Default is 4.

 `android:fillType`
 : For SDK 24+, sets the fillType for a path. The types can be either "evenOdd" or "nonZero". They behave the same as SVG's "fill-rule" properties. Default is nonZero. For more details, see [FillRuleProperty](https://www.w3.org/TR/SVG/painting.html#FillRuleProperty)

`<clip-path>`
: Defines path to be the current clip. Note that the clip path only apply to the current group and its children.

 `android:name`
 : Defines the name of the clip path.
 : Animatable : No.

 `android:pathData`
 : Defines clip path using the same format as "d" attribute in the SVG's path data.
 : Animatable : Yes.

- Here is a simple VectorDrawable in this vectordrawable.xml file.

  ```kotlin
  <vector xmlns:android="http://schemas.android.com/apk/res/android"
        android:height="64dp"
        android:width="64dp"
        android:viewportHeight="600"
        android:viewportWidth="600" >
        <group
            android:name="rotationGroup"
            android:pivotX="300.0"
            android:pivotY="300.0"
            android:rotation="45.0" >
            <path
                android:name="v"
                android:fillColor="#000000"
                android:pathData="M300,70 l 0,-70 70,70 0,0 -70,70z" />
        </group>
    </vector>
    
  ```

#### Gradient support

We support 3 types of gradients: `https://developer.android.com/reference/kotlin/android/graphics/LinearGradient.html#`, `https://developer.android.com/reference/kotlin/android/graphics/RadialGradient.html#`, or `https://developer.android.com/reference/kotlin/android/graphics/SweepGradient.html#`. And we support all of 3 types of tile modes `https://developer.android.com/reference/kotlin/android/graphics/Shader.TileMode.html#`: CLAMP, REPEAT, MIRROR. All of the attributes are listed in `https://developer.android.com/reference/kotlin/android/R.styleable.html#GradientColor:kotlin.IntArray`. Note that different attributes are relevant for different types of gradient.

| LinearGradient | RadialGradient | SweepGradient |
|---|---|---|
| startColor | startColor | startColor |
| centerColor | centerColor | centerColor |
| endColor | endColor | endColor |
| --- | --- | --- |
| type | type | type |
| tileMode | tileMode | tileMode |
| startX | centerX | centerX |
| --- | --- | --- |
| startY | centerY | centerY |
| endX | gradientRadius | |
| endY | | |
| --- | --- | --- |

Also note that if any color item `https://developer.android.com/reference/kotlin/android/R.styleable.html#GradientColorItem:kotlin.IntArray` is defined, then startColor, centerColor and endColor will be ignored. See more details in `https://developer.android.com/reference/kotlin/android/R.styleable.html#GradientColor:kotlin.IntArray` and `https://developer.android.com/reference/kotlin/android/R.styleable.html#GradientColorItem:kotlin.IntArray`. Here is a simple example that defines a linear gradient.

```kotlin
<gradient xmlns:android="http://schemas.android.com/apk/res/android"
      android:startColor="?android:attr/colorPrimary"
      android:endColor="?android:attr/colorControlActivated"
      android:centerColor="#f00"
      android:startX="0"
      android:startY="0"
      android:endX="100"
      android:endY="100"
      android:type="linear">
  </gradient>
  
```
And here is a simple example that defines a radial gradient using color items.

```kotlin
<gradient xmlns:android="http://schemas.android.com/apk/res/android"
      android:centerX="300"
      android:centerY="300"
      android:gradientRadius="100"
      android:type="radial">
      <item android:offset="0.1" android:color="#0ff"/>
      <item android:offset="0.4" android:color="#fff"/>
      <item android:offset="0.9" android:color="#ff0"/>
  </gradient>
  
```

## Summary

| Public constructors ||
|---|---|
| VectorDrawable <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | applyTheme Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canApplyTheme <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | draw Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAlpha Gets the current alpha value for the drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getChangingConfigurations Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| open [ColorFilter](../android.graphics/ColorFilter.md)? | getColorFilter Returns the current color filter, or `null` if none set. |
| --- | --- |
| open [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | getConstantState Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getIntrinsicHeight Returns the drawable's intrinsic height. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getIntrinsicWidth Returns the drawable's intrinsic width. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOpacity Return the opacity/transparency of this Drawable. |
| open [Insets](../android.graphics/Insets.md) | getOpticalInsets Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasFocusStateSpecified Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | inflate Inflate this Drawable from an XML resource optionally styled by a theme. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAutoMirrored Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isStateful Indicates whether this drawable will change its appearance based on state. |
| --- | --- |
| open [Drawable](Drawable.md) | mutate Make this drawable mutable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAlpha Specify an alpha value for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAutoMirrored Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColorFilter Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTintBlendMode Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTintList Specifies tint color for this drawable as a color state list. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onStateChange Override this in your subclass to change appearance if you recognize the specified state. |

| Inherited functions ||
|---|---|
| From class Drawable |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | clearColorFilter Removes the color filter for this drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | copyBounds Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | copyBounds Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | Drawable | createFromPath Create a drawable from file path name. <br /> | | Drawable | createFromResourceStream Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | Drawable | createFromResourceStream Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | Drawable | createFromStream Create a drawable from an inputstream <br /> | | Drawable | createFromXml Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | Drawable | createFromXml Create a drawable from an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | Drawable | createFromXmlInner Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | Drawable | createFromXmlInner Create a drawable from inside an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | getBounds Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?` | getCallback Return the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation attached to this Drawable. <br /> | | Drawable | getCurrent <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | getDirtyBounds Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | getHotspotBounds Populates `outRect` with the hotspot bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getLayoutDirection Returns the resolved layout direction for this Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getLevel Retrieve the current level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMinimumHeight Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMinimumWidth Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | getOutline Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#` to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getPadding Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | getState Describes the current state, as a union of primitive states, such as `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int`, etc. Some drawables may modify their imagery based on the selected state. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Region.html#?` | getTransparentRegion Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | inflate Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invalidateSelf Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isFilterBitmap <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isProjected Whether this drawable requests projection. Indicates that the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#` this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isVisible <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | jumpToCurrentState If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onBoundsChange Override this in your subclass to change appearance if you vary based on the bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onLayoutDirectionChanged Called when the drawable's resolved layout direction changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onLevelChange Override this in your subclass to change appearance if you vary based on level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | resolveOpacity Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing getOpacity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | scheduleSelf Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setBounds Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setBounds Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setCallback Bind a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` object to this Drawable. Required for clients that want to support animated drawables. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setChangingConfigurations Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setColorFilter Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for setColorFilter which constructs a `https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#`. **Note:** Setting a color filter disables setTintList. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDither Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFilterBitmap Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setHotspot Specifies the hotspot's location within the drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setHotspotBounds Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | setLayoutDirection Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | setLevel Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling invalidateSelf in order to have itself redrawn, *and* true will be returned from this function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | setState Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \[`https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int`\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling invalidateSelf in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTint Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to setColorFilter. To clear the tint, pass `null` to setTintList. **Note:** Setting a color filter via setColorFilter or setColorFilter overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTintMode Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`. **Note:** Setting a color filter via setColorFilter or setColorFilter overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | setVisible Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unscheduleSelf Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## Public constructors

### VectorDrawable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
VectorDrawable()
```

## Public methods

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|---|---|
| `t` | [Resources.Theme](../android/content/res/Resources.Theme.md): the theme to apply. This value cannot be `null`. |

### canApplyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canApplyTheme(): Boolean
```

### draw

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun draw(canvas: Canvas): Unit
```

Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter).

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md): The canvas to draw into. This value cannot be `null`. |

### getAlpha

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlpha(): Int
```

Gets the current alpha value for the drawable. 0 means fully transparent, 255 means fully opaque. This method is implemented by Drawable subclasses and the value returned is specific to how that class treats alpha. The default return value is 255 if the class does not override this method to return a value specific to its use of alpha.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 0 and 255 inclusive |

### getChangingConfigurations

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChangingConfigurations(): Int
```

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through setChangingConfigurations or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int` |

### getColorFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColorFilter(): ColorFilter?
```

Returns the current color filter, or `null` if none set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?` | the current color filter, or `null` if none set |

### getConstantState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConstantState(): Drawable.ConstantState?
```

Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState?` | The ConstantState associated to that Drawable. This value may be `null`. |

### getIntrinsicHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntrinsicHeight(): Int
```

Returns the drawable's intrinsic height.

Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the intrinsic height, or -1 if no intrinsic height |

### getIntrinsicWidth

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntrinsicWidth(): Int
```

Returns the drawable's intrinsic width.

Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the intrinsic width, or -1 if no intrinsic width |

### getOpacity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpacity(): Int
```

Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`: `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int`.

An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT.

Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method resolveOpacity to perform a standard reduction of two opacities to the appropriate single output.

Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the setAlpha or #setColorFilter methods. Some subclasses, such as BitmapDrawable, ColorDrawable, and GradientDrawable, do account for the value of setAlpha, but the general behavior is dependent upon the implementation of the subclass.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int The opacity class of the Drawable. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int` |

### getOpticalInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpticalInsets(): Insets
```

Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Insets.html#` | This value cannot be `null`. |

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFocusStateSpecified(): Boolean
```

Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`.

Note: A View uses a Drawable instance as its background and it changes its appearance based on a state. On keyboard devices, it should specify its `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` to make sure the user knows which view is holding the focus.

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
| `r` | [Resources](../android.content.res/Resources.md): This value cannot be `null`. |
| `parser` | [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md): This value cannot be `null`. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md): This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |
| `org.xmlpull.v1.XmlPullParserException` | |

### isAutoMirrored

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAutoMirrored(): Boolean
```

Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean Returns true if this Drawable will be automatically mirrored. |

### isStateful

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStateful(): Boolean
```

Indicates whether this drawable will change its appearance based on state. Clients can use this to determine whether it is necessary to calculate their state and call setState.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this drawable changes its appearance based on state, false otherwise. |

### mutate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mutate(): Drawable
```

Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect.

| Return ||
|---|---|
| Drawable | This drawable. This value cannot be `null`. |

### setAlpha

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAlpha(alpha: Int): Unit
```

Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque.

| Parameters ||
|---|---|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is between 0 and 255 inclusive |

### setAutoMirrored

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutoMirrored(mirrored: Boolean): Unit
```

Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`.

| Parameters ||
|---|---|
| `mirrored` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if the Drawable should be mirrored, false if not. |

### setColorFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorFilter(colorFilter: ColorFilter?): Unit
```

Specify an optional color filter for the drawable.

If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas.

Pass `null` to remove any existing color filter.

**Note:** Setting a non-`null` color filter disables setTintList.

| Parameters ||
|---|---|
| `colorFilter` | [ColorFilter](../android.graphics/ColorFilter.md)?: The color filter to apply, or `null` to remove the existing color filter |

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintBlendMode(blendMode: BlendMode!): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

**Note:** Setting a color filter via setColorFilter

| Parameters ||
|---|---|
| `blendMode` | [BlendMode](../android.graphics/BlendMode.md)!: This value cannot be `null`. |

### setTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to setColorFilter.

**Note:** Setting a color filter via setColorFilter or setColorFilter overrides tint.

| Parameters ||
|---|---|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?: Color state list to use for tinting this drawable, or `null` to clear the tint |

## Protected methods

### onStateChange

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onStateChange(stateSet: IntArray): Boolean
```

Override this in your subclass to change appearance if you recognize the specified state.

| Parameters ||
|---|---|
| `state` | This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |
