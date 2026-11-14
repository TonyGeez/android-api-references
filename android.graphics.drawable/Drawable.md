Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Drawable

```
abstract class Drawable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#) |

| Known Direct Subclasses [AdaptiveIconDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable), [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable), [AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable), [BitmapDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable), [ColorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable), [ColorStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable), [DrawableContainer](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer), [DrawableWrapper](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableWrapper), [GradientDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable), [LayerDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable), [NinePatchDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable), [PictureDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/PictureDrawable), and 2 others. |---|---| | [AdaptiveIconDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable) | This class can also be created via XML inflation using `<adaptive-icon>` tag in addition to dynamic creation. | | [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#` for drawing animated images (like GIF). | | [AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable) | This class animates properties of a `https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable` with animations defined using `https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator.html#` or `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.html#`. | | [BitmapDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable) | A Drawable that wraps a bitmap and can be tiled, stretched, or aligned. | | [ColorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable) | A specialized Drawable that fills the Canvas with a specified color. | | [ColorStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable) | A Drawable that manages a `https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable` to make it stateful and backed by a `https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#`. | | [DrawableContainer](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer) | A helper class that contains several `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#`s and selects which one to use. | | [DrawableWrapper](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableWrapper) | Drawable container with only one child element. | | [GradientDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable) | A Drawable with a color gradient for buttons, backgrounds, etc. | | [LayerDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable) | A Drawable that manages an array of other Drawables. | | [NinePatchDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable) | A resizeable bitmap, with stretchable areas that you define. | | [PictureDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/PictureDrawable) | Drawable subclass that wraps a Picture, allowing the picture to be used wherever a Drawable is supported. | | [ShapeDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ShapeDrawable) | A Drawable object that draws primitive shapes. | | [VectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable) | This lets you create a drawable based on an XML vector graphic. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AnimatedStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedStateListDrawable), [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable), [ClipDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ClipDrawable), [InsetDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/InsetDrawable), [LevelListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/LevelListDrawable), [PaintDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/PaintDrawable), [RippleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable), [RotateDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/RotateDrawable), [ScaleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ScaleDrawable), [StateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable), [TransitionDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/TransitionDrawable) |---|---| | [AnimatedStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedStateListDrawable) | Drawable containing a set of Drawable keyframes where the currently displayed keyframe is chosen based on the current state set. | | [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable) | An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background. | | [ClipDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ClipDrawable) | A Drawable that clips another Drawable based on this Drawable's current level value. | | [InsetDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/InsetDrawable) | A Drawable that insets another Drawable by a specified distance or fraction of the content bounds. | | [LevelListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/LevelListDrawable) | A resource that manages a number of alternate Drawables, each assigned a maximum numerical value. | | [PaintDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/PaintDrawable) | Drawable that draws its bounds in the given paint, with optional rounded corners. | | [RippleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable) | Drawable that shows a ripple effect in response to state changes. | | [RotateDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/RotateDrawable) | A Drawable that can rotate another Drawable based on the current level value. | | [ScaleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ScaleDrawable) | A Drawable that changes the size of another Drawable based on its current level value. | | [StateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable) | Lets you assign a number of graphic images to a single Drawable and swap out the visible item by a string ID value. | | [TransitionDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/TransitionDrawable) | An extension of LayerDrawables that is intended to cross-fade between the first and second layer. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Drawable is a general abstraction for "something that can be drawn." Most often you will deal with Drawable as the type of resource retrieved for drawing things to the screen; the Drawable class provides a generic API for dealing with an underlying visual resource that may take a variety of forms. Unlike a `https://developer.android.com/reference/kotlin/android/view/View.html#`, a Drawable does not have any facility to receive events or otherwise interact with the user.

In addition to simple drawing, Drawable provides a number of generic mechanisms for its client to interact with what is being drawn:

