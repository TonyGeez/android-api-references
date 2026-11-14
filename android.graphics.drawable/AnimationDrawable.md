# AnimationDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimationDrawable

Kotlin| [Java](AnimationDrawable.md) 
| --- | --- |

```
open class AnimationDrawable : DrawableContainer, Animatable, Runnable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](Drawable.md) |||
| | ↳ | [android.graphics.drawable.DrawableContainer](DrawableContainer.md) ||
| | | ↳ | [android.graphics.drawable.AnimationDrawable](AnimationDrawable.md) |
| --- | --- | --- | --- |

An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background.

The simplest way to create a frame-by-frame animation is to define the animation in an XML file, placed in the res/drawable/ folder, and set it as the background to a View object. Then, call [start()](AnimationDrawable.md))to run the animation.

An AnimationDrawable defined in XML consists of a single`<animation-list>`element and a series of nested`<item>`tags. Each item defines a frame of the animation. See the example below.

spin_animation.xml file in res/drawable/ folder: 

```kotlin
<!-- Animation frames are wheel0.png through wheel5.png
      files inside the res/drawable/ folder -->
  <animation-list android:id="@+id/selected" android:oneshot="false">
     <item android:drawable="@drawable/wheel0" android:duration="50" />
     <item android:drawable="@drawable/wheel1" android:duration="50" />
     <item android:drawable="@drawable/wheel2" android:duration="50" />
     <item android:drawable="@drawable/wheel3" android:duration="50" />
     <item android:drawable="@drawable/wheel4" android:duration="50" />
     <item android:drawable="@drawable/wheel5" android:duration="50" />
  </animation-list>
```

Here is the code to load and play this animation. 

```kotlin
// Load the ImageView that will host the animation and
  // set its background to our AnimationDrawable XML resource.
  ImageView img = (ImageView)findViewById(R.id.spinning_wheel_image);
  img.setBackgroundResource(R.drawable.spin_animation);
 
  // Get the background, which has been compiled to an AnimationDrawable object.
  AnimationDrawable frameAnimation = (AnimationDrawable) img.getBackground();
 
  // Start the animation (looped playback by default).
  frameAnimation.start();
  