- The #setBounds method must be called to tell the Drawable where it is drawn and how large it should be. All Drawables should respect the requested size, often simply by scaling their imagery. A client can find the preferred size for some Drawables with the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getIntrinsicHeight()` and `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getIntrinsicWidth()` methods.
- The `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getPadding(android.graphics.Rect)` method can return from some Drawables information about how to frame content that is placed inside of them. For example, a Drawable that is intended to be the frame for a button widget would need to return padding that correctly places the label inside of itself.
- The `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray)` method allows the client to tell the Drawable in which state it is to be drawn, such as "focused", "selected", etc. Some drawables may modify their imagery based on the selected state.
- The `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int)` method allows the client to supply a single continuous controller that can modify the Drawable is displayed, such as a battery level or progress level. Some drawables may modify their imagery based on the current level.
- A Drawable can perform animations by calling back to its client through the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` interface. All clients should support this interface (via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback)`) so that animations will work. A simple way to do this is through the system facilities such as `https://developer.android.com/reference/kotlin/android/view/View.html#setBackground(android.graphics.drawable.Drawable)` and `https://developer.android.com/reference/kotlin/android/widget/ImageView.html#`.

Though usually not visible to the application, Drawables may take a variety of forms:

<!-- -->

- **Bitmap**: the simplest Drawable, a PNG or JPEG image.
- **Nine Patch**: an extension to the PNG format allows it to specify information about how to stretch it and place things inside of it.
- **Vector**: a drawable defined in an XML file as a set of points, lines, and curves along with its associated color information. This type of drawable can be scaled without loss of display quality.
- **Shape**: contains simple drawing commands instead of a raw bitmap, allowing it to resize better in some cases.
- **Layers**: a compound drawable, which draws multiple underlying drawables on top of each other.
- **States**: a compound drawable that selects one of a set of drawables based on its state.
- **Levels**: a compound drawable that selects one of a set of drawables based on its level.
- **Scale**: a compound drawable with a single child drawable, whose overall size is modified based on the current level.

### Custom drawables

All versions of Android allow the Drawable class to be extended and used at run time in place of framework-provided drawable classes. Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, custom drawables classes may also be used in XML.

**Note:** Custom drawable classes are only accessible from within your application package. Other applications will not be able to load them.

At a minimum, custom drawable classes must implement the abstract methods on Drawable and should override the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#draw(android.graphics.Canvas)` method to draw content.

Custom drawables classes may be used in XML in multiple ways:

- Using the fully-qualified class name as the XML element name. For this method, the custom drawable class must be a public top-level class.

  ```kotlin
  <com.myapp.MyCustomDrawable xmlns:android="http://schemas.android.com/apk/res/android"
        android:color="#ffff0000" />
    
  ```
- Using *drawable* as the XML element name and specifying the fully-qualified class name from the *class* attribute. This method may be used for both public top-level classes and public static inner classes.

  ```kotlin
  <drawable xmlns:android="http://schemas.android.com/apk/res/android"
        class="com.myapp.MyTopLevelClass$InnerCustomDrawable"
        android:color="#ffff0000" />
    
  ```

> [!NOTE]
>
> ### Developer Guides
>
> For more information about how to use drawables, read the [Canvas and Drawables](https://developer.android.com/guide/topics/graphics/2d-graphics.html) developer guide. For information and examples of creating drawable resources (XML or bitmap files that can be loaded in code), read the [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html) document.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` Implement this interface if you want to create an animated drawable that extends `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#`. |
| abstract | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` This abstract class is used by `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#`s to store shared constant state and data between Drawables. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#Drawable()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#applyTheme(android.content.res.Resources.Theme)(t: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#canApplyTheme()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter()()` Removes the color filter for this drawable. |
| --- | --- |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds()()` Return a copy of the drawable's bounds in a new Rect. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). |
| open static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String)(pathName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Create a drawable from file path name. |
| --- | --- |
| open static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#?, value: https://developer.android.com/reference/kotlin/android/util/TypedValue.html#?, is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Create a drawable from an inputstream, using the given resources and value to determine density information. |
| open static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#?, value: https://developer.android.com/reference/kotlin/android/util/TypedValue.html#?, is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, opts: https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#?)` Create a drawable from an inputstream, using the given resources and value to determine density information. |
| open static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String)(is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Create a drawable from an inputstream |
| --- | --- |
| open static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)` Create a drawable from an XML document. |
| open static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Create a drawable from an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. |
| open static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)` Create from inside an XML document. |
| --- | --- |
| open static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Create a drawable from inside an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#draw(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)` Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getAlpha()()` Gets the current alpha value for the drawable. |
| --- | --- |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds()()` Return the drawable's bounds Rect. |
| open [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback()()` Return the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation attached to this Drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getChangingConfigurations()()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| --- | --- |
| open [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getColorFilter()()` Returns the current color filter, or `null` if none set. |
| open [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getConstantState()()` Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCurrent()()` <br /> |
| --- | --- |
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds()()` Return the drawable's dirty bounds Rect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getHotspotBounds(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Populates `outRect` with the hotspot bounds. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getIntrinsicHeight()()` Returns the drawable's intrinsic height. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getIntrinsicWidth()()` Returns the drawable's intrinsic width. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection()()` Returns the resolved layout direction for this Drawable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel()()` Retrieve the current level. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumHeight()()` Returns the minimum height suggested by this Drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumWidth()()` Returns the minimum width suggested by this Drawable. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()()` Return the opacity/transparency of this Drawable. |
| --- | --- |
| open [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpticalInsets()()` Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOutline(android.graphics.Outline)(outline: https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)` Called to get the drawable to populate the Outline that defines its drawing area. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getPadding(android.graphics.Rect)(padding: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState()()` Describes the current state, as a union of primitive states, such as `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int`, etc. |
| open [Region](https://developer.android.com/reference/kotlin/android/graphics/Region.html#)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getTransparentRegion()()` Returns a Region representing the part of the Drawable that is completely transparent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#hasFocusStateSpecified()()` Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)` Inflate this Drawable from an XML resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Inflate this Drawable from an XML resource optionally styled by a theme. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()()` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isAutoMirrored()()` Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isFilterBitmap()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isProjected()()` Whether this drawable requests projection. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isStateful()()` Indicates whether this drawable will change its appearance based on state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#jumpToCurrentState()()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. |
| --- | --- |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#mutate()()` Make this drawable mutable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onLayoutDirectionChanged(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the drawable's resolved layout direction changes. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)(op1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, op2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the appropriate opacity value for two source opacities. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long)(what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable scheduled. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify an alpha value for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAutoMirrored(kotlin.Boolean)(mirrored: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Specify a bounding rectangle for the Drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify a bounding rectangle for the Drawable. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback)(cb: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?)` Bind a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` object to this Drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)(configs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)(colorFilter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?)` Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)` Specify a color and Porter-Duff mode to be the color filter for this drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setDither(kotlin.Boolean)(dither: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setFilterBitmap(kotlin.Boolean)(filter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspot(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Specifies the hotspot's location within the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the layout direction for this drawable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify the level for the drawable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray)(stateSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Specify a set of states for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int)(tintColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies tint color for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintBlendMode(android.graphics.BlendMode)(blendMode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?)` Specifies a tint blending mode for this drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)(tint: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?)` Specifies tint color for this drawable as a color state list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode)(tintMode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?)` Specifies a tint blending mode for this drawable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setVisible(kotlin.Boolean,%20kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, restart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is visible. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable)(what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable unscheduled. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onBoundsChange(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Override this in your subclass to change appearance if you vary based on the bounds. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onLevelChange(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Override this in your subclass to change appearance if you vary based on level. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#onStateChange(kotlin.IntArray)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Override this in your subclass to change appearance if you recognize the specified state. |
| --- | --- |

## Public constructors

### Drawable

```
Drawable()
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
| `t` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#): the theme to apply. This value cannot be `null`. |

### canApplyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canApplyTheme(): Boolean
```

### clearColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearColorFilter(): Unit
```

Removes the color filter for this drawable.

### copyBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copyBounds(): Rect
```

Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | A copy of the drawable's bounds. This value cannot be `null`. |

### copyBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copyBounds(bounds: Rect): Unit
```

Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called.

| Parameters ||
|---|---|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): Rect to receive the drawable's bounds (allocated by the caller). This value cannot be `null`. |

### createFromPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromPath(pathName: String!): Drawable?
```

Create a drawable from file path name.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#?` | This value may be `null`. |

### createFromResourceStream

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromResourceStream(
    res: Resources?, 
    value: TypedValue?, 
    is: InputStream?, 
    srcName: String?
): Drawable?
```

Create a drawable from an inputstream, using the given resources and value to determine density information.

| Parameters ||
|---|---|
| `res` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?: This value may be `null`. |
| `value` | [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?: This value may be `null`. |
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?: This value may be `null`. |
| --- | --- |
| `srcName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#?` | This value may be `null`. |

### createFromResourceStream

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromResourceStream(
    res: Resources?, 
    value: TypedValue?, 
    is: InputStream?, 
    srcName: String?, 
    opts: BitmapFactory.Options?
): Drawable?
```

**Deprecated:** *Prefer the version without an Options object.*

Create a drawable from an inputstream, using the given resources and value to determine density information.

| Parameters ||
|---|---|
| `res` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)?: This value may be `null`. |
| `value` | [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)?: This value may be `null`. |
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?: This value may be `null`. |
| --- | --- |
| `srcName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `opts` | [BitmapFactory.Options](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#?` | This value may be `null`. |

### createFromStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromStream(
    is: InputStream?, 
    srcName: String?
): Drawable?
```

Create a drawable from an inputstream

| Parameters ||
|---|---|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)?: This value may be `null`. |
| `srcName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#?` | This value may be `null`. |

### createFromXml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromXml(
    r: Resources, 
    parser: XmlPullParser
): Drawable
```

Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

| Parameters ||
|---|---|
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#` | This value cannot be `null`. |

### createFromXml

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromXml(
    r: Resources, 
    parser: XmlPullParser, 
    theme: Resources.Theme?
): Drawable
```

Create a drawable from an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html).

| Parameters ||
|---|---|
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): This value cannot be `null`. |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#` | This value cannot be `null`. |

### createFromXmlInner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromXmlInner(
    r: Resources, 
    parser: XmlPullParser, 
    attrs: AttributeSet
): Drawable
```

Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable.

| Parameters ||
|---|---|
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): This value cannot be `null`. |
| --- | --- |

### createFromXmlInner

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromXmlInner(
    r: Resources, 
    parser: XmlPullParser, 
    attrs: AttributeSet, 
    theme: Resources.Theme?
): Drawable
```

Create a drawable from inside an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable.

| Parameters ||
|---|---|
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: This value may be `null`. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun draw(canvas: Canvas): Unit
```

Draw in its bounds (set via setBounds) respecting optional effects such as alpha (set via setAlpha) and color filter (set via setColorFilter).

| Parameters ||
|---|---|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): The canvas to draw into. This value cannot be `null`. |

### getAlpha

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlpha(): Int
```

Gets the current alpha value for the drawable. 0 means fully transparent, 255 means fully opaque. This method is implemented by Drawable subclasses and the value returned is specific to how that class treats alpha. The default return value is 255 if the class does not override this method to return a value specific to its use of alpha.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 0 and 255 inclusive |

### getBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBounds(): Rect
```

Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | The bounds of the drawable (which may change later, so caller beware). DO NOT ALTER the returned object as it may change the stored bounds of this drawable. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds()`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect)`

### getCallback

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCallback(): Drawable.Callback?
```