```
|
| ### Developer Guides
|
| For more information about animating with`AnimationDrawable`, read the [Drawable Animation](https://developer.android.com/guide/topics/graphics/drawable-animation.html) developer guide.

## Summary

| XML attributes ||
|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [`android:drawable`](AnimationDrawable.md) | Reference to a drawable resource to use for the frame. |
| [`android:duration`](AnimationDrawable.md) | Amount of time (in milliseconds) to display this frame. |
| [`android:oneshot`](AnimationDrawable.md) | If true, the animation will only run a single time and then stop. |
| --- | --- |
| [`android:variablePadding`](AnimationDrawable.md) | If true, allows the drawable's padding to change based on the current state that is selected. |
| [`android:visible`](AnimationDrawable.md) | Provides initial visibility state of the drawable; the default value is false. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimationDrawable](AnimationDrawable.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFrame](AnimationDrawable.md))`(`frame:` ` [Drawable](Drawable.md)`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a frame to the animation |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuration](AnimationDrawable.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Drawable](Drawable.md)! | [getFrame](AnimationDrawable.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumberOfFrames](AnimationDrawable.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](AnimationDrawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOneShot](AnimationDrawable.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](AnimationDrawable.md))`()` Indicates whether the animation is currently running or not. |
| open [Drawable](Drawable.md) | [mutate](AnimationDrawable.md))`()` Make this drawable mutable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](AnimationDrawable.md))`()` This method exists for implementation purpose only and should not be called directly. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOneShot](AnimationDrawable.md))`(`oneShot:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the animation should play once or repeat. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setVisible](AnimationDrawable.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `restart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this AnimationDrawable is visible. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](AnimationDrawable.md))`()` Starts the animation from the first frame, looping if necessary. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](AnimationDrawable.md))`()` Stops the animation at the current frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](AnimationDrawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConstantState](AnimationDrawable.md))`(`state:` ` [DrawableContainer.DrawableContainerState](../android/graphics/drawable/DrawableContainer.DrawableContainerState.md)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [DrawableContainer](DrawableContainer.md) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTheme](DrawableContainer.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canApplyTheme](DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](DrawableContainer.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlpha](DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](DrawableContainer.md))`()` <br /> Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through [setChangingConfigurations(int)](Drawable.md))or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold. <br /> | | [Drawable.ConstantState](../android/graphics/drawable/Drawable.ConstantState.md)? | [getConstantState](DrawableContainer.md))`()` <br /> | | [Drawable](Drawable.md) | [getCurrent](DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHotspotBounds](DrawableContainer.md))`(`outRect:` ` [Rect](../android.graphics/Rect.md)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicHeight](DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntrinsicWidth](DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumHeight](DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumWidth](DrawableContainer.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpacity](DrawableContainer.md))`()` <br /> | | [Insets](../android.graphics/Insets.md) | [getOpticalInsets](DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](DrawableContainer.md))`(`outline:` ` [Outline](../android.graphics/Outline.md)`)` <br /> Called to get the drawable to populate the Outline that defines its drawing area. This method is called by the default [android.view.ViewOutlineProvider](../android.view/ViewOutlineProvider.md) to define the outline of the View. The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPadding](DrawableContainer.md))`(`padding:` ` [Rect](../android.graphics/Rect.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFocusStateSpecified](DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateDrawable](DrawableContainer.md))`(`who:` ` [Drawable](Drawable.md)`)` <br /> Called when the drawable needs to be redrawn. A view at this point should invalidate itself (or at least the part of itself where the drawable appears). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoMirrored](DrawableContainer.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateful](DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](DrawableContainer.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBoundsChange](DrawableContainer.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLayoutDirectionChanged](DrawableContainer.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the drawable's resolved layout direction changes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLevelChange](DrawableContainer.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStateChange](DrawableContainer.md))`(`state:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleDrawable](DrawableContainer.md))`(`who:` ` [Drawable](Drawable.md)`, `what:` ` [Runnable](../java.lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> A Drawable can call this to schedule the next frame of its animation. An implementation can generally simply call [android.os.Handler#postAtTime(Runnable, Object, long)](../android.os/Handler.md))with the parameters (what, who, when) to perform the scheduling. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [selectDrawable](DrawableContainer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the currently displayed drawable by index. If an invalid index is specified, the current drawable will be set to`null`and the index will be set to`-1`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](DrawableContainer.md))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoMirrored](DrawableContainer.md))`(`mirrored:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](DrawableContainer.md))`(`colorFilter:` ` [ColorFilter](../android.graphics/ColorFilter.md)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDither](DrawableContainer.md))`(`dither:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterFadeDuration](DrawableContainer.md))`(`ms:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the global fade duration when a new drawable is entering the scene. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitFadeDuration](DrawableContainer.md))`(`ms:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the global fade duration when a new drawable is leaving the scene. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspot](DrawableContainer.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHotspotBounds](DrawableContainer.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintBlendMode](DrawableContainer.md))`(`blendMode:` ` [BlendMode](../android.graphics/BlendMode.md)!`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [BlendMode.SRC_IN](../android.graphics/BlendMode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintList](DrawableContainer.md))`(`tint:` ` [ColorStateList](../android.content.res/ColorStateList.md)?`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleDrawable](DrawableContainer.md))`(`who:` ` [Drawable](Drawable.md)`, `what:` ` [Runnable](../java.lang/Runnable.md)`)` <br /> A Drawable can call this to unschedule an action previously scheduled with [scheduleDrawable](../android/graphics/drawable/Drawable.Callback.md)). An implementation can generally simply call [android.os.Handler#removeCallbacks(Runnable, Object)](../android.os/Handler.md))with the parameters (what, who) to unschedule the drawable. <br /> | ||
| From class [Drawable](Drawable.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorFilter](Drawable.md))`()` <br /> Removes the color filter for this drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [copyBounds](Drawable.md))`()` <br /> Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | [Drawable](Drawable.md)? | [createFromPath](Drawable.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a drawable from file path name. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromResourceStream](Drawable.md))`(`res:` ` [Resources](../android.content.res/Resources.md)?`, `value:` ` [TypedValue](../android.util/TypedValue.md)?`, `is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `opts:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?`)` <br /> Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | [Drawable](Drawable.md)? | [createFromStream](Drawable.md))`(`is:` ` [InputStream](../java.io/InputStream.md)?`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Create a drawable from an inputstream <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`)` <br /> Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXml](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` <br /> Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | [Drawable](Drawable.md) | [createFromXmlInner](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Create a drawable from inside an XML document using an optional [Theme](../android/content/res/Resources.Theme.md). Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns`null`if the tag is not a valid drawable. <br /> | | [Rect](../android.graphics/Rect.md) | [getBounds](Drawable.md))`()` <br /> Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)? | [getCallback](Drawable.md))`()` <br /> Return the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation attached to this Drawable. <br /> | | [ColorFilter](../android.graphics/ColorFilter.md)? | [getColorFilter](Drawable.md))`()` <br /> Returns the current color filter, or`null`if none set. <br /> | | [Rect](../android.graphics/Rect.md) | [getDirtyBounds](Drawable.md))`()` <br /> Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirection](Drawable.md))`()` <br /> Returns the resolved layout direction for this Drawable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](Drawable.md))`()` <br /> Retrieve the current level. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getState](Drawable.md))`()` <br /> Describes the current state, as a union of primitive states, such as [android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_selected](../android/R.attr.md), etc. Some drawables may modify their imagery based on the selected state. <br /> | | [Region](../android.graphics/Region.md)? | [getTransparentRegion](Drawable.md))`()` <br /> Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`)` <br /> Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](Drawable.md))`(`r:` ` [Resources](../android.content.res/Resources.md)`, `parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidateSelf](Drawable.md))`()` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFilterBitmap](Drawable.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProjected](Drawable.md))`()` <br /> Whether this drawable requests projection. Indicates that the [android.graphics.RenderNode](../android.graphics/RenderNode.md) this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](Drawable.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveOpacity](Drawable.md))`(`op1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing [getOpacity](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`, `when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](Drawable.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](Drawable.md))`(`cb:` ` [Drawable.Callback](../android/graphics/drawable/Drawable.Callback.md)?`)` <br /> Bind a [Callback](../android/graphics/drawable/Drawable.Callback.md) object to this Drawable. Required for clients that want to support animated drawables. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChangingConfigurations](Drawable.md))`(`configs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorFilter](Drawable.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` <br /> Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for [setColorFilter(android.graphics.ColorFilter)](Drawable.md))which constructs a [PorterDuffColorFilter](../android.graphics/PorterDuffColorFilter.md). **Note:** Setting a color filter disables [tint](Drawable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterBitmap](Drawable.md))`(`filter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLayoutDirection](Drawable.md))`(`layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setLevel](Drawable.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setState](Drawable.md))`(`stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \ [[android.R.attr#state_focused](../android/R.attr.md), [android.R.attr#state_pressed](../android/R.attr.md)\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling [invalidateSelf](Drawable.md))in order to have itself redrawn,*and*true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTint](Drawable.md))`(`tintColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md)). To clear the tint, pass`null`to [setTintList(android.content.res.ColorStateList)](Drawable.md)). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTintMode](Drawable.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` <br /> Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md). **Note:** Setting a color filter via [setColorFilter(android.graphics.ColorFilter)](Drawable.md))or [setColorFilter(int,android.graphics.PorterDuff.Mode)](Drawable.md))overrides tint. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unscheduleSelf](Drawable.md))`(`what:` ` [Runnable](../java.lang/Runnable.md)`)` <br /> Use the current [Callback](../android/graphics/drawable/Drawable.Callback.md) implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## XML attributes