Return the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation attached to this Drawable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?` | A `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` instance or null if no callback was set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback)`

### getChangingConfigurations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChangingConfigurations(): Int
```

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)` or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns a mask of the changing configuration parameters, as defined by `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#`

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConstantState(): Drawable.ConstantState?
```

Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState?` | The ConstantState associated to that Drawable. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#mutate()`

### getCurrent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrent(): Drawable
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#` | The current drawable that will be used by this drawable. For simple drawables, this is just the drawable itself. For drawables that change state like `https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable` and `https://developer.android.com/reference/kotlin/android/graphics/drawable/LevelListDrawable` this will be the child drawable currently in use. This value cannot be `null`. |

### getDirtyBounds

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDirtyBounds(): Rect
```

Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed).

By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | The dirty bounds of this drawable. This value cannot be `null`. |

### getHotspotBounds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHotspotBounds(outRect: Rect): Unit
```

Populates `outRect` with the hotspot bounds.

| Parameters ||
|---|---|
| `outRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): the rect to populate with the hotspot bounds. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### getIntrinsicHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntrinsicHeight(): Int
```

Returns the drawable's intrinsic height.

Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the intrinsic height, or -1 if no intrinsic height |

### getIntrinsicWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntrinsicWidth(): Int
```

Returns the drawable's intrinsic width.

Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the intrinsic width, or -1 if no intrinsic width |

### getLayoutDirection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutDirection(): Int
```