### android:drawable

```
android:drawable
```
Reference to a drawable resource to use for the frame. If not given, the drawable must be defined by the first child tag.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:duration

```
android:duration
```
Amount of time (in milliseconds) to display this frame.

May be an integer value, such as "`100`". 

### android:oneshot

```
android:oneshot
```
If true, the animation will only run a single time and then stop. If false (the default), it will continually run, restarting at the first frame after the last has finished.

May be a boolean value, such as "`true`" or "`false`". 

### android:variablePadding

```
android:variablePadding
```
If true, allows the drawable's padding to change based on the current state that is selected. If false, the padding will stay the same (based on the maximum padding of all the states). Enabling this feature requires that the owner of the drawable deal with performing layout when the state changes, which is often not supported.

May be a boolean value, such as "`true`" or "`false`". 

### android:visible

```
android:visible
```
Provides initial visibility state of the drawable; the default value is false. See [android.graphics.drawable.Drawable#setVisible](Drawable.md)).

May be a boolean value, such as "`true`" or "`false`".

## Public constructors

### AnimationDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnimationDrawable()
```

## Public methods

### addFrame

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFrame(
    frame: Drawable, 
    duration: Int
): Unit
```

Adds a frame to the animation

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `frame` | [Drawable](Drawable.md):The frame to add This value cannot be`null`. |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How long in milliseconds the frame should appear |

### getDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDuration(i: Int): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The duration in milliseconds of the frame at the specified index |

### getFrame

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrame(index: Int): Drawable!
```

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Drawable](Drawable.md)! | The Drawable at the specified frame index |

### getNumberOfFrames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumberOfFrames(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of frames in the animation |

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

### isOneShot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOneShot(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True of the animation will play once, false otherwise |

### isRunning

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRunning(): Boolean
```

Indicates whether the animation is currently running or not.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the animation is running, false otherwise |

### mutate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mutate(): Drawable
```

Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [Drawable](Drawable.md) | This value cannot be`null`. |

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun run(): Unit
```

This method exists for implementation purpose only and should not be called directly. Invoke [start()](AnimationDrawable.md))instead. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#start()> 