Returns the resolved layout direction for this Drawable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int)`

### getLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLevel(): Int
```

Retrieve the current level.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int Current level, from 0 (minimum) to 10000 (maximum). Value is between 0 and 10000 inclusive |

### getMinimumHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumHeight(): Int
```

Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The minimum height suggested by this Drawable. If this Drawable doesn't have a suggested minimum height, 0 is returned. |

### getMinimumWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumWidth(): Int
```

Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The minimum width suggested by this Drawable. If this Drawable doesn't have a suggested minimum width, 0 is returned. |

### getOpacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getOpacity(): Int
```

**Deprecated:** *This method is no longer used in graphics optimizations*

Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`: `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int`.

An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT.

Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)` to perform a standard reduction of two opacities to the appropriate single output.

Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)` or #setColorFilter methods. Some subclasses, such as `https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable`, `https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable`, and `https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable`, do account for the value of `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)`, but the general behavior is dependent upon the implementation of the subclass.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int The opacity class of the Drawable. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### getOpticalInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpticalInsets(): Insets
```

Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Insets.html#` | This value cannot be `null`. |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOutline(outline: Outline): Unit
```

Called to get the drawable to populate the Outline that defines its drawing area.

This method is called by the default `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#` to define the outline of the View.

The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method.

| Parameters ||
|---|---|
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setOutlineProvider(android.view.ViewOutlineProvider)`

### getPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPadding(padding: Rect): Boolean
```

Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset).

| Parameters ||
|---|---|
| `padding` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this drawable actually has a padding, else false. When false is returned, the padding is always set to 0. |

### getState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getState(): IntArray
```

Describes the current state, as a union of primitive states, such as `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int`, etc. Some drawables may modify their imagery based on the selected state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array of resource Ids describing the current state. This value cannot be `null`. |

### getTransparentRegion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransparentRegion(): Region?
```

Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Region.html#?` | Returns null if the Drawables has no transparent region to report, else a Region holding the parts of the Drawable's bounds that are transparent. |

### hasFocusStateSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFocusStateSpecified(): Boolean
```

Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`.

Note: A View uses a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#` instance as its background and it changes its appearance based on a state. On keyboard devices, it should specify its `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` to make sure the user knows which view is holding the focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` is specified for this drawable. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun inflate(
    r: Resources, 
    parser: XmlPullParser, 
    attrs: AttributeSet
): Unit
```

Inflate this Drawable from an XML resource. Does not apply a theme.

| Parameters ||
|---|---|
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): This value cannot be `null`. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)`

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
| `r` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): Resources used to resolve attribute values. This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): XML parser from which to inflate this Drawable. This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): Base set of attribute values. This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: Theme to apply, may be null |

| Exceptions ||
|---|---|
| `java.io.IOException` | |
| `org.xmlpull.v1.XmlPullParserException` | |

### invalidateSelf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateSelf(): Unit
```

Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#invalidateDrawable(android.graphics.drawable.Drawable)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback()`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback)`

### isAutoMirrored

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAutoMirrored(): Boolean
```

Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean Returns true if this Drawable will be automatically mirrored. |

### isFilterBitmap

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFilterBitmap(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this drawable filters its bitmaps |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setFilterBitmap(kotlin.Boolean)`

### isProjected

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isProjected(): Boolean
```

Whether this drawable requests projection. Indicates that the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#` this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#setProjectBackwards(kotlin.Boolean)`

### isStateful

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStateful(): Boolean
```

Indicates whether this drawable will change its appearance based on state. Clients can use this to determine whether it is necessary to calculate their state and call setState.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this drawable changes its appearance based on state, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray)`

### isVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isVisible(): Boolean
```

### jumpToCurrentState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun jumpToCurrentState(): Unit
```

If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations.

### mutate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mutate(): Drawable
```

Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#` | This drawable. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getConstantState()`

### onLayoutDirectionChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onLayoutDirectionChanged(layoutDirection: Int): Boolean
```

Called when the drawable's resolved layout direction changes.

| Parameters ||
|---|---|
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new resolved layout direction. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the layout direction change has caused the appearance of the drawable to change such that it needs to be re-drawn, `false` otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int)`

### resolveOpacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun resolveOpacity(
    op1: Int, 
    op2: Int
): Int
```

Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned.

This is to help in implementing `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()`.

| Parameters ||
|---|---|
| `op1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One opacity value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int` |
| `op2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Another opacity value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int The combined opacity value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()`

### scheduleSelf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scheduleSelf(
    what: Runnable, 
    when: Long
): Unit
```

Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable.

| Parameters ||
|---|---|
| `what` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): The action being scheduled. This value cannot be `null`. |
| `when` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in milliseconds) to run. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#scheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable,%20kotlin.Long)`

### setAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setAlpha(alpha: Int): Unit
```

Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque.

| Parameters ||
|---|---|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is between 0 and 255 inclusive |

### setAutoMirrored

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutoMirrored(mirrored: Boolean): Unit
```

Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`.

| Parameters ||
|---|---|
| `mirrored` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if the Drawable should be mirrored, false if not. |

### setBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBounds(bounds: Rect): Unit
```

Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called.

| Parameters ||
|---|---|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): This value cannot be `null`. |

### setBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBounds(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called.

### setCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCallback(cb: Drawable.Callback?): Unit
```

Bind a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` object to this Drawable. Required for clients that want to support animated drawables.

| Parameters ||
|---|---|
| `cb` | [Drawable.Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback)?: The client's Callback implementation. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback()`

### setChangingConfigurations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChangingConfigurations(configs: Int): Unit
```

Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created.

| Parameters ||
|---|---|
| `configs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A mask of the changing configuration parameters, as defined by `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#`

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setColorFilter(colorFilter: ColorFilter?): Unit
```

Specify an optional color filter for the drawable.

If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas.

Pass `null` to remove any existing color filter.

**Note:** Setting a non-`null` color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`.

| Parameters ||
|---|---|
| `colorFilter` | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?: The color filter to apply, or `null` to remove the existing color filter |

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorFilter(
    color: Int, 
    mode: PorterDuff.Mode
): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` with an instance of `https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter.html#`*

Specify a color and Porter-Duff mode to be the color filter for this drawable.