### setOneShot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOneShot(oneShot: Boolean): Unit
```

Sets whether the animation should play once or repeat.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `oneShot` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Pass true if the animation should only play once |

### setVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVisible(
    visible: Boolean, 
    restart: Boolean
): Boolean
```

Sets whether this AnimationDrawable is visible.

When the drawable becomes invisible, it will pause its animation. A subsequent change to visible with`restart`set to true will restart the animation from the first frame. If`restart`is false, the drawable will resume from the most recent frame. If the drawable has already reached the last frame, it will then loop back to the first frame, unless it's a one shot drawable (set through [setOneShot(boolean)](AnimationDrawable.md))), in which case, it will stay on the last frame.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if visible, false otherwise |
| `restart` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):when visible, true to force the animation to restart from the first frame |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the new visibility is different than its previous state |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Starts the animation from the first frame, looping if necessary. This method has no effect if the animation is running.

**Note:** Do not call this in the android.app.Activity#onCreate method of your activity, because the [AnimationDrawable](AnimationDrawable.md) is not yet fully attached to the window. If you want to play the animation immediately without requiring interaction, then you might want to call it from the [android.app.Activity#onWindowFocusChanged](../android.app/Activity.md))method in your activity, which will get called when Android brings your window into focus. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#isRunning()>
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#stop()> 

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Stops the animation at the current frame. This method has no effect if the animation is not running. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#isRunning()>
- <https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable#start()> 

### unscheduleSelf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unscheduleSelf(what: Runnable): Unit
```

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `what` | [Runnable](../java.lang/Runnable.md):The runnable that you no longer want called. This value cannot be`null`. |

## Protected methods

### setConstantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setConstantState(state: DrawableContainer.DrawableContainerState): Unit
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [DrawableContainer.DrawableContainerState](../android/graphics/drawable/DrawableContainer.DrawableContainerState.md):This value cannot be`null`. |