Convenience for `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` which constructs a `https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#`.

**Note:** Setting a color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`.

| Parameters ||
|---|---|
| `mode` | [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)`

### setDither

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDither(dither: Boolean): Unit
```

Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setDither(kotlin.Boolean)`

### setFilterBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFilterBitmap(filter: Boolean): Unit
```

Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated.

This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isFilterBitmap()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFilterBitmap(kotlin.Boolean)`

### setHotspot

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHotspot(
    x: Float, 
    y: Float
): Unit
```

Specifies the hotspot's location within the drawable.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X coordinate of the center of the hotspot |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y coordinate of the center of the hotspot |

### setHotspotBounds

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHotspotBounds(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the left bound |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the top bound |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the right bound |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the bottom bound |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getHotspotBounds(android.graphics.Rect)`

### setLayoutDirection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLayoutDirection(layoutDirection: Int): Boolean
```

Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own.

| Parameters ||
|---|---|
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the resolved layout direction for the drawable, either `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the layout direction change has caused the appearance of the drawable to change such that it needs to be re-drawn, `false` otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection()`

### setLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLevel(level: Int): Boolean
```

Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level.

If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()` in order to have itself redrawn, *and* true will be returned from this function.

| Parameters ||
|---|---|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new level, from 0 (minimum) to 10000 (maximum). Value is between 0 and 10000 inclusive |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if this change in level has caused the appearance of the Drawable to change (hence requiring an invalidate), otherwise returns false. |

### setState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setState(stateSet: IntArray): Boolean
```

Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \[`https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int`\].

If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()` in order to have itself redrawn, *and* true will be returned from this function.

Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time.

| Parameters ||
|---|---|
| `stateSet` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): The new set of states to be displayed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if this change in state has caused the appearance of the Drawable to change (hence requiring an invalidate), otherwise returns false. |

### setTint

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTint(tintColor: Int): Unit
```

Specifies tint color for this drawable.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`.

To clear the tint, pass `null` to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint.

| Parameters ||
|---|---|
| `tintColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Color to use for tinting this drawable |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintBlendMode(android.graphics.BlendMode)`

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintBlendMode(blendMode: BlendMode?): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)`

| Parameters ||
|---|---|
| `blendMode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)?: BlendMode to apply to the drawable, a value of null sets the default blend mode value of `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`

### setTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint.

| Parameters ||
|---|---|
| `tint` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?: Color state list to use for tinting this drawable, or `null` to clear the tint |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintBlendMode(android.graphics.BlendMode)`

### setTintMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintMode(tintMode: PorterDuff.Mode?): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint.

| Parameters ||
|---|---|
| `tintMode` | [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)?: A Porter-Duff blending mode to apply to the drawable, a value of null sets the default Porter-Diff blending mode value of `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`

### setVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVisible(
    visible: Boolean, 
    restart: Boolean
): Boolean
```

Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations.

| Parameters ||
|---|---|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if visible, false if not. |
| `restart` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): You can supply true here to force the drawable to behave as if it has just become visible, even if it had last been set visible. Used for example to force animations to restart. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean Returns true if the new visibility is different than its previous state. |

### unscheduleSelf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unscheduleSelf(what: Runnable): Unit
```

Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable.

| Parameters ||
|---|---|
| `what` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): The runnable that you no longer want called. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback#unscheduleDrawable(android.graphics.drawable.Drawable,%20java.lang.Runnable)`

## Protected methods

### onBoundsChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

Override this in your subclass to change appearance if you vary based on the bounds.

| Parameters ||
|---|---|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): This value cannot be `null`. |

### onLevelChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onLevelChange(level: Int): Boolean
```

Override this in your subclass to change appearance if you vary based on level.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the level change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last level. |

### onStateChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onStateChange(state: IntArray): Boolean
```

Override this in your subclass to change appearance if you recognize the specified state.

| Parameters ||
|---|---|
| `state` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |
